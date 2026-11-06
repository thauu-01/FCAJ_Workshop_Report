---
title: "Week 7 Worklog"
date: 2026-11-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Understand and apply Infrastructure as Code (IaC) paradigms in modern cloud engineering.
* Master declarative cloud provisioning with AWS CloudFormation (JSON/YAML, Parameters, Resources, Outputs, Intrinsic Functions).
* Learn the AWS Cloud Development Kit (CDK) to define cloud infrastructure using expressive programming languages.
* Eliminate SSH bastion dependencies and secure instance management using AWS Systems Manager (SSM).

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study Infrastructure as Code (IaC) principles: Repeatability, version control, automated change auditing, and human error mitigation.<br>- Dissect AWS CloudFormation template sections: Parameters, Mappings, Conditions, Resources, and Outputs.<br>- Understand the CloudFormation stack lifecycle and preview infrastructural diffs using Change Sets. |
| 3 | - Author a modular CloudFormation template (YAML) orchestrating a complete VPC topology: Subnets, Route Tables, and Gateways.<br>- Apply intrinsic functions: `Ref`, `!Sub`, `!GetAtt`, `!Join`, and `!Select`.<br>- Execute stack provisioning and updates, testing automated rollbacks upon synthesized resource deployment failures. |
| 4 | - Explore AWS Cloud Development Kit (CDK): Architecture of Apps, Stacks, and L1/L2/L3 Constructs.<br>- Compare declarative YAML specifications against programmatic infrastructure definitions (TypeScript/Python).<br>- Master essential CDK CLI workflows: `cdk init`, `cdk synth`, `cdk diff`, and `cdk deploy`. |
| 5 | - Investigate AWS Systems Manager (SSM) suite: SSM Agent, Session Manager, Parameter Store, and Run Command.<br>- Attach IAM roles with the `AmazonSSMManagedInstanceCore` policy to EC2 instances.<br>- Test keyless, zero-open-port administrative terminal access via SSM Session Manager directly in the browser. |
| 6 | - **Comprehensive IaC & Systems Management Lab:** Provision a multi-tier application stack via AWS CDK.<br>- Securely inject database credentials and app configs utilizing SSM Parameter Store (SecureString with KMS encryption).<br>- Execute remote fleet software updates across EC2 nodes using Systems Manager Run Command. |

---

### Core Hands-on Lab & Practice:

#### Automated Cloud Provisioning with CloudFormation/CDK & Keyless Operations via SSM
In this technical project, I encoded cloud infrastructure into reusable code utilizing AWS CloudFormation and AWS CDK (TypeScript). The automated deployment provisioned an entire isolated VPC network along with compute tiers. For fleet administration, I integrated AWS Systems Manager Session Manager, completely closing inbound port 22 on all Security Groups while enabling audited, encrypted browser-based shell access and managing application configurations via SSM Parameter Store.

---

### Key Achievements & Learning Outcomes:

* Mastered Infrastructure as Code principles and git-based infrastructure lifecycle management.
* Authored and deployed production CloudFormation templates featuring dynamic parameterization and intrinsic functions.
* Gained hands-on competency developing reusable infrastructure constructs using the AWS CDK in TypeScript.
* Eliminated traditional SSH attack vectors by transitioning completely to AWS Systems Manager Session Manager.
* Implemented secure centralized configuration management leveraging encrypted SSM Parameter Store values.
