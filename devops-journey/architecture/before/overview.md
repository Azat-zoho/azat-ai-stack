# Infrastructure: When I Joined

## Overview

When I joined NovaTerra, the infrastructure was a mixed bag — some workloads
on AWS but heavily relying on manually provisioned EC2 instances and a legacy
bare-metal rack in a Chicago co-lo facility.

## Key Pain Points

- No IaC — everything was click-ops in AWS Console
- Deployments were SSH + rsync scripts maintained by one engineer
- No centralized logging; teams used CloudWatch inconsistently
- 3 monolithic apps deployed as fat JARs on EC2
- Secrets stored in plaintext in config files on servers
- No container usage whatsoever
- Single-region (us-east-1), no DR plan
- Manual database backups; untested restore procedures

## Tech Stack (Before)

- **Cloud:** AWS (EC2, RDS, S3, CloudWatch)
- **Servers:** 12 EC2 instances + 4 bare-metal servers (co-lo)
- **Deployments:** Bash scripts, manual SSH
- **CI:** Jenkins (self-hosted, single node, barely maintained)
- **Monitoring:** CloudWatch + one Datadog trial license
- **Databases:** PostgreSQL on RDS (no read replicas), MySQL on bare-metal
- **Networking:** Default VPC, no private subnets
- **Secrets:** Plaintext `.env` files on servers

## Team Sentiment

Engineers were frustrated with deployment toil. On average, a production
deployment took 45-90 minutes and often required manual intervention.
