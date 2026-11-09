---
title: "Worklog Tuần 11"
date: 2026-12-17
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Nghiên cứu các chiến lược duy trì tính liên tục của doanh nghiệp, sao lưu tập trung và phục hồi thảm họa (Disaster Recovery - DR).
* Làm chủ dịch vụ sao lưu tập trung AWS Backup: Backup Plans, Backup Vaults, Lifecycle Rules và Cross-Region Backup.
* Hiểu và ứng dụng các mô hình phục hồi thảm họa trên Cloud: Backup & Restore, Pilot Light, Warm Standby, Multi-Region Active-Active.
* Làm chủ công cụ quản lý chi phí AWS Cost Explorer, AWS Budgets và tối ưu hóa hạ tầng với AWS Trusted Advisor.

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu các chỉ số cốt lõi trong Phục hồi thảm họa: Thời gian phục hồi mục tiêu (RTO - Recovery Time Objective) và Điểm phục hồi mục tiêu (RPO - Recovery Point Objective).<br>- Phân tích 4 chiến lược Disaster Recovery trên AWS: Backup & Restore, Pilot Light, Warm Standby, Multi-Site Active/Active.<br>- Đánh giá mối quan hệ tương quan giữa chi phí đầu tư và thời gian phục hồi RTO/RPO. |
| 3 | - Tìm hiểu dịch vụ sao lưu tập trung AWS Backup: Backup Plans, Backup Rules, Backup Vaults, Vault Lock.<br>- Cấu hình lịch sao lưu tự động (Daily, Weekly, Monthly) cho nhiều dịch vụ: Amazon EC2, EBS, RDS, DynamoDB, S3.<br>- Thiết lập chính sách chuyển đổi bản sao lưu sang Cold Storage sau 30 ngày và tự động xóa sau 365 ngày.<br>- Cấu hình Cross-Region Backup: Sao chép bản backup sang Region thứ hai phục vụ kịch bản thảm họa toàn vùng. |
| 4 | - Nghiên cứu bộ công cụ Quản lý chi phí AWS Cost Management: AWS Billing Dashboard, Cost Allocation Tags (Environment, Project, Owner).<br>- Sử dụng AWS Cost Explorer để phân tích chi phí lịch sử, xu hướng chi tiêu và dự báo chi phí tháng tới.<br>- Phân tích chi phí theo từng dịch vụ, khu vực và các loại phí truyền dữ liệu (Data Transfer costs). |
| 5 | - Thiết lập ngân sách với AWS Budgets: Tạo Cost Budget theo dõi chi tiêu hàng tháng.<br>- Cấu hình cảnh báo thông minh: Gửi email khi chi phí thực tế đạt 80% ngân sách hoặc khi chi phí dự báo (Forecasting) có nguy cơ vượt 100% ngân sách.<br>- Tìm hiểu các mô hình cam kết tiết kiệm chi phí dài hạn: Compute Savings Plans, EC2 Instance Savings Plans, Reserved Instances (RI). |
| 6 | - **Thực hành kiểm thử DR & Tối ưu chi phí:** Thực hiện khôi phục (Restore) máy chủ EC2 và cơ sở dữ liệu RDS từ bản sao lưu AWS Backup và kiểm tra tính toàn vẹn của dữ liệu.<br>- Chạy đánh giá AWS Trusted Advisor trên 5 trụ cột (Cost Optimization, Performance, Security, Fault Tolerance, Service Limits).<br>- Xác định và thu hồi các tài nguyên nhàn rỗi gây lãng phí: Xóa các ổ EBS Volume unattached, giải phóng Elastic IP không sử dụng. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Thiết lập sao lưu tự động với AWS Backup & Tối ưu hóa chi phí với AWS Budgets
Trong bài thực hành tuần 11, em đã cấu hình một Backup Plan tập trung trên AWS Backup để tự động tạo snapshot hàng ngày cho toàn bộ cụm máy chủ EC2 và Amazon RDS, đồng thời kích hoạt chính sách sao chép Cross-Region sang vùng dự phòng. Em cũng đã thực hành kịch bản giả lập sự cố và thực hiện khôi phục thành công dữ liệu từ Recovery Point. Về mặt quản trị tài chính, em gắn thẻ Cost Allocation Tags cho toàn bộ tài nguyên, thiết lập AWS Budgets gửi cảnh báo qua email khi chi phí vượt 80% ngưỡng định mức, và dọn dẹp các tài nguyên dư thừa theo gợi ý của Trusted Advisor.

---

### Kết quả và thành tựu đạt được:

* Hiểu sâu các mô hình chiến lược phục hồi thảm họa (DR) và tối ưu hóa hai chỉ số then chốt RTO và RPO.
* Tập trung hóa công tác sao lưu dữ liệu toàn doanh nghiệp với chính sách vòng đời và sao lưu chéo vùng của AWS Backup.
* Thực hành thành công kịch bản phục hồi dữ liệu từ Recovery Point, đảm bảo tính liên tục của hệ thống.
* Làm chủ công cụ phân tích tài chính AWS Cost Explorer và thiết lập cảnh báo ngân sách tự động với AWS Budgets.
* Áp dụng thành công các khuyến nghị từ AWS Trusted Advisor để cắt giảm chi phí lãng phí và rightsizing tài nguyên.
