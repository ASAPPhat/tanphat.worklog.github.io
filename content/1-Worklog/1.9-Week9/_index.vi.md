---
title: "Worklog Tuần 9"
date: "2025-11-12"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

**Khoảng thời gian tuần: 3 - 9 tháng 11, 2025**

### Mục tiêu tuần 9:

- Tìm hiểu giám sát nâng cao với CloudWatch và Grafana
- Thành thạo CloudFront CDN để phân phối nội dung
- Hiểu gắn tag tài nguyên và kiểm soát truy cập IAM
- Thực hành AWS Systems Manager và hoạt động xuất sắc

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                           | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                 |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Monday    | - Giám sát nâng cao với CloudWatch và Grafana <br> - Công việc liên quan đến đề xuất                                                                | 11/03/2025   | 11/03/2025      | <https://000029.awsstudygroup.com/vi/>                                                                                         |
| Tuesday   | - CloudFront với S3 <br> - Quản lý Truy cập dịch vụ EC2 bằng Thẻ tài nguyên thông qua Dịch vụ IAM                                                   | 11/04/2025   | 11/04/2025      | <https://000094.awsstudygroup.com/vi/> <br> <https://000048.awsstudygroup.com/vi/>                                             |
| Wednesday | - Quản lý patches và chạy lệnh trên nhiều máy chủ với AWS Systems Manager <br> - Làm việc với AWS Systems Manager - Trình quản lý phiên             | 11/05/2025   | 11/05/2025      | <https://000031.awsstudygroup.com/vi/> <br> <https://000058.awsstudygroup.com/vi/>                                             |
| Thursday  | - Chọn kích thước EC2 đúng <br> - Giám sát cơ sở hạ tầng mạng <br> - Tự động lưu trữ Bản chụp EBS Amazon bằng Trình quản lý Vòng đời dữ liệu Amazon | 11/06/2025   | 11/06/2025      | <https://000032.awsstudygroup.com/vi/> <br> <https://000074.awsstudygroup.com/vi/> <br> <https://000088.awsstudygroup.com/vi/> |
| Friday    | - Hoàn tất chuẩn bị đề xuất                                                                                                                         | 11/07/2025   | 11/07/2025      | Tài liệu AWS                                                                                                                   |
| Saturday  | - Tóm tắt tuần 9                                                                                                                                    | 11/08/2025   | 11/08/2025      | <https://cloudjourney.awsstudygroup.com/>                                                                                      |

### Kết quả đạt được tuần 9:

- **Thành thạo Giám sát Nâng cao CloudWatch và Grafana:**

  - Cấu hình các dàn hình tùy chỉnh CloudWatch với metrics và alarms
  - Triển khai CloudWatch Logs Insights cho phân tích và truy vấn log
  - Thiết lập aggregation metrics trên nhiều dịch vụ
  - Cấu hình phát hiện anomaly và predictive alarms
  - Tích hợp Grafana với CloudWatch data sources
  - Tạo các dàn hình Grafana cho visualization và alerting
  - Thực hành các mẫu và phương pháp hay nhất giám sát
  - Cấu hình kiến trúc giám sát cross-account

- **Triển khai CloudFront CDN cho Phân phối Nội dung:**

  - Tạo các CloudFront distributions với S3 origins
  - Cấu hình origin access identity (OAI) cho truy cập S3 an toàn
  - Thiết lập nhiều origins với failover behavior
  - Triển khai cache behaviors và tối ưu hóa TTL
  - Cấu hình request/response custom headers
  - Triển khai geo-restriction và geo-based routing
  - Thực hành các chiến lược invalidation và cache busting
  - Tối ưu hóa CloudFront cho hiệu suất và chi phí

- **Thành thạo Tagging Tài nguyên và Kiểm soát Truy cập IAM:**

  - Triển khai chiến lược tagging toàn diện cho tài nguyên
  - Tạo các chín sách kiểm soát truy cập dựa trên tag trong IAM
  - Thiết lập tag compliance và cost allocation tags
  - Sử dụng tags cho tổ chức và quản lý tài nguyên
  - Triển khai attribute-based access control (ABAC)
  - Áp dụng tag-based resource policies
  - Thực hành lọc tài nguyên theo tags trong AWS Management Console
  - Xem xét tag governance và enforcement

- **Thực hành AWS Systems Manager cho Operational Excellence:**

  - Cấu hình Systems Manager Agent trên EC2 instances
  - Thiết lập thư viện Systems Manager Document (SSM Document)
  - Triển khai quản lý bản với tự động
  - Sử dụng Patch Manager cho quản lý và patching compliance
  - Thực hành chạy lệnh trên nhiều instances
  - Sử dụng Automation documents cho các tác vụ hoạt động phức tạp
  - Thiết lập maintenance windows cho các hoạt động lập lịch
  - Xem xét các phương pháp hay nhất Systems Manager

- **Thành thạo AWS Systems Manager Session Manager:**

  - Cấu hình Session Manager cho truy cập shell an toàn
  - Thiết lập đằng nhập IAM cho sử dụng Session Manager
  - Thực hành logging và audit session history
  - Triển khai mã hóa KMS cho dữ liệu phiên
  - Sử dụng Session Manager thay thế SSH/RDP
  - Cấu hình session preferences và cài đặt kết nối
  - Thực hành chia sẻ và cộng tác trên phiên
  - Hiểu các lợi ích bảo mật của Session Manager

- **Tối ưu hóa EC2 Instance Sizing và Hiệu suất:**

  - Phân tích EC2 instance performance metrics
  - Sử dụng AWS Compute Optimizer cho khuyến nghị sizing
  - Điều chỉnh kích thước instances dựa trên mẫu sử dụng
  - Đánh giá burstable vs. dedicated performance
  - Xem xét các family types và use cases của instances
  - Thực hành thiết lập baseline hiệu suất
  - Triển khai monitoring cho lập kế hoạch dự đằng
  - Tính toán tiết kiệm chi phí từ right-sizing

- **Quản lý Cơ sở hạ tầng Mạng và Giám sát:**

  - Cấu hình VPC Flow Logs cho phân tích lược lương
  - Thiết lập CloudWatch Network Insights cho troubleshooting kết nối
  - Giám sát elastic network interface (ENI) metrics
  - Phân tích đườ thông và latency patterns của mạng
  - Triển khai network topology analysis
  - Thực hành xác định network bottlenecks
  - Cấu hình network monitoring alarms
  - Xem xét các kỹ thuật tối ưu hóa hiệu suất mạng

- **Tự động hóa Quản lý EBS Snapshot bằng Data Lifecycle Manager:**

  - Cấu hình các chín sách Data Lifecycle Manager (DLM)
  - Thiết lập lịch tạo snapshot tự động
  - Triển khai các chín sách giữ lưu snapshots
  - Cấu hình sao chép snapshot cross-region
  - Thiết lập snapshot tagging tự động
  - Giám sát thực hiện chín sách DLM
  - Thực hành snapshot lifecycle automation
  - Tính toán chi phí lưu trữ cho snapshot retention

- **Chuẩn Bị Project Proposal với Chi tiết Kỹ thuật:**

  - Tinh chỉnh scope và kiến trúc dự án dựa trên các bài học
  - Kết hợp các chiến lược giám sát nâng cao
  - Tài liệu hóa scheme tagging tài nguyên
  - Đưa vào Systems Manager automation trong proposal
  - Cập nhật khuyến nghị kích thước cơ sở hạ tầng
  - Thêm các thương làm operational excellence
  - Chuẩn bị timeline và milestones triển khai
  - Xác thực khả năng kỹ thuật của giải pháp đề xuất
