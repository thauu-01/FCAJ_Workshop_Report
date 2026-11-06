---
title: "Worklog Tuần 10"
date: 2026-12-09
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Nghiên cứu kiến trúc bảo mật đa lớp (Defense-in-Depth) theo tiêu chuẩn AWS Well-Architected Security Pillar.
* Làm chủ dịch vụ mã hóa dữ liệu AWS Key Management Service (KMS) và quản lý bí mật với AWS Secrets Manager.
* Bảo vệ ứng dụng web trước các cuộc tấn công mạng phổ biến với tường lửa AWS WAF (Web Application Firewall).
* Phát hiện các mối đe dọa an ninh tự động với Amazon GuardDuty và quản trị tuân thủ an toàn với AWS Security Hub.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu 7 nguyên tắc thiết kế bảo mật trên Cloud của AWS.<br>- Áp dụng IAM Best Practices nâng cao: Phân tích quyền với IAM Access Analyzer, thực thi MFA bắt buộc qua Condition Keys trong JSON Policy.<br>- Tìm hiểu IAM Permission Boundaries và Service Control Policies (SCP) trong môi trường AWS Organizations. |
| 3 | - Tìm hiểu AWS Key Management Service (KMS): Khái niệm Customer Managed Keys (CMK), AWS Managed Keys, Envelope Encryption.<br>- Cấu hình Key Policies phân quyền mã hóa/giải mã.<br>- Áp dụng mã hóa dữ liệu nghỉ (Encryption at Rest) cho S3 Buckets, EBS Volumes và RDS Instances.<br>- Nghiên cứu AWS Secrets Manager: Lưu trữ thông tin đăng nhập DB, cấu hình tự động xoay vòng mật khẩu (Automatic Rotation via Lambda). |
| 4 | - Khám phá tường lửa tầng ứng dụng AWS WAF (Web Application Firewall): Web ACLs, Rule Groups, Rules.<br>- Kích hoạt AWS Managed Rules: Core Rule Set (CRS), SQL Injection Rule Set, Known Bad Inputs.<br>- Cấu hình Rate-based Rules chống tấn công từ chối dịch vụ (DDoS tầng ứng dụng) và brute-force login.<br>- Gắn Web ACL vào Application Load Balancer và CloudFront. |
| 5 | - Nghiên cứu Amazon GuardDuty: Dịch vụ phát hiện mối đe dọa thông minh sử dụng Machine Learning phân tích dữ liệu từ VPC Flow Logs, DNS Query Logs, CloudTrail Events.<br>- Kích hoạt AWS Security Hub: Tổng hợp các phát hiện bảo mật từ GuardDuty, IAM Access Analyzer, Inspector.<br>- Đánh giá mức độ tuân thủ theo tiêu chuẩn CIS AWS Foundations Benchmark và AWS Foundational Security Best Practices. |
| 6 | - **Thực hành kiểm thử phòng thủ đa lớp:** Gửi các request độc hại (chứa SQL injection payload \`OR 1=1\`) tới ALB và kiểm tra AWS WAF chặn đứng request với mã lỗi HTTP 403 Forbidden.<br>- Thực hiện xoay vòng mật khẩu database tự động với Secrets Manager và kiểm tra ứng dụng vẫn kết nối thông suốt.<br>- Phân tích báo cáo phát hiện và khắc phục các lỗ hổng trên bảng điều khiển Security Hub. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Thiết lập bảo vệ đa lớp với AWS KMS, Secrets Manager, AWS WAF & Security Hub
Trong bài thực hành này, tôi đã triển khai chiến lược bảo mật toàn diện cho hệ thống. Toàn bộ cơ sở dữ liệu và ổ đĩa được mã hóa bằng khóa tùy chỉnh AWS KMS CMK. Thông tin mật khẩu database được lưu trong AWS Secrets Manager và thiết lập cơ chế tự động xoay vòng định kỳ. Ở lớp ngoài cùng, tôi đã cấu hình AWS WAF Web ACL gắn trực tiếp vào Application Load Balancer để ngăn chặn các cuộc tấn công web theo OWASP Top 10 (SQLi, XSS) và kích hoạt Amazon GuardDuty cùng AWS Security Hub để giám sát tuân thủ an toàn liên tục.

---

### Kết quả và thành tựu đạt được:

* Làm chủ kiến trúc bảo mật Defense-in-Depth và các nguyên tắc bảo mật chuẩn AWS Well-Architected.
* Thành thạo mã hóa dữ liệu nghỉ (at-rest) và dữ liệu truyền tải (in-transit) với AWS KMS Envelope Encryption.
* Triển khai thành công quản lý và tự động xoay vòng thông tin xác thực với AWS Secrets Manager.
* Bảo vệ thành công hệ thống trước các cuộc tấn công web nguy hiểm nhờ tường lửa AWS WAF và Rate-limiting.
* Ứng dụng Amazon GuardDuty và AWS Security Hub để theo dõi an ninh và đánh giá tuân thủ tự động.
