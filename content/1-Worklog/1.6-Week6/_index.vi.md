---
title: "Worklog Tuần 6"
date: 2026-11-08
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Nghiên cứu mô hình điện toán không máy chủ (Serverless Computing) và tư duy kiến trúc hướng sự kiện (Event-Driven Architecture).
* Làm chủ dịch vụ tính toán Serverless AWS Lambda: Khởi tạo function, cấu hình execution roles, biến môi trường và xử lý runtime.
* Xây dựng các cổng giao tiếp API với Amazon API Gateway (REST APIs, HTTP APIs, CORS, Authorizers).
* Làm chủ các dịch vụ truyền tin bất đồng bộ: Amazon Simple Queue Service (SQS) và Amazon Simple Notification Service (SNS).

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Tìm hiểu nền tảng của Serverless: Lợi ích về vận hành (Zero server management), khả năng tự động mở rộng theo yêu cầu và mô hình Pay-as-you-go.<br>- Khám phá AWS Lambda: Vòng đời function, Memory allocation, Timeout, Concurrency limits (Reserved vs Provisioned).<br>- Cấu hình IAM Execution Role cấp quyền truy cập tối thiểu cho Lambda function. |
| 3 | - Viết Lambda Function bằng Node.js / Python thực hiện xử lý dữ liệu và tương tác với Amazon DynamoDB.<br>- Khảo sát Amazon CloudWatch Logs cho Lambda để phân tích execution duration, memory used và gỡ lỗi runtime.<br>- Tìm hiểu khái niệm Cold Start và các phương pháp tối ưu hóa tốc độ khởi động hàm. |
| 4 | - Nghiên cứu Amazon API Gateway: Phân biệt REST API và HTTP API.<br>- Cấu hình API Resources, Methods (GET, POST, PUT, DELETE) và Lambda Proxy Integration.<br>- Thiết lập API Stages (dev, prod), Stage Variables và kích hoạt CORS để kết nối với Frontend. |
| 5 | - Tìm hiểu cơ chế truyền tin phi tập trung (Decoupling Architecture): So sánh Pub/Sub (SNS) và Message Queuing (SQS).<br>- Nghiên cứu Amazon SQS: Standard Queue vs FIFO Queue, Visibility Timeout, Dead-Letter Queue (DLQ).<br>- Nghiên cứu Amazon SNS: Topics, Subscriptions (Email, SMS, Lambda, SQS), Fan-out Pattern. |
| 6 | - **Thực hành triển khai Serverless Microservice:** Xây dựng ứng dụng đặt hàng (Order Processing System).<br>- API Gateway tiếp nhận đơn hàng -> Lambda xử lý -> ghi vào DynamoDB -> xuất message tới SNS Topic -> Fan-out sang SQS Queues để gửi email và xử lý thanh toán bất đồng bộ. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Xây dựng Serverless Event-Driven Order Processing API với Lambda, API Gateway & SQS/SNS
Trong bài thực hành này, tôi đã thiết kế và triển khai một hệ thống xử lý đơn hàng hoàn toàn không máy chủ (Serverless). Hệ thống sử dụng Amazon API Gateway làm điểm tiếp nhận request HTTP POST `/orders`, kích hoạt AWS Lambda function để validate dữ liệu và lưu vào Amazon DynamoDB. Sau khi lưu thành công, Lambda gửi một thông điệp sự kiện tới Amazon SNS Topic, từ đó áp dụng mô hình Fan-out để phân phối song song tới Amazon SQS Queue phục vụ tác vụ gửi email hóa đơn và cập nhật tồn kho.

---

### Kết quả và thành tựu đạt được:

* Nắm vững nguyên lý hoạt động của điện toán Serverless và tư duy thiết kế hệ thống hướng sự kiện.
* Phát triển, triển khai và tối ưu hóa hiệu năng cho các hàm xử lý dữ liệu với AWS Lambda.
* Xây dựng thành công cổng giao diện RESTful API hoàn chỉnh trên Amazon API Gateway tích hợp Lambda Proxy.
* Làm chủ kiến trúc phân tán tách rời (Decoupled Architecture) với mẫu thiết kế SNS Fan-out sang SQS.
* Xử lý lỗi và cơ chế thử lại (Retry) thông minh sử dụng Dead-Letter Queues (DLQ).
