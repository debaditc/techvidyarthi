---
title: "CAP Theorem in Nutshell"
date: 2020-08-19T21:22:43-04:00
tags: ["database","cap"]
draft: false
---

### About CAP Theorem
It is also known as Brewer's theorem after computer scientist Eric Brewer

### Simple terms
It states no distributed data store can provide more than 2 out of 3 gurantees

- **Consistency** : Every client views the same data. Every node in distributed cluster recieves same data.

- **Availability** : During node failure time, every node must respond in a reasonable amount of time.

- **Partition tolerance** : Gurantees partition tolerance can recover from partitions once the partition heals.

{{< figure src="/images/cap.png" >}}

Image credits [here](https://www.researchgate.net/figure/Database-Systems-according-to-the-CAP-Theorem_fig1_334554423)