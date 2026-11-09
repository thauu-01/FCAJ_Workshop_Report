---
title: "Worklog Tuần 12"
date: 2026-12-24
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Tổng hợp toàn bộ kiến thức và kỹ năng thực hành tích lũy được trong 12 tuần thực tập tại chương trình FCAJ.
* Thiết kế và triển khai một đồ án ứng dụng Cloud hoàn chỉnh (Capstone Project) chuẩn kiến trúc 3-Tier Enterprise.
* Thực hiện đánh giá toàn diện hệ thống theo 6 trụ cột của AWS Well-Architected Framework.
* Hoàn thiện tài liệu báo cáo thực tập, tổ chức thuyết trình bảo vệ đồ án và định hướng lộ trình phát triển Cloud Engineer.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Hệ thống hóa toàn bộ kiến thức các mảng dịch vụ AWS đã học: Networking (VPC), Compute (EC2, ECS, Fargate), Database (RDS, DynamoDB, ElastiCache), Storage (S3, EBS), Security (IAM, KMS, WAF), Monitoring (CloudWatch), DevOps (CI/CD).<br>- Lên ý tưởng, phân tích yêu cầu nghiệp vụ và phác thảo sơ đồ kiến trúc tổng thể cho đồ án tốt nghiệp Capstone Project. |
| 3 | - **Triển khai tầng Mạng & Bảo mật cho Capstone Project:**<br>&emsp;+ Khởi tạo Custom VPC Multi-AZ (2 Public Subnets, 2 Private App Subnets, 2 Private DB Subnets, 1 IGW, 2 NAT Gateways).<br>&emsp;+ Thiết lập Security Groups nhiều lớp và phân quyền IAM Roles theo nguyên tắc Least Privilege.<br>&emsp;+ Cấu hình AWS KMS để mã hóa toàn bộ dữ liệu lưu trữ. |
| 4 | - **Triển khai tầng Ứng dụng & Cơ sở dữ liệu:**<br>&emsp;+ Triển khai Amazon RDS MySQL Multi-AZ và cụm đệm ElastiCache Redis trong Private DB Subnets.<br>&emsp;+ Đóng gói ứng dụng web microservices thành Docker container và đẩy lên Amazon ECR.<br>&emsp;+ Triển khai dịch vụ lên Amazon ECS Fargate tích hợp Application Load Balancer và Auto Scaling.<br>&emsp;+ Lưu trữ tài nguyên tĩnh trên Amazon S3 và phân phối qua Amazon CloudFront CDN kèm chứng chỉ ACM SSL. |
| 5 | - **Kiểm thử hệ thống & Đánh giá Well-Architected:**<br>&emsp;+ Thực hiện kiểm thử tải (Load Testing), kiểm tra cơ chế Auto Scaling và mô phỏng failover database.<br>&emsp;+ Tích hợp AWS WAF bảo vệ ALB và cấu hình CloudWatch Dashboard, Alarms giám sát toàn diện.<br>&emsp;+ Sử dụng công cụ AWS Well-Architected Tool để rà soát kiến trúc theo 6 trụ cột và ghi nhận các điểm cải tiến. |
| 6 | - **Tổng kết chương trình & Báo cáo tốt nghiệp:**<br>&emsp;+ Rà soát và hoàn thiện toàn bộ tài liệu báo cáo thực tập, nhật ký công việc (Worklog 12 tuần) và mã nguồn trên GitHub.<br>&emsp;+ Thuyết trình bảo vệ đồ án Capstone trước Hội đồng đánh giá và Mentor chương trình FCAJ.<br>&emsp;+ Nhận xét, đánh giá kết quả từ Mentor và đề ra kế hoạch ôn luyện các chứng chỉ AWS Certified Solutions Architect. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Triển khai Đồ án Capstone 3-Tier Enterprise & Đánh giá AWS Well-Architected Framework
Trong tuần cuối cùng, em đã thiết kế và triển khai thành công một giải pháp Cloud hoàn chỉnh đạt chuẩn doanh nghiệp (Enterprise 3-Tier Cloud Solution). Hệ thống kết hợp đầy đủ: CloudFront + S3 (Presentation Tier), Application Load Balancer + Amazon ECS Fargate Auto Scaling (Application Tier), và Amazon RDS MySQL Multi-AZ + ElastiCache (Database Tier) trong một Custom VPC cô lập chặt chẽ. Hệ thống được bảo vệ bởi AWS WAF và KMS, tự động hóa cập nhật mã nguồn bằng CI/CD CodePipeline và giám sát tập trung bởi CloudWatch. Em đã sử dụng công cụ AWS Well-Architected Tool để rà soát và tối ưu toàn diện đồ án.

---

### Kết quả và thành tựu đạt được:

* Tự thiết kế và triển khai thành công một giải pháp Cloud hoàn chỉnh quy mô Enterprise tích hợp hơn 15 dịch vụ AWS.
* Làm chủ phương pháp đánh giá và chuẩn hóa kiến trúc hạ tầng theo 6 trụ cột của AWS Well-Architected Framework.
* Vận dụng nhuần nhuyễn các kỹ năng về Mạng (VPC), Điện toán (Fargate), Cơ sở dữ liệu (RDS Multi-AZ), Bảo mật (WAF/KMS) và Tự động hóa (CI/CD).
* Nâng cao vượt bậc tư duy giải quyết vấn đề, khả năng xử lý sự cố (troubleshooting) và phân tích tối ưu chi phí trong môi trường thực tế.
* Hoàn thành xuất sắc toàn bộ chương trình thực tập 12 tuần của First Cloud AI Journey (FCAJ), tạo tiền đề vững chắc trên con đường trở thành Cloud Solutions Architect.
