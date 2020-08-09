---
title: "About Kafka"
date: 2020-08-08T18:04:27-04:00
draft: false
---

## Kafka Architecture 

- Kafka uses ZooKeeper to manage the cluster. 
- ZooKeeper is used to coordinate the brokers/cluster topology. 
- ZooKeeper gets used for leadership election for Broker Topic Partition Leaders.

- Kafka producers write to Topics -> Kafka consumers read from Topics. 

- Topic is associated with a log which is data structure on disk. Kafka appends records from a producer(s) to the end of a topic log. A topic log consists of many partitions that are spread over multiple files which can be spread on multiple Kafka cluster nodes. Consumers read from Kafka topics at their cadence and can pick where they are (offset) in the topic log. Each consumer group tracks offset from where they left off reading. Kafka distributes topic log partitions on different nodes in a cluster for high performance with horizontal scalability. Spreading partitions aids in writing data quickly. Topic log partitions are Kafka way to shard reads and writes to the topic log. 


{{< figure src="/images/kafka.jpg" >}}

More details are [here](http://cloudurable.com/blog/kafka-architecture/index.html)

#### Kafka Brokers
- A Kafka cluster is made up of multiple Kafka Brokers. 
- Each Kafka Broker has a unique ID (number). 
- Kafka Brokers contain topic log partitions. 
- For failover, you want to start with at least three to five brokers. 
- A Kafka cluster can have, 10, 100, or 1,000 brokers in a cluster if needed.

#### Kafka Disaster Recover 

Use of Kafka Mirror Maker - It replicates kafka cluster to another data center.

#### Install Zookeeper and Kafka ####
Step by step procedure is [here](https://dzone.com/articles/running-apache-kafka-on-windows-os)

Once Zookeeper and Kafka are installed - You can play with below commands

**Start Zookeeper in background**
```
zkserver
```

**Start Kafka in background**

Make sure to shorten the parent directory - else you would recieve error as "Tool long input line"
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

**Create topic in Kafka**
```
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic testtopic
```

**Start producer**
```
kafka-console-producer.bat --broker-list localhost:9092 --topic testtopic
```

**Start consumer**
```
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic testtopic
```