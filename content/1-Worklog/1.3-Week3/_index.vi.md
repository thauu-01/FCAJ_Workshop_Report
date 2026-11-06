---
title: "Worklog Tuần 3"
date: 2026-10-16
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Làm chủ dịch vụ lưu trữ đối tượng Amazon Simple Storage Service (S3).
* Triển khai Static Website Hosting, quản lý Bucket Policies, CORS và Versioning trên S3.
* Tìm hiểu hệ thống phân giải tên miền toàn cầu Amazon Route 53 và các chiến lược định tuyến.
* Tăng tốc độ truyền tải nội dung toàn cầu và bảo mật với Amazon CloudFront CDN kết hợp AWS Certificate Manager (ACM).

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu Amazon S3: Cấu trúc Bucket/Object, khóa định danh (Key), metadata.<br>- Phân tích các lớp lưu trữ (S3 Storage Classes): Standard, Intelligent-Tiering, Standard-IA, One Zone-IA, Glacier Instant/Flexible/Deep Archive.<br>- Cấu hình S3 Lifecycle Rules để tự động chuyển đổi lớp lưu trữ và tối ưu hóa chi phí. |
| 3 | - Thực hành cấu hình S3 Static Website Hosting (index.html, error.html).<br>- Tắt Block Public Access và thiết lập Bucket Policy JSON cho phép truy xuất công khai an toàn.<br>- Kích hoạt tính năng S3 Versioning và Server-Side Encryption (SSE-S3, SSE-KMS). |
| 4 | - Tìm hiểu Amazon Route 53: Khái niệm Hosted Zones (Public vs Private), Domain Registration.<br>- Phân biệt các bản ghi DNS: A, AAAA, CNAME, ALIAS Records.<br>- Khảo sát các chính sách định tuyến (Routing Policies): Simple, Weighted, Latency, Failover, Geolocation. |
| 5 | - Tìm hiểu mạng lưới phân phối nội dung Amazon CloudFront (CDN): Edge Locations, Regional Edge Caches.<br>- Cấu hình CloudFront Distribution trỏ đến S3 Origin.<br>- Áp dụng Origin Access Control (OAC) để khóa hoàn toàn quyền đọc trực tiếp từ S3, buộc người dùng truy cập qua CDN. |
| 6 | - **Thực hành tích hợp toàn diện:** Khởi tạo chứng chỉ SSL/TLS miễn phí với AWS Certificate Manager (ACM).<br>- Gắn tên miền tùy chỉnh vào CloudFront Distribution qua Route 53 Alias Record.<br>- Xác thực phân phối HTTPS tốc độ cao trên toàn cầu, kiểm tra cơ chế Cache Invalidation khi cập nhật mã nguồn. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Triển khai Static Website toàn cầu tốc độ cao với S3, CloudFront & Route 53
Trong bài thực hành này, tôi đã lưu trữ trang web tĩnh lên Amazon S3, kích hoạt Versioning và mã hóa SSE-S3. Sau đó, tôi cấu hình Amazon CloudFront Distribution với Origin Access Control (OAC) để bảo mật tuyệt đối cho bucket (chặn toàn bộ truy cập public trực tiếp vào S3). Cuối cùng, tôi tích hợp Route 53 và chứng chỉ SSL từ AWS Certificate Manager (ACM) để cung cấp trải nghiệm duyệt web HTTPS an toàn, tốc độ phản hồi cực nhanh từ các Edge Location gần nhất.

---

### Kết quả và thành tựu đạt được:

* Nắm vững kiến trúc lưu trữ đối tượng S3, cơ chế phân lớp lưu trữ và quản trị vòng đời dữ liệu Lifecycle Policies.
* Thành thạo cấu hình phân quyền dữ liệu S3 với Bucket Policies, CORS và kiểm soát truy cập công khai.
* Hiểu sâu cơ chế hoạt động của DNS toàn cầu và cấu hình các bản ghi Route 53 Alias tối ưu.
* Triển khai thành công CDN CloudFront kết hợp OAC và chứng chỉ ACM giúp tăng tốc độ tải trang và bảo mật HTTPS.
* Hiểu rõ phương thức vô hiệu hóa bộ nhớ đệm (Cache Invalidation) khi triển khai phiên bản web mới.
