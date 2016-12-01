---
title: >-
  MAC303 Zillow Group: Developing Classification and Recommendation Engines with
  Amazon EMR and Apache Spark
---

# Spark for Fast Processing

# Spark ML Addresses the full ML Pipeline

- Built on top of dataFrame API
- Extract, transform and select features

..

# Extracting features in DataFrames

- Feature Extractors

  - countvectorizer

- Feature Transformers

  - tokenizer
  - binarizer

...

# Many storage layers to choose from

- S3 is most often used, but you can use
- Dynamodb
- RDS
- Elasticsearch
- Kafka (kinesis)
- S3

# Classification Models is SparkML

# What are decision trees?

# Spark ML pipelines - testing

# Tools to pick the right Models

- CrossValidator and TrainValidationSplit select the model produed by the best=performing set p

# Why amazon EMR

- Elastic...
- Managed
- Open source Variety

  - Spark 2 was implemented 2 days after general availability

- you get root access to the underlying instances, bootstrap at custer creation

# Develop fast using notebooks and IDES

- Zeppelin
- jypter
- R Studio

# Spark on YARN

# Monitor your Spark Jobs

# Auto Scaling for data science on demand

- autoscaling with YARN

# Coming soon: advanced Spot provisioning

- typically YARN can handle nodes being taken away since it's a distributed system
- several spot bids on different instance sizes / AZs

EMR will handle this

# Productionizing your pipelines

- Amazon EMR step API (Spark application)
- AWS lambda
- AWS Data pipelines
- Airflow, Lugii,...

# Recommendation Systems @ Zillow Group

# Agenda

- Intro to Zillow
- Recommendation Use Cases
- Architecture
- Algorithms
- Training & Scoring Pipeline
- Metrics

# Zillow Group

> Build the world's largest, most trusted, and vibrant home-related marketplace.

- Hotpads
- StreetEasy
- Retsly
- dotLoop

  - Making the real estate transaction paperless

# Recommendation Use Cases

- Email - homes for sale / for requirements
- Home details -homes for sale / homes like this
- Personalized Search
- Mobile - smart SMS and push notifications
- Home owner / pre-seller predictions
- Lender selection algo
- Similar photos / video

# Architecture

# Like vs Dislike

> Predict homes per user using behavior of similar users

# Wedge Count

<http://www.jmlr.org/proceedings/papers/v18/kong12a/kong12a.pdf>

# Classifier

# User profile

> User matrix - user preferences

# Ranking

> Property matrix - feature space same as user profile

Age decay for older listings

# Training & Scoring
