---
title: "Week 10 Worklog"
date: 2026-12-09
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Explore multi-layered Defense-in-Depth security adhering to the AWS Well-Architected Security Pillar.
* Master cryptographic operations with AWS Key Management Service (KMS) and credential rotation via Secrets Manager.
* Protect internet-facing applications against web exploits using AWS WAF (Web Application Firewall).
* Enable continuous threat detection with Amazon GuardDuty and consolidate security posture using AWS Security Hub.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study the 7 design principles for security in the cloud.<br>- Apply advanced IAM hardening: IAM Access Analyzer, enforcing MFA via JSON Policy condition keys (`aws:MultiFactorAuthPresent`).<br>- Explore IAM Permission Boundaries and Service Control Policies (SCPs) within AWS Organizations. |
| 3 | - Explore AWS Key Management Service (KMS): Customer Managed Keys (CMKs), AWS Managed Keys, and Envelope Encryption.<br>- Formulate granular Key Policies scoping cryptographic grants.<br>- Enforce Encryption at Rest across S3 buckets, EBS volumes, and RDS databases.<br>- Study AWS Secrets Manager: Secret caching, automated database password rotation via managed Lambda functions. |
| 4 | - Examine AWS WAF (Web Application Firewall): Web ACLs, Managed Rule Groups, and custom rule development.<br>- Deploy AWS Managed Rules: Core Rule Set (CRS), SQL database inspection, and Known Bad Inputs.<br>- Configure Rate-based rules protecting endpoints against application-layer DDoS and credential stuffing.<br>- Associate Web ACLs with Application Load Balancers and CloudFront distributions. |
| 5 | - Study Amazon GuardDuty: Machine learning-driven threat detection analyzing VPC Flow Logs, DNS query logs, and CloudTrail management events.<br>- Enable AWS Security Hub: Aggregating findings across GuardDuty, IAM Access Analyzer, and AWS Inspector.<br>- Measure security compliance postures against CIS AWS Foundations Benchmark standards. |
| 6 | - **Security Defense Validation Lab:** Inject synthetic malicious payloads (e.g. SQL Injection strings \`OR 1=1\`) verifying immediate HTTP 403 blocks by AWS WAF.<br>- Trigger automated secret rotation in Secrets Manager and confirm zero connection dropouts.<br>- Review synthesized findings and remediate compliance warnings in the Security Hub dashboard. |

---

### Core Hands-on Lab & Practice:

#### Enforcing Deep Defense Security with AWS KMS, Secrets Manager, AWS WAF & Security Hub
In this rigorous hands-on laboratory, I established an end-to-end security perimeter across the infrastructure. All stored assets and database volumes were protected using custom AWS KMS CMKs with strict key usage policies. Production database secrets were managed and automatically rotated by AWS Secrets Manager. At the edge, an AWS WAF Web ACL actively protected the Application Load Balancer against OWASP Top 10 vulnerabilities, while Amazon GuardDuty and Security Hub provided 24/7 posture surveillance.

---

### Key Achievements & Learning Outcomes:

* Mastered multi-layered Defense-in-Depth design methodologies aligned with AWS Well-Architected standards.
* Implemented enterprise-grade encryption at rest and in transit using AWS KMS Envelope Encryption.
* Successfully automated application database secret lifecycle and credentials rotation via AWS Secrets Manager.
* Shielded internet-facing web assets against OWASP Top 10 exploits and DDoS attacks utilizing AWS WAF.
* Operated Amazon GuardDuty and AWS Security Hub to enforce regulatory compliance and threat remediation.
