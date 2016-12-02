---
title: >-
  SVR401  --  Using AWS Lambda to Build Control Systems for Your AWS
  Infrastructure
---

# Randal Hunt

Randal Hunt @jrhunt

randhunt@amazon.com

# Agenda

- Brief overview of AWS Lambda
- Why automate?
- Why Lambda for automation and control systems?
- Event-driven policy enforcement

  - PCI
  - HIPPA
  - Lambda is one of the easiest way to get done

- Lambda as an infrastructure control plane

- Best practices

# Owning server means dealing with a lot of crap

# Serverless compute: AWS Lambda

Puts the ownership of issues on AWS, not you.

## Codebuild can do your lambda packaging for you

- Codecommit
- codepipeline
- codebuild

Lambda is cost by Gb/s - memory / time

# Why automate?

- Just do it

# Dangers of incorrect automation

- Code maintenance issues

# Why is automation Key

When you have a few things, it's easier to manage by yourself

At some point it becomes non-trivial to maintain infrastructure on your own

# What sort of things can we automate?

Just about anything!

Take a selfie and tweet at @awscloudninja

- finds faces, replaces faces with ninja

# Why lambda for automation

# Event driven automation

# Policy enforcement

You have to define what's appropriate

- AWS Config Rules
- Cloudwatch
- CloudTrail

# AWS Config

# IAM Enforcement

# Infrastructure Automation

- Cloudwatch Events

  - Autoscaling events
  - Api call
  - lambda

# Create/Update Route53 records from tag

# Best practices

- log everything
- report failures

  - on stream failures, you'll see retries, but if you're not reporting the errors - you'll be scratching your head

- iterate
- bite-sized code
- version lambda functions

# Recap
