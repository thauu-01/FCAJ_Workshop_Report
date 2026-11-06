---
title: "Worklog Tuần 7"
date: 2026-11-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Hiểu và áp dụng triết lý Hạ tầng dưới dạng mã (Infrastructure as Code - IaC) trong kỷ nguyên Cloud.
* Làm chủ công cụ tự động hóa hạ tầng gốc AWS CloudFormation: Viết templates JSON/YAML, Parameters, Mappings, Resources và Outputs.
* Tìm hiểu và thực hành với AWS Cloud Development Kit (CDK): Xây dựng hạ tầng bằng ngôn ngữ lập trình hiện đại (TypeScript / Python).
* Quản trị, cấu hình và kết nối máy chủ không cần mở port SSH thông qua AWS Systems Manager (SSM).

---

### Các công việc triển khai trong tuần:

| Thứ | Công việc |
| :---: | :--- |
| 2 | - Tìm hiểu các nguyên lý của Infrastructure as Code (IaC): Tính nhất quán, khả năng tái sử dụng, kiểm soát phiên bản và giảm thiểu sai sót do con người.<br>- Nghiên cứu cấu trúc AWS CloudFormation Template: Format Version, Description, Parameters, Resources, Outputs.<br>- Phân tích vòng đời của CloudFormation Stacks và cơ chế xem trước thay đổi bằng Change Sets. |
| 3 | - Thực hành viết CloudFormation Template (YAML) để tự động hóa việc khởi tạo một hệ thống mạng VPC hoàn chỉnh: Subnets, Route Tables, Internet Gateway.<br>- Sử dụng các hàm nội tại (Intrinsic Functions): `Ref`, `!Sub`, `!GetAtt`, `!Join`, `!Select`.<br>- Triển khai và cập nhật Stack an toàn, kiểm tra tính năng tự động khôi phục (Rollback) khi gặp lỗi. |
| 4 | - Nghiên cứu AWS Cloud Development Kit (CDK): Kiến trúc CDK (Apps, Stacks, Constructs L1, L2, L3).<br>- So sánh sự khác nhau giữa việc định nghĩa hạ tầng bằng tệp tĩnh (YAML/JSON) và ngôn ngữ lập trình bậc cao (TypeScript/Python).<br>- Nắm vững các lệnh cốt lõi của CDK CLI: `cdk init`, `cdk synth`, `cdk diff`, `cdk deploy`. |
| 5 | - Khám phá bộ giải pháp AWS Systems Manager (SSM): SSM Agent, Session Manager, Parameter Store, Run Command.<br>- Cấu hình IAM Role với policy `AmazonSSMManagedInstanceCore` để gắn vào máy chủ EC2.<br>- Thực hành kết nối vào dòng lệnh EC2 qua Session Manager mà không cần mở cổng 22 (SSH) trên Security Group. |
| 6 | - **Thực hành triển khai IaC & Quản trị bảo mật:** Triển khai một ứng dụng web hoàn chỉnh bằng AWS CDK.<br>- Lưu trữ chuỗi kết nối và thông tin cấu hình an toàn bằng SSM Parameter Store (SecureString mã hóa bởi KMS).<br>- Thực hiện chạy lệnh cập nhật phần mềm hàng loạt trên nhiều máy chủ thông qua Systems Manager Run Command. |

---

### Bài thực hành Hands-on Lab trọng tâm:

#### Tự động hóa triển khai hạ tầng với CloudFormation/CDK & Quản trị không mở port với SSM
Trong bài thực hành này, tôi đã lập trình toàn bộ hạ tầng đám mây bao gồm VPC, Subnets, EC2 và RDS bằng AWS CloudFormation và AWS CDK (TypeScript). Sau khi stack được khởi tạo tự động, tôi đã cấu hình máy chủ EC2 kết nối với AWS Systems Manager. Thay vì sử dụng SSH truyền thống, tôi đã thực hiện truy cập Shell thông qua SSM Session Manager trên trình duyệt mà không cần mở port 22, đồng thời quản lý các thông số cấu hình mật qua SSM Parameter Store.

---

### Kết quả và thành tựu đạt được:

* Nắm vững tư duy Infrastructure as Code (IaC) và các thực hành quản lý phiên bản hạ tầng bằng mã nguồn.
* Tự tay thiết kế và triển khai thành công các template AWS CloudFormation phức tạp có sử dụng Intrinsic Functions.
* Làm chủ quy trình phát triển hạ tầng với AWS CDK, tận dụng sức mạnh của ngôn ngữ lập trình bậc cao và Constructs L2.
* Loại bỏ hoàn toàn rủi ro bảo mật cổng SSH bằng cách áp dụng giải pháp quản trị từ xa AWS Systems Manager Session Manager.
* Quản lý cấu hình tập trung và bảo mật biến môi trường ứng dụng thông qua SSM Parameter Store.
