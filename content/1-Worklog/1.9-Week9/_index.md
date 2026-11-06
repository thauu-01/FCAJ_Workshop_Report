---
title: "Week 9 Worklog"
date: 2026-12-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Explore DevOps practices, Continuous Integration (CI), and Continuous Deployment/Delivery (CD) principles.
* Master the AWS Developer Tools suite: AWS CodeCommit, AWS CodeBuild, AWS CodeDeploy, and AWS CodePipeline.
* Author declarative build scripts (`buildspec.yml`) and deployment lifecycle hooks (`appspec.yml`).
* Build a production-grade automated CI/CD pipeline bridging source code commits to live application deployments.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Study DevOps culture and CI/CD mechanics: Automated testing, delivery velocity, and human intervention reduction.<br>- Survey the AWS Developer Tools ecosystem and benchmark against alternatives (GitHub Actions, Jenkins, GitLab CI). |
| 3 | - Examine AWS CodeCommit: Secure Git repository hosting, IAM policy scoping, and credential helper setups.<br>- Study AWS CodeBuild: Managed ephemeral build container environments, artifact caching, and test reporting.<br>- Author structured `buildspec.yml` files configuring `install`, `pre_build`, `build`, and `post_build` phases. |
| 4 | - Study AWS CodeDeploy: Deployment Groups, targets, and Deployment Configurations (AllAtOnce, HalfAtATime, OneAtATime).<br>- Compare deployment topologies: In-Place updates vs zero-downtime Blue/Green deployments.<br>- Define `appspec.yml` specifications and lifecycle hooks (`BeforeInstall`, `AfterInstall`, `ApplicationStart`, `ValidateService`). |
| 5 | - Study AWS CodePipeline orchestration: Pipeline Stages (Source, Build, Test, Deploy), triggers, and S3 artifact buckets.<br>- Integrate Amazon SNS notifications broadcasting pipeline state transitions (Success, Failed).<br>- Implement Manual Approval action gates prior to triggering production deployments. |
| 6 | - **Comprehensive CI/CD Pipeline Implementation:** Build an automated delivery pipeline for a containerized application.<br>- Git push trigger -> CodePipeline ingests source -> CodeBuild executes tests and compiles Docker image to ECR -> CodeDeploy executes rolling rollout to ECS Fargate.<br>- Validate automated rollback triggers upon synthetic smoke test failures. |

---

### Core Hands-on Lab & Practice:

#### Building an Automated End-to-End CI/CD Pipeline with AWS CodePipeline & CodeBuild
In this technical implementation, I constructed an end-to-end continuous delivery pipeline powered by AWS CodePipeline. Upon detecting Git commits to `main`, CodePipeline retrieved the source revision and forwarded the workspace to AWS CodeBuild. CodeBuild executed automated unit tests, compiled application assets, built a multi-stage Docker image tagged with the commit SHA, and pushed it to Amazon ECR. The pipeline concluded by triggering an ECS rolling deployment cutover without downtime.

---

### Key Achievements & Learning Outcomes:

* Attained thorough mastery of cloud-native CI/CD automation and DevOps operational models on AWS.
* Authored and tuned complex build specifications (`buildspec.yml`) and deployment lifecycles (`appspec.yml`).
* Acquired actionable expertise in choosing appropriate release strategies (In-Place vs Blue/Green).
* Successfully orchestrated AWS CodeCommit, CodeBuild, CodeDeploy, and CodePipeline into a cohesive pipeline.
* Configured automated quality gates, approval stages, and automated recovery rollback policies.
