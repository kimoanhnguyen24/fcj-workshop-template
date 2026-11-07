---
title: "Worklog Tuần 4"
date: 2026-10-23
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
 
* Hiểu sâu hơn về AWS IAM: quy trình xác thực request, cơ chế Assume Role và cách giới hạn quyền truy cập bằng Condition.
* Thực hành tạo IAM Group, User, Role và giới hạn việc switch role theo địa chỉ IP và thời gian.
* Hiểu cách đóng gói và triển khai ứng dụng bằng Docker (Docker image, Docker Compose).
* Thực hành triển khai ứng dụng container trên AWS với EC2, RDS và lưu trữ image trên Amazon ECR, Docker Hub.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu AWS IAM nâng cao <br>&emsp; + Quy trình gửi request tới dịch vụ AWS <br>&emsp; + Cách AWS xác thực request <br>&emsp; + Quy trình Assume Role <br>&emsp; + Nguyên tắc Least Privilege khi phân quyền cho admin <br> - Tìm hiểu IAM Role Condition: giới hạn truy cập theo địa chỉ IP và theo thời gian | 23/10/2026 | 23/10/2026 | <https://000044.awsfcaj.com/> |
| 3 | - **Thực hành:** IAM Role & Condition <br>&emsp; + Tạo IAM Group <br>&emsp; + Tạo IAM User <br>&emsp; + Kiểm tra quyền truy cập của user <br>&emsp; + Tạo Admin IAM Role <br>&emsp; + Cấu hình Switch role <br>&emsp; + Giới hạn switch role theo IP <br>&emsp; + Giới hạn switch role theo thời gian <br>&emsp; + Dọn dẹp tài nguyên | 24/10/2026 | 24/10/2026 | <https://000044.awsfcaj.com/> |
| 4 | - Tìm hiểu Docker: container, Docker image, Docker Hub, Amazon ECR <br> - Tìm hiểu kiến trúc triển khai ứng dụng Docker trên AWS (EC2, RDS, ECR) <br> - Tìm hiểu DB Subnet Group, Amazon RDS và IAM Role cho phép EC2 truy cập ECR <br> - **Thực hành:** Deploy Application on Docker <br>&emsp; + Cài đặt các thành phần phụ thuộc trên máy local <br>&emsp; + Triển khai ứng dụng trên local <br>&emsp; + Kiểm tra ứng dụng | 25/10/2026 | 25/10/2026 | <https://000015.awsfcaj.com/> |
| 5 | - **Thực hành:** Deploy Application on Docker <br>&emsp; + Cấu hình VPC và Security Group <br>&emsp; + Tạo IAM Role để truy cập ECR <br>&emsp; + Đăng nhập Docker Hub <br>&emsp; + Tạo DB Subnet Group <br>&emsp; + Khởi tạo RDS Instance <br>&emsp; + Cấu hình và khởi tạo EC2 Instance <br>&emsp; + Cài đặt các thư viện cần thiết trên EC2 <br>&emsp; + Thêm dữ liệu vào database để kiểm thử | 26/10/2026 | 26/10/2026 | <https://000015.awsfcaj.com/> |
| 6 | - Tìm hiểu cách triển khai ứng dụng chỉ bằng Docker image <br> - Tìm hiểu Docker Compose và cách quản lý nhiều container <br> - Tìm hiểu cách lưu trữ và phân phối image với Amazon ECR và Docker Hub <br> - **Thực hành:** Deploy Application on Docker <br>&emsp; + Triển khai ứng dụng bằng Docker image và kiểm tra <br>&emsp; + Triển khai ứng dụng bằng Docker Compose và kiểm tra <br>&emsp; + Push image lên Amazon ECR <br>&emsp; + Push image lên Docker Hub <br>&emsp; + Dọn dẹp tài nguyên | 27/10/2026 | 27/10/2026 | <https://000015.awsfcaj.com/> |
 
 
### Kết quả đạt được tuần 4:
 
* Hiểu sâu hơn về AWS IAM:
  * Nắm quy trình gửi request tới dịch vụ AWS và cách AWS xác thực request
  * Hiểu quy trình Assume Role và vai trò của Role trong việc cấp quyền tạm thời
  * Áp dụng nguyên tắc Least Privilege khi cấp quyền admin theo từng dịch vụ
* Thực hành IAM Role & Condition:
  * Tạo IAM Group, IAM User và kiểm tra quyền truy cập
  * Tạo Admin IAM Role và cấu hình Switch role
  * Giới hạn việc switch role theo địa chỉ IP
  * Giới hạn việc switch role theo khung thời gian
  * Dọn dẹp tài nguyên sau khi thực hành
* Hiểu các khái niệm cơ bản về Docker:
  * Container, Docker image, Docker Hub, Amazon ECR
  * Sự khác nhau giữa triển khai trực tiếp và triển khai bằng container
* Thực hành triển khai ứng dụng trên Docker:
  * Cài đặt dependencies, triển khai và kiểm tra ứng dụng trên máy local
  * Chuẩn bị hạ tầng AWS: VPC, Security Group, IAM Role truy cập ECR
  * Tạo DB Subnet Group và khởi tạo Amazon RDS Instance
  * Cấu hình EC2 Instance, cài đặt thư viện và thêm dữ liệu kiểm thử vào database
  * Triển khai ứng dụng bằng Docker image
  * Triển khai ứng dụng bằng Docker Compose
* Thực hành quản lý Docker image:
  * Push image lên Amazon ECR
  * Push image lên Docker Hub
