---
title: "Event Driven model"
date: 2020-08-01T15:03:38-04:00
draft: false
---

### Event Driven Model

Event driven model is based on either Pub/sub or Event streaming model

### Pub-sub model
Messaging infrastructure is based on subscription based model (Active MQ)

### Event streaming model
Events are written into logs. Consumers need not require to subscribe event - rather they can be read or join from any part of the stream (Kafka)


### System Design - Microservice + Kafka + KSQL

Picture credits : Please visit [Confluent site](https://www.confluent.io/blog/building-a-microservices-ecosystem-with-kafka-streams-and-ksql/) for more details

{{< figure src="/images/eventdr.JPG" >}}




