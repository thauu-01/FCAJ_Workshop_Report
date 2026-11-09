---
title: "Worklog Tuần 5"
date: 2026-11-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Nghiên cứu các dịch vụ giám sát hệ thống, cảnh báo và nhật ký với Amazon CloudWatch.
* Làm chủ dịch vụ cân bằng tải đàn hồi Elastic Load Balancing (ELB), đặc biệt là Application Load Balancer (ALB).
* Tìm hiểu cơ chế tự động co giãn tài nguyên tính toán với Amazon EC2 Auto Scaling.
* Thiết kế và triển khai kiến trúc ứng dụng web có tính sẵn sàng cao (High Availability), chịu lỗi (Fault-Tolerant) và tự phục hồi (Self-Healing).

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Nghiên cứu Amazon CloudWatch: CloudWatch Metrics, CloudWatch Logs, Log Groups, Log Streams, Dashboards.<br>- Phân tích cơ chế hoạt động của CloudWatch Alarms và trạng thái cảnh báo (OK, ALARM, INSUFFICIENT_DATA).<br>- Tích hợp Amazon Simple Notification Service (SNS) để gửi email thông báo khi kích hoạt alarm. |
| 3 | - Thực hành cấu hình CloudWatch Agent trên máy chủ EC2 để thu thập các số liệu chi tiết (Memory utilization, Disk space).<br>- Tạo CloudWatch Alarm giám sát ngưỡng CPU > 70% trong 2 chu kỳ liên tiếp và gửi email qua SNS.<br>- Thiết kế một CloudWatch Dashboard trực quan hóa toàn bộ chỉ số hoạt động của hạ tầng. |
| 4 | - Tìm hiểu Elastic Load Balancing (ELB): So sánh Application Load Balancer (Layer 7), Network Load Balancer (Layer 4) và Gateway Load Balancer.<br>- Nghiên cứu Target Groups, Health Checks, Routing Rules (Path-based, Host-based routing).<br>- Cấu hình Application Load Balancer phân bổ lưu lượng truy cập tới nhiều EC2 instances. |
| 5 | - Tìm hiểu Amazon EC2 Auto Scaling: Launch Templates (cấu hình AMI, instance type, user data, security group).<br>- Tạo Auto Scaling Group (ASG) trải dài trên nhiều Availability Zones (Multi-AZ).<br>- Cấu hình các chính sách co giãn: Target Tracking Scaling, Step Scaling, Simple Scaling và Scheduled Scaling. |
| 6 | - **Thực hành tích hợp toàn diện:** Gắn Auto Scaling Group vào Application Load Balancer Target Group.<br>- Thực hiện stress test tải CPU trên các máy chủ EC2 bằng công cụ `stress`.<br>- Quan sát hành vi tự động khởi tạo máy chủ mới (Scale-Out) và tự động thu hồi (Scale-In) khi tải giảm. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Xây dựng kiến trúc Web High Availability tự phục hồi với ALB & Auto Scaling
Trong bài thực hành này, em đã xây dựng một hệ thống hoàn chỉnh có khả năng tự phục hồi và co giãn tự động. Hệ thống sử dụng một Application Load Balancer phân phối tải tới một Auto Scaling Group trải trên 2 Availability Zones. Khi chạy lệnh stress test đẩy tải CPU vượt 70%, CloudWatch Alarm đã kích hoạt chính sách Target Tracking Scaling để tự động khởi chạy thêm 2 EC2 instances mới, tự động đăng ký vào Target Group và tiếp nhận lưu lượng một cách liền mạch mà không làm gián đoạn người dùng.

---

### Kết quả và thành tựu đạt được:

* Làm chủ dịch vụ Amazon CloudWatch, cấu hình các bộ chỉ số đo lường nâng cao và bảng điều khiển trực quan.
* Thiết lập hệ thống thông báo sự cố tức thời qua CloudWatch Alarms và Amazon SNS.
* Thành thạo cấu hình Application Load Balancer với Health Checks chặt chẽ và thuật toán cân bằng tải tối ưu.
* Triển khai thành công Launch Template và Auto Scaling Group đảm bảo hệ thống có tính sẵn sàng cao và tự động co giãn.
* Nắm vững phương pháp kiểm thử tải và đánh giá khả năng chịu lỗi của hạ tầng điện toán đám mây.
