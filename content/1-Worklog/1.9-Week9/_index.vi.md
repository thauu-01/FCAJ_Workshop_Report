---
title: "Worklog Tuần 9"
date: 2026-12-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Nghiên cứu văn hóa và quy trình DevOps, các nguyên lý Tích hợp liên tục và Triển khai liên tục (CI/CD).
* Làm chủ bộ công cụ lập trình viên của AWS: AWS CodeCommit, AWS CodeBuild, AWS CodeDeploy và AWS CodePipeline.
* Viết cấu hình build tự động với tệp `buildspec.yml` và kịch bản triển khai với tệp `appspec.yml`.
* Xây dựng đường ống tự động hóa hoàn chỉnh từ khi lập trình viên commit mã nguồn cho đến khi triển khai lên môi trường Production.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Tìm hiểu triết lý DevOps và quy trình CI/CD: Continuous Integration (tự động build & test), Continuous Delivery và Continuous Deployment.<br>- Khảo sát kiến trúc bộ công cụ AWS Developer Tools và so sánh với các công cụ nguồn mở phổ biến (GitHub Actions, Jenkins, GitLab CI). |
| 3 | - Tìm hiểu AWS CodeCommit: Quản trị Git repository an toàn trên AWS, phân quyền truy cập qua IAM và HTTPS/SSH Git credentials.<br>- Nghiên cứu AWS CodeBuild: Cơ chế khởi tạo Build Environment container, quản lý artifact và báo cáo kiểm thử.<br>- Soạn thảo tệp cấu hình `buildspec.yml`: Các pha `install`, `pre_build`, `build`, `post_build`. |
| 4 | - Nghiên cứu AWS CodeDeploy: Deployment Groups, Deployment Configurations (AllAtOnce, HalfAtATime, OneAtATime).<br>- Phân biệt các chiến lược triển khai: In-Place Deployment và Blue/Green Deployment (giảm thiểu rủi ro downtime).<br>- Soạn thảo tệp cấu hình `appspec.yml` và các lifecycle event hooks (`BeforeInstall`, `AfterInstall`, `ApplicationStart`, `ValidateService`). |
| 5 | - Tìm hiểu dịch vụ điều phối tự động AWS CodePipeline: Pipeline Stages (Source, Build, Test, Deploy), Triggers và Artifact Stores (Amazon S3).<br>- Tích hợp thông báo qua Amazon SNS khi pipeline chuyển trạng thái (Success, Failed).<br>- Cấu hình Manual Approval Stage trước khi đưa code lên môi trường Production. |
| 6 | - **Thực hành triển khai Pipeline CI/CD hoàn chỉnh:** Xây dựng luồng CI/CD tự động cho ứng dụng web container.<br>- Push mã nguồn lên Git -> CodePipeline tự động kích hoạt -> CodeBuild biên dịch và build Docker image đẩy vào ECR -> CodeDeploy cập nhật ECS Fargate Service.<br>- Kiểm tra quy trình triển khai thành công và kiểm tra cơ chế tự động Rollback khi bài kiểm thử thất bại. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Xây dựng đường ống CI/CD tự động hoàn chỉnh với AWS CodePipeline & CodeBuild
Trong bài thực hành tuần này, em đã thiết lập một đường ống CI/CD tự động hóa end-to-end với AWS CodePipeline. Khi có commit mới được đẩy lên nhánh `main`, CodePipeline tự động tải mã nguồn, chuyển tiếp tới AWS CodeBuild để cài đặt dependencies, chạy các bài unit test tự động và đóng gói Docker image với thẻ commit SHA. Sau khi image được đẩy thành công lên Amazon ECR, CodePipeline kích hoạt bước deploy để cập nhật Task Definition của dịch vụ Amazon ECS Fargate mà không làm gián đoạn người dùng.

---

### Kết quả và thành tựu đạt được:

* Hiểu sâu sắc các nguyên lý CI/CD và kiến trúc tự động hóa DevOps hiện đại trên nền tảng AWS.
* Làm chủ cú pháp và các pha thực thi trong tệp cấu hình `buildspec.yml` và `appspec.yml`.
* Phân biệt rõ ràng và lựa chọn linh hoạt giữa các chiến lược triển khai In-Place vs Blue/Green Deployment.
* Tích hợp thành công chuỗi công cụ AWS CodeCommit, CodeBuild, CodeDeploy và CodePipeline thành luồng khép kín.
* Thiết lập cổng phê duyệt thủ công (Manual Approval) và cơ chế tự động Rollback an toàn cho hệ thống Production.
