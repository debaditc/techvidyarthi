---
title: "Vertical vs Horizontal Scaling"
date: 2020-07-26T16:30:42-04:00
draft: true
---

# Nutshell 
- **Horizontal scaling** means that we scale by adding more machines into  pool of resources 
- **Vertical scaling** means that we scale by adding more power (CPU, RAM) to an existing machine.

# High level difference

{{< figure src="/images/horver.JPG" >}}


# Real world implementation

Take the benfits of both Horizontal and Vertical scaling

- **Vertical scaling** :  Inter process communication and data consistency
- **Horizontal scaling** : Scalability and Resilient (no single point of failure)

Ideal way - First have the veritical scaling (optimal level) and scale horizontally.

#### Credits 
[Gaurav Sen](https://www.youtube.com/watch?v=xpDnVSmNFX0) - Please watch video in Youtube