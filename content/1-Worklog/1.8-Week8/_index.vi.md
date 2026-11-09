---
title: "Worklog Tuần 8"
date: 2026-11-24
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Nghiên cứu công nghệ Containerization và làm chủ Docker: Xây dựng Dockerfile, tối ưu image đa tầng (Multi-stage build).
* Quản lý, bảo mật và quét lỗ hổng image container trên Amazon Elastic Container Registry (ECR).
* Tìm hiểu nền tảng điều phối container Amazon Elastic Container Service (ECS): Clusters, Task Definitions, Services.
* Triển khai ứng dụng container trên nền tảng Serverless AWS Fargate và cân bằng tải với Application Load Balancer.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu sự khác biệt cốt lõi giữa Containers (chia sẻ OS kernel, nhẹ, khởi động tức thì) và Virtual Machines (hypervisor, nặng).<br>- Nắm vững kiến trúc Docker: Docker Engine, Images, Containers, Dockerfile instructions (`FROM`, `WORKDIR`, `COPY`, `RUN`, `CMD`, `EXPOSE`).<br>- Viết Dockerfile tối ưu kích thước image với kỹ thuật Multi-stage build. |
| 3 | - Tìm hiểu Amazon Elastic Container Registry (ECR): Private Repositories, Image Tagging, KMS Encryption.<br>- Đăng nhập Docker client vào AWS ECR thông qua lệnh `aws ecr get-login-password`.<br>- Build Docker image cục bộ, gắn thẻ (tag) và push lên ECR repository.<br>- Kích hoạt tính năng Scan on Push để quét lỗ hổng bảo mật (CVE) của container image. |
| 4 | - Khám phá Amazon Elastic Container Service (ECS): So sánh EC2 Launch Type (tự quản trị máy chủ cụm) và AWS Fargate (Serverless, không cần quản trị máy chủ).<br>- Thiết kế ECS Task Definition: Khai báo tài nguyên CPU/RAM, Container Definitions, Port Mappings, IAM Task Role và Task Execution Role.<br>- Nghiên cứu ECS Services: Quản lý số lượng Task duy trì (Desired count) và chiến lược triển khai Rolling Updates. |
| 5 | - Cấu hình ECS Cluster và triển khai ECS Service chạy trên AWS Fargate.<br>- Tích hợp ECS Service với Application Load Balancer để tiếp nhận lưu lượng truy cập từ Internet.<br>- Cấu hình định tuyến cổng (Target Group) và thiết lập Health Check kiểm tra trạng thái hoạt động của Container Tasks. |
| 6 | - **Thực hành cập nhật phiên bản:** Thay đổi mã nguồn ứng dụng, đóng gói phiên bản image mới v2.0 và đẩy lên ECR.<br>- Cập nhật Task Definition và kích hoạt Rolling Update trên ECS Service.<br>- Quan sát quá trình Fargate khởi tạo các Task mới, chuyển đổi traffic qua ALB và hủy các Task cũ mà không gây gián đoạn dịch vụ (Zero-Downtime Deployment). |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Đóng gói ứng dụng với Docker & Triển khai Microservices trên Amazon ECS Fargate
Trong bài thực hành tuần này, em đã đóng gói một ứng dụng web microservice bằng Dockerfile tối ưu đa tầng (multi-stage), sau đó đẩy image lên Amazon ECR với tính năng quét lỗ hổng tự động. Tiếp theo, em cấu hình một ECS Cluster sử dụng AWS Fargate để chạy các containers mà hoàn toàn không cần quản lý máy chủ EC2 bên dưới. ECS Service được kết nối với Application Load Balancer để tự động phân phối tải và thực hiện cập nhật phiên bản ứng dụng theo cơ chế Rolling Update mượt mà không có downtime.

---

### Kết quả và thành tựu đạt được:

* Nắm vững kỹ thuật đóng gói container Docker tối ưu dung lượng và bảo mật.
* Làm chủ quy trình lưu trữ, quản lý vòng đời và quét lỗ hổng bảo mật image với Amazon ECR.
* Hiểu sâu kiến trúc điều phối container của Amazon ECS và sự khác biệt giữa EC2 vs Fargate Launch Types.
* Triển khai thành công ứng dụng web microservices trên nền tảng Serverless AWS Fargate kết hợp ALB.
* Thành thạo cơ chế triển khai không gián đoạn (Zero-Downtime Rolling Update) cho các ứng dụng container hóa.
