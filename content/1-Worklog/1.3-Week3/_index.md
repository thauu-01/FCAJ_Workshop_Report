---
title: "Week 3 Worklog"
date: 2026-10-16
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Master Amazon Simple Storage Service (S3) object storage mechanics and security architecture.
* Deploy Static Website Hosting, configure Bucket Policies, CORS, and S3 Versioning.
* Study Amazon Route 53 global DNS management and diverse routing policies.
* Accelerate content delivery globally using Amazon CloudFront CDN protected by Origin Access Control (OAC) and ACM SSL.

---

### Tasks to be Carried Out This Week:

| Day | Task |
| :---: | :--- |
| 2 | - Explore Amazon S3 architecture: Buckets, Objects, Keys, and Metadata.<br>- Analyze S3 Storage Classes: Standard, Intelligent-Tiering, Standard-IA, Glacier tiers.<br>- Configure S3 Lifecycle Rules to automate tiering transitions and optimize recurring storage expenses. |
| 3 | - Configure S3 Static Website Hosting with designated index and error HTML documents.<br>- Manage Block Public Access settings and apply granular JSON Bucket Policies.<br>- Enable S3 Object Versioning and Server-Side Encryption (SSE-S3, SSE-KMS). |
| 4 | - Study Amazon Route 53: Public vs Private Hosted Zones, domain registrar services.<br>- Examine DNS record specifications: A, AAAA, CNAME, ALIAS, MX, TXT.<br>- Evaluate routing policies: Simple, Weighted, Latency, Failover, and Geolocation. |
| 5 | - Investigate Amazon CloudFront CDN global infrastructure: Edge Locations and Regional Edge Caches.<br>- Create a CloudFront Distribution mapping to an S3 origin.<br>- Enforce Origin Access Control (OAC) to prohibit direct bucket reads, requiring all requests through CDN. |
| 6 | - **End-to-End Integration:** Provision a public SSL/TLS certificate via AWS Certificate Manager (ACM).<br>- Bind a custom domain to CloudFront using Route 53 Alias record.<br>- Validate global HTTPS edge delivery and execute cache invalidations upon updating assets. |

---

### Core Hands-on Lab & Practice:

#### Global High-Performance Static Website Deployment with S3, CloudFront & Route 53
In this comprehensive laboratory, I hosted a production static web application in Amazon S3 protected by Object Versioning and SSE-S3 encryption. A CloudFront Distribution was established with Origin Access Control (OAC) to completely seal the origin bucket from direct internet access. By configuring AWS Certificate Manager (ACM) SSL certificates and Route 53 Alias records, the application was published with HTTPS encryption and sub-second global edge latency.

---

### Key Achievements & Learning Outcomes:

* Mastered S3 object storage capabilities, lifecycle transition logic, and cost-effective tiered storage.
* Implemented secure bucket policies, CORS cross-origin rules, and granular bucket permissions.
* Acquired firm understanding of Route 53 DNS architectures and specialized Alias apex routing.
* Successfully configured CloudFront CDN with modern OAC safeguards and ACM SSL certificate bindings.
* Demonstrated practical proficiency in edge cache management and cache invalidation strategies.
