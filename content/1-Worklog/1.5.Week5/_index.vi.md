---
title: "Worklog Tuần 5"
date: 2026-11-02
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Hiểu rõ mô hình Serverless: Lambda hoạt động theo sự kiện như thế nào, vì sao không cần quản lý server, và vai trò của từng dịch vụ trong một ứng dụng web Serverless.
* Hiểu cách các dịch vụ tương tác với nhau: S3 kích hoạt Lambda, Lambda ghi dữ liệu vào DynamoDB, và vai trò của IAM Policy trong việc cấp quyền cho Lambda.
* Hiểu AWS PrivateLink và VPC Endpoint: vì sao cần truy cập dịch vụ AWS mà không đi qua Internet công cộng.
* Phân biệt được Gateway Endpoint và Interface Endpoint về cơ chế định tuyến, trường hợp sử dụng và cách bảo mật.
* Hiểu bài toán truy cập S3 từ on-premises (hybrid) và vấn đề DNS đi kèm.
* Hiểu VPC Endpoint Policy và cách kết hợp với bucket policy để kiểm soát truy cập.
* Thực hành các lab để kiểm chứng lại kiến thức đã tìm hiểu.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu Serverless Computing <br>&emsp; + Khái niệm: chạy code, quản lý dữ liệu, tích hợp ứng dụng mà không cần quản lý hạ tầng server <br>&emsp; + So sánh với mô hình truyền thống (tự quản lý EC2) <br> - Tìm hiểu kiến trúc ứng dụng web Serverless trên AWS <br>&emsp; + AWS Lambda: xử lý logic <br>&emsp; + Amazon DynamoDB: lưu trữ dữ liệu <br>&emsp; + Amazon API Gateway: tiếp nhận request từ người dùng <br>&emsp; + S3 / AWS Amplify: host ứng dụng web tĩnh <br> - Tìm hiểu kiến trúc tổng thể của ứng dụng Book Store trong series <br>&emsp; + Chức năng người dùng: đăng ký, đăng nhập, xem sách, thêm giỏ hàng, thanh toán <br>&emsp; + Chức năng admin: thêm, sửa, xóa sách, quản lý đơn hàng <br>&emsp; + Các dịch vụ liên quan trong series: Cognito, SNS, SQS, API Gateway | 02/11/2026 | 02/11/2026 | <https://000078.awsfcaj.com/> |
| 3 | - Tìm hiểu AWS Lambda <br>&emsp; + Lambda function được kích hoạt bởi sự kiện (event-driven) <br>&emsp; + Cơ chế trigger từ S3 khi có object mới <br>&emsp; + Execution role và IAM Policy giúp Lambda truy cập S3 <br>&emsp; + Áp dụng nguyên tắc Least Privilege khi cấp quyền cho Lambda <br> - Tìm hiểu Amazon DynamoDB <br>&emsp; + Khái niệm table, item, attribute, primary key <br>&emsp; + Vai trò của bảng Books lưu thông tin sách, S3 Bucket lưu hình ảnh sách <br> - **Thực hành:** Image Processing and Optimization on AWS <br>&emsp; + Tạo Lambda function xử lý hình ảnh <br>&emsp; + Tạo S3 Bucket, tạo IAM Policy cho Lambda <br>&emsp; + Kiểm tra hoạt động của Lambda function | 03/11/2026 | 03/11/2026 | <https://000078.awsfcaj.com/> |
| 4 | - Tìm hiểu cách Lambda ghi dữ liệu vào DynamoDB <br>&emsp; + Quyền cần cấp cho Lambda để ghi vào table <br>&emsp; + Luồng dữ liệu: S3 / Lambda / DynamoDB <br> - **Thực hành:** Writing Data to Amazon DynamoDB <br>&emsp; + Tạo DynamoDB Table <br>&emsp; + Tạo Lambda function ghi dữ liệu <br>&emsp; + Dọn dẹp tài nguyên (xóa table Books, empty và xóa S3 Bucket, xóa Lambda function) <br> - Tìm hiểu AWS PrivateLink <br>&emsp; + Kết nối riêng tư từ VPC và on-premises tới dịch vụ AWS <br>&emsp; + Traffic không đi qua Public Internet <br>&emsp; + Vì sao không cần Internet Gateway hoặc NAT Gateway để truy cập S3 | 04/11/2026 | 04/11/2026 | <https://000078.awsfcaj.com/> <br> <https://000111.awsfcaj.com/> |
| 5 | - Tìm hiểu các loại VPC Endpoint <br>&emsp; + Gateway Endpoint: dùng cho S3 và DynamoDB, đưa traffic qua route table bằng private IP <br>&emsp; + Interface Endpoint: dùng ENI có private IP trong subnet, phân giải qua DNS, dùng Security Group để kiểm soát <br>&emsp; + Gateway Load Balancer Endpoint: chuyển traffic tới thiết bị bảo mật <br> - Tìm hiểu bài toán truy cập S3 từ on-premises <br>&emsp; + Kết nối hybrid qua AWS Direct Connect hoặc Site-to-Site VPN <br>&emsp; + Vì sao Gateway Endpoint không dùng được từ on-premises <br>&emsp; + Giải pháp: Interface Endpoint cho S3 <br> - Tìm hiểu vấn đề DNS khi truy cập S3 qua Interface Endpoint <br>&emsp; + Dùng endpoint-specific DNS name hoặc tham số --endpoint-url <br>&emsp; + Cấu hình DNS on-premises trỏ domain S3 về IP của endpoint (Route 53 Resolver Inbound Endpoint, private hosted zone) <br>&emsp; + Lưu ý IP của endpoint có thể thay đổi khi thêm/bớt subnet <br> - **Thực hành:** Access S3 from VPC <br>&emsp; + Chuẩn bị môi trường, tạo và kiểm tra Gateway Endpoint | 05/11/2026 | 05/11/2026 | <https://000111.awsfcaj.com/> |
| 6 | - Tìm hiểu VPC Endpoint Policy <br>&emsp; + Là IAM resource policy gắn vào endpoint, tách biệt với IAM policy của user <br>&emsp; + Giới hạn bucket nào, principal nào được truy cập qua endpoint <br>&emsp; + Kết hợp với bucket policy để chỉ cho phép truy cập từ endpoint cụ thể <br> - Tìm hiểu kiến trúc triển khai endpoint <br>&emsp; + Tập trung (centralized) so với đặt endpoint trong từng VPC riêng <br>&emsp; + Lợi ích về chi phí và bảo mật khi dùng VPC Endpoint <br> - **Thực hành:** Access S3 from on-premises <br>&emsp; + Tạo và kiểm tra S3 Interface Endpoint <br>&emsp; + Mô phỏng DNS on-premises <br> - **Thực hành:** VPC Endpoint Policies (bonus) và dọn dẹp tài nguyên | 06/11/2026 | 06/11/2026 | <https://000111.awsfcaj.com/> |


### Kết quả đạt được tuần 5:

* Hiểu mô hình Serverless:
  * Serverless cho phép chạy code, quản lý dữ liệu và tích hợp ứng dụng mà không cần quản lý server
  * Nắm vai trò từng thành phần: Lambda (xử lý logic), DynamoDB (lưu dữ liệu), API Gateway (nhận request), S3/Amplify (host web tĩnh)
  * Hiểu kiến trúc ứng dụng Book Store và cách các dịch vụ (Cognito, SNS, SQS, API Gateway) sẽ được ghép vào ở các phần sau của series
* Hiểu cách Lambda tương tác với S3 và DynamoDB:
  * Lambda chạy theo sự kiện, được trigger khi có thay đổi trên S3
  * Lambda cần IAM Policy phù hợp để đọc/ghi S3 và ghi DynamoDB, cấp đúng quyền cần thiết (Least Privilege)
  * Nắm luồng dữ liệu: hình ảnh vào S3, Lambda xử lý, thông tin sách lưu vào DynamoDB
* Hiểu AWS PrivateLink và VPC Endpoint:
  * Truy cập dịch vụ AWS riêng tư, không đi qua Public Internet, không cần Internet Gateway hay NAT Gateway
  * Phân biệt 3 loại endpoint: Gateway, Interface, Gateway Load Balancer
  * Gateway Endpoint: định tuyến bằng route table, chỉ hỗ trợ S3 và DynamoDB, chỉ dùng được từ bên trong VPC
  * Interface Endpoint: tạo ENI với private IP, phân giải bằng DNS, dùng Security Group, truy cập được từ on-premises qua Direct Connect/VPN
* Hiểu bài toán hybrid access tới S3:
  * Vì sao on-premises cần Interface Endpoint thay vì Gateway Endpoint
  * Các vấn đề DNS và các hướng xử lý: endpoint-specific DNS name, --endpoint-url, Route 53 Resolver Inbound Endpoint, private hosted zone
  * Lưu ý khi dùng TLS/SSL và khi IP của endpoint thay đổi
* Hiểu cách kiểm soát truy cập bằng VPC Endpoint Policy:
  * Endpoint policy là resource policy riêng gắn vào endpoint
  * Kết hợp endpoint policy và bucket policy để giới hạn truy cập theo bucket, principal hoặc endpoint cụ thể
  * Biết hai hướng triển khai endpoint: tập trung và theo từng VPC
* Thực hành kiểm chứng kiến thức:
  * Lambda xử lý hình ảnh từ S3 và ghi dữ liệu vào DynamoDB
  * Tạo và kiểm tra Gateway Endpoint, Interface Endpoint, mô phỏng DNS on-premises
  * Cấu hình VPC Endpoint Policy và dọn dẹp tài nguyên sau mỗi lab