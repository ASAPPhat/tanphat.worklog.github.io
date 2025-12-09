---
title: "Worklog Tuần 5"
date: "2025-10-15"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

**Khoảng thời gian tuần: 6 - 12 tháng 10, 2025**

### Mục tiêu tuần 5:

- Thành thạo dịch vụ bảo vệ dữ liệu AWS (AWS Backup)
- Tìm hiểu tích hợp mạng và quản lý (VPC Peering, Transit Gateway)
- Hiểu các dịch vụ nhắn tin (SQS, SNS)
- Thực hành các chiến lược sao lưu và phục hồi thảm họa

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| Monday    | - Các nguyên tắc cơ bản AWS Backup <br> - Lập kế hoạch sao lưu và chính sách <br> - Lập kế hoạch phục hồi thảm họa                                                      | 10/06/2025   | 10/06/2025      | <https://000013.awsstudygroup.com/vi/>    |
| Tuesday   | - Cấu hình VPC Peering <br> - Liên lạc giữa các VPC <br> - Mô hình tích hợp mạng                                                                                        | 10/07/2025   | 10/07/2025      | AWS Documentation                         |
| Wednesday | - AWS Transit Gateway cho quản lý mạng tập trung <br> - Kết nối nhiều VPC <br> - Định tuyến và chính sách định tuyến                                                    | 10/08/2025   | 10/08/2025      | <https://000020.awsstudygroup.com/vi/>    |
| Thursday  | - Amazon SQS (Simple Queue Service) <br> - Amazon SNS (Simple Notification Service) <br> - Định tuyến và lọc tin nhắn                                                   | 10/09/2025   | 10/09/2025      | <https://000077.awsstudygroup.com/vi/>    |
| Friday    | - **Thực hành:** <br>&emsp; + Tạo kế hoạch sao lưu <br>&emsp; + Thiết lập kết nối VPC Peering <br>&emsp; + Cấu hình SQS và SNS <br>&emsp; + Kiểm tra quy trình nhắn tin | 10/10/2025   | 10/10/2025      | AWS Documentation                         |
| Saturday  | - Mô hình nhắn tin nâng cao <br> - Kiểm tra sao lưu và phục hồi <br> - Tóm tắt tuần 5                                                                                   | 10/11/2025   | 10/11/2025      | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 5:

- **Thành thạo AWS Backup và Disaster Recovery:**

  - Tạo kế hoạch sao lưu toàn diện cho nhiều tài nguyên AWS
  - Cấu hình chính sách sao lưu phù hợp với yêu cầu tuân thủ
  - Triển khai chiến lược disaster recovery (DR)
  - Thực hành các quy trình sao lưu và khôi phục
  - Xác thực Recovery Time Objective (RTO) và Recovery Point Objective (RPO)
  - Thiết lập chính sách lưu giữ sao lưu và lifecycle rules

- **Triển khai VPC Peering:**

  - Cấu hình thành công VPC peering giữa nhiều VPCs
  - Thiết lập giao tiếp cross-VPC và định tuyến
  - Áp dụng các mô hình tích hợp mạng và phương pháp hay nhất
  - Quản lý route tables và network ACLs cho các VPCs được peering
  - Hiểu các giới hạn và trường hợp sử dụng của VPC Peering
  - Kiểm tra kết nối giữa các VPCs được peering

- **Thành thạo AWS Transit Gateway:**

  - Triển khai AWS Transit Gateway cho quản lý mạng tập trung
  - Thiết lập kết nối đa VPC thông qua Transit Gateway
  - Cấu hình chính sách định tuyến nâng cao
  - Kết nối mạng on-premises với AWS
  - Hiểu lợi thế của Transit Gateway so với VPC Peering
  - Triển khai phân đoạn mạng và cô lập lưu lượng

- **Cấu hình Dịch vụ Nhắn tin Amazon:**

  - Thiết lập Amazon SQS (Simple Queue Service) cho xây dựng hàng đợi
  - Cấu hình Amazon SNS (Simple Notification Service) cho mô hình pub/sub
  - Triển khai định tuyến và lọc tin nhắn
  - Thực hành quy trình nhắn tin được kích hoạt bởi sự kiện
  - Tích hợp SQS và SNS với các dịch vụ AWS khác
  - Thiết lập Dead Letter Queues (DLQ) cho xử lý lỗi

- **Thực hành Lab:**

  - Tạo và kiểm tra kế hoạch sao lưu và khôi phục toàn diện
  - Cấu hình thành công kết nối VPC Peering
  - Thiết lập SQS queues và SNS topics
  - Kiểm tra quy trình nhắn tin từ đầu đến cuối
  - Cấu hình Security Groups với các quy tắc ingress/egress chính xác
  - Tích hợp EC2 instances với VPC networking
  - Xác thực giao tiếp cross-VPC

- **Kiến trúc Mạng Nâng cao:**

  - Thiết kế các mô hình kết nối mạng hybrid
  - Xây dựng kiến trúc mạng có tính sẵn sàng cao và phục hồi lỗi
  - Triển khai disaster recovery với chiến lược sao lưu và failover
  - Áp dụng phương pháp bảo mật mạng cho môi trường sản xuất
  - Hiểu khả năng mở rộng mạng và tối ưu hóa hiệu suất

- **Giám sát CloudWatch và Tối ưu hóa:**

  - Cấu hình CloudWatch metrics cho giám sát tài nguyên
  - Thiết lập cảnh báo cho các sự kiện sao lưu và khôi phục
  - Triển khai theo dõi chi phí và chiến lược tối ưu hóa
  - Áp dụng phương pháp tốt nhất cho tối ưu hóa hiệu suất
  - Giám sát hiệu suất dịch vụ nhắn tin và throughput
