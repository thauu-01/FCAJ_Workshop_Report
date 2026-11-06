---
title: "Week 2 Worklog"
date: 2026-10-09
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Master cloud network architecture using Amazon Virtual Private Cloud (VPC).
* Design IP address schemas using CIDR blocks and implement Public/Private subnet separation.
* Configure routing tables with Internet Gateways (IGW) and NAT Gateways for secure egress.
* Implement defense-in-depth network access control using Security Groups (Stateful) and NACLs (Stateless).

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study Amazon VPC architecture, RFC 1918 private IP spaces, and CIDR subnetting (`10.0.0.0/16`).<br>- Differentiate Public and Private Subnets across Multi-Availability Zones for High Availability.<br>- Examine Route Table architecture and local routing mechanisms. |
| 3 | - Understand Internet Gateway (IGW) attachment and default egress routing (`0.0.0.0/0 -> igw`).<br>- Design Public Subnet Route Tables enabling Internet-facing traffic.<br>- Configure NAT Gateways in Public Subnets granting outbound internet access for private workloads. |
| 4 | - Compare Security Groups (Layer 4 - Stateful, instance-level) against Network ACLs (Layer 3/4 - Stateless, subnet-level).<br>- Configure granular Inbound/Outbound rules for HTTP (80), HTTPS (443), and SSH (22). |
| 5 | - Study Elastic IP (EIP) addresses and Elastic Network Interfaces (ENI).<br>- Associate and reallocate EIPs seamlessly between instances for failover resilience.<br>- Review billing implications of unattached idle Elastic IPs. |
| 6 | - **Comprehensive Practice:** Build a custom 2-Tier VPC spanned across 2 Availability Zones.<br>- Deploy a Bastion Host in the Public Subnet and an isolated workload in the Private Subnet.<br>- Verify Bastion SSH tunneling and validate outbound package updates via NAT Gateway. |

---

### Core Hands-on Lab & Practice:

#### Designing & Deploying a Multi-Tier Production-Ready Custom VPC
In this hands-on lab, I architected a custom VPC (`10.0.0.0/16`) comprising two Public Subnets and two Private Subnets across dual Availability Zones. The architecture incorporated an Internet Gateway for public ingress/egress and an allocated NAT Gateway routing private outbound connections. Workloads in private subnets were verified to have zero direct internet exposure, accessible strictly via an encrypted Bastion Host tunnel.

---

### Key Achievements & Learning Outcomes:

* Architected an enterprise-grade VPC with resilient Multi-AZ topology and clean subnet segmentation.
* Configured end-to-end routing incorporating Internet Gateways, NAT Gateways, and isolated Route Tables.
* Implemented rigorous multi-layered filtering combining Stateful Security Groups and Stateless NACLs.
* Gained practical expertise in deploying Bastion Host jump boxes for secure administrative access.
* Developed acute troubleshooting skills for resolving network routing and CIDR overlap bottlenecks.
