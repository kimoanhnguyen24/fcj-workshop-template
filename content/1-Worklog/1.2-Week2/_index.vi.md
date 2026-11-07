---
title: "Worklog Tuần 2"
date: 2026-10-12
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2:

* Kết nối, làm quen với các thành viên trong First Cloud AI Journey.
* Nắm cách quản lý chi phí trên AWS với AWS Budgets và biết cách sử dụng AWS Support.
* Hiểu và thực hành quản lý quyền truy cập với AWS IAM (user, group, policy, role).
* Hiểu và thực hành xây dựng hạ tầng mạng với Amazon VPC và kết nối AWS Site-to-Site VPN.
* Hiểu và thực hành với Amazon EC2: khởi tạo, kết nối, quản lý instance và triển khai ứng dụng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu tổng quan về AWS <br>&emsp; + Cơ sở hạ tầng toàn cầu: Region, Availability Zone <br>&emsp; + Mô hình trách nhiệm chia sẻ (Shared Responsibility) <br> - Làm quen với AWS Management Console: tìm kiếm và truy cập dịch vụ, chọn Region <br> - Tìm hiểu Budgets, Support, IAM, VPC, EC2 | 12/10/2026 | 12/10/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tìm hiểu quản lý chi phí với AWS Budgets <br>&emsp; + 4 loại budget: Cost, Usage, RI, Savings Plans <br>&emsp; + Cách đặt ngưỡng và cấu hình cảnh báo <br> - Tìm hiểu AWS Support <br>&emsp; + Các gói AWS Support <br>&emsp; + Các loại support request và mức độ nghiêm trọng (severity) <br> - **Thực hành:** Cost Management with AWS Budgets <br>&emsp; + Tạo Cost Budget <br>&emsp; + Tạo Usage Budget <br>&emsp; + Tạo RI Budget <br>&emsp; + Tạo Savings Plans Budget <br>&emsp; + Dọn dẹp tài nguyên <br> - **Thực hành:** AWS Support <br>&emsp; + Truy cập AWS Support <br>&emsp; + Thay đổi gói support <br>&emsp; + Tạo support request và chọn mức độ nghiêm trọng (severity) | 13/10/2026 | 13/10/2026 | <https://000007.awsfcaj.com/> <br> <https://000009.awsfcaj.com/> |
| 4 | - Tìm hiểu AWS IAM <br>&emsp; + IAM Group, IAM User, IAM Policy, IAM Role <br>&emsp; + Nguyên tắc Least Privilege <br>&emsp; + Cơ chế switch role <br> - **Thực hành:** Managing Access Control with AWS IAM <br>&emsp; + Tạo Admin Group và Admin User, đăng nhập bằng Admin User <br>&emsp; + Tạo Admin Role và OperatorUser <br>&emsp; + Cho phép OperatorUser switch role, truy cập Console và switch role <br>&emsp; + Dọn dẹp tài nguyên | 14/10/2026 | 14/10/2026 | <https://000002.awsfcaj.com/> |
| 5 | - Tìm hiểu Amazon VPC <br>&emsp; + Subnet, Route Table, Internet Gateway, NAT Gateway <br>&emsp; + Security Group, Network ACL, VPC Resource Map <br> - Tìm hiểu AWS Site-to-Site VPN <br>&emsp; + Virtual Private Gateway, Customer Gateway, VPN Connection <br> - **Thực hành:** Amazon VPC and AWS Site-to-Site VPN <br>&emsp; + Tạo VPC, Subnet, Internet Gateway, Route Table, Security Group <br>&emsp; + Bật VPC Flow Logs <br>&emsp; + Tạo EC2 server trong VPC và kiểm tra kết nối <br>&emsp; + Tạo NAT Gateway <br>&emsp; + Dùng Reachability Analyzer <br>&emsp; + Kết nối bằng AWS Systems Manager Session Manager <br>&emsp; + Giám sát và cảnh báo với CloudWatch <br>&emsp; + Thiết lập Site-to-Site VPN: Virtual Private Gateway, Customer Gateway, VPN Connection <br>&emsp; + Dọn dẹp tài nguyên | 15/10/2026 | 15/10/2026 | <https://000003.awsfcaj.com/> |
| 6 | - Tìm hiểu Amazon EC2 <br>&emsp; + Instance type <br>&emsp; + EBS Snapshot và AMI <br>&emsp; + Key pair và cách khôi phục truy cập instance <br>&emsp; + IAM Policy giới hạn chi phí và quyền sử dụng EC2 (theo Region, instance family, instance type, loại EBS volume, IP, thời gian) <br> - **Thực hành:** Introduction to Amazon EC2 <br>&emsp; + Tạo VPC và Security Group cho Linux instance và Windows instance <br>&emsp; + Khởi tạo và kết nối Microsoft Windows Server 2025 instance <br>&emsp; + Khởi tạo và kết nối Amazon Linux instance <br>&emsp; + Thay đổi instance type <br>&emsp; + Tạo và quản lý EBS Snapshot <br>&emsp; + Tạo Custom AMI và khởi tạo instance từ Custom AMI <br>&emsp; + Khôi phục truy cập vào Windows và Linux instance <br>&emsp; + Triển khai ứng dụng AWS User Management (LAMP, Node.js) trên Amazon Linux 2023 và Windows <br>&emsp; + Giới hạn chi phí và quyền sử dụng EC2 bằng IAM <br>&emsp; + Dọn dẹp tài nguyên | 16/10/2026 | 16/10/2026 | <https://000004.awsfcaj.com/> |


### Kết quả đạt được tuần 2:

* Hiểu và sử dụng AWS Budgets để quản lý chi phí:
  * Phân biệt 4 loại budget: Cost, Usage, RI, Savings Plans
  * Tạo budget và cấu hình ngưỡng cảnh báo khi chi phí vượt mức cho phép
  * Dọn dẹp budget sau khi thực hành

* Hiểu AWS Support và cách yêu cầu hỗ trợ:
  * Phân biệt các gói support và cách thay đổi gói support
  * Biết các loại support request
  * Tạo support request và chọn mức độ nghiêm trọng (severity) phù hợp

* Nắm được AWS IAM và thực hành phân quyền:
  * Phân biệt IAM Group, IAM User, IAM Policy, IAM Role
  * Tạo Admin Group, Admin User và đăng nhập bằng Admin User
  * Tạo Admin Role và OperatorUser, thực hiện switch role
  * Áp dụng nguyên tắc Least Privilege, dùng Role để cấp quyền tạm thời

* Hiểu và thực hành xây dựng mạng với Amazon VPC:
  * Subnet, Route Table, Internet Gateway, NAT Gateway
  * Lớp bảo vệ trong VPC: Security Group và Network ACL
  * Bật VPC Flow Logs, dùng VPC Resource Map và Reachability Analyzer để kiểm tra luồng mạng
  * Triển khai EC2 trong VPC, kết nối bằng Session Manager
  * Giám sát và cảnh báo bằng CloudWatch

* Thiết lập kết nối AWS Site-to-Site VPN:
  * Tạo Virtual Private Gateway, Customer Gateway, VPN Connection
  * Cấu hình Customer Gateway và tham khảo hướng dẫn xử lý sự cố VPN

* Thực hành Amazon EC2:
  * Khởi tạo và kết nối Windows Server 2025 instance và Amazon Linux instance
  * Thay đổi instance type
  * Tạo EBS Snapshot, tạo Custom AMI và khởi tạo instance từ AMI
  * Khôi phục quyền truy cập vào Windows và Linux instance khi mất key pair

* Triển khai ứng dụng AWS User Management (Node.js):
  * Cài đặt LAMP Server, phpMyAdmin và Node.js trên Amazon Linux 2023
  * Cài đặt XAMPP và Node.js trên Windows Server
  * Triển khai ứng dụng trên cả Linux và Windows

* Kiểm soát chi phí và quyền sử dụng EC2 bằng IAM Policy:
  * Giới hạn dịch vụ theo Region
  * Giới hạn theo instance family và instance type
  * Giới hạn loại EBS volume
  * Giới hạn quyền xóa tài nguyên theo IP công ty và theo khung thời gian

* Biết dọn dẹp tài nguyên sau mỗi bài thực hành để tránh phát sinh chi phí ngoài ý muốn.