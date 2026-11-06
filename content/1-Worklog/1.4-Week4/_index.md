---
title: "Week 4 Worklog"
date: 2026-10-24
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Explore AWS managed database ecosystems: Relational (RDBMS), NoSQL, and In-Memory caching solutions.
* Deploy and manage Amazon RDS (MySQL/PostgreSQL) with Multi-AZ redundancy and Read Replicas.
* Master distributed NoSQL mechanics with Amazon DynamoDB, schema design, and secondary indexes.
* Investigate Amazon ElastiCache (Redis) architectures for latency reduction and read-heavy workload acceleration.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study Amazon Relational Database Service (RDS): Supported engines, DB instance specifications, and storage options.<br>- Configure DB Subnet Groups spanning across private subnets in at least two Availability Zones.<br>- Review Automated Backups, backup retention windows, and Point-In-Time Recovery (PITR). |
| 3 | - Compare RDS Multi-AZ synchronous replication (High Availability) vs asynchronous Read Replicas (Read Scalability).<br>- Provision an Amazon RDS MySQL instance in a Private Subnet with tightly controlled Security Groups accepting inbound traffic strictly from application instances. |
| 4 | - Explore Amazon DynamoDB NoSQL primitives: Tables, Items, and Attributes.<br>- Design primary key structures: Simple Partition Key (HASH) vs Composite Primary Key (HASH + RANGE).<br>- Evaluate capacity modes: On-Demand vs Provisioned throughput.<br>- Study indexing mechanisms: Local Secondary Indexes (LSI) and Global Secondary Indexes (GSI). |
| 5 | - Study Amazon ElastiCache in-memory acceleration: Redis (rich data types, clustering, persistence) vs Memcached (simple multi-threaded caching).<br>- Analyze standard caching architectural patterns: Cache-Aside (Lazy Loading) and Write-Through.<br>- Evaluate database offloading strategies using in-memory Redis layers. |
| 6 | - **Hands-on Implementation:** Establish secure connectivity from an EC2 instance to RDS MySQL to execute DDL/DML operations.<br>- Provision a DynamoDB table via AWS CLI, populate JSON documents, and execute targeted queries via partition keys and GSIs.<br>- Compare query latency and scalability characteristics between RDS and DynamoDB. |

---

### Core Hands-on Lab & Practice:

#### Deploying Amazon RDS MySQL Multi-AZ & NoSQL Data Modeling with DynamoDB
In this technical lab, I configured a dedicated DB Subnet Group across dual private subnets and deployed an Amazon RDS MySQL instance in a Multi-AZ standby configuration. Security Groups strictly isolated database access to designated application tiers. In parallel, I structured a high-throughput DynamoDB table modeling user session state, attached Global Secondary Indexes (GSI) to support flexible query patterns, and benchmarked single-digit millisecond response times.

---

### Key Achievements & Learning Outcomes:

* Attained deep competence in choosing suitable AWS database paradigms based on workload requirements.
* Successfully architected an automated failover-ready Amazon RDS Multi-AZ deployment within isolated private subnets.
* Mastered DynamoDB schema engineering including Partition Keys, Sort Keys, and GSI query optimizations.
* Acquired actionable understanding of in-memory caching design patterns with Amazon ElastiCache.
* Validated hands-on database operations across both relational SQL schemas and unstructured NoSQL payloads.
