---
title: "Worklog Tuần 6"
date: "2025-10-22"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

**Khoảng thời gian tuần: 13 - 19 tháng 10, 2025**

### Mục tiêu tuần 6:

- Thành thạo triển khai và quản lý cơ sở dữ liệu RDS
- Tìm hiểu triển khai ứng dụng với Auto Scaling
- Hiểu giám sát bằng CloudWatch
- Thực hành DynamoDB cho khối lượng công việc NoSQL
- Tìm hiểu mạng và phân phối nội dung

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                     |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ---------------------------------------------------------------------------------- |
| Monday    | - Tạo VPC, nhóm bảo mật EC2, nhóm bảo mật RDS <br> - Thiết lập nhóm con cơ sở dữ liệu <br> - Khởi chạy EC2 instance cho RDS <br> - Tạo RDS Database instance <br> - Triển khai ứng dụng <br> - Sao lưu và khôi phục cơ sở dữ liệu                                  | 10/13/2025   | 10/13/2025      | <https://000005.awsstudygroup.com/vi/>                                             |
| Tuesday   | - Thiết lập VPC cho Auto Scaling <br> - Tạo EC2 Instance và cơ sở dữ liệu với Amazon RDS <br> - Tạo AMI từ EC2 và Launch template <br> - Tạo target group và Load balancer <br> - Tạo Auto Scaling Group <br> - Kiểm tra thang scaling thủ công, theo lịch và động | 10/14/2025   | 10/14/2025      | <https://000006.awsstudygroup.com/vi/>                                             |
| Wednesday | - CloudWatch cơ bản và chỉ số <br> - Cấu hình và quản lý Amazon DynamoDB                                                                                                                                                                                           | 10/15/2025   | 10/15/2025      | <https://000008.awsstudygroup.com/vi/> <br> <https://000060.awsstudygroup.com/vi/> |
| Thursday  | - **Workshop Khoa học Dữ liệu trên AWS:** <br>&emsp; + AWS AI/ML Stack <br>&emsp; + Amazon Comprehend, Translate, Textract <br>&emsp; + Amazon Polly, Transcribe, Rekognition                                                                                      | 10/16/2025   | 10/16/2025      | Workshop Link                                                                      |
| Friday    | - AWS Networking and Content Delivery cơ bản <br> - CloudFront, Route 53 và các phương pháp tốt nhất CDN                                                                                                                                                           | 10/17/2025   | 10/17/2025      | <https://000092.awsstudygroup.com/vi/>                                             |
| Saturday  | - Xem xét các kiến trúc bảo mật (IAM, MFA, SCP, Mã hóa, Security Groups, NACLs) <br> - Xem xét GuardDuty, Shield, WAF, Secrets Manager <br> - Xem xét tối ưu hóa chi phí                                                                                           | 10/18/2025   | 10/18/2025      | <https://cloudjourney.awsstudygroup.com/>                                          |

### Kết quả đạt được tuần 6:

- **Thành thạo Triển khai Amazon RDS Database:**

  - Tạo VPC, security groups và DB subnet groups
  - Khởi chạy thành công RDS database instances
  - Cấu hình sao lưu tự động và thủ tục khôi phục cơ sở dữ liệu
  - Triển khai ứng dụng với kết nối cơ sở dữ liệu an toàn
  - Triển khai Multi-AZ cho tính sẵn sàng cao
  - Hiểu RDS parameter groups và option groups

- **Triển khai Giải pháp Auto Scaling:**

  - Tạo AMI tùy chỉnh từ EC2 instances
  - Cấu hình launch templates với các cấu hình cụ thể
  - Thiết lập Application Load Balancers với target groups
  - Triển khai các chính sách thang scaling thủ công, theo lịch và động
  - Kiểm tra các giải pháp thang scaling dưới tải
  - Giám sát các hoạt động thang scaling và metrics hiệu suất
  - Cấu hình lifecycle hooks cho scaling groups

- **Thành thạo CloudWatch Monitoring và Observability:**

  - Cấu hình CloudWatch metrics cho tất cả tài nguyên AWS
  - Tạo custom dashboards cho giám sát thực tế
  - Thiết lập cảnh báo và notifications cho các sự kiện quan trọng
  - Triển khai aggregation và phân tích logs
  - Hiểu metric math và custom metrics
  - Tạo chiến lược giám sát chi tiết

- **Khám phá DynamoDB NoSQL Database:**

  - Cấu hình DynamoDB tables và indexes
  - Hiểu partition keys và sort keys
  - Thực hành quản lý read/write capacity
  - Khám phá DynamoDB Streams cho xử lý sự kiện
  - Cấu hình TTL (Time-to-Live) cho hết hạn dữ liệu
  - Học các phương pháp hay nhất của DynamoDB

- **Tìm hiểu Dịch vụ AWS AI/ML:**

  - Khám phá kiến trúc AWS AI/ML Stack
  - Sử dụng Amazon Comprehend cho phân tích văn bản
  - Thực hành Amazon Translate cho dịch ngôn ngữ
  - Thử nghiệm Amazon Textract cho xử lý tài liệu
  - Cấu hình Amazon Polly cho chuyển đổi text-to-speech
  - Sử dụng Amazon Transcribe cho speech-to-text
  - Khám phá Amazon Rekognition cho phân tích hình ảnh

- **Thành thạo AWS Networking và Content Delivery:**

  - Cấu hình CloudFront CDN cho phân phối nội dung toàn cầu
  - Thiết lập CloudFront distributions với S3 origins
  - Sử dụng Route 53 cho quản lý DNS và routing policies
  - Triển khai geo-routing và failover strategies
  - Hiểu hành vi caching và invalidation
  - Áp dụng các phương pháp hay nhất về networking

- **Xem xét và Tăng cường Kiến trúc Bảo mật:**

  - Tăng cường hiểu biết về IAM, MFA và Service Control Policies (SCPs)
  - Xem xét các chiến lược mã hóa (KMS, TLS/ACM)
  - Nghiên cứu AWS GuardDuty cho phát hiện mối đe dọa
  - Hiểu AWS Shield cho bảo vệ DDoS
  - Xem xét AWS WAF cho bảo vệ ứng dụng
  - Thực hành với AWS Secrets Manager
  - Hiểu kết nối VPN và networking hybrid

- **Khắc phục sự cố Thực tế:**
  - Giải quyết các vấn đề kết nối giữa các instances
  - Sửa chữa xung đột định tuyến trong VPCs
  - Sửa lỗi cấu hình security groups
  - Xác thực kết nối ứng dụng end-to-end
