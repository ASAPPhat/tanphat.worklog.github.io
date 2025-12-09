---
title: "Worklog Tuần 4"
date: "2025-10-08"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

**Khoảng thời gian tuần: 29 tháng 9 - 5 tháng 10, 2025**

### Mục tiêu tuần 4:

- Thành thạo các dịch vụ bảo mật AWS cơ bản và quản lý danh tính
- Tìm hiểu mã hóa, quản lý bí mật và tuân thủ bảo mật
- Hiểu các cơ chế phát hiện và bảo vệ mối đe dọa
- Thực hành triển khai các phương pháp hay nhất về bảo mật AWS

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                 |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Monday    | - Liên kết danh tính với AWS Single Sign-On <br> - Quản lý quyền hạn với IAM Permission Boundaries <br> - Kiểm soát truy cập với IAM Policies và Conditions | 09/29/2025   | 09/29/2025      | AWS IAM Documentation                                                                                                          |
| Tuesday   | - Truy cập riêng tư đến S3 với VPC Endpoints <br> - Bảo vệ ứng dụng với AWS WAF                                                                             | 09/30/2025   | 09/30/2025      | <https://000111.awsstudygroup.com/vi/> <br> <https://000026.awsstudygroup.com/vi/>                                             |
| Wednesday | - Mã hóa với AWS Key Management Service (KMS) <br> - Bảo vệ dữ liệu với Amazon Macie <br> - Quản lý thông tin xác thực với AWS Secrets Manager              | 10/01/2025   | 10/01/2025      | <https://000033.awsstudygroup.com/vi/> <br> <https://000090.awsstudygroup.com/vi/> <br> <https://000096.awsstudygroup.com/vi/> |
| Thursday  | - Quản trị bảo mật với AWS Firewall Manager <br> - Phát hiện mối đe dọa với AWS GuardDuty                                                                   | 10/02/2025   | 10/02/2025      | <https://000097.awsstudygroup.com/vi/> <br> <https://000098.awsstudygroup.com/vi/>                                             |
| Friday    | - Xác thực liên miền với Amazon Cognito <br> - Các phương pháp bảo mật tốt nhất cho S3 <br> - Thực hành tích hợp các dịch vụ bảo mật                        | 10/03/2025   | 10/03/2025      | <https://000141.awsstudygroup.com/vi/> <br> AWS Identity Services                                                              |
| Saturday  | - Xem xét toàn bộ các dịch vụ bảo mật đã học <br> - Hoàn thành tài liệu tóm tắt Tuần 4                                                                      | 10/04/2025   | 10/04/2025      | AWS Well-Architected Framework                                                                                                 |

### Kết quả đạt được tuần 4:

- **Thành thạo AWS Identity and Access Management (IAM):**

  - Triển khai Identity Federation với AWS Single Sign-On (SSO)
  - Cấu hình IAM Permission Boundaries cho kiểm soát truy cập chi tiết
  - Thiết kế Advanced IAM Policies với conditions
  - Áp dụng nguyên tắc least privilege trên tất cả các dịch vụ

- **Triển khai Mã hóa Dữ liệu và Bảo vệ:**

  - Quản lý khóa mã hóa với AWS Key Management Service (KMS)
  - Cấu hình mã hóa dữ liệu lúc lưu trữ và truyền tải
  - Triển khai AWS Secrets Manager cho lưu trữ credentials an toàn
  - Tự động hóa rotation bí mật và access logging

- **Cấu hình Các Dịch vụ Bảo mật Nâng cao:**

  - Triển khai AWS WAF để bảo vệ lớp ứng dụng
  - Thiết lập AWS Firewall Manager cho quản lý bảo mật tập trung
  - Bật VPC Endpoints cho truy cập riêng tư S3
  - Cấu hình Security Groups và Network ACLs

- **Triển khai Phát hiện Mối đe dọa và Ứng phó:**

  - Kích hoạt AWS GuardDuty cho phát hiện mối đe dọa thông minh
  - Cấu hình Amazon Macie cho phát hiện và bảo vệ dữ liệu nhạy cảm
  - Bật AWS Security Hub cho giám sát bảo mật tập trung
  - Thiết lập cảnh báo tự động và quy trình ứng phó

- **Quản lý Tuân thủ Hệ thống và Vá lỗi:**

  - Sử dụng EC2 Image Builder cho tạo AMI tự động
  - Cấu hình quy trình vá lỗi hệ thống tự động
  - Triển khai giám sát tuân thủ thông qua Security Hub
  - Tiến hành xem xét audit trail

- **Triển khai Xác thực và Ủy quyền Người dùng:**

  - Cấu hình Amazon Cognito cho xác thực liên miền
  - Thiết lập Multi-Factor Authentication (MFA) enforcement
  - Tạo và quản lý user pools và identity pools
  - Triển khai role-based access control (RBAC)

- **Áp dụng Phương pháp Bảo mật Hay nhất:**

  - Triển khai các phương pháp bảo mật hay nhất cho S3
  - Cấu hình mã hóa cho tất cả các kho dữ liệu
  - Thiết lập CloudTrail logging cho mục đích audit
  - Áp dụng chiến lược bảo mật defense-in-depth

- **Tích hợp AWS CLI cho Quản lý Bảo mật:**

  - Sử dụng AWS CLI cho các hoạt động IAM theo lập trình
  - Quản lý credentials và authentication profiles
  - Thực hiện cấu hình bảo mật qua dòng lệnh
  - Tự động hóa các hoạt động bảo mật bằng scripts

- **Kiến trúc Bảo mật Toàn diện:**
  - Thiết kế chiến lược bảo mật defense-in-depth
  - Tích hợp nhiều dịch vụ bảo mật AWS
  - Tài liệu hóa các yêu cầu tuân thủ bảo mật
  - Chuẩn bị cho cơ sở hạ tầng AWS an toàn
