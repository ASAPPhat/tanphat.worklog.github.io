---
title: "Worklog Tuần 11"
date: "2025-11-26"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

**Khoảng thời gian tuần: 17 - 23 tháng 11, 2025**

### Mục tiêu tuần 11:

- Tiếp tục phát triển các hàm Lambda bằng Python
- Tạo dữ liệu demo cho ứng dụng
- Tìm hiểu Docker
- Triển khai container Docker đến ECR
- Xây dựng chatbot và chức năng quản lý nhân viên vắng mặt

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                     |
| --------- | ------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------------------------------------------- |
| Monday    | - AWS Cloud Mastery #2 DevOps on AWS <br> - Code demo chức năng quản lý nhân viên vắng mặt | 11/17/2025   | 11/17/2025      |                                                    |
| Tuesday   | - Tạo dữ liệu demo cho ứng dụng <br> - Update dashboard                                    | 11/18/2025   | 11/18/2025      | Kho lưu trữ dự án                                  |
| Wednesday | - Update Lambda function <br> - Code chức năng quản lý vắng mặt                            | 11/19/2025   | 11/19/2025      | Tài liệu dự án                                     |
| Thursday  | - Hướng dẫn Docker và containerization <br> - Demo và push Docker đến ECR                  | 11/20/2025   | 11/20/2025      | <https://youtu.be/pg19Z8LL06w?si=QyLqSkxfBPJ1ygbu> |
| Friday    | - Sửa triển khai Docker cho ML model được train local lên môi trường AWS                   | 11/21/2025   | 11/21/2025      | https://youtu.be/AYAh6YDXuho?si=Q1FOV2DCQgcKDKAo   |
| Saturday  | - Phản hồi giao diện người dùng/trải nghiệm bảng điều khiển <br> - Tóm tắt tuần 11         | 11/22/2025   | 11/22/2025      | <https://cloudjourney.awsstudygroup.com/>          |

### Kết quả đạt được tuần 11:

- **Tiếp tục Phát triển Lambda Functions bằng Python:**

  - Nâng cao các triển khai Lambda functions với thêm các tính năng
  - Triển khai logic kinh doanh phức tạp hơn bằng Python
  - Tối ưu hóa hiệu suất và sử dụng tài nguyên hàm
  - Thêm xử lý lỗi và logging toàn diện
  - Triển khai versioning và aliases hàm
  - Tối ưu hóa gói đặc triển khai Lambda
  - Thực hành tổ chức và tái sử dụng code
  - Triển khai giám sát và alerting cho hàm

- **Tạo Dữ liệu Demo cho Kiểm tra Ứng dụng:**

  - Tạo các bộ dữ liệu demo thực tế cho kiểm tra
  - Triển khai các kịch bản tạo dữ liệu bằng Python
  - Tạo dữ liệu metrics và time-series mẫu
  - Tạo các kịch bản kiểm tra cho xác thực hàm
  - Đổ vào DynamoDB với dữ liệu demo
  - Tạo các kịch bản alert cho kiểm tra
  - Đổ vào hơn cơ sở dữ liệu người dùng mẫu
  - Đảm bảo tính nhất quán và tính toàn vẹn dữ liệu

- **Mã hóa Chức năng Quản lý Nhân viên Vắng mặt:**

  - Thiết kế kiến trúc hàm cho quản lý thẳng dựu nhân viên
  - Triển khai logic theo dõi thẳng dựu nhân viên
  - Tạo các hàm ghi lại sự kiện vắng mặt
  - Xây dựng các hàm báo cáo cho các mẫu thẳng dựu
  - Tích hợp với DynamoDB cho tự lưu trữ dữ liệu
  - Triển khai logic thông báo cho nhân viên vắng mặt
  - Tạo các widget bảng điều khiển cho metrics thẳng dựu
  - Tích hợp với các hệ thống nhân sự cho đồng bộ dữ liệu

- **Thành thạo Docker Containerization:**

  - Tạo hệ cơ bản Docker và các khái niệm container hóa
  - Tạo Dockerfiles cho Lambda functions
  - Hiểu các layer hình ảnh Docker và tối ưu hóa
  - Xây dựng hình ảnh Docker với các phụ thuộc thích hợp
  - Thực hành multi-stage builds cho tối ưu hóa
  - Triển khai các phương pháp hay nhất Docker cho production
  - Tạo .dockerignore files cho hiệu suất
  - Thực hành kiểm tra Docker cở đỉa trước triển khai

- **Triển khai Container Docker đến ECR (Elastic Container Registry):**

  - Thiết lập kho lưu trữ ECR cho container
  - Cấu hình kiểm soát truy cập và quyền ECR
  - Gán thẻ các hình ảnh Docker với các phiên bản thích hợp
  - Đẩy các hình ảnh Docker đến kho lưu trữ ECR
  - Thiết lập các chính sách vòng đời hình ảnh
  - Cấu hình quản lý hình ảnh và phát hiện lỗi hổ
  - Triển khai các chính sách giữ lưu và dức dữ
  - Thực hành quản lý và tổ chức kho lưu trữ ECR

- **Tham dự Hội thảo AWS Cloud Mastery Series: DevOps trên AWS:**

  - Tìm hiểu các thường lâm DevOps và tự động hóa
  - Khám phá các đường ứng CI/CD trên AWS
  - Hiểu các khái niệm Infrastructure as Code (IaC)
  - Thực hành kiểm tra và triển khai tự động
  - Tìm hiểu về các chiến lược triển khai
  - Khám phá các phương pháp hay nhất giám sát và logging
  - Kết nối với các chuyên gia AWS DevOps
  - Tạo cơ sở cho tự động hóa dự án

- **Cập nhật Các Hàm Bảng Điều Khiển với Các Tính năng Nâng cao:**

  - Thêm các metrics và khả năng visualization mới
  - Triển khai cập nhật dữ liệu real-time
  - Nâng cao tính phản hồi của bảng điều khiển
  - Thêm các tính năng lọc và tổng hợp
  - Triển khai tùy chỉnh bảng điều khiển
  - Thêm khả năng chi tiết cho phân tích cột lại
  - Nâng cao hiệu suất cho các tập dữ liệu lớn
  - Triển khai các chiến lược lưu vào bản điều khiển

- **Thu thập Phản hồi UI/UX và Triển khai Các Cải Thiện:**

  - Thu thập phản hồi từ các bên quan đôi
  - Đánh giá các cải thiện trải nghiệm người dùng
  - Triển khai các tân chỉn thiết kế
  - Tối ưu hóa bản đặc của giao diện người dùng
  - Nâng cao các tính năng khử trợ cấp
  - Nâng cao thiết kế và thương hiệu trực quan
  - Triển khai thiết kế phản hồi cho các thiết bị di động
  - Tài liệu hóa các quyết định thiết kế dựa trên phản hồi

- **Chu Bị cho Giai đoạn Tích hợp và Kiểm tra:**

  - Xác thực tất cả các thành phần sẵn sàng tích hợp
  - Chu bị các kịch bản và test cases
  - Thiết lập các môi trường kiểm tra
  - Tài liệu hóa các thủ tục tích hợp
  - Tạo các kịch bản triển khai
  - Thiết lập các thủ tục rollback
  - Chu bị giám sát và alerting cho production
  - Tiến hành xác thực trước triển khai
