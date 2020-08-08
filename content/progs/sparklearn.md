---
title: "Spark Learnings"
date: 2020-08-08T17:14:45-04:00
draft: true
---

### Install Spark ###
For Windows : Please follow [this site](https://phoenixnap.com/kb/install-spark-on-windows-10)

#### Basics of Spark Flow ####
```
Run Spark application -> Driver program starts -> Main function starts ->  
SparkContext gets initiated -> Driver program runs the operations inside the executors on worker nodes.
```

SparkContext uses Py4J to launch a JVM and creates a JavaSparkContext. 
By default, PySpark has SparkContext available as ‘sc’, so creating a new SparkContext won't work.

{{< figure src="/images/spark1.jpg" >}}

credits : TutoialPoint

#### Lazy Execution ####

#### Basic commands ####

#### Data frame vs RDD ####

#### Spark SQL ####

#### Broadcast and Accumulators ####

#### Catalyst ####

#### Cache in Spark ####

#### Streaming ####