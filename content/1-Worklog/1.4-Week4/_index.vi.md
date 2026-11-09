---
title: "Worklog Tuần 4"
date: 2026-10-24
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Nghiên cứu các giải pháp cơ sở dữ liệu trên AWS: RDBMS quan hệ, NoSQL và In-Memory Caching.
* Làm chủ dịch vụ cơ sở dữ liệu quan hệ Amazon RDS (MySQL/PostgreSQL) với kiến trúc Multi-AZ và Read Replicas.
* Tìm hiểu cơ sở dữ liệu NoSQL phi quan hệ siêu tốc Amazon DynamoDB với mô hình Key-Value và Document.
* Khám phá giải pháp bộ nhớ đệm Amazon ElastiCache (Redis) nhằm tối ưu độ trễ cho tầng dữ liệu.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu Amazon Relational Database Service (RDS): Các database engines được hỗ trợ, DB Instance classes.<br>- Cấu hình DB Subnet Groups trải rộng trên các Private Subnets của ít nhất 2 Availability Zones.<br>- Phân tích cơ chế sao lưu tự động (Automated Backups), Retention Period và Point-In-Time Recovery (PITR). |
| 3 | - Phân tích chuyên sâu kiến trúc RDS Multi-AZ phục vụ High Availability (đồng bộ sang Standby DB) vs Read Replicas phục vụ mở rộng đọc (bất đồng bộ).<br>- Khởi chạy một RDS MySQL instance trong Private Subnet và cấu hình Security Group chỉ chấp nhận kết nối từ Application Server. |
| 4 | - Tìm hiểu cơ sở dữ liệu NoSQL phân tán Amazon DynamoDB: Tables, Items, Attributes.<br>- Thiết kế khóa chính: Partition Key (HASH) và Composite Key (HASH + RANGE).<br>- Phân tích các chế độ tính toán dung lượng: On-Demand Capacity vs Provisioned Capacity Mode.<br>- Nghiên cứu chỉ mục phụ: Local Secondary Indexes (LSI) và Global Secondary Indexes (GSI). |
| 5 | - Tìm hiểu dịch vụ In-Memory Cache Amazon ElastiCache: So sánh Redis (hỗ trợ data structures, clustering, persistence) và Memcached (đơn giản, multi-threading).<br>- Khảo sát các chiến lược Caching phổ biến: Cache-Aside (Lazy Loading) và Write-Through.<br>- Đánh giá kiến trúc giảm tải cho cơ sở dữ liệu quan hệ bằng tầng đệm Redis. |
| 6 | - **Thực hành:** Kết nối từ máy chủ EC2 vào RDS MySQL để thực hiện tạo Schema, Index và truy vấn dữ liệu.<br>- Tạo bảng DynamoDB qua AWS CLI, chèn dữ liệu JSON và truy vấn theo Partition Key và GSI.<br>- Thực hiện kiểm tra thời gian đáp ứng giữa RDS và DynamoDB. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Triển khai Amazon RDS MySQL Multi-AZ & Quản lý dữ liệu NoSQL với DynamoDB
Trong bài lab tuần này, em đã tạo DB Subnet Group trên 2 Private Subnets và triển khai một Amazon RDS MySQL instance với cấu hình Multi-AZ để đảm bảo khả năng tự động chuyển đổi dự phòng (failover). Em kết nối an toàn từ EC2 thông qua MySQL client, tạo database và kiểm tra snapshot tự động. Tiếp đó, em thiết kế bảng dữ liệu DynamoDB quản lý thông tin phiên làm việc, thiết lập GSI để tối ưu hóa truy vấn và đánh giá độ trễ milisecond của NoSQL.

---

### Kết quả và thành tựu đạt được:

* Hiểu rõ sự khác biệt giữa các dịch vụ cơ sở dữ liệu trên AWS và chọn đúng dịch vụ cho từng bài toán nghiệp vụ.
* Triển khai thành công Amazon RDS Multi-AZ trong mạng Private an toàn, bảo mật thông tin xác thực.
* Làm chủ kỹ thuật thiết kế khóa Partition Key, Sort Key và chỉ mục GSI trên Amazon DynamoDB.
* Nắm vững nguyên lý hoạt động của tầng đệm In-Memory ElastiCache và các chiến lược Caching.
* Tích hợp thành thạo ứng dụng với cả hai mô hình lưu trữ quan hệ (RDBMS) và NoSQL trên AWS.
