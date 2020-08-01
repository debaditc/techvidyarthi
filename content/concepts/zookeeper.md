---
title: "About Zookeeper"
date: 2020-07-16T21:19:21-04:00
draft: true
---

Zookeeper is registry for large distributed systems. It is beneficial for tasks like master election, crash detection and managing meta data related to distributed systems.

The ZooKeeper framework was originally built at “Yahoo!” for accessing their applications in an easy and robust manner. Apache ZooKeeper is a standard for organized service used by Hadoop, HBase, and other distributed frameworks. 

# Services Provided by Zookeeper (NCCLLH - thats How I remember) 

- **Naming service** − Identifying the nodes in a cluster by name.

- **Configuration management** − Update configuration information of the system for a joining node.

- **Cluster management** − Joining / leaving of a node in a cluster and node status at real time.

- **Leader election** − Electing a node as leader for coordination purpose. (SOLR)

- **Locking and synchronization service** − Locking the data while modifying it.

- **Highly reliable data registry** − Availability of data even when one or a few nodes are down.


# How does Zookeeper work ?

The data within Zookeeper is divided across multiple collection of nodes (**ZNODES**) and this is how it achieves its high availability and consistency. In case a node fails, Zookeeper can perform instant failover migration; e.g. if a master node fails, a new one is selected in real-time by polling within an ensemble. A client connecting to the server can query a different node if the first one fails to respond.

# Can Load Balancer act as Zookeeper?

**NO** - Load balancer helps in distribution of work loads across multiple servers.
Whereas , Zookeeper is good for master election , crash detection , storing configurations / state of the services , etc.


# Why is Zookeeper necessary for Apache Kafka?
I remember it as "C-CAM" 

- **Controller election**

The controller is one of the most important broking entity in a Kafka ecosystem, and it also has the responsibility to maintain the leader-follower relationship across all the partitions. If a node by some reason is shutting down, it’s the controller’s responsibility to tell all the replicas to act as partition leaders in order to fulfill the duties of the partition leaders on the node that is about to fail. So, whenever a node shuts down, a new controller can be elected and it can also be made sure that at any given time, there is only one controller and all the follower nodes have agreed on that.

- **Configuration Of Topics**

The configuration regarding all the topics including the list of existing topics, the number of partitions for each topic, the location of all the replicas, list of configuration overrides for all topics and which node is the preferred leader, etc.

- **Access control lists**

Access control lists or ACLs for all the topics are also maintained within Zookeeper.

- **Membership of the cluster**

Zookeeper also maintains a list of all the brokers that are functioning at any given moment and are a part of the cluster.

{{< figure src="/images/zkkafka.JPG" >}}