# Infrastructure: What I've Built

## Summary

Over ~2 years I led the modernization of NovaTerra's platform from click-ops
bare-metal to a fully containerized, IaC-managed, multi-AZ Kubernetes environment.

## Key Achievements

- Migrated all workloads to EKS (Kubernetes on AWS)
- Wrote all infrastructure in Terraform (modular, team-maintained)
- Implemented GitOps with ArgoCD — deployments are now PR-driven
- Reduced average deployment time from 60 min to 4 min
- Built centralized observability: Prometheus + Grafana + Loki stack
- Migrated secrets to HashiCorp Vault + AWS Secrets Manager
- Decommissioned all bare-metal servers
- Implemented multi-AZ RDS with read replicas + automated backups
- Set up DR runbooks and quarterly restore drills

## Current Tech Stack

- **Cloud:** AWS (EKS, RDS Multi-AZ, S3, ALB, Route53, ACM, SQS, MSK)
- **IaC:** Terraform (remote state in S3 + DynamoDB lock)
- **Containers:** Docker, Kubernetes (EKS 1.29)
- **GitOps:** ArgoCD
- **CI/CD:** GitHub Actions
- **Monitoring:** Prometheus, Grafana, Alertmanager, Loki
- **Secrets:** HashiCorp Vault + AWS Secrets Manager
- **Networking:** Custom VPC, private/public subnets, NAT Gateway, Security Groups
- **Messaging:** Apache Kafka (MSK)
- **Databases:** RDS PostgreSQL (Multi-AZ) + ElastiCache Redis

## Interview Talking Points

- "I inherited a single Jenkins node and replaced it with GitHub Actions pipelines..."
- "We had zero Terraform. I introduced it by starting with the VPC module..."
- "The biggest cultural win was getting developers to trust GitOps..."
