---
title: "Basic code : Spark streaming"
date: 2020-08-09T02:47:18-04:00
draft: false
---

A simple code to read words in stream and count number of words.

Save the code for word count and run producer with netcat command

```python
from pyspark.sql import SparkSession
from pyspark.sql.functions import explode
from pyspark.sql.functions import split

spark = SparkSession \
    .builder \
    .appName("Word Count") \
    .getOrCreate()


# Create DataFrame representing the stream of input lines from connection to localhost:9999
lines = spark \
    .readStream \
    .format("socket") \
    .option("host", "localhost") \
    .option("port", 9999) \
    .load()

# Split the lines into words
words = lines.select(
   explode(
       split(lines.value, " ")
   ).alias("word")
)

# Generate running word count
wordCounts = words.groupBy("word").count()

# Start running the query that prints the running counts to the console
query = wordCounts \
    .writeStream \
    .outputMode("complete") \
    .format("console") \
    .start()

query.awaitTermination()
```

For Unix users
```shell
nc -lk 9999
```

For Windows , install nmap from [here](https://nmap.org/download.html#windows)
```shell
ncat.exe -lk 9999
```

Open another CMD (in Windows) or Terminal (in Linux/Mac) and the run the code to see the result
```shell
spark-submit sparkstream.py localhost 9999
```