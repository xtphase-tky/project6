# Pipelines depicting Blue Green Deployment to production server with minimal downtime and rollback safety

## Overview

These pipelines demonstrate how a docker image can built, pushed to appropriate registry and safely deployed to production server with maximum uptime

it enforces principles such as:

1. blue green deployment
2. rollback availability
3. proper sequence of jobs
4. appleboy for ssh action

---

## Problem Statement

Typical pipelines or setups may include:

1. manual deployment
2. no rollback option if deployment fails
3. downtime
4. no health checking

## Solution

A project demonstrating:

1. blue green strategy to reduce downtime
2. rollback container always available
3. safe ssh to servers
4. tracking image_uri
5. Multiple smoke tests

---

## Rollback strategy

1. Older version of container is always available
2. Newer container is first tried on seperate port
3. Newer container is only promoted if health check is fine
4. In production port, it is health checked again
5. If it ever returns an error, it is immediately switched with last safe container

---

## Tech Stack

- Github actions (Pipelines)
- Docker (image, containers)
- Dockerhub
- Elastic Container Registry
- AWS (EC2 Server, IAM Role)

---

## Activation

- Push event to main branch
- Manual trigger through Github UI
