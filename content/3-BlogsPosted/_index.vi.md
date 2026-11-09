---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Dưới đây là danh sách các bài viết kỹ thuật chuyên sâu về các dịch vụ điện toán đám mây AWS mà em đã biên soạn và chia sẻ trên cộng đồng [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj):

---

### [Blog 1 - Host website tĩnh trên Amazon S3: Từ triển khai cơ bản đến bảo mật với CloudFront](3.1-Blog1/)
* 🔗 **Link bài viết trên AWS Study Group:** [Xem bài đăng trên Facebook](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2320770352021257/)

Bài viết phân tích hai phương án triển khai website tĩnh trên AWS: sử dụng S3 Static Website Hosting (học tập/thử nghiệm) và giải pháp tối ưu kết hợp **S3 Private Bucket với CloudFront Origin Access Control (OAC)** chuẩn production. Đồng thời, bài viết hướng dẫn xử lý triệt để lỗi routing cho React Single Page Application (lỗi 403/404 khi refresh trang), thiết lập chiến lược bộ nhớ đệm `Cache-Control` thông minh, tối ưu lệnh CloudFront Invalidation và kiểm soát chi phí hiệu quả với AWS Budgets.

---

### [Blog 2 - Triển khai ứng dụng Docker trên AWS với Amazon ECS và AWS Fargate](3.2-Blog2/)
* 🔗 **Link bài viết trên AWS Study Group:** [Xem bài đăng trên Facebook](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2323062025125423/)

Bài viết hướng dẫn toàn diện quy trình vận hành ứng dụng container hóa trên nền tảng Serverless Container của AWS: từ việc lưu trữ image trên **Amazon ECR**, điều phối vòng đời container với **Amazon ECS (Task Definition, Task, Service)**, đến việc chạy ứng dụng không cần quản lý máy chủ với **AWS Fargate**. Ngoài ra, bài viết phân tích sâu sự khác biệt giữa **Task Execution Role vs. Task Role**, thiết kế mạng bảo mật đa tầng với **Application Load Balancer (ALB)** trong Private Subnets, triển khai không gián đoạn (Zero-Downtime Rolling Update) và các giải pháp tối ưu chi phí với Fargate Spot và VPC Endpoints.

---

### [Blog 3 - Xây dựng Serverless REST API với AWS Lambda, API Gateway và DynamoDB](3.3-Blog3/)
* 🔗 **Link bài viết trên AWS Study Group:** [Xem bài đăng trên Facebook](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2325505481547744/)

Bài viết trình bày chi tiết quy trình xây dựng hệ thống backend RESTful API phi máy chủ (Serverless) hoàn chỉnh với đầy đủ các thao tác CRUD: tiếp nhận và định tuyến lưu lượng qua **Amazon API Gateway (HTTP API)**, xử lý logic nghiệp vụ theo sự kiện với **AWS Lambda (Node.js & AWS SDK v3)**, và lưu trữ dữ liệu hiệu năng cao với **Amazon DynamoDB (On-Demand Mode)**. Bài viết so sánh chuyên sâu giữa **HTTP API vs. REST API**, phân tích nguy cơ của thao tác `Scan`, hướng dẫn cấu hình CORS, tối ưu hóa Cold Start và quản lý định danh IAM theo nguyên tắc đặc quyền tối thiểu.
