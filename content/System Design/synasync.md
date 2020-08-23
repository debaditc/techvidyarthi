---
title: "Synchronous and Asynchronous process"
date: 2020-08-01T23:36:51-04:00
tags: ["system design","Synchronous","Asynchronous"]
draft: false
---


### Real life examples

- Synchronous processing : Getting movie ticket from counter , Phone call , video conferencing.

- Asynchronous processing : Ordering food in restaurant , FTP , email , social media.


### Synchronous and Asynchronous process

- **Synchronous processing**  :   Synchronous execution means the execution happens in a single series.

### Single Thread
```
|<---T1---->||<----T2---------->||<------T3----->|
```
### Multi Thread
```
thread A -> |<---A---->|   
                        
thread B ---------------->|<----B---------->|   

thread C ------------------------------------->|<------C----->|
```

- **Asynchronous processing** : Execution of a multiple process can happen without having dependency on each other.
```
   |--------A--------|
         |--------B--------|
```

