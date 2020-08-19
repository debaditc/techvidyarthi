---
title: "Load Balancer"
date: 2020-07-16T20:54:54-04:00
tags: ["system design","performance"]
draft: false
---

### Definition

Load Balancing is the process of re-distributing network traffic across multiple server.

{{< figure src="/images/lb.JPG" >}}

### What Load Balancers can perform ?

- Detect server failures and redirect client traffic automatically/
- Provide automated disaster recovery to backup sites
- Add and remove application servers without disruption
- Monitor and block malicious content

### Load Balance Algorithms (remember as CRRI)

There is a variety of load balancing methods, which use different algorithms best suited for a particular situation.

- **Least Connection Method** — directs traffic to the server with the fewest active connections
- **Least Response Time Method** — directs traffic to the server with the fewest active connections and the lowest average response time.
- **Round Robin Method** — rotates servers by directing traffic to the first available server and then moves that server to the bottom of the queue.
- **IP Hash** — the IP address of the client determines which server receives the request.

### Layer 4 and Layer 7 Load balacing

- Layer 4 operates on Transport layer which involves TCP , UDP. 
- It does not inspect the message contents 

- Layer 7 operates on application layer basically combines 5,6,7 - http,https,ssl,etc
- It has application awareness and can use this additional application information to make more complex and informed load balancing decisions.
- It has great feature "Cookie Persistance"


### About DNS
The Domain Name System (DNS) is the phonebook of the Internet. Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources.
The process of DNS resolution involves converting a hostname (such as www.example.com) into a computer-friendly IP address (such as 192.168.1.1)