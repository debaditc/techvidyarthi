---
title: "All about Eventual and Strongly Consistency"
date: 2020-07-28T23:15:05-04:00
draft: false
---

### Eventual Consistent

- Mainly used in NoSQL databases (Solr, Cassandra , MongoDb)
- Used for analytics  , time series analysis , etc
- Low latency - Faster writes

{{< figure src="/images/evenct.JPG" >}}

Please follow Werner Voggel's blog - [here](https://www.allthingsdistributed.com/2008/12/eventually_consistent.html) 


### Strongly Consistent 

- Mainly used in RDBMS like Oracle , MySQL , PostgreSQL
- Primarily used in banking and payment systems
- High latency - Slower writes

{{< figure src="/images/strct.JPG" >}}


### Please read about F1 database by Google [here](https://research.google/pubs/pub41344/)


Photo Credits : Google Blog
