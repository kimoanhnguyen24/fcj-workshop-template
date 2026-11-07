---
title: "Worklog Tuần 3"
date: 2026-10-19
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
 
 
### Mục tiêu tuần 3:
 
* Hiểu cách xây dựng hệ thống Hybrid DNS giữa DNS on-premise và Amazon Route 53 bằng Route 53 Resolver.
* Thực hành triển khai Microsoft AD và cấu hình Outbound Endpoint, Inbound Endpoint, Resolver Rules.
* Hiểu và sử dụng Amazon CloudWatch để giám sát tài nguyên: Metrics, Logs, Alarms, Dashboards.
* Nắm cách phân tích log và thiết lập cảnh báo để theo dõi hệ thống.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu Amazon Route 53 và Route 53 Resolver <br>&emsp; + Các chức năng của Route 53: private DNS zone, hybrid DNS, phân giải tên miền <br>&emsp; + 3 thành phần của hybrid DNS: Outbound Endpoint, Inbound Endpoint, Resolver Rules <br>&emsp; + Kiến trúc tổng quan của lab Hybrid DNS <br> - **Thực hành:** <br>&emsp; + Tạo Key Pair <br>&emsp; + Khởi tạo hạ tầng bằng CloudFormation Template <br>&emsp; + Cấu hình Security Group | 16/11/2026 | 16/11/2026 | <https://000010.awsfcaj.com/> |
| 3 | - Tìm hiểu vai trò của Remote Desktop Gateway và Microsoft AD trong mô hình giả lập DNS on-premise <br> - Tìm hiểu cách hoạt động của Route 53 Outbound Endpoint (gửi truy vấn DNS từ AWS về DNS on-premise) <br> - **Thực hành:** <br>&emsp; + Kết nối tới RDGW <br>&emsp; + Triển khai Microsoft AD <br>&emsp; + Tạo Route 53 Outbound Endpoint | 17/10/2026 | 17/10/2026 | <https://000010.awsfcaj.com/> |
| 4 | - Tìm hiểu Route 53 Resolver Rules (chuyển tiếp truy vấn của domain cụ thể) <br> - Tìm hiểu Route 53 Inbound Endpoint (nhận truy vấn DNS từ on-premise) <br> - Tìm hiểu luồng truy vấn DNS hai chiều giữa AWS và on-premise <br> - **Thực hành:** <br>&emsp; + Tạo Route 53 Resolver Rules <br>&emsp; + Tạo Route 53 Inbound Endpoint <br>&emsp; + Kiểm tra kết quả phân giải tên miền hai chiều <br>&emsp; + Dọn dẹp tài nguyên | 18/10/2026 | 18/10/2026 | <https://000010.awsfcaj.com/> |
| 5 | - Tìm hiểu Amazon CloudWatch <br>&emsp; + Tổng quan: thu thập và phân tích metrics, logs ở một nơi thống nhất <br>&emsp; + CloudWatch Metrics: Search expressions, Math expressions, Dynamic Labels <br>&emsp; + CloudWatch Logs: log group, log stream <br> - **Thực hành:** <br>&emsp; + Chuẩn bị môi trường thực hành <br>&emsp; + CloudWatch Metrics: xem metrics, Search expressions, Math expressions, Dynamic Labels <br>&emsp; + CloudWatch Logs: xem và quản lý log group, log stream | 19/10/2026 | 19/10/2026 | <https://000008.awsfcaj.com/> |
| 6 | - Tìm hiểu CloudWatch Logs Insights (cú pháp truy vấn log) và Metric Filter <br> - Tìm hiểu CloudWatch Alarms (ngưỡng, các trạng thái alarm, hành động thông báo) <br> - Tìm hiểu CloudWatch Dashboards <br> - **Thực hành:** <br>&emsp; + Dùng Logs Insights để truy vấn và phân tích log <br>&emsp; + Tạo Metric Filter từ log <br>&emsp; + Tạo Alarm và cấu hình thông báo <br>&emsp; + Tạo Dashboard tổng hợp <br>&emsp; + Dọn dẹp tài nguyên | 20/10/2026 | 20/10/2026 | <https://000008.awsfcaj.com/> |

### Kết quả đạt được tuần 3:
 
* Hiểu Amazon Route 53 và Route 53 Resolver:
  * Phân biệt các chức năng của Route 53: đăng ký domain, private DNS zone, hybrid DNS, phân giải tên miền
  * Hiểu vai trò của Outbound Endpoint (gửi truy vấn DNS từ AWS về DNS on-premise)
  * Hiểu vai trò của Inbound Endpoint (nhận truy vấn DNS từ on-premise tới domain trên AWS)
  * Hiểu Resolver Rules (chuyển tiếp truy vấn của domain cụ thể tới DNS on-premise)
* Thực hành thiết lập Hybrid DNS:
  * Tạo Key Pair, khởi tạo hạ tầng bằng CloudFormation và cấu hình Security Group
  * Kết nối tới RDGW và triển khai Microsoft AD
  * Tạo Outbound Endpoint, Resolver Rules và Inbound Endpoint
  * Kiểm tra phân giải tên miền giữa môi trường on-premise (Microsoft AD) và AWS
  * Dọn dẹp tài nguyên sau khi hoàn thành
* Hiểu Amazon CloudWatch và vai trò trong giám sát hệ thống:
  * Thu thập và phân tích metrics, logs ở một nơi thống nhất
  * Hiểu khả năng giám sát end-to-end và tự động hóa hành động dựa trên cảnh báo
* Thực hành CloudWatch Metrics:
  * Xem và tra cứu metrics của tài nguyên AWS
  * Dùng Search expressions để tìm nhiều metric cùng lúc
  * Dùng Math expressions để tính toán trên metric
  * Dùng Dynamic Labels để hiển thị nhãn có ý nghĩa trên biểu đồ
* Thực hành CloudWatch Logs:
  * Quản lý log group và log stream
  * Dùng Logs Insights để truy vấn và phân tích log
  * Dùng Metric Filter để biến dữ liệu log thành metric
* Thực hành CloudWatch Alarms và Dashboards:
  * Tạo alarm theo ngưỡng và cấu hình thông báo
  * Xây dựng dashboard để theo dõi tập trung các chỉ số quan trọng