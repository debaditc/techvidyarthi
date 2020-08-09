---
title: "Brief on Spark Memory and Optimizer "
date: 2020-08-08T20:28:12-04:00
draft: false
---

## Spark Memory and Optimizer

#### Optimizer
- Core of Spark SQL has **Catalyst optimizer** which leverages 2 important Scala features 
    - Pattern matching 
    - Quasi Notes (Easy to generate code at runtime from composable expressions)

- Catalyst supports both rule-based and cost-based optimization.

- Designed for 2 main pruposes :
    -   Easily add new optimization techniques and features to Spark SQL
    -   Enable external developers to extend the optimizer (e.g. adding data source specific rules, support for new data types, etc)

More details are [here](https://databricks.com/glossary/catalyst-optimizer)

#### Memory
For better memory management - Spark included **Tungsten**

It has 3 basic features

- **Memory management and binary processing**   :   It removes the overhead of JVM and Garbage collection
- **Cache aware computaion** : algorithms and data structures to exploit memory hierarchy
- **Code generation** : using code generation to exploit modern compilers and CPUs

More details are [here](https://databricks.com/blog/2015/04/28/project-tungsten-bringing-spark-closer-to-bare-metal.html)