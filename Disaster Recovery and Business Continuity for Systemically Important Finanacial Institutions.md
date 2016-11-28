---
title: >-
  FIN302  --  Disaster Recovery and Business Continuity for Systemically
  Important Financial Institutions
---

# The takeaway

- systemicatically important workloads for financial services running on AWS
- Disaster recovery can be automated, auditable, * ElasticYou can leverage AWS for disaster recovery while meeting regulatory requirements

# Agenda

- moderninizing disaster revoery
- trading refresher
- customer implmenation
- disaster reco ery demo

# Moderninzing Disaster Recovery

Current Disaster Recovery Methds

- BCP weekend

  - _"Business Continuity Planning"_

  - usually results in a shiny new environment for disaster Recovery

Cons:

- manual
- capital intensive
- infrequently used

# Moderninzing Disaster Recovery

- codify
- only pay for it when it's instatiatied

- audit trail

- NO MORE BCP weeknds

# Securities Exchange Commision

- must

RegSCI requirements

- comprehensive policies and procedures in place to help ensure the robustness and resiliency of their technological systems
- geographical diversity
- two hour recovery geographical

# ISE (International Securities Exchange)

"Announces first implemenation of a securities exchange on AWS"

Disaster recovery is "_baked-in_"

# Trading refresher

...

# AEX Tech Stack

- AWS Cloudformation - Infrastructure as code
- Troposphere - Generates cloudfomration templates
- Amazon EC2 Container Service - Container Management service

  - will talk through multicast

- Weaveworks Weave Net - Provides container overlay network

- Amazon Route 53 - DNS

- Amazon S3 _duplicate ledger_

- Amazon Kinesis Firehose _duplicate ledger_

The exchange's redundancy is provided by the edger duplication

# Recovery Time objective * recovery point objective

- Data loss may occur at RPO
- RTO the amount of time the business can be without the service without loss

# RPO for AEX is 0 (in this demo)

There is no data loss because of the implemenation of the kinesis + s3 redundancy

(Anytime there is a transaction, it's automatically replicated)

## The more closesly you couple the way you replicate your state, the lower your RPO will be

# RTO is lower if you're DR environment is always on

- RTO ~7mins (demo)

  - manually
  - cloudformation
  - lower if DR was 24/7

# Disaster Recovery Demo

- Application code is aware if it's in "Recovery mode"

  - similar to `cfn-init` awareness on Platform

# In Depth Route-53

Route 53 with every symbol for an consumer to look up the multicast address

- AEX Private hosted zone, can only be resolved by AEX

# In-depth ECS cluster

Weavenet makes the multicast address possible

But how did they link it to route 53

# Benefits of Modernized Recovery

- only pay for when it's running
