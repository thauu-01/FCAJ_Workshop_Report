---
title: "Week 5 Worklog"
date: 2026-11-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Explore infrastructure observability, logging, and automated alerting using Amazon CloudWatch.
* Master Elastic Load Balancing (ELB) architectures, focusing on Layer-7 Application Load Balancer (ALB).
* Learn automated horizontal scaling strategies with Amazon EC2 Auto Scaling Groups (ASG).
* Design and deploy a resilient, fault-tolerant, self-healing web architecture across Multiple Availability Zones.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Explore Amazon CloudWatch foundations: Metrics, Logs, Log Groups, Log Streams, and Dashboards.<br>- Analyze CloudWatch Alarm state machines (OK, ALARM, INSUFFICIENT_DATA).<br>- Integrate Amazon Simple Notification Service (SNS) for immediate email notifications upon alarm triggers. |
| 3 | - Configure CloudWatch Agent on EC2 instances to harvest detailed system metrics (RAM utilization, disk metrics).<br>- Construct CloudWatch Alarms monitoring CPU thresholds exceeding 70% over consecutive evaluation periods.<br>- Build an operations dashboard consolidating comprehensive infrastructure health telemetry. |
| 4 | - Study Elastic Load Balancing: Application Load Balancer (Layer 7), Network Load Balancer (Layer 4), and Gateway Load Balancers.<br>- Examine Target Groups, Health Checks, and Listener routing rules (path-based and host-based routing).<br>- Configure an Application Load Balancer distributing incoming traffic across compute nodes. |
| 5 | - Study Amazon EC2 Auto Scaling: Launch Templates specifying AMI, instance sizes, user data, and security controls.<br>- Configure Multi-AZ Auto Scaling Groups (ASG) ensuring high availability and fault isolation.<br>- Evaluate scaling policy designs: Target Tracking, Step Scaling, Simple Scaling, and Scheduled actions. |
| 6 | - **End-to-End Hands-on Integration:** Attach Auto Scaling Group to ALB Target Groups.<br>- Execute synthetic CPU load generation via `stress` utility on running EC2 nodes.<br>- Observe automated scale-out events, target registrations, and subsequent scale-in stabilization. |

---

### Core Hands-on Lab & Practice:

#### Architecting a Self-Healing High-Availability Web Tier with ALB & Auto Scaling
In this advanced laboratory, I engineered a highly available, self-healing compute topology. The system placed an Application Load Balancer in public subnets routing requests into an Auto Scaling Group spanning two Availability Zones. Upon executing synthetic stress benchmarks driving CPU utilization past 70%, CloudWatch Alarms dynamically instructed the Auto Scaling Group to provision additional instances, seamlessly pass health checks, and distribute the incoming load without downtime.

---

### Key Achievements & Learning Outcomes:

* Mastered Amazon CloudWatch observability, custom metrics ingestion, and centralized operational dashboards.
* Configured real-time incident alerting pipelines utilizing CloudWatch Alarms and Amazon SNS topics.
* Gained hands-on proficiency with Application Load Balancer configurations, target health checks, and listener rules.
* Successfully deployed resilient Auto Scaling Groups driven by modern Launch Templates and target tracking policies.
* Acquired practical verification skills for chaos resilience, synthetic load testing, and self-healing validation.
