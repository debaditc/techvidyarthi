---
title: "Database Sharding"
date: 2020-08-16T15:47:23-04:00
draft: false
---

#### Simple definition
Process of making paritions of data in database

#### Vertical and Horizontal Sharding

Let us understand using simple example

**Table**

{{< figure src="/images/dbshard1.JPG" >}}


**Veritical Sharding**
{{< figure src="/images/dbshard2.JPG" >}}

**Horizontal Sharding**

Sharding is performed on the basis of salary.
- Horizontal Shard1 = salary < 100000
- Horizontal Shard2 = salary > 100000 AND salary < 250000
- Horizontal Shard3 = salary > 250000

{{< figure src="/images/dbshard3.JPG" >}}


#### Benefits of Sharding
- Improves the efficiency of queries
- Sharding results to small logical table which makes query faster
Read and write performance increases

#### Problems with Sharding
- Joining data across shards is expensive process as the join happens across the network
- Too many shards is a problem and increase the overhead

#### What happens the shard fails ?
Have Master Slave architechture where we wont have single point of failure. As leader is chosen when master fails.