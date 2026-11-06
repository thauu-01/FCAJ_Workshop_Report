---
title: "Week 12 Worklog"
date: 2026-12-24
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Synthesize and demonstrate the comprehensive theoretical knowledge and hands-on skills acquired across the 12-week FCAJ journey.
* Architect, provision, and deploy a production-grade 3-Tier Enterprise Cloud Capstone Project.
* Conduct a thorough architectural evaluation against the 6 pillars of the AWS Well-Architected Framework.
* Finalize internship documentation, present the capstone defense to mentors, and outline future Cloud Architect milestones.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Consolidate mastery across AWS disciplines: Networking (VPC), Compute (EC2, ECS, Fargate), Databases (RDS, DynamoDB, ElastiCache), Storage (S3, EBS), Security (IAM, KMS, WAF), Observability (CloudWatch), and DevOps (CI/CD).<br>- Formulate business specifications, data flow diagrams, and architectural blueprints for the final Capstone Project. |
| 3 | - **Capstone Infrastructure & Security Tier Provisioning:**<br>&emsp;+ Provision a Multi-AZ custom VPC (2 Public Subnets, 2 Private App Subnets, 2 Private DB Subnets, 1 IGW, 2 NAT Gateways).<br>&emsp;+ Formulate least-privilege Security Groups and IAM execution roles.<br>&emsp;+ Implement AWS KMS customer managed keys for pervasive data encryption at rest. |
| 4 | - **Capstone Application & Data Tier Implementation:**<br>&emsp;+ Deploy an Amazon RDS MySQL Multi-AZ cluster and an ElastiCache Redis cluster inside private DB subnets.<br>&emsp;+ Containerize application microservices and register images within Amazon ECR.<br>&emsp;+ Deploy services to Amazon ECS Fargate fronted by an Application Load Balancer and Auto Scaling.<br>&emsp;+ Host frontend static assets in Amazon S3 distributed globally via Amazon CloudFront with ACM SSL certificates. |
| 5 | - **System Stress Testing & Well-Architected Review:**<br>&emsp;+ Conduct synthetic load tests, validating automatic container scale-out and simulating database failover.<br>&emsp;+ Attach an AWS WAF Web ACL to the ALB and configure consolidated CloudWatch operational dashboards and alarms.<br>&emsp;+ Utilize the AWS Well-Architected Tool to review the workload against all 6 pillars and document architectural trade-offs. |
| 6 | - **Program Conclusion & Final Capstone Defense:**<br>&emsp;+ Audit and polish the 12-week worklog documentation, lab guides, and GitHub project codebase.<br>&emsp;+ Deliver the final Capstone Project presentation and defense before FCAJ mentors and technical review boards.<br>&emsp;+ Receive evaluations, celebrate program graduation, and outline certification goals for the AWS Certified Solutions Architect pathway. |

---

### Core Hands-on Lab & Practice:

#### Deploying an Enterprise 3-Tier Capstone Architecture & AWS Well-Architected Review
In this culminating milestone, I designed and deployed an enterprise-grade 3-Tier cloud application. The solution synthesized Amazon CloudFront + S3 (Presentation Tier), an Application Load Balancer + Amazon ECS Fargate Auto Scaling (Application Tier), and Amazon RDS MySQL Multi-AZ + ElastiCache Redis (Database Tier) within an isolated Multi-AZ custom VPC. The deployment was hardened by AWS WAF and KMS, automated via a continuous CodePipeline CI/CD engine, and audited against the 6 pillars of the AWS Well-Architected Framework.

---

### Key Achievements & Learning Outcomes:

* Successfully architected and deployed an enterprise-grade cloud solution orchestrating over 15 distinct AWS services.
* Mastered infrastructure auditing methodologies aligned with the 6 pillars of the AWS Well-Architected Framework.
* Flawlessly synthesized advanced networking, serverless container orchestration, database clustering, and security automation.
* Demonstrated elite operational troubleshooting, performance optimization, and architectural decision-making competencies.
* Successfully graduated from the 12-week First Cloud AI Journey (FCAJ) internship, laying a world-class foundation for becoming a Cloud Solutions Architect.
