---
title: "Blog 2: Xây dựng Các Agents AI Thế hệ tiếp theo"
date: "2025-09-18"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

## **[Blog Lĩnh vực công của AWS](https://aws.amazon.com/blogs/publicsector/)**

# Xây dựng các agent AI thế hệ tiếp theo: AWS trao quyền cho các đối tác với mô-đun agent AI mới của Chương trình Chuyển đổi Đối tác AWS dành cho lĩnh vực công

bởi Jasmine Thakkar và Mohan CV vào ngày 15 THÁNG 9 2025 trong[ ](https://aws.amazon.com/blogs/publicsector/category/post-types/announcements/)[Thông báo](https://aws.amazon.com/blogs/publicsector/category/post-types/announcements/),[ ](https://aws.amazon.com/blogs/publicsector/category/artificial-intelligence/)[Trí tuệ nhân tạo](https://aws.amazon.com/blogs/publicsector/category/artificial-intelligence/),[ ](https://aws.amazon.com/blogs/publicsector/category/post-types/partner-solutions/)[Giải pháp của đối tác](https://aws.amazon.com/blogs/publicsector/category/post-types/partner-solutions/),[ ](https://aws.amazon.com/blogs/publicsector/category/public-sector/)[Lĩnh vực công](https://aws.amazon.com/blogs/publicsector/category/public-sector/),[ ](https://aws.amazon.com/blogs/publicsector/category/public-sector/public-sector-partners/)[Đối tác lĩnh vực công](https://aws.amazon.com/blogs/publicsector/category/public-sector/public-sector-partners/)[ ](https://aws.amazon.com/blogs/publicsector/build-next-gen-ai-agents-aws-empowers-partners-with-aws-partner-transformation-programs-new-agentic-ai-module-for-public-sector/)[Đường dẫn cố định](https://aws.amazon.com/blogs/publicsector/build-next-gen-ai-agents-aws-empowers-partners-with-aws-partner-transformation-programs-new-agentic-ai-module-for-public-sector/)[ ](https://aws.amazon.com/blogs/publicsector/build-next-gen-ai-agents-aws-empowers-partners-with-aws-partner-transformation-programs-new-agentic-ai-module-for-public-sector/#)[Chia sẻ](https://aws.amazon.com/blogs/publicsector/build-next-gen-ai-agents-aws-empowers-partners-with-aws-partner-transformation-programs-new-agentic-ai-module-for-public-sector/#)

![Enter image alt description](/images/Blog/blog2/AWS-Public-Sector-Blog-Featured-Images-Blog-Header-static-template-Autosaved-13.png)

Cuộc cách mạng trí tuệ nhân tạo (AI) đã bước vào một giai đoạn mới đầy hứng khởi và Amazon Web Services (AWS) đang trao quyền cho các đối tác để dẫn đầu sự chuyển đổi này. Hôm nay, chúng tôi vui mừng thông báo ra mắt mô-đun agent AI mới trong[ ](https://aws.amazon.com/partners/programs/partner-transformation/)[Chương trình Chuyển đổi Đối tác AWS (PTP)](https://aws.amazon.com/partners/programs/partner-transformation/), được thiết kế để tăng tốc khả năng của các đối tác trong việc xây dựng các giải pháp AI tự trị. Sáng kiến chiến lược này ra đời vào một thời điểm quan trọng, khi số lượng ứng dụng doanh nghiệp tích hợp agent AI tiếp tục tăng vọt, mang đến những cơ hội chưa từng có cho sự đổi mới trong lĩnh vực công và hơn thế nữa.

Tuy nhiên, cũng như bất kỳ công nghệ mang tính chuyển đổi nào, nhiều tổ chức đều tự đặt ra câu hỏi giống nhau: Làm thế nào để chúng ta chuyển từ những ý tưởng lớn sang thực thi thực tế bằng cách sử dụng agent AI ? Đó là lý do tại sao mô-đun PTP mới có hai lộ trình được xây dựng cẩn thận, phù hợp để đáp ứng các đối tác ở bất cứ đâu trong hành trình agent AI của họ. Lộ trình Nền tảng được thiết kế cho các đối tác bắt đầu hành trình agnet AI của họ, cung cấp thông tin chi tiết chiến lược và phát triển trường hợp sử dụng có hướng dẫn, đỉnh cao là một bằng chứng khái niệm chức năng. Đối với các đối tác sẵn sàng chuyển sang sản xuất, Lộ trình Phát triển Giải pháp cung cấp triển khai kỹ thuật tăng tốc tận dụng các dịch vụ AWS mạnh mẽ bao gồm[ ](https://aws.amazon.com/bedrock/agentcore/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[Amazon Bedrock AgentCore](https://aws.amazon.com/bedrock/agentcore/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833),[ ](https://strandsagents.com/latest/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[Strands Agents](https://strandsagents.com/latest/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833) và các công nghệ khác dẫn đến các sản phẩm khả thi tối thiểu (MVP) sẵn sàng cho sản xuất mang lại giá trị ngay lập tức cho khách hàng. Các Đối tác AWS cũng có thể xuất bản các giải pháp đã hoàn thành lên trang giải pháp[ ](https://aws.amazon.com/marketplace/solutions/ai-agents-and-tools/?ams#interactive-card-vertical#pattern-data.filter=%7B%22filters%22%3A%5B%5D%7D)[AI Agent & Tools](https://aws.amazon.com/marketplace/solutions/ai-agents-and-tools/?ams#interactive-card-vertical#pattern-data.filter=%7B%22filters%22%3A%5B%5D%7D) trong AWS Marketplace.

“Các Đối tác AWS đang tiếp tục thúc đẩy việc áp dụng AI nhanh chóng trong lĩnh vực công. Với mô-đun PTP mới này, chúng tôi không chỉ chia sẻ công nghệ, chúng tôi đang cung cấp một kế hoạch chi tiết để tăng tốc các dịch vụ của Đối tác AWS trong không gian agebt AI,” Mike Cannady, giám đốc đối tác cốt lõi cho lĩnh vực công tại AWS cho biết.

Các đối tác tham gia chương trình có quyền truy cập vào một bộ tài nguyên phong phú, bao gồm nội dung hội thảo độc quyền, hỗ trợ triển khai từ các chuyên gia AWS, tín dụng sandbox để phát triển và hướng dẫn toàn diện để niêm yết trên AWS Marketplace.

![Enter image alt description](/images/Blog/blog2/Picture3-5.png)

_Hình 1. Mô-đun agent AI của AWS PTP để xây dựng và mở rộng quy mô các giải pháp tác nhân thông minh_

Trọng tâm của sáng kiến này là danh mục toàn diện các dịch vụ ageny AI của AWS, chẳng hạn như[ ](https://aws.amazon.com/bedrock/agentcore/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[Amazon Bedrock AgentCore](https://aws.amazon.com/bedrock/agentcore/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833),[ ](https://aws.amazon.com/q/developer/build/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[Amazon Q](https://aws.amazon.com/q/developer/build/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833),[ ](https://aws.amazon.com/transform/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[AWS Transform](https://aws.amazon.com/transform/?refid=6da207ce-1440-41a4-b16f-3003bf7e4833),[ ](https://aws.amazon.com/blogs/opensource/introducing-strands-agents-1-0-production-ready-multi-agent-orchestration-made-simple/)[Strands Agents,](https://aws.amazon.com/blogs/opensource/introducing-strands-agents-1-0-production-ready-multi-agent-orchestration-made-simple/) và[ ](https://labs.amazon.science/blog/nova-act?refid=6da207ce-1440-41a4-b16f-3003bf7e4833)[Amazon Nova Act](https://labs.amazon.science/blog/nova-act?refid=6da207ce-1440-41a4-b16f-3003bf7e4833). Những công cụ mạnh mẽ này cho phép các đối tác xây dựng các agent AI tinh vi có thể hiểu, quyết định và hành động tự trị trong khi vẫn duy trì các tiêu chuẩn cao nhất về bảo mật và tuân thủ—những yêu cầu quan trọng đối với các triển khai trong lĩnh vực công.

“Dựa trên sự phấn khích của[ ](https://aws.amazon.com/events/summits/new-york/)[AWS Summit New York City](https://aws.amazon.com/events/summits/new-york/), chúng tôi đang biến AWS thành nơi tốt nhất cho các tác nhân hữu ích nhất thế giới. PTP mang lại sự hỗ trợ kỹ thuật để trao quyền cho các đối tác của chúng tôi tạo ra các trải nghiệm có tính tác nhân, thay đổi căn bản cách lĩnh vực công phục vụ công dân của mình,_”_ Alex Martinez, giám đốc lĩnh vực công, kiến trúc giải pháp đối tác tại AWS chia sẻ.

Các ứng dụng tiềm năng có tính chuyển đổi: từ các agent AI tối ưu hóa hoạt động của chính phủ và nâng cao dịch vụ công dân đến các hệ thống cách mạng hóa việc cung cấp dịch vụ chăm sóc sức khỏe và trải nghiệm giáo dục. Khi các tổ chức trên toàn thế giới tìm cách khai thác những khả năng này, các Đối tác AWS có vị thế độc đáo để dẫn đầu làn sóng đổi mới tiếp theo này, được hỗ trợ bởi nền tảng đám mây toàn diện và an toàn nhất để phát triển AI.

Dựa trên cam kết của AWS đối với sự thành công của đối tác, mô-đun PTP mới cung cấp một khuôn khổ vững chắc gồm các phương pháp tiếp cận có cấu trúc, các phương pháp hay nhất, quản trị và các biện pháp bảo vệ—cho phép các đối tác tăng tốc chu kỳ phát triển, giảm thiểu rủi ro và khai thác toàn bộ tiềm năng của các giải pháp agent AI.

Các đối tác quan tâm đến việc tham gia mô-đun mới này có thể liên hệ với người quản lý tài khoản Đối tác AWS hoặc người quản lý phát triển đối tác của họ để tìm hiểu thêm về[ ](https://aws.amazon.com/partners/programs/partner-transformation/)[chương trình PTP](https://aws.amazon.com/partners/programs/partner-transformation/) và bắt đầu hành trình agent AI của họ. Tương lai của AI là dựa trên tác nhân, an toàn và được xây dựng trên AWS—và các đối tác của chúng tôi đang đi đầu trong sự chuyển đổi thú vị này.

![Enter image alt description](/images/Blog/blog2/Picture2-6.png)

### **Jasmine Thakkar**

Jasmine là người đứng đầu toàn cầu của Chương trình Chuyển đổi Đối tác AWS (PTP), nơi cô giúp các Đối tác AWS tăng tốc hành trình đám mây của họ và thúc đẩy sự chuyển đổi có ý nghĩa cho công dân thông qua đổi mới trong lĩnh vực công. Cô dẫn dắt một chương trình trang bị toàn diện cho các đối tác hướng dẫn chiến lược, chuyên môn kỹ thuật và các phương pháp hay nhất cho phép họ xây dựng các điện toán đám mây thực tiễn thành công đồng thời thúc đẩy tăng trưởng và mang lại kết quả tốt hơn cho khách hàng.

![Enter image alt description](/images/Blog/blog2/Picture1-13.png)

### **Mohan CV**

Mohan là một kiến trúc sư chính tại AWS, đam mê giúp đỡ các đối tác và khách hàng tận dụng các công nghệ mới nổi như agent AI để chuyển đổi tổ chức của họ và cung cấp các giải pháp sáng tạo giải quyết các thách thức kinh doanh phức tạp. Anh có nhiều kinh nghiệm trong việc dẫn dắt các chuyển đổi kỹ thuật số quy mô lớn, chuyên về dữ liệu và AI.
