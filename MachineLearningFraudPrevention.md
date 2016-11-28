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

# How is it built for devs?

- ask simple questions
- multi-class classification, ask questions of categorization
- regression, possiblilty of "fraud" in this set of inputs

## Explore and understand your data

- Amazon machine learning can ingest data from _your_ data sources

_when a bank does millions of transactions, 1-3 might be fraud_

choose the right data sets:

- a smaller set of positives

- categorical distributions

**It should be better than flipping a coin**

Amazon machine learning gives tools to evaluate

# Credit card transaction dataset

**is this a real dataset?**

# Model Creation And training - reference Architecture

PCI compliance

- AWS Config (Snapshots your settings)
- Cloudtrail
- AWS KMS
- VPC

VPC

- subnets allow for additional separation
- VPCs by default have 0 connectivity without a gateway
- 2/3 firewalls exist with VPC

EMR + AML (+ RDS, etc ... )

The outcomes of the aws Solution

- **Cost**: Solution price down from $100K to $10K (per month)
- **Speed**: Development down from months to days

  - cloudformation, automation cut down to stand up time from months to days

- **Resources** Focus shift from managment to development

# Next evolution of the Platform

Use lambda and api gateway

Cost is the MS for the execution time
