---
title: "Week 1 Worklog"
date: 2026-10-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:

* Get acquainted with the team, mentors, and the First Cloud AI Journey (FCAJ) development roadmap.
* Grasp core Cloud Computing fundamentals and the AWS Global Infrastructure (Regions, AZs, Edge Locations).
* Create and harden an AWS Free Tier account with AWS IAM following the Principle of Least Privilege.
* Install, configure AWS CLI v2, and gain hands-on proficiency with Amazon Elastic Compute Cloud (EC2).

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Meet with FCAJ members and mentor.<br>- Review internship regulations, workplace culture, and the 12-week development roadmap.<br>- Setup development environment: VS Code, Git, and terminal utilities. |
| 3 | - Learn Cloud Computing foundations and cloud service models (IaaS, PaaS, SaaS).<br>- Study the AWS Shared Responsibility Model.<br>- Explore AWS Global Infrastructure: Regions, Availability Zones (AZs), and Edge Locations. |
| 4 | - Register an AWS Free Tier account and enable Multi-Factor Authentication (MFA) on the Root Account.<br>- Study AWS Identity and Access Management (IAM): Users, Groups, Policies, and Roles.<br>- Create a dedicated IAM Admin user and enforce the Principle of Least Privilege. |
| 5 | - Install AWS CLI v2 on the local workstation.<br>- Configure Access Key ID, Secret Access Key, default region, and output format via `aws configure`.<br>- Execute essential CLI commands: verify caller identity (`sts get-caller-identity`), describe regions and instances. |
| 6 | - Study Amazon EC2 architecture: Instance Types (t2/t3.micro), AMIs, EBS storage, Key Pairs.<br>- Configure Security Groups restricting SSH (port 22) to trusted CIDR.<br>- Launch an Amazon Linux EC2 instance and establish a secure SSH session. |

---

### Core Hands-on Lab & Practice:

#### Secure AWS Account Hardening & Amazon EC2 Deployment
In this foundational hands-on laboratory, I secured the AWS Root Account by activating Virtual MFA, constructed an IAM Admin Group with granular policies, and completely decommissioned root access keys. Subsequently, I configured AWS CLI v2 on the local environment and provisioned an Amazon Linux 2023 EC2 instance with an encrypted gp3 EBS volume, associated SSH Key Pairs, and validated remote terminal connectivity.

---

### Key Achievements & Learning Outcomes:

* Mastered cloud delivery models and the AWS Shared Responsibility framework.
* Hardened the AWS Root account with MFA and implemented IAM best practices compliant with CIS benchmarks.
* Attained practical fluency in managing AWS infrastructure via both Management Console and AWS CLI v2.
* Successfully provisioned, configured, and remotely accessed Amazon EC2 virtual servers.
* Established a dependable engineering baseline for advanced cloud networking in Week 2.
