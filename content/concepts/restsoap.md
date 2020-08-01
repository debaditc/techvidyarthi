+++ 
draft = true
date = 2020-07-13T19:54:23-04:00
title = "What is REST & SOAP"
description = ""
slug = "" 
tags = []
categories = []
externalLink = ""
series = []
+++

REST and SOAP are terms which are often used by engineers. But one must know that REST is architechtural style while SOAP is protocol.

# REST vs SOAP

{{< figure src="/images/restsoap.JPG" >}}

# When to use REST & SOAP

**REST Usage**

- **Limited resources and bandwidth**
- **Statelessness** – Any Use-case which doesnot need to store the state. This means REST is not suitable for any online purchase site. Saving the state is very critical for any purchase site. 
- **Caching** – Use-case where we need to cache a lot of requests , then REST is way to go. Use-case where it demands usage of similar requests.
- **Ease of coding** – Coding + Implementation REST Services  is far easier than SOAP. 


**SOAP Usage**

- **Asynchronous processing and subsequent invocation** – if there is a requirement that the client needs a guaranteed level of reliability and security 
- **Strict format** – if both the client and server have an agreement on the exchange format then SOAP 1.2 gives the rigid specifications for this type of interaction.
- **Stateful operations** – Any Use-case which needs to store the state. This means SOAP is suitable for any online purchase site. Saving the state is very critical for any purchase site. 
