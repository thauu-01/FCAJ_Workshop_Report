---
title: "Week 6 Worklog"
date: 2026-11-08
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Explore the principles of Serverless Computing and Event-Driven Architecture (EDA).
* Master AWS Lambda serverless execution: Function authoring, execution roles, environment parameters, and concurrency.
* Build and expose serverless RESTful APIs using Amazon API Gateway (Resources, Methods, Stages, CORS).
* Implement asynchronous enterprise messaging paradigms utilizing Amazon SQS and Amazon SNS.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study Serverless Computing foundations: Zero infrastructure overhead, instantaneous elasticity, and pay-per-use economics.<br>- Explore AWS Lambda: Invocations, memory sizing, timeouts, and execution concurrency models (Reserved vs Provisioned).<br>- Author granular IAM Execution Roles enforcing least privilege access for Lambda workloads. |
| 3 | - Develop Lambda functions in Node.js/Python executing CRUD logic interacting with Amazon DynamoDB.<br>- Analyze Amazon CloudWatch Logs for Lambda metrics: billed duration, memory consumption, and runtime stack traces.<br>- Examine Lambda Cold Starts and techniques for initialization optimization. |
| 4 | - Study Amazon API Gateway: Comparing REST APIs against low-latency HTTP APIs.<br>- Configure API Resources, HTTP Methods (GET, POST, PUT, DELETE), and Lambda Proxy Integrations.<br>- Implement deployment stages (dev, prod), stage variables, and manage CORS headers for web client integrations. |
| 5 | - Examine decoupled distributed messaging patterns: Comparing Pub/Sub (SNS) against Point-to-Point Queues (SQS).<br>- Study Amazon SQS: Standard vs FIFO queues, Visibility Timeouts, and Dead-Letter Queues (DLQ).<br>- Study Amazon SNS: Topics, Subscriptions (Email, Lambda, SQS), and the Fan-out pattern. |
| 6 | - **Comprehensive Serverless Microservice Lab:** Construct an Event-Driven Order Processing System.<br>- API Gateway accepts orders -> Lambda validates payload -> persists state into DynamoDB -> publishes event to SNS Topic -> Fan-out to SQS queues for asynchronous processing. |

---

### Core Hands-on Lab & Practice:

#### Building an Event-Driven Serverless Order Processing API with Lambda, API Gateway & SQS/SNS
In this technical project, I constructed a completely serverless order pipeline. Amazon API Gateway served as the front-door HTTP endpoint handling `/orders` requests via Lambda Proxy Integration. An AWS Lambda function ingested and validated payloads, wrote state to Amazon DynamoDB, and emitted order events into an Amazon SNS Topic. Using the SNS Fan-out pattern, messages were routed concurrently into Amazon SQS queues for billing ingestion and notifications.

---

### Key Achievements & Learning Outcomes:

* Mastered serverless design methodologies and event-driven decoupled architecture standards.
* Authored and tuned production-ready AWS Lambda functions with optimized memory footprints and IAM role scoping.
* Engineered secure, scalable RESTful API interfaces with Amazon API Gateway and CORS configuration.
* Successfully implemented high-throughput asynchronous messaging utilizing SNS-to-SQS Fan-out architectures.
* Configured fault tolerance and failed message recovery pipelines leveraging Dead-Letter Queues (DLQ).
