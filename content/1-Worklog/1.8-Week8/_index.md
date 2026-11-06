---
title: "Week 8 Worklog"
date: 2026-11-24
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Explore containerization principles and master Docker: Dockerfile authoring, layer caching, and multi-stage builds.
* Secure and maintain container repositories with Amazon Elastic Container Registry (ECR) and image vulnerability scanning.
* Study Amazon Elastic Container Service (ECS) orchestration concepts: Clusters, Task Definitions, and Services.
* Deploy production container workloads on serverless AWS Fargate integrated with Application Load Balancers.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Contrast Containers (shared OS kernel, lightweight, instant startup) against traditional Virtual Machines.<br>- Dissect Docker architecture: Docker Daemon, Images, Containers, and Dockerfile directives (`FROM`, `WORKDIR`, `COPY`, `RUN`, `CMD`).<br>- Author production Dockerfiles applying multi-stage build patterns for minimal image footprints. |
| 3 | - Explore Amazon Elastic Container Registry (ECR): Private Repositories, Image Tagging, and KMS Encryption.<br>- Authenticate local Docker daemon to AWS ECR via `aws ecr get-login-password`.<br>- Build, tag, and push container images into Amazon ECR.<br>- Enable Enhanced Image Scanning to automatically inspect images for Common Vulnerabilities and Exposures (CVEs). |
| 4 | - Study Amazon Elastic Container Service (ECS): Comparing EC2 Launch Type against serverless AWS Fargate.<br>- Author ECS Task Definitions: Resource allocations (vCPU/RAM), container port bindings, Task Roles, and Task Execution Roles.<br>- Examine ECS Services: Maintaining desired task counts, service discovery, and rolling update strategies. |
| 5 | - Initialize an ECS Cluster and launch a multi-task ECS Service using the AWS Fargate launch type.<br>- Integrate the ECS Service with an Application Load Balancer to accept incoming HTTP/HTTPS traffic.<br>- Configure ALB Target Groups and define healthy threshold parameters for container task endpoints. |
| 6 | - **Release Cycle Hands-on:** Modify application source code, rebuild image version 2.0, and push to ECR.<br>- Trigger an ECS Service rolling update with updated task revisions.<br>- Observe zero-downtime traffic cutover managed by the ALB as old tasks deregister and new tasks pass health checks. |

---

### Core Hands-on Lab & Practice:

#### Dockerizing Applications & Running Serverless Microservices on Amazon ECS Fargate
In this technical project, I containerized a full-stack web application using multi-stage Dockerfiles and pushed the secured artifacts into Amazon ECR. I orchestrated the workload using Amazon ECS on top of AWS Fargate serverless infrastructure, removing all underlying virtual machine administration. The service was fronted by an Application Load Balancer, and I verified that deploying updated image versions resulted in automated zero-downtime rolling updates.

---

### Key Achievements & Learning Outcomes:

* Mastered containerization engineering with optimized multi-stage Docker build pipelines.
* Implemented secure container lifecycle management, KMS encryption, and automated vulnerability scanning on ECR.
* Attained deep expertise in Amazon ECS orchestration, contrasting EC2 and serverless AWS Fargate launch types.
* Successfully deployed high-availability container microservices backed by Application Load Balancers.
* Demonstrated seamless zero-downtime rolling deployments for cloud-native containerized applications.
