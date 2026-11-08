---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Dưới đây là danh sách các bài viết kỹ thuật chuyên sâu về các dịch vụ điện toán đám mây AWS mà tôi đã biên soạn và chia sẻ trên cộng đồng [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj):

---

### [Blog 1 - Host website tĩnh trên Amazon S3: Từ triển khai cơ bản đến bảo mật với CloudFront](3.1-Blog1/)
Bài viết phân tích hai phương án triển khai website tĩnh trên AWS: sử dụng S3 Static Website Hosting (học tập/thử nghiệm) và giải pháp tối ưu kết hợp **S3 Private Bucket với CloudFront Origin Access Control (OAC)** chuẩn production. Đồng thời, bài viết hướng dẫn xử lý triệt để lỗi routing cho React Single Page Application (lỗi 403/404 khi refresh trang), thiết lập chiến lược bộ nhớ đệm `Cache-Control` thông minh, tối ưu lệnh CloudFront Invalidation và kiểm soát chi phí hiệu quả với AWS Budgets.

### [Blog 2 - Triển khai ứng dụng Docker trên AWS với Amazon ECS và AWS Fargate](3.2-Blog2/)
Bài viết hướng dẫn toàn diện quy trình vận hành ứng dụng container hóa trên nền tảng Serverless Container của AWS: từ việc lưu trữ image trên **Amazon ECR**, điều phối vòng đời container với **Amazon ECS (Task Definition, Task, Service)**, đến việc chạy ứng dụng không cần quản lý máy chủ với **AWS Fargate**. Ngoài ra, bài viết phân tích sâu sự khác biệt giữa **Task Execution Role vs. Task Role**, thiết kế mạng bảo mật đa tầng với **Application Load Balancer (ALB)** trong Private Subnets, triển khai không gián đoạn (Zero-Downtime Rolling Update) và các giải pháp tối ưu chi phí với Fargate Spot và VPC Endpoints.

### [Blog 3 - ...](3.3-Blog3/)
*(Bài viết kỹ thuật đang được cập nhật...)*
