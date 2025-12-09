---
title: "Worklog Tuần 12"
date: "2025-12-03"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

**Khoảng thời gian tuần: 24 - 30 tháng 11, 2025**

### Mục tiêu tuần 12:

- Kiểm tra và triển khai chatbot Amazon Bedrock
- Hoàn thành chatbot với nghiên cứu RAG
- Xây dựng các chức năng quản lý tham dự và vắng mặt
- Hoàn thiện tất cả các thành phần dự án
- Chuẩn bị triển khai dự án và bản trình bày

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                      | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --------- | -------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| Monday    | - Demo và Kiểm tra Amazon Bedrock <br> - Thực hiện chức năng quản lý nhân viên vắng mặt                        | 11/24/2025   | 11/24/2025      | Tài liệu AWS Bedrock                      |
| Tuesday   | - Mã hóa chức năng chatbot <br> - Sửa chức năng auto_scoring <br> - Tạo quy trình làm việc để quản lý vắng mặt | 11/25/2025   | 11/25/2025      | Kho lưu trữ dự án                         |
| Wednesday | - Cấu hình và triển khai chatbot đến AWS Lambda <br> - Cấu hình tích hợp API Gateway                           | 11/26/2025   | 11/26/2025      | Hướng dẫn triển khai AWS                  |
| Thursday  | - Sửa chức năng truy vấn chatbot <br> - Nghiên cứu và thực hiện RAG                                            | 11/27/2025   | 11/27/2025      | Tài nguyên AWS AI/ML                      |
| Friday    | - Hoàn thiện chatbot <br> - Tạo lại các chức năng tham dự: check in/out và quản lý vắng mặt                    | 11/28/2025   | 11/28/2025      | Tài liệu dự án                            |
| Saturday  | - Kiểm tra và triển khai cuối cùng <br> - Chuẩn bị bài thuyết trình dự án <br> - Tóm tắt thực tập tuần 12      | 11/30/2025   | 11/30/2025      | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 12:

- **Kiểm tra và Triển khai Chatbot Amazon Bedrock:**

  - Hiểu khả năng và mô hình chatbot Bedrock
  - Tạo kiến trúc hàm chatbot trong Lambda
  - Tích hợp Bedrock với Lambda cho tạo văn bản
  - Kiểm tra các kịch bản trò chuyện khác nhau
  - Tối ưu hóa prompt engineering cho các phản hồi tốt hơn
  - Triển khai quản lý lịch sử trò chuyện
  - Thiết lập API Gateway cho truy cập chatbot
  - Triển khai chatbot đến môi trường production

- **Triển khai Retrieval-Augmented Generation (RAG):**

  - Nghiên cứu kiến trúc RAG và mô hình triển khai
  - Tạo cơ sở kiến thức cho chatbot
  - Triển khai truy xuất và xếp hạng tài liệu
  - Tích hợp tìm kiếm ngữ nghĩa với Bedrock
  - Tối ưu hóa truy xuất cho phản hồi liên quan
  - Triển khai tạo phản hồi với ngữ cảnh
  - Kiểm tra hiệu quả RAG với các truy vấn khác nhau
  - Tài liệu hóa cấu hình và thủ tục RAG

- **Xây dựng Hệ thống Quản lý Tham dự:**

  - Thiết kế các chức năng theo dõi tham dự
  - Triển khai chức năng check-in/check-out
  - Tạo bản ghi tham dự trong DynamoDB
  - Xây dựng các chức năng báo cáo tham dự
  - Triển khai logic xác thực tham dự
  - Tạo bảng điều khiển cho metrics tham dự
  - Thiết lập cảnh báo tham dự tự động
  - Tích hợp với hệ thống quản lý nhân viên

- **Thực hiện Chức năng Quản lý Nhân viên Vắng mặt:**

  - Tạo logic ghi lại và theo dõi vắng mặt
  - Xây dựng quy trình làm việc xác thực và phê duyệt vắng mặt
  - Triển khai hệ thống thông báo vắng mặt
  - Tạo báo cáo và phân tích vắng mặt
  - Thiết lập theo dõi tuân thủ vắng mặt
  - Tích hợp với hệ thống lịch và lên lịch
  - Triển khai quản lý giai đoạn vắng mặt
  - Tạo bảng điều khiển cho metrics vắng mặt

- **Sửa và Tối ưu hóa Chức năng Auto-Scoring:**

  - Gỡ lỗi vấn đề logic auto-scoring
  - Tối ưu hóa hiệu suất thuật toán scoring
  - Triển khai xử lý lỗi phù hợp
  - Sửa định dạng đầu vào và đầu ra dữ liệu
  - Kiểm tra scoring với các bộ dữ liệu khác nhau
  - Cải thiện độ chính xác và độ tin cậy scoring
  - Tài liệu hóa phương pháp luận scoring
  - Tạo kiểm tra tự động cho chức năng scoring

- **Cấu hình Tích hợp API Gateway:**

  - Thiết lập endpoints API Gateway cho chatbot
  - Cấu hình các mô hình request/response
  - Triển khai xác thực và ủy quyền
  - Thiết lập giới hạn tốc độ và điều chế
  - Cấu hình CORS cho các ứng dụng web
  - Triển khai ghi nhật ký và giám sát API
  - Tạo tài liệu API
  - Kiểm tra endpoints API end-to-end

- **Hoàn thiện Dự án và Triển khai:**

  - Thực hiện kiểm tra hệ thống toàn diện
  - Sửa và giải quyết tất cả các sự cố xác định
  - Tối ưu hóa hiệu suất và sử dụng tài nguyên
  - Thiết lập giám sát và cảnh báo
  - Tạo runbooks và thủ tục vận hành
  - Thiết lập các thủ tục khôi phục thảm họa
  - Triển khai tất cả các thành phần cho production
  - Xác minh chức năng production

- **Chuẩn bị Bản trình bày Dự án:**

  - Tài liệu hóa kiến trúc và thiết kế dự án
  - Tạo các slide bản trình bày với hình ảnh
  - Chuẩn bị thể hiện các tính năng chính
  - Tài liệu hóa thành tích và metrics dự án
  - Phác thảo timeline triển khai dự án
  - Làm nổi bật các bài học và insight
  - Chuẩn bị cho các phiên Q&A
  - Thực hành cách truyền bạt bản trình bày

- **Hoàn thành Hành trình Học AWS Toàn diện:**

  - Xem xét tất cả các dịch vụ AWS cốt lõi
  - Tổng hợp các bài học trong 12 tuần
  - Hiểu các mô hình tích hợp dịch vụ
  - Thành thạo các phương pháp hay nhất kiến trúc AWS
  - Xây dựng các giải pháp serverless end-to-end
  - Tích hợp nhiều dịch vụ AWS hiệu quả
  - Chuẩn bị cho các bài thi chứng chỉ AWS
  - Suy ngẫm về sự phát triển và thành tích thực tập

- **Hoàn thành Thực tập 12 Tuần FCAJ-AWS:**

  - Hoàn thành thành công tất cả các mục tiêu học tập
  - Xây dựng các giải pháp đám mây sẵn sàng production
  - Thành thạo các dịch vụ AWS cốt lõi và mô hình
  - Phát triển các kỹ năng kỹ thuật đám mây thực tế
  - Cộng tác với nhóm trên dự án thực tế
  - Đạt được sự phát triển kỹ thuật đáng kể
  - Chuẩn bị cho các vai trò đám mây chuyên nghiệp
  - Tài liệu hóa hành trình học tập toàn diện
