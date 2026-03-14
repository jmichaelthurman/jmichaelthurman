# J. Michael Thurman

> I build the platforms 100-engineer teams ship on —
> multi-account AWS, EKS at scale, GitOps from day one.

[![CV Chat](https://img.shields.io/badge/Chat_with_my_CV-4a9eff?style=for-the-badge&logo=anthropic&logoColor=white)](https://jmichaelthurman.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/jmichaelthurman)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jmthurman@cloudbrook.net)

---

10+ years in cloud infrastructure. Currently running the platform at **SumerSports** — 10 EKS clusters, 15 AWS accounts, 100 engineers. Previously **Senior SRE at Moonswitch**, operating 12 EKS clusters across 5 client environments including Azure Government Cloud air-gapped workloads.

AWS Certified: **DevOps Professional** · **SysOps Associate**

Some things I've shipped:
- Reduced full-environment disaster recovery from **72 hours → 12–18 hours** by codifying all client infrastructure in Terraform
- Led a 12-month program that recovered **$600k from a $1.2M undocumented Azure footprint** (approved budget: $0)
- Cut Aurora cluster provisioning from **10 business days → 30 minutes** via self-service IaC bundles (Terramate Catalyst)
- Diagnosed cascading failures in a **65-node EKS cluster** running 250+ preview environments — DNS quota exhaustion, 800+ leaked DB connections

---

## Activity

Most of my production contributions live under my work account.

**Work Account:** [@mthurman-sumer](https://github.com/mthurman-sumer) | **Org:** [SumerSports](https://github.com/SumerSports)

### Work
![](https://raw.githubusercontent.com/jmichaelthurman/jmichaelthurman/main/profile-cards/work/tokyonight/0-profile-details.svg)
![](https://raw.githubusercontent.com/jmichaelthurman/jmichaelthurman/main/profile-cards/work/tokyonight/3-stats.svg)

### Personal
![](https://raw.githubusercontent.com/jmichaelthurman/jmichaelthurman/main/profile-cards/personal/tokyonight/0-profile-details.svg)
![](https://raw.githubusercontent.com/jmichaelthurman/jmichaelthurman/main/profile-cards/personal/tokyonight/3-stats.svg)

---

## Stack

### Cloud & IaC
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Terramate](https://img.shields.io/badge/Terramate-00ADD8?style=for-the-badge&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

### GitOps & CI/CD
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

### Languages & Tools
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![HCL](https://img.shields.io/badge/HCL-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)

### Observability & Data
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Aurora](https://img.shields.io/badge/Aurora-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

---

## Open Source

### [eks-upgrade-check](https://github.com/jmichaelthurman/eks-upgrade-check)
> Python CLI for Kubernetes upgrade readiness assessment. Built to replace manual pre-upgrade checklists with scored, CI-gateable output.

- 0–100 readiness scoring engine with weighted categories across deprecations, addon versions, CRD compatibility, workload health, and security policies
- 12 typed exit codes for CI/CD pipeline integration — gate on specific failure conditions, not just pass/fail
- MCP server integration exposes checks as callable tools for AI agents
- Containerized deployment: Docker image with all required tools and MCP servers, designed to run as a scheduled scan
- v3.5.0 · 123+ merged PRs

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-4a9eff?style=flat-square&logoColor=white)

---

### [open-brain-cloud](https://github.com/jmichaelthurman/open-brain-cloud)
> A cloud-native personal AI memory system — capture thoughts from any Claude client, retrieve them semantically from anywhere.

MCP server running on Fly.io, storing knowledge in Supabase Postgres with pgvector. Every thought is embedded with Voyage AI (`voyage-3-lite`, 512-dim HNSW index) and linked into a typed knowledge graph you build yourself.

- 6 MCP tools: `capture_thought`, `search_thoughts`, `list_recent`, `link_thoughts`, `get_links`, `stats`
- Metadata extraction (people, topics, action items) via claude-haiku-4 through OpenRouter
- `/capture` REST endpoint for iOS Shortcuts — capture from any device, query from any Claude session
- Typed directional knowledge graph: `related` · `supports` · `contradicts` · `follows_from` · `part_of` · `example_of` · `references`

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Fly.io](https://img.shields.io/badge/Fly.io-7C3AED?style=flat-square&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-4a9eff?style=flat-square&logoColor=white)

---

## Featured Projects

### Terramate Catalyst Bundles Framework
> Infrastructure scaffolding framework: composable AWS patterns provisioned via a single `catalyst scaffold` command.

- Architected a 5-layer bundle system (Objects > Components > Bundles > Stacks > Generated Files) consumed across a 15-account AWS org
- Built RDS Aurora Global Cluster bundle: multi-region failover, IRSA integration, CloudWatch monitors, Datadog observability, KMS encryption
- Implemented typed schema validation, Checkov security scanning, and automated code generation
- Components include: IRSA roles, Route53 subdomains, ArgoCD applications, S3 buckets

**Technologies:** OpenTofu/Terraform · Terramate Catalyst · AWS (Aurora, EKS, KMS, Route53, ACM) · HCL

---

### AWS Multi-Account Infrastructure Platform
> Multi-account AWS platform serving 9+ environments — OpenTofu, Terramate, and ArgoCD at the core.

- Managed EKS clusters with Karpenter autoscaling, node group normalization, and ALB controller integration
- Built Aurora Serverless v2 with cross-region failover and environment-specific capacity tuning
- Implemented Serverless PrivateLink with Lambda-automated RDS failover for cross-VPC database connectivity
- Provisioned CloudFront CDN, KMS key management, and SQS queues for data pipelines
- 1,293 commits · 100+ merged PRs · 11 repositories · trunk-based development

**Technologies:** OpenTofu · Terramate · AWS (EKS, Aurora, CloudFront, Lambda, PrivateLink, KMS, SQS) · Karpenter

---

### ArgoCD GitOps Platform
> Kubernetes application deployment platform across multiple EKS clusters, managed entirely through GitOps.

- Defined ArgoCD ApplicationSet patterns for multi-cluster system application deployment
- Configured Datadog agent for RDS monitoring and APM tracing
- Managed Helm chart lifecycle for C#/.NET and TypeScript microservices
- Led Kafka/Strimzi decommissioning across production clusters
- Deployed LiteLLM AI gateway with autoscaling and GitHub Actions Runner Controller (ARC)

**Technologies:** ArgoCD · Helm · Kubernetes · Datadog · GitHub Actions

---

### Shared OpenTofu Module Library
> Reusable infrastructure modules consumed across all stacks in a multi-account AWS organization.

- Aurora RDS module with KMS key rotation and environment-specific configuration
- Serverless PrivateLink module with Lambda-automated cross-VPC failover
- IRSA role module with configurable trust policies
- CloudFront module with S3 origin access and cache behavior ordering

**Technologies:** OpenTofu/Terraform · AWS

---

## Experience

**DevOps / Platform Engineer** — SumerSports *(2025 – Present)*
Own the full infrastructure lifecycle across a 15-account AWS org: IaC authoring, GitOps deployment, production monitoring. 1,293 commits and 100+ merged PRs across 11 repositories in year one.

**Senior Site Reliability Engineer** — Moonswitch *(Prior)*
Operated 12 EKS clusters across 5 client environments. Reduced disaster recovery time from 72 hours to 12–18 hours by codifying all client infrastructure in Terraform. Led a $600k Azure cost recovery program. Managed Azure Government Cloud air-gapped workloads under FedRAMP/FISMA/NIST-800-53 compliance frameworks.

---

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=jmichaelthurman&color=blueviolet&style=flat-square&label=Profile+Views)

</div>
