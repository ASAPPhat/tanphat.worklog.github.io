---
title: "Worklog Tuần 10"
date: "2025-11-19"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

**Khoảng thời gian tuần: 10 - 16 tháng 11, 2025**

### Mục tiêu tuần 10:

- Tìm hiểu AWS Lambda với lập trình Python
- Tạo vai trò và quyền IAM cho dự án
- Xây dựng các hàm bảng điều khiển không máy chủ
- Thực hành phát triển và kiểm tra chức năng
- Khám phá AI/ML trên AWS

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ----------------------------------------- |
| Monday    | - Chia công việc dự án <br> - Tìm hiểu AWS Lambda với Python <br> - Tạo IAM roles cho dự án <br> - Cập nhật proposal <br> - code Dashboard | 11/10/2025   | 11/10/2025      | AWS Documentation                         |
| Tuesday   | - Tiếp tục tìm hiểu AWS Lambda với Python <br> - Xem xét và sửa proposal                                                                   | 11/11/2025   | 11/11/2025      | AWS Documentation                         |
| Wednesday | - code và deploy demo dashboard <br> - Feedback function                                                                                   | 11/12/2025   | 11/12/2025      | Project Repository                        |
| Thursday  | - Sửa dashboard <br> - Brainstorm thiết kế mẫu giao diện người dùng <br> - Feedback function                                               | 11/13/2025   | 11/13/2025      | Design Templates                          |
| Friday    | - AWS Cloud Mastery Series #1: AI/ML Fundamentals                                                                                          | 11/14/2025   | 11/14/2025      | Workshop Link                             |
| Saturday  | - Sửa và deploy dashboard function <br> - Tóm tắt tuần 10                                                                                  | 11/15/2025   | 11/15/2025      | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 10:

- **Thành thạo AWS Lambda với Lập trình Python:**

  - Tạo Lambda functions bằng Python từ đầu
  - Hiểu cú pháp hàm handler và tham số
  - Làm việc với môi trường thực thi và runtime
  - Triển khai Lambda layers cho tái sử dụng code
  - Thực hành quản lý phụ thuộc với pip trong Lambda
  - Làm việc với biến môi trường và secrets bảo mật
  - Triển khai context object và xử lý request/response
  - Thực hành xử lý lỗi và exception management

- **Tạo Vai trò IAM và Chín sách cho Bảo mật Dự án:**

  - Thiết kế các quyền IAM chi tiết cho Lambda functions
  - Tạo service roles với các quyền thích hợp
  - Cấu hình trust relationships cho service assumptions
  - Triển khai nguyên tắc least privilege access
  - Tạo chín sách cho các dịch vụ AWS cụ thể (S3, DynamoDB, CloudWatch)
  - Kiểm tra quyền IAM và debug các sự cố permission
  - Tài liệu hóa cấu trúc role và yêu cầu quyền
  - Xem xét các phương pháp hay nhất IAM

- **Phát triển Các Hàm Bảng Điều Khiển Serverless:**

  - Tạo Lambda functions để lấy và tổng hợp metrics
  - Triển khai logic cải biến dữ liệu bằng Python
  - Kết nối Lambda với DynamoDB cho lưu trữ dữ liệu
  - Tích hợp thu thập metrics CloudWatch
  - Triển khai logic tính toán tương quan và root cause analysis
  - Tạo các hàm alerting và notification
  - Triển khai aggregation và định dạng dữ liệu bảng điều khiển
  - Kiểm tra hành động hàm trong các kịch bản khác nhau

- **Thiết kế và Triển khai Hệ thống Quản lý Canh báo:**

  - Phát triển các chiến lược quản lý cảnh báo mọp
  - Tạo các hàm tương quan cánh báo
  - Triển khai logic deduplication cánh báo
  - Cấu hình routing và grouping cánh báo
  - Tạo quản lý threshold cánh báo
  - Triển khai tracking lịch sử cánh báo
  - Thiết kế mẫu notification cánh báo
  - Thực hành quản lý vòng đời cánh báo

- **Chia Công việc Dự án và Lập Kế hoạch Quy trình Nhóm:**

  - Xác định các thành phần và khả năng giao hàng dự án
  - Gán các tác vụ cho thành viên dựa trên kỳ năng
  - Tạo timeline và milestones dự án
  - Thiết lập quy trình cộng tác và giao tiếp
  - Thiết lập thủ tục review code và kiểm tra
  - Tài liệu hóa yêu cầu và đặc tả chỉ năng dự án
  - Tạo chiến lược version control và nhánh
  - Thiết lập quy trình triển khai và release

- **Cập nhật Dự án Proposal với Các Đặc Tả Kỹ Thuật:**

  - Tài liệu hóa thiết kế kế quả các thành phần và sử dụng
  - Xác định yêu cầu Lambda functions và interfaces
  - Xác định cáu trúc và chín sách IAM role
  - Chi tiết các mô hình dữ liệu và chiến lược lưu trữ
  - Xác định endpoints API và điểm tích hợp
  - Tài liệu hóa yêu cầu giám sát và logging
  - Thêm ước tính chi phí và chiến lược tối ưu hóa
  - Đưa vào quy trình triển khai và hoạt động

- **Thiết kế Mẫu UI/UX và Brainstorm Giải pháp Thiết kế:**

  - Tạo wireframes cho giao diện bảng điều khiển
  - Thiết kế layouts phản hồi cho các kích thước thiết bị
  - Triển khai mẫu màu và các hướng dẫn branding
  - Tạo mẫu visualization cho metrics
  - Thiết kế giao diện alert và notification
  - Triển khai các mẫu user navigation và interaction
  - Thực hành usability testing và gộp ý
  - Tài liệu hóa quyết định và lý do thiết kế

- **Tham gia Workshop AWS Cloud Mastery Series: AI/ML Fundamentals:**

  - Tìm hiểu cơ bản AI/ML trên AWS
  - Khám phá các dịch vụ AWS AI/ML khác nhau
  - Hiểu quỏ trình machine learning và phương pháp hay nhất
  - Thực hành với các triển khai dịch vụ AI/ML
  - Kết nối với các người học AWS và chuyên gia khác
  - Tạo cơ sở cho các cải tiến dự án tiềm năng
  - Cập nhật kiến thức về khả năng AI/ML AWS đang trớen dấu

- **Triển khai và Kiểm tra Các Hàm Bảng Điều Khiển:**

  - Đóng gói và triển khai Lambda functions
  - Cấu hình function triggers và event sources
  - Kiểm tra thực thi hàm và định dạng đầu ra
  - Triển khai CI/CD pipeline cho triển khai hàm
  - Thực hiện load testing và tối ưu hóa hiệu suất
  - Triển khai giám sát và logging hàm
  - Tạo các test cases và tự động hóa kiểm tra
  - Xác thực chức năng bảng điều khiển end-to-end
