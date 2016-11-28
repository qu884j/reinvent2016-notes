---
title: FIN301 -- Fraud Detection with Amazon Machine Learning on AWS
---

# Solving for Multipe Layers Simultaneously

Layer 1 Address endpoint authentication

Layer 2 analyzes session behavior

Layer 3 Monitors accound behavior for a channel

Layer 4 Monitor account behavior across multiple channels

Layer 5 Monitoring multiple account behaviors across multiple channels

# Rule-Based Fraud Detection

Transaction comes in » goes through a rule engine » approve / deny

# Rules Fall short for Fraud Detection

- Static set of Rules

  - Cannot do multi-level fraud Detection

- Human errors and bias with rulesets

- Difficult to manage

- _cannot scale_

# Solution requirements

- process billions of transations a day
- **Make decisions in milliseconds**
- Train with large amounts of data
- secure and alight to compliance requirements

  - DSI, PCI

- Low cost

- Flexible and adaptable

  - _log data needs to be prcoessed at levels 1 & 5_

- Agile and scalable

  - use new models, validate accuracy is up to par

# Machine learning overview

## Supervised learning

- INPUT » OUTPUT

Machine learning will work better if there is a history of data, with validated results.

# Tools of the Trade

- Banks have a lot of data to

S3 is ideal for this data

- s3 » redshift
- s3 » aurora
- s3 » quicksight -

# Amazon Elastic Map Reduce

_Managed hadoop_

- MapReduce, Apache Spark, Presto
- Launch a cluster in minutes
- Built-in security features
- Elastic, can scale on demand
- Can pay by the hour and save with Spot instances (uses ec2 nder the hood)

# An example emr cluster

- Master Node
- Slave Node

  - core
  - and ... task nodes...

    - Aws has extended the slave node concept so that it can scale on tasks vs ...
    - you can also add task nodes with spot, at the price you bid on

# Flexibility to add Hadoop* applications to EMR

# Amazon Machine Learning

- easy to use service built for devs
- ability to create models for your data
