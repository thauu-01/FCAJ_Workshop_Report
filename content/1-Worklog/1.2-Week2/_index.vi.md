---
title: "Worklog Tuần 2"
date: 2026-10-09
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Nắm vững kiến trúc mạng ảo đám mây với Amazon Virtual Private Cloud (VPC).
* Hiểu và phân bổ dải địa chỉ IP qua kỹ thuật CIDR Block và phân tách Public / Private Subnets.
* Thiết lập định tuyến với Internet Gateway, NAT Gateway và Route Tables.
* Làm chủ các cơ chế bảo mật mạng đa lớp với Security Groups (Stateful) và Network ACLs (Stateless).

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu kiến trúc Amazon VPC, dải địa chỉ mạng riêng RFC 1918 và cơ chế tính toán CIDR (`10.0.0.0/16`).<br>- Phân tích khái niệm Public Subnet, Private Subnet và tính sẵn sàng cao (High Availability) qua Multi-AZ.<br>- Tìm hiểu cấu trúc Route Table và cơ chế định tuyến nội bộ (Local Route). |
| 3 | - Tìm hiểu Internet Gateway (IGW) và cơ chế gắn kết với VPC.<br>- Cấu hình Route Table cho Public Subnet hướng lưu lượng ra Internet (`0.0.0.0/0 -> igw`).<br>- Nghiên cứu NAT Gateway trong Public Subnet để cho phép Private Subnet kết nối Internet một chiều. |
| 4 | - So sánh cơ chế hoạt động của Security Group (Lớp 4 - Stateful, áp dụng cấp Instance) và Network ACL (Lớp 3/4 - Stateless, áp dụng cấp Subnet).<br>- Thiết lập quy tắc Inbound/Outbound Rules kiểm soát chặt chẽ các cổng HTTP (80), HTTPS (443) và SSH (22). |
| 5 | - Tìm hiểu địa chỉ Elastic IP (EIP) và Elastic Network Interface (ENI).<br>- Gắn và điều chuyển EIP linh hoạt giữa các EC2 instances khi cần bảo trì hoặc failover.<br>- Nắm rõ các lưu ý về chi phí khi duy trì Elastic IP không gắn với instance đang hoạt động. |
| 6 | - **Thực hành chuyên sâu:** Xây dựng Custom VPC 2-Tier trên 2 Availability Zones (AZ-a & AZ-b).<br>- Khởi tạo Bastion Host tại Public Subnet và máy chủ nội bộ trong Private Subnet.<br>- Kiểm tra đường truyền SSH qua Bastion Host và xác thực khả năng tải bản cập nhật từ Private Subnet qua NAT Gateway. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Thiết kế & Triển khai kiến trúc mạng Custom Multi-Tier VPC
Trong bài lab này, tôi đã khởi tạo một Custom VPC (`10.0.0.0/16`) bao gồm 2 Public Subnets và 2 Private Subnets trải đều trên 2 Availability Zones. Tôi cấu hình 1 Internet Gateway cho Public Route Table và 1 NAT Gateway cho Private Route Table. Hệ thống máy chủ Web được đặt tại Public Subnet trong khi Database Server được cô lập an toàn trong Private Subnet, cho phép quản trị an toàn thông qua mô hình Bastion Host (Jump Box).

---

### Kết quả và thành tựu đạt được:

* Hiểu sâu kiến trúc mạng đám mây chuẩn Enterprise với mô hình mạng đa vùng sẵn sàng cao.
* Thiết kế và triển khai chính xác sơ đồ mạng VPC với đầy đủ IGW, NAT Gateway và Route Tables.
* Phân định rạch ròi và kết hợp hiệu quả giữa Security Group (Stateful) và Network ACL (Stateless).
* Thành thạo kỹ năng thiết lập Bastion Host để truy cập bảo mật vào các vùng mạng nội bộ (Private).
* Nắm vững kỹ năng xử lý sự cố (troubleshooting) kết nối mạng, định tuyến và phân giải DNS trong VPC.
