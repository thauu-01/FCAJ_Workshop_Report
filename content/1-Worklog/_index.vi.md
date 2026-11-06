---
title: "Nhật ký công việc"
date: 2026-10-01
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Trang này tổng hợp toàn bộ quá trình học tập, nghiên cứu và thực hành của tôi trong **12 tuần** tham gia chương trình thực tập **First Cloud AI Journey (FCAJ)**. Trong suốt chương trình, tôi đã tiếp cận và làm chủ các dịch vụ cốt lõi của **Amazon Web Services (AWS)**, hoàn thành các bài thực hành chuyên sâu (hands-on labs), đồng thời từng bước xây dựng kỹ năng thiết kế, triển khai và tối ưu hóa hệ thống Cloud đạt tiêu chuẩn AWS Well-Architected Framework.

### Lộ trình đào tạo 12 tuần:

| Tuần | Thời gian | Chủ đề chính | Dịch vụ AWS trọng tâm | Kết quả đầu ra |
| :---: | :---: | :--- | :--- | :--- |
| **[Tuần 1](1.1-week1/)** | 01/10/2026 - 08/10/2026 | Giới thiệu Cloud, IAM & Compute cơ bản | AWS IAM, AWS CLI, Amazon EC2, EBS | Khởi tạo tài khoản an toàn, quản trị IAM & máy chủ EC2 |
| **[Tuần 2](1.2-week2/)** | 09/10/2026 - 15/10/2026 | Thiết kế hạ tầng mạng đám mây | Amazon VPC, Subnets, Route Tables, IGW, NAT GW, SG, NACL | Xây dựng mạng Multi-AZ cô lập và bảo mật cao |
| **[Tuần 3](1.3-week3/)** | 16/10/2026 - 23/10/2026 | Lưu trữ đối tượng & Phân phối nội dung | Amazon S3, Route 53, CloudFront, ACM | Triển khai Static Website toàn cầu tốc độ cao kèm SSL/TLS |
| **[Tuần 4](1.4-week4/)** | 24/10/2026 - 31/10/2026 | Cơ sở dữ liệu & Giải pháp Caching | Amazon RDS (Multi-AZ), DynamoDB, ElastiCache (Redis) | Vận hành RDBMS quan hệ, NoSQL siêu tốc và caching |
| **[Tuần 5](1.5-week5/)** | 01/11/2026 - 07/11/2026 | Giám sát & Khả năng sẵn sàng cao (HA) | Amazon CloudWatch, Alarms, SNS, ALB, Auto Scaling | Thiết kế hệ thống tự động co giãn và cân bằng tải linh hoạt |
| **[Tuần 6](1.6-week6/)** | 08/11/2026 - 15/11/2026 | Điện toán Serverless & Kiến trúc sự kiện | AWS Lambda, API Gateway, Amazon SQS, Amazon SNS | Xây dựng RESTful API không máy chủ và xử lý bất đồng bộ |
| **[Tuần 7](1.7-week7/)** | 16/11/2026 - 23/11/2026 | Hạ tầng dưới dạng mã (IaC) & Quản trị | AWS CloudFormation, AWS CDK, Systems Manager (SSM) | Tự động hóa hạ tầng bằng code, quản trị không cần mở port SSH |
| **[Tuần 8](1.8-week8/)** | 24/11/2026 - 30/11/2026 | Containerization & Điều phối Microservices | Docker, Amazon ECR, Amazon ECS, AWS Fargate | Đóng gói và chạy ứng dụng container serverless quy mô lớn |
| **[Tuần 9](1.9-week9/)** | 01/12/2026 - 08/12/2026 | Tự động hóa CI/CD & DevOps trên Cloud | AWS CodeCommit, CodeBuild, CodeDeploy, CodePipeline | Xây dựng luồng CI/CD tự động từ commit đến production |
| **[Tuần 10](1.10-week10/)** | 09/12/2026 - 16/12/2026 | Bảo mật chuyên sâu & Quản trị rủi ro | IAM Best Practices, KMS, Secrets Manager, WAF, GuardDuty, Security Hub | Bảo mật nhiều lớp, mã hóa dữ liệu và phát hiện mối đe dọa tự động |
| **[Tuần 11](1.11-week11/)** | 17/12/2026 - 23/12/2026 | Sao lưu, Phục hồi thảm họa & Tối ưu chi phí | AWS Backup, Cost Explorer, AWS Budgets, Trusted Advisor | Thiết lập DR, cảnh báo ngân sách và tối ưu tài nguyên lãng phí |
| **[Tuần 12](1.12-week12/)** | 24/12/2026 - 01/01/2027 | Dự án Capstone tổng hợp & Đánh giá kiến trúc | Kiến trúc tích hợp VPC + ALB + ECS/Fargate + RDS + S3/CF | Hoàn thiện đồ án Cloud toàn diện, đánh giá và tổng kết thực tập |

---

### Danh sách chi tiết từng tuần:

- **Tuần 1:** [Giới thiệu AWS, Tài khoản AWS, IAM, AWS CLI và Amazon EC2](1.1-week1/)
- **Tuần 2:** [Amazon VPC, Subnet, Route Table, Security Group, Network ACL và Elastic IP](1.2-week2/)
- **Tuần 3:** [Amazon S3, Static Website Hosting, Amazon Route 53 và Amazon CloudFront](1.3-week3/)
- **Tuần 4:** [Amazon RDS, Amazon DynamoDB và Amazon ElastiCache](1.4-week4/)
- **Tuần 5:** [Amazon CloudWatch, Elastic Load Balancing và Auto Scaling](1.5-week5/)
- **Tuần 6:** [AWS Lambda, Amazon API Gateway, Amazon SQS và Amazon SNS](1.6-week6/)
- **Tuần 7:** [AWS CloudFormation, AWS CDK và AWS Systems Manager](1.7-week7/)
- **Tuần 8:** [Docker, Amazon ECR và Amazon ECS](1.8-week8/)
- **Tuần 9:** [AWS CodeCommit, CodeBuild, CodeDeploy và CodePipeline (CI/CD)](1.9-week9/)
- **Tuần 10:** [Các dịch vụ bảo mật AWS: IAM Best Practices, KMS, Secrets Manager, WAF, GuardDuty và Security Hub](1.10-week10/)
- **Tuần 11:** [AWS Backup, Cost Explorer, AWS Budgets, Trusted Advisor và Tối ưu chi phí](1.11-week11/)
- **Tuần 12:** [Triển khai giải pháp Cloud hoàn chỉnh, Đánh giá kiến trúc và Tổng kết chương trình](1.12-week12/)
