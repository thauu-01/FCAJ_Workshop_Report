---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Below is the directory of in-depth technical blogs focusing on Amazon Web Services (AWS) solutions that I authored and published on the [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj) community:

---

### [Blog 1 - Hosting Static Websites on Amazon S3: From Basic Deployment to CloudFront & OAC Security](3.1-Blog1/)
* 🔗 **Published Article Link:** [View Facebook Post on AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2320770352021257/)

An end-to-end technical deep-dive comparing two AWS static web deployment patterns: direct S3 Static Website Hosting (for prototyping) and production-grade **S3 Private Bucket integrated with CloudFront Origin Access Control (OAC)**. The article provides definitive solutions for React SPA client-side routing errors (403/404 upon browser refresh), advanced HTTP `Cache-Control` header tuning, cost-effective CloudFront invalidation practices, and proactive budget monitoring via AWS Budgets.

---

### [Blog 2 - Deploying Docker Applications on AWS with Amazon ECS and AWS Fargate](3.2-Blog2/)
* 🔗 **Published Article Link:** [View Facebook Post on AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2323062025125423/)

A comprehensive architectural and practical guide to running containerized applications on AWS's serverless container infrastructure: from managing versioned images in **Amazon ECR**, orchestrating container lifecycles via **Amazon ECS (Task Definitions, Tasks, Services)**, to running serverless compute fleets with **AWS Fargate**. The guide dissects the critical distinction between **Task Execution Roles vs. Task Roles**, layered network isolation with **Application Load Balancers (ALB)** in Private Subnets, Zero-Downtime Rolling Deployments with Circuit Breakers, and cost governance with Fargate Spot and VPC Endpoints.

---

### [Blog 3 - Building a Serverless REST API with AWS Lambda, Amazon API Gateway, and Amazon DynamoDB](3.3-Blog3/)
* 🔗 **Published Article Link:** [View Facebook Post on AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2325505481547744/)

A hands-on engineering guide to constructing a production-ready serverless CRUD REST API: routing and rate-limiting incoming traffic with **Amazon API Gateway (HTTP API)**, executing event-driven business logic with **AWS Lambda (Node.js & AWS SDK v3)**, and persisting data with sub-10ms latency using **Amazon DynamoDB (On-Demand capacity)**. The post offers an in-depth architectural comparison between **HTTP APIs vs. REST APIs**, addresses DynamoDB `Scan` operational risks, details CORS integration, cold start mitigation, and IAM Least Privilege configuration.
