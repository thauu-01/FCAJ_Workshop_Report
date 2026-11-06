---
title: "Worklog Tuần 1"
date: 2026-10-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Làm quen với môi trường, các thành viên và lộ trình chương trình First Cloud AI Journey (FCAJ).
* Hiểu vững nền tảng điện toán đám mây và hạ tầng toàn cầu của AWS (Regions, Availability Zones, Edge Locations).
* Khởi tạo, bảo mật tài khoản AWS Free Tier và thiết lập quản trị danh tính với AWS IAM theo nguyên tắc Least Privilege.
* Cài đặt, cấu hình thành thạo AWS CLI v2 và làm quen với dịch vụ máy chủ ảo Amazon EC2.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Gặp gỡ và kết nối với các thành viên và các anh chị Admin chương trình FCAJ.<br>- Đọc và nắm vững nội quy thực tập, quy chuẩn văn hóa và lộ trình đào tạo 12 tuần.<br>- Chuẩn bị môi trường máy trạm: cài đặt Visual Studio Code, Git, Terminal. |
| 3 | - Tìm hiểu nền tảng của Cloud Computing và các mô hình dịch vụ (IaaS, PaaS, SaaS).<br>- Phân tích mô hình trách nhiệm chung (AWS Shared Responsibility Model).<br>- Khảo sát hạ tầng toàn cầu AWS: Regions, Availability Zones (AZ), Edge Locations. |
| 4 | - Đăng ký tài khoản AWS Free Tier và kích hoạt xác thực đa yếu tố (MFA) cho Root Account.<br>- Tìm hiểu AWS Identity and Access Management (IAM): Users, User Groups, Policies, Roles.<br>- Tạo tài khoản IAM Administrator độc lập và áp dụng nguyên tắc đặc quyền tối thiểu (Least Privilege). |
| 5 | - Cài đặt AWS CLI v2 trên hệ điều hành cục bộ.<br>- Cấu hình Access Key ID, Secret Access Key, Default Region và Output Format qua `aws configure`.<br>- Thực hành các lệnh AWS CLI cơ bản: kiểm tra danh tính (`sts get-caller-identity`), liệt kê tài nguyên EC2, S3. |
| 6 | - Nghiên cứu kiến trúc Amazon EC2: Instance Types (t2/t3.micro), AMI, EBS storage, Key Pairs.<br>- Cấu hình Security Group cho phép truy cập SSH (port 22) từ IP an toàn.<br>- Khởi chạy một Linux EC2 instance và thực hiện kết nối SSH từ máy trạm. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Khởi tạo tài khoản AWS an toàn & Triển khai máy chủ Amazon EC2
Trong bài thực hành tuần đầu tiên, tôi đã thực hiện thiết lập bảo mật cấp cao cho AWS Root Account bằng Virtual MFA, tạo IAM Admin Group có chính sách kiểm soát chặt chẽ và tắt toàn bộ Access Key của tài khoản Root. Tiếp theo, tôi cấu hình AWS CLI v2 trên máy trạm cá nhân và dùng lệnh CLI để khởi chạy một máy chủ ảo EC2 chạy Amazon Linux 2023 kèm EBS Volume (gp3), gán Key Pair bảo mật và kết nối thành công qua SSH.

---

### Kết quả và thành tựu đạt được:

* Nắm vững các mô hình điện toán đám mây và mô hình chia sẻ trách nhiệm (Shared Responsibility Model).
* Bảo mật thành công AWS Account bằng MFA và áp dụng kiến trúc IAM đạt chuẩn CIS AWS Foundations Benchmark.
* Sử dụng thành thạo AWS Management Console và AWS CLI v2 để truy xuất thông tin tài nguyên.
* Khởi chạy, quản lý vòng đời và kết nối an toàn vào máy chủ tính toán Amazon EC2.
* Xây dựng nền tảng vững chắc để chuyển sang thiết kế hệ thống mạng đám mây ở Tuần 2.
