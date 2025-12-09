---
title: "Worklog Tuần 7"
date: "2025-10-29"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

**Khoảng thời gian tuần: 20 - 26 tháng 10, 2025**

### Mục tiêu tuần 7:

- Thành thạo kiến trúc serverless với Lambda, S3, DynamoDB
- Tìm hiểu code phía trước cho API Gateway
- Thực hành triển khai serverless
- Xem xét và cải thiện tài liệu đề xuất

### Các công việc cần triển khai trong tuần này:

| Thứ       | Công việc                                                                                                                                                                    | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                     |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------- |
| Monday    | - Optimizing EC2 Costs with Lambda                                                                                                                                           | 10/20/2025   | 10/20/2025      | https://000022.awsstudygroup.com/                                                  |
| Tuesday   | - **Serverless Lambda, S3, DynamoDB:** Tìm hiểu cơ sở kiến trúc serverless <br> - **Serverless Front-End:** Tìm hiểu cách viết code phía trước gọi API Gateway               | 10/21/2025   | 10/21/2025      | <https://000078.awsstudygroup.com/vi/> <br> <https://000079.awsstudygroup.com/vi/> |
| Wednesday | - **Ôn tập Giữa kỳ:** Tìm hiểu các mẫu kiến trúc có khả năng phục hồi                                                                                                        | 10/22/2025   | 10/22/2025      | AWS Documentation                                                                  |
| Thursday  | - **Tiếp tục ôn tập Kiến trúc Có khả năng Phục hồi** <br> - **Vẽ Sơ đồ Kiến trúc AWS** cho thiết kế dự án                                                                    | 10/23/2025   | 10/23/2025      | Workshop Materials                                                                 |
| Friday    | - **Hướng dẫn Amazon Bedrock:** <br>&emsp; + Cách sử dụng Bedrock <br>&emsp; + Tích hợp Lex + Lambda + Bedrock <br> - **Workshop AWS CLI:** Hoạt động S3, SNS, IAM, VPC, EC2 | 10/24/2025   | 10/24/2025      | <https://000011.awsstudygroup.com/vi/>                                             |
| Saturday  | - Ôn tập giữa kỳ <br> - Xem xét và hoàn thiện Proposal <br> - Tóm tắt tuần 7                                                                                                 | 10/25/2025   | 10/25/2025      | <https://cloudjourney.awsstudygroup.com/>                                          |

### Kết quả đạt được tuần 7:

- **Thành thạo Thiết kế Kiến trúc Serverless:**

  - Hiểu các mẫu kiến trúc hướng sự kiện và phương pháp hay nhất
  - Tìm hiểu về tạo, cấu hình và triển khai Lambda functions
  - Thành thạo các mô hình thực thi, triggers và quyền trong Lambda
  - Thiết kế các quy trình ứng dụng serverless sử dụng nhiều dịch vụ AWS
  - Hiểu hành vi scaling và concurrency trong serverless
  - Thực hành soạn thảo Lambda functions thành các hệ thống hoàn chỉnh
  - Tìm hiểu Lambda layers và chiến lược tái sử dụng code

- **Triển khai Giải pháp Lambda, S3 và DynamoDB:**

  - Tạo Lambda functions cho các hoạt động tính toán
  - Cấu hình S3 triggers để gửi Lambda functions
  - Thiết lập DynamoDB tables cho lưu trữ dữ liệu serverless
  - Tích hợp Lambda với DynamoDB cho hoạt động đọc/ghi
  - Triển khai event source mappings cho xử lý asynchronous
  - Thực hành xử lý lỗi và logic retry trong serverless
  - Kiểm tra các quy trình serverless end-to-end

- **Phát triển Front-End Code cho API Gateway:**

  - Tạo ứng dụng client HTML/JavaScript
  - Triển khai các lệnh gọi API đến API Gateway endpoints
  - Xử lý các mẫu request/response không đồng bộ
  - Triển khai xử lý lỗi và validation trên phía client
  - Thực hành cấu hình CORS cho các ứng dụng web
  - Kiểm tra tích hợp front-end với backend APIs
  - Triển khai static front-end lên S3 với CloudFront CDN

- **Ôn tập và Thành thạo Khái niệm Giữa kỳ:**

  - Tìm hiểu các nguyên tắc và mẫu thiết kế kiến trúc có khả năng phục hồi
  - Xem xét các chiến lược triển khai multi-AZ
  - Thành thạo các khái niệm auto-scaling và load balancing
  - Hiểu lập kế hoạch phục hồi thảm họa và tiếp tục hoạt động kinh doanh
  - Xem xét các thủ tục sao lưu và khôi phục
  - Tìm hiểu các cơ chế fault-tolerance trên các dịch vụ AWS
  - Thực hành thiết kế các hệ thống có tính sẵn sàng cao

- **Thiết kế Sơ đồ Kiến trúc AWS:**

  - Tạo các sơ đồ kiến trúc toàn diện bằng draw.io
  - Trực quan hóa các giải pháp serverless đa dịch vụ
  - Tài liệu hóa mỗi quan hệ giữa các thành phần và luồng dữ liệu
  - Áp dụng các phương pháp hay nhất về thiết kế kiến trúc AWS
  - Tạo sơ đồ kiến trúc triển khai và mạng
  - Thực hành xem xét và tài liệu hóa kiến trúc
  - Sử dụng bộ icon AWS chính thức cho sơ đồ chuyên nghiệp

- **Khám phá Amazon Bedrock cho AI Generative:**

  - Tìm hiểu các khái niệm cơ bản và khả năng của Bedrock
  - Hiểu các mô hình cơ sở có sẵn trong Bedrock (Claude, Llama, v.v.)
  - Thực hành kỹ thuật prompt engineering cho tương tác AI hiệu quả
  - Tích hợp Bedrock với Lambda functions cho AI serverless
  - Khám phá Bedrock knowledge bases cho retrieval-augmented generation (RAG)
  - Thử nghiệm các template prompt khác nhau và tham số mô hình
  - Hiểu các giới hạn API và xem xét giá cả

- **Tích hợp Lex, Lambda và Bedrock cho Chatbots:**

  - Cấu hình bot AI trò chuyện Amazon Lex
  - Thiết lập intents, slots và logic fulfillment
  - Tích hợp Lambda functions cho xử lý backend
  - Kết nối Bedrock cho nhận thức ngôn ngữ tự nhiên
  - Triển khai các luồng trò chuyện đa lần
  - Kiểm tra các tương tác bot thông qua các kênh khác nhau
  - Thực hành triển khai và giám sát các giải pháp chatbot

- **Thành thạo AWS CLI cho Hoạt động Cơ sở hạ tầng:**

  - Thực hiện các hoạt động S3 theo chương trình (tạo, liệt kê, tải lên, tải xuống)
  - Quản lý SNS topics và subscriptions qua CLI
  - Cấu hình IAM roles, policies và permissions thông qua CLI
  - Quản lý VPC resources bao gồm subnets, security groups và route tables
  - Tạo và quản lý EC2 instances theo chương trình
  - Thực hành các hoạt động hàng loạt và kịch bản tự động hóa
  - Hiểu các tùy chọn định dạng và lọc đầu ra CLI

- **Tối ưu hóa Chi phí EC2 bằng Các Giải pháp Serverless:**

  - Phân tích các mẫu sử dụng EC2 và xác định các cơ hội tối ưu hóa
  - Đánh giá Lambda như một giải pháp hiệu quả về chi phí cho các khối lượng công việc cụ thể
  - So sánh các mô hình giá giữa các cách tiếp cận truyền thống và serverless
  - Triển khai các biện pháp tiết kiệm chi phí bằng cách di chuyển khối lượng công việc sang Lambda
  - Thực hành cân nhắc các trường hợp dành riêng và spot instance
  - Tìm hiểu các khuyến nghị AWS Compute Optimizer
