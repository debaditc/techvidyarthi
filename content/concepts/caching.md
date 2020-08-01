---
title: "What is Caching and its importance"
date: 2020-07-19T22:20:15-04:00
draft: true
---

# 3 Main use-case of Cache
- Avoid Network calls
- Avoid repeated computation
- Avoid load on Database / System


# Why not use cache every time
- Hardware where Cache runs are mainly in SSDs which are expensive
- More data in Cache will increase the search time - so it will make cache data retrieval slower

# Cache Policy
The way we decide to load or evict data from cache is called Cache policy

# LRU - Least Recently Used Cache
It organizes items in order of use, allowing us to quickly identify which item hasn't been used for the longest amount of time. Its similar as a clothes rack, where clothes are always hung up on one side. Unsed clothes are at other end.

LRU cache is often implemented by pairing a doubly linked list with a hash map.

- Strengths:

    - Super fast accesses. LRU caches store items in order from most-recently used to least-recently used. That means both can be accessed in **O(1) time.**

    - Super fast updates. Each time an item is accessed, updating the cache takes **O(1) time.**

- Weaknesses

    - Space heavy. An LRU cache tracking nn items requires a linked list of length nn, and a hash map holding nn items. That's **O(n) space.**


# LRU eviction
[More details](https://www.interviewcake.com/concept/java/lru-cache)

An LRU cache is an efficient cache data structure that can be used to figure out what we should evict when the cache is full. The goal is to always have the least-recently used item accessible in O(1) time.


Sliding window cache
Global cache - About redis

Varnish Cache