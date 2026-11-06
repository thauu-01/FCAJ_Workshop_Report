---
title: "Week 11 Worklog"
date: 2026-12-17
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Explore enterprise business continuity, centralized data protection, and Disaster Recovery (DR) strategies.
* Master centralized lifecycle backup orchestration with AWS Backup (Plans, Vaults, Cross-Region replication).
* Study cloud disaster recovery topologies: Backup & Restore, Pilot Light, Warm Standby, and Multi-Site Active/Active.
* Attain operational competence in cloud financial governance: AWS Cost Explorer, AWS Budgets, and AWS Trusted Advisor.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Analyze foundational Disaster Recovery metrics: Recovery Time Objective (RTO) and Recovery Point Objective (RPO).<br>- Evaluate 4 cloud DR architectural patterns: Backup & Restore, Pilot Light, Warm Standby, and Multi-Site Active/Active.<br>- Balance trade-offs between implementation costs, architectural complexity, and RTO/RPO targets. |
| 3 | - Study AWS Backup centralized management: Backup Plans, Backup Rules, Vaults, and Vault Lock policies.<br>- Configure automated daily/weekly backup schedules covering Amazon EC2, EBS, RDS, DynamoDB, and S3.<br>- Define lifecycle transitions moving recovery points to cold storage after 30 days and expiring after 365 days.<br>- Configure Cross-Region Backup replication to an auxiliary secondary region for regional disaster survivability. |
| 4 | - Explore AWS Cost Management tools: Billing Dashboard and Cost Allocation Tags (Environment, Project, Owner).<br>- Leverage AWS Cost Explorer to dissect historical cost patterns, usage trends, and forecast upcoming monthly commitments.<br>- Isolate data transfer expenses, inter-AZ network fees, and service-specific cost drivers. |
| 5 | - Configure financial guardrails in AWS Budgets: Establish monthly recurring cost budgets.<br>- Configure intelligent alerting thresholds notifying stakeholders when actual spending hits 80% or forecasted spending breaches 100%.<br>- Evaluate long-term commitment savings models: Compute Savings Plans, EC2 Instance Savings Plans, and Reserved Instances (RI). |
| 6 | - **DR Restoration & Cost Optimization Practice:** Execute simulated DR drills restoring an EC2 instance and RDS database from AWS Backup recovery points.<br>- Execute full AWS Trusted Advisor inspections spanning all 5 pillars (Cost, Performance, Security, Fault Tolerance, Limits).<br>- Identify and eliminate orphaned zombie resources: Unattached EBS volumes and idle unassociated Elastic IPs. |

---

### Core Hands-on Lab & Practice:

#### Automating Enterprise Backups with AWS Backup & Financial Governance with AWS Budgets
In this technical project, I centralized enterprise data protection by authoring an AWS Backup Plan with automated daily schedules and cross-region replication to a secondary region. I executed disaster recovery drills, verifying that compute and database instances could be seamlessly restored from recovery points within defined RTO windows. Concurrently, I enacted cost governance by enforcing Cost Allocation Tags, deploying automated threshold alarms via AWS Budgets, and purging orphaned EBS volumes and unused Elastic IPs.

---

### Key Achievements & Learning Outcomes:

* Mastered enterprise Disaster Recovery design principles, optimizing critical RTO and RPO benchmarks.
* Centralized automated backup lifecycles and cross-region disaster replication via AWS Backup.
* Validated operational resilience by successfully executing end-to-end data recovery drills from cold recovery points.
* Implemented proactive cloud financial management using AWS Cost Explorer and threshold alerting via AWS Budgets.
* Leveraged AWS Trusted Advisor intelligence to rightsize resources and eliminate unutilized cloud spending.
