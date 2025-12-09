---
title: "Blog 3: Strands Agents và Phương pháp Hướng mô hình"
date: "2025-09-20"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## **[Blog mã nguồn mở của AWS](https://aws.amazon.com/blogs/opensource/)**

# Strands Agents và Phương pháp tiếp cận theo mô hình

bởi Arron Bailiss vào 12 THÁNG 9 2025 trong[ ](https://aws.amazon.com/blogs/opensource/category/artificial-intelligence/)[Trí tuệ nhân tạo](https://aws.amazon.com/blogs/opensource/category/artificial-intelligence/),[ ](https://aws.amazon.com/blogs/opensource/category/open-source/)[Mã nguồn mở](https://aws.amazon.com/blogs/opensource/category/open-source/),[ ](https://aws.amazon.com/blogs/opensource/category/post-types/technical-how-to/)[Hướng dẫn kỹ thuật](https://aws.amazon.com/blogs/opensource/category/post-types/technical-how-to/)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/)[Permalink](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#Comments)[Bình luận](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#Comments)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#)[Chia sẻ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#)

Cho đến gần đây, việc xây dựng các agent AI có nghĩa là phải vật lộn với các khung điều phối phức tạp. Các nhà phát triển đã viết các trạng thái máy phức tạp, các quy trình làm việc được xác định trước và mã xử lý lỗi mở rộng để hướng dẫn các mô hình ngôn ngữ thông qua các tác vụ nhiều bước. Chúng tôi cần xây dựng các cây quyết định phức tạp để xử lý các trường hợp “nếu lệnh gọi API không thành công?” hoặc “nếu người dùng hỏi điều gì đó bất ngờ?” Mặc dù đã nỗ lực, các tác nhân vẫn bị hỏng khi gặp phải các tình huống không lường trước được.

Strands Agents SDK áp dụng một **phương pháp tiếp cận theo mô hình** giúp loại bỏ hoàn toàn sự mong manh này. Thay vì cố gắng dự đoán và lập trình cho mọi tình huống có thể xảy ra, chúng tôi để các mô hình ngôn ngữ lớn hiện đại tự điều khiển hành vi của chúng, đưa ra các quyết định thông minh về việc sử dụng công cụ và thích ứng linh hoạt với bất cứ điều gì xảy ra. Cách tiếp cận này bền bỉ, có khả năng phục hồi tốt hơn vì nó cho phép các mô hình suy luận các vấn đề một cách linh hoạt. Khi một lệnh gọi API không thành công, mô hình không bị sập – nó suy luận về các giải pháp thay thế. Khi người dùng hỏi điều gì đó bất ngờ, mô hình không tuân theo một đường dẫn được xác định trước “Tôi không hiểu” – nó tìm ra cách để giúp đỡ, sử dụng các công cụ có sẵn. Khả năng suy luận của mô hình xử lý các trường hợp đặc biệt tốt hơn bất kỳ máy trạng thái nào chúng tôi có thể viết.

Cách tiếp cận dựa trên mô hình xuất phát từ kinh nghiệm thực tế của các nhóm AWS trong việc xây dựng các agent sản xuất cho[ ](https://kiro.dev/)[Kiro](https://kiro.dev/),[ ](https://aws.amazon.com/q/developer/)[Amazon Q Developer](https://aws.amazon.com/q/developer/) và[ ](https://aws.amazon.com/glue/)[AWS Glue](https://aws.amazon.com/glue/). Những gì chúng tôi khám phá đã thay đổi hoàn toàn cách chúng tôi nghĩ về kiến trúc agent: các khung điều phối mà chúng tôi đã xây dựng để hướng dẫn các mô hình trước đó giờ đây đang cản trở những gì các LLM hiện đại có thể làm một cách tự nhiên.

Tuy nhiên, việc sử dụng mô hình làm bộ điều phối không có nghĩa là hy sinh quyền kiểm soát của nhà phát triển. Strands cung cấp một giao diện gọn gàng, đơn giản giúp bạn bắt đầu trong vài phút, đồng thời cung cấp khả năng cấu hình mạnh mẽ khi bạn cần. Các công cụ đánh giá tích hợp giúp bạn hiểu và xác thực hành vi của tác nhân, đảm bảo bạn duy trì sự tự tin ngay cả khi các mô hình đưa ra quyết định tự chủ. Sự cân bằng giữa tính đơn giản và tính linh hoạt này là điều làm cho phương pháp tiếp cận theo mô hình trở nên thực tế cho cả việc tạo mẫu nhanh và các hệ thống sản xuất. Strands phát triển cùng với bạn.

Trong bài đăng này, chúng ta sẽ khám phá cách phương pháp tiếp cận theo mô hình xuất phát từ kinh nghiệm sản xuất thực tế và chỉ cho bạn các mẫu thực tế để xây dựng các agent có thể tự suy nghĩ.

## **Khi việc điều phối trở thành một hạn chế**

Các khung tác nhân truyền thống xuất hiện khi các mô hình ngôn ngữ cần được hướng dẫn nhiều. Các nhà phát triển đã xây dựng các máy trạng thái phức tạp, quy trình làm việc được xác định trước và logic điều phối phức tạp vì các mô hình không thể suy luận một cách đáng tin cậy về các bước tiếp theo của chúng. Chúng tôi sẽ viết hàng trăm dòng mã chỉ để xử lý luồng giữa "thu thập thông tin", "phân tích dữ liệu" và "cung cấp phản hồi" – và cuối cùng vẫn có những tác nhân bị hỏng khi người dùng đặt câu hỏi theo những cách bất ngờ.

Các nhóm AWS mà tôi đã làm việc cùng để xây dựng Amazon Q Developer đã trực tiếp trải nghiệm điều này. Ban đầu, chúng tôi đã sử dụng các khung điều phối truyền thống, nhưng những thay đổi trong yêu cầu sản phẩm và hành vi của người dùng đòi hỏi nỗ lực khoa học và kỹ thuật đáng kể để hiệu chỉnh hệ thống nhằm xử lý các trường hợp sử dụng mới. Các bộ định tuyến và bộ phân loại học máy (ML) sẽ trả về các đầu ra cứng nhắc cho các biện pháp bảo vệ – văn bản tĩnh như “Tôi xin lỗi, tôi không thể trả lời câu hỏi đó” – mà không cung cấp các giải pháp thay thế hoặc giải thích theo cách tương tác hữu ích và có vẻ thông minh.

**Các mô hình hiện đại đủ tinh vi để tự điều phối.** Đây là cái nhìn sâu sắc quan trọng đã thay đổi mọi thứ đối với chúng tôi. Mặc dù các quy trình làm việc có cấu trúc vẫn có vị trí của chúng – đặc biệt là đối với các yêu cầu tuân thủ hoặc các quy trình kinh doanh được xác định rõ ràng – phương pháp tiếp cận theo mô hình loại bỏ nhu cầu điều phối cứng nhắc trong hầu hết các tình huống.

Khi các nhóm Q Developer chuyển sang phương pháp tiếp cận theo mô hình, hệ thống có thể xử lý linh hoạt các yêu cầu sản phẩm đang thay đổi và phản hồi một cách mạch lạc bất kể điều gì xảy ra. Thay vì các phản hồi bảo vệ cứng nhắc, tác nhân có thể đưa ra các giải pháp thay thế và sử dụng đầu ra của biện pháp bảo vệ làm ngữ cảnh để mô hình hiểu tại sao nó không thể trả lời một số đầu vào nhất định. Điều này cho phép một cá tính và giọng điệu duy nhất trên các hệ thống đa tác nhân, cho phép các kỹ sư trên khắp Amazon đóng góp kiến thức chuyên môn của họ trong khi vẫn duy trì sự mạch lạc. Nó cũng cung cấp ngữ cảnh phù hợp cho mô hình vào đúng thời điểm với các công cụ mạnh mẽ để có các phản hồi hữu ích, thông minh.

Khi bạn cung cấp cho một mô hình các công cụ, nó không chỉ thực thi chúng một cách máy móc. Nó suy luận về cách tiếp cận tốt nhất, xem xét nhiều chiến lược và điều chỉnh hành vi của mình dựa trên những gì nó khám phá. Một mô hình phân tích vấn đề về hiệu suất có thể bắt đầu với các chỉ số hệ thống, nhận ra nút thắt thực sự nằm trong cơ sở dữ liệu, chuyển sang phân tích truy vấn, và sau đó đề xuất cả các bản sửa lỗi ngay lập tức và các cải tiến kiến trúc dài hạn – tất cả mà không cần được lập trình rõ ràng cho trình tự đó.

Những lợi ích về hoạt động mang tính chuyển đổi. Những gì trước đây mất hàng tháng để phát triển giờ chỉ mất vài tuần. Các nhóm của chúng tôi có thể nhanh chóng tận dụng các tính năng mới nhất của mô hình ngôn ngữ lớn (LLM) như gọi công cụ, suy nghĩ mở rộng và xen kẽ, hệ thống đa tác nhân, siêu tác nhân,[ ](https://modelcontextprotocol.io/docs/getting-started/intro)[MCP](https://modelcontextprotocol.io/docs/getting-started/intro), và[ ](https://a2a-protocol.org/latest/)[A2A](https://a2a-protocol.org/latest/) – tất cả trong khi vẫn giữ một giao diện đơn giản cho các nhà phát triển có thể được tùy chỉnh hoàn toàn cho việc triển khai các agent AI trong sản xuất.

Triết lý này mở rộng ra ngoài các tác nhân đơn lẻ. Cho dù bạn đang xây dựng một tác nhân phân tích dữ liệu đơn giản hay một hệ thống đa tác nhân phức tạp, mô hình sẽ quyết định khi nào cần cộng tác với các tác nhân khác, khi nào cần ủy thác nhiệm vụ, khi nào cần tìm hiểu sâu hơn về một vấn đề và khi nào cần cung cấp câu trả lời cuối cùng.

## **The agent loop**: Nơi trí tuệ gặp hành động

Trọng tâm của triết lý này là [agent loop](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/agent-loop/) – một chu trình tự nhiên của việc suy luận và hành động phản ánh cách các hệ thống thông minh suy nghĩ và làm việc. Cách tiếp cận này được xây dựng dựa trên mô hình ReAct ([ReAct: Kết hợp lý luận và hành động trong các mô hình ngôn ngữ](https://react-lm.github.io/)), mô hình này chứng minh cách các mô hình ngôn ngữ có thể tạo ra cả các dấu vết suy luận và các hành động cụ thể cho nhiệm vụ một cách xen kẽ, tạo ra sự hợp lực lớn hơn giữa việc suy nghĩ và hành động.

Mô hình tham gia vào quá trình suy luận liên tục, đặt ra các câu hỏi như:

- _"Tôi đang cố gắng đạt được điều gì ở đây?"_

- _"Tôi cần thông tin gì?"_

- _"Công cụ nào sẽ hiệu quả nhất?"_

- _"Những kết quả này thay đổi sự hiểu biết của tôi như thế nào?"_

- _"Tôi nên tiếp tục khám phá hay cung cấp một câu trả lời?"_

Quá trình suy luận nội bộ này là điều làm cho các tác nhân dựa trên mô hình trở nên mạnh mẽ. Chúng không chỉ thực hiện các bước được xác định trước – chúng suy nghĩ, thích ứng và phát triển cách tiếp cận của mình trong thời gian thực.

## **Hướng dẫn trí thông minh thông qua ngữ cảnh**

Mặc dù mô hình tự điều khiển hành vi của mình, hành vi đó được định hình bởi ngữ cảnh mà nó nhận được. Trong phương pháp tiếp cận theo mô hình, bạn hướng dẫn trí thông minh của tác nhân không phải thông qua các cấu trúc điều khiển cứng nhắc, mà thông qua ngữ cảnh được xây dựng cẩn thận bao gồm các lời nhắc hệ thống, thông số kỹ thuật của công cụ và lịch sử cuộc trò chuyện.

Hãy nghĩ về nó như việc thuê một nhà tư vấn lành nghề. Bạn không can thiệp vàvào từng bước của họ – thay vào đó, bạn đưa cho họ các mục tiêu rõ ràng, giải thích những nguồn lực nào có sẵn và cung cấp thông tin nền tảng liên quan. Phương pháp tiếp cận theo mô hình hoạt động theo cách tương tự.

[Các lời nhắc hệ thống](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/prompts/) thiết lập vai trò và mục tiêu của tác nhân – chúng thiết lập danh tính nền tảng và các mục tiêu cấp cao hướng dẫn mọi quá trình ra quyết định. Thay vì ra lệnh cho các bước cụ thể, các lời nhắc hệ thống hiệu quả mô tả thành công trông như thế nào và cung cấp các nguyên tắc để ra quyết định. Thay vì “Đầu tiên kiểm tra cơ sở dữ liệu, sau đó xác thực đầu vào, sau đó xử lý yêu cầu”, bạn có thể viết “Bạn giúp người dùng phân tích dữ liệu của họ một cách hiệu quả và chính xác, luôn xác thực đầu vào trước khi xử lý”.

[Các thông số kỹ thuật của công cụ](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/tools/tools_overview/) xác định các ranh giới khả năng và hướng dẫn sử dụng – chúng không chỉ truyền đạt những công cụ nào có sẵn, mà còn cách thức và thời điểm chúng nên được sử dụng. Các mô tả công cụ được thiết kế tốt sẽ trở thành một phần của quá trình suy luận của mô hình. Một mô tả công cụ như “Sử dụng công cụ này cho các phép tính toán học phức tạp đòi hỏi độ chính xác cao” giúp mô hình lựa chọn phù hợp giữa một công cụ máy tính và việc viết mã Python.

[Lịch sử cuộc trò chuyện](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/conversation-management/) duy trì tính liên tục của nhiệm vụ và ngữ cảnh đang phát triển – nó cung cấp các chi tiết cụ thể cho phép các tác nhân duy trì sự mạch lạc qua các tương tác. Khi các cuộc trò chuyện trở nên dài hơn, việc quản lý ngữ cảnh này trở nên quan trọng để duy trì hiệu suất trong khi vẫn giữ lại thông tin liên quan. Quản lý ngữ cảnh rất quan trọng đối với các tác nhân dựa trên mô hình – đó là sự khác biệt giữa một tác nhân duy trì các cuộc trò chuyện mạch lạc, thông minh và một tác nhân mất dấu các chi tiết quan trọng hoặc vượt quá giới hạn mã thông báo. Strands cung cấp một giao diện đơn giản cho phép các nhà phát triển xác định các lời nhắc hệ thống, công cụ và hành vi quản lý ngữ cảnh của tác nhân mà không bị lạc trong sự phức tạp của việc triển khai.

Các phương pháp tiếp cận cửa sổ trượt giữ lại các tin nhắn gần đây và loại bỏ những tin nhắn cũ hơn: đơn giản và hiệu quả. Các kỹ thuật tóm tắt giữ lại thông tin quan trọng từ các cuộc trò chuyện dài hơn trong giới hạn mã thông báo – tốt hơn cho các cuộc thảo luận phức tạp, đang phát triển. Mục tiêu là cung cấp cho mô hình ngữ cảnh phù hợp nhất để đưa ra quyết định tốt về trường hợp sử dụng cụ thể của bạn.

Điều này thể hiện một sự thay đổi lớn từ lập trình thủ tục sang lập trình theo ngữ cảnh. Thay vì viết logic "nếu thế này, thì thế kia", bạn đang tạo ra ngữ cảnh giúp mô hình tự tìm ra cách tiếp cận tốt nhất.

from strands import Agent

from strands_tools import calculator, file_write, python_repl

Simple: Get started in seconds
agent = Agent(

    tools=[calculator, file_write, python_repl],

    system_prompt="You are a helpful assistant that can perform calculations and verify them with code."

)

The model autonomously decides: calculate first, then verify with code
agent("Calculate the compound interest on $10,000 at 5% annually for 10 years")

Triết lý thiết kế này được áp dụng xuyên suốt Strands. Bạn có thể xây dựng các tác nhân phức tạp mà không bị lạc trong việc cấu hình, nhưng mọi khía cạnh vẫn có thể tùy chỉnh khi trường hợp sử dụng của bạn yêu cầu.

## **Mở rộng quy mô các tác nhân theo mô hình với Strands**

Phương pháp tiếp cận theo mô hình có thể mở rộng một cách tự nhiên trong khi vẫn duy trì trải nghiệm nhà phát triển gọn gàng. Một tác nhân duy nhất được trang bị các công cụ phù hợp có thể xử lý các tác vụ phức tạp mà theo truyền thống sẽ yêu cầu nhiều thành phần chuyên biệt. Khi bạn cần nhiều tác nhân, các mô hình sẽ tự phối hợp với nhau thông qua một số mẫu đã được chứng minh. Strands cung cấp bốn phương pháp tiếp cận chính để phối hợp đa tác nhân, mỗi phương pháp phù hợp với các trường hợp sử dụng khác nhau:

- **Tác nhân dưới dạng công cụ:** Các hệ thống phân cấp trong đó các chuyên gia đóng vai trò là các công cụ thông minh

- **Bầy đàn:** Hợp tác tự chủ với các nhóm tác nhân tự tổ chức

- **Đồ thị:** Các quy trình công việc có cấu trúc với các đường thực thi xác định

- **Siêu tác nhân:** Các tác nhân động có thể sửa đổi hành vi điều phối của chính chúng

Cho dù bạn đang xây dựng các hệ thống phân cấp đơn giản hay các hệ thống thích ứng phức tạp, Strands vẫn giữ giao diện gọn gàng trong khi cung cấp khả năng cấu hình cần thiết cho các hệ thống sản xuất.

## **Tác nhân dưới dạng công cụ: Trí tuệ phân cấp**

Khi một tác nhân duy nhất cần chuyên môn chuyên biệt,[ ](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/agents-as-tools/)[tác nhân dưới dạng công cụ](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/agents-as-tools/) sẽ biến các tác nhân khác thành các công cụ thông minh. Điều này tạo ra các hệ thống phân cấp tự nhiên, nơi một tác nhân điều phối ủy thác cho các chuyên gia, duy trì sự phân chia trách nhiệm rõ ràng trong khi tận dụng phương pháp tiếp cận theo mô hình ở mọi cấp độ. Làm thế nào tác nhân điều phối quyết định nên tham khảo ý kiến của chuyên gia nào? Mô hình suy luận yêu cầu giống như cách nó suy luận về việc lựa chọn công cụ. Khi người dùng hỏi “Lên kế hoạch cho một chuyến công tác đến Tokyo và nghiên cứu cơ hội thị trường ở đó,” tác nhân điều phối nhận ra rằng điều này đòi hỏi cả chuyên môn về lập kế hoạch du lịch và nghiên cứu thị trường. Nó có thể tham khảo ý kiến của cố vấn du lịch trước để hiểu về hậu cần, sau đó sử dụng những ràng buộc đó để hướng dẫn công việc của nhà phân tích nghiên cứu.

from strands import Agent, tool

@tool

def research_analyst(request: str) -> str:

    """Research specialist for market analysis"""

    research_agent = Agent(

        system_prompt="You are a research specialist who gathers and analyzes market information.",

        tools=[web_search, calculator]

    )

    return str(research_agent(request))

@tool

def travel_advisor(request: str) -> str:

    """Travel planning specialist for logistics and recommendations"""

    travel_agent = Agent(

        system_prompt="You are a travel planning specialist who helps with logistics, bookings, and recommendations.",

        tools=[flight_search, hotel_search, weather_api]

    )

    return str(travel_agent(request))

Orchestrator decides when to consult specialists and how to synthesize their input
executive_assistant = Agent(

    system_prompt="You coordinate with specialists to provide comprehensive assistance.",

    tools=[research_analyst, travel_advisor]

)

Mô hình điều phối quyết định chuyên gia nào cần tham khảo và cách tổng hợp thông tin đầu vào của họ – không cần quy trình làm việc được xác định trước. Mô hình này hoạt động tốt khi bạn cần ranh giới chuyên môn rõ ràng và muốn các mô hình ủy quyền với một tác nhân chính dẫn đầu.

## **Swarms: Hợp tác tự động**

[Swarms](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/swarm/) cho phép các tác nhân hợp tác tự trị theo cách tự tổ chức, quyết định khi nào chuyển giao nhiệm vụ cho nhau. Điều này hoạt động tốt cho việc hợp tác sáng tạo và giải quyết vấn đề theo cách phát sinh, nơi nhiều quan điểm khác nhau tạo thêm giá trị.

Hãy xem xét một dự án nghiên cứu thị trường nơi bạn cần phân tích một cơ hội sản phẩm mới. Một phương pháp truyền thống có thể tuân theo một trình tự cứng nhắc: nghiên cứu → phân tích → viết. Nhưng nghiên cứu thực tế lộn xộn hơn – bạn có thể phát hiện ra trong quá trình phân tích rằng bạn cần dữ liệu bổ sung, hoặc nhận ra trong khi viết rằng một khung phân tích khác sẽ hấp dẫn hơn.

from strands import Agent

from strands.multiagent import Swarm

researcher = Agent(name="researcher", system_prompt="You research topics thoroughly...")

analyst = Agent(name="analyst", system_prompt="You analyze data and create insights...")

writer = Agent(name="writer", system_prompt="You write comprehensive reports...")

Agents coordinate autonomously through model-driven handoffs
market_research_team = Swarm([researcher, analyst, writer])

Trong một bầy đàn, nhà nghiên cứu có thể bắt đầu thu thập thông tin, sau đó chuyển giao cho nhà phân tích khi họ đã tìm thấy những mẫu thú vị. Nhà phân tích có thể phát hiện ra những lỗ hổng và chuyển lại cho nhà nghiên cứu để có thêm dữ liệu cụ thể. Người viết có thể tham gia vào cuộc trò chuyện từ sớm để giúp định hình hướng nghiên cứu dựa trên những gì sẽ tạo nên một câu chuyện hấp dẫn.

Sự khác biệt chính so với các tác nhân dưới dạng công cụ là ngữ cảnh được chia sẻ. Trong các hệ thống phân cấp, người điều phối quyết định thông tin nào sẽ được chuyển giữa các chuyên gia. Trong các bầy đàn, tất cả các tác nhân đều có quyền truy cập vào cùng một lịch sử cuộc trò chuyện, cho phép hợp tác linh hoạt hơn và các hướng dẫn cấp cao. Bạn có thể nói với một bầy đàn “hãy nghiên cứu cơ hội thị trường này” mà không cần chỉ định chính xác công việc nên được phân chia như thế nào – các tác nhân sẽ tự tìm ra dựa trên sự hiểu biết chung của chúng về nhiệm vụ đang phát triển.

Bầy đàn đánh đổi việc thực thi có thể dự đoán được để lấy các khả năng mới nổi, khiến chúng trở nên lý tưởng cho các nhiệm vụ nghiên cứu phức tạp, các tình huống động não và các dự án sáng tạo mà cách tiếp cận tốt nhất không rõ ràng ngay từ đầu.

## **Đồ thị: Quy trình làm việc có cấu trúc**

[Đồ thị](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/graph/) cung cấp các quy trình làm việc xác định trong đó việc thực thi tuân theo các đường dẫn được xác định trước. Trong khi các tác nhân riêng lẻ trong đồ thị sử dụng thực thi theo mô hình, cấu trúc đồ thị đảm bảo các trình tự và sự phụ thuộc cụ thể được duy trì.

Mô hình này vượt trội cho các quy trình kinh doanh yêu cầu các điểm kiểm tra bắt buộc hoặc các yêu cầu tuân thủ. Ví dụ, một quy trình phân tích tài chính có thể yêu cầu nghiên cứu → đánh giá rủi ro → xem xét quy định → đề xuất cuối cùng, với mỗi bước xây dựng trên bước trước đó và một số bước yêu cầu phê duyệt cụ thể.

from strands import Agent

from strands.multiagent import GraphBuilder

builder = GraphBuilder()

builder.add_node(researcher, "research")

builder.add_node(analyst, "analysis")

builder.add_node(writer, "report")

builder.add_edge("research", "analysis")

builder.add_edge("analysis", "report")

graph = builder.build()

Các nhóm AWS đã sử dụng đồ thị để điều phối đường ống dữ liệu, nơi một số phép biến đổi nhất định phải diễn ra theo trình tự, và cho các quy trình tuân thủ, nơi các dấu vết kiểm toán yêu cầu tài liệu từng bước cụ thể. Phương pháp tiếp cận theo mô hình vẫn được áp dụng trong mỗi nút – tác nhân nghiên cứu có thể điều chỉnh phương pháp của mình dựa trên những gì nó khám phá – nhưng luồng tổng thể vẫn có thể dự đoán được.

Hạn chế của đồ thị là sự cứng nhắc của chúng. Nếu nhà phân tích phát hiện ra họ cần nghiên cứu bổ sung, họ không thể yêu cầu trực tiếp – quy trình làm việc sẽ cần phải hoàn thành và có khả năng khởi động lại. Điều này làm cho đồ thị trở nên lý tưởng cho các quy trình đã được hiểu rõ nhưng ít phù hợp hơn cho công việc khám phá hoặc sáng tạo.

## **Siêu tác nhân: Điều phối linh hoạt**

Siêu tác nhân là các tác nhân đơn lẻ được trang bị các công cụ cho phép chúng suy nghĩ về việc suy nghĩ – chúng có thể tự động tạo ra các tác nhân khác, điều phối các quy trình công việc và tham gia vào việc giải quyết vấn đề đệ quy. Chúng đại diện cho biểu hiện cuối cùng của phương pháp tiếp cận theo mô hình: các tác nhân có thể tự kiến trúc các kỹ thuật điều phối của riêng mình.

Hãy nghĩ về một siêu tác nhân như một kiến trúc sư cấp cao không chỉ có thể giải quyết vấn đề mà còn có thể quyết định cách cấu trúc phương pháp giải quyết vấn đề. Khi đối mặt với một thách thức phức tạp, nó có thể suy luận: “Điều này đòi hỏi cả nghiên cứu sâu và tổng hợp sáng tạo. Tôi nên tạo ra một bầy đàn các chuyên gia và sau đó sử dụng một biểu đồ để đảm bảo sản phẩm cuối cùng đáp ứng các tiêu chuẩn chất lượng.”

from strands import Agent

from strands_tools import graph, swarm, use_agent, think, workflow

meta_agent = Agent(

    system_prompt="You can dynamically create specialized agents and orchestrate complex workflows.",

    tools=[graph, swarm, use_agent, think, workflow]

)

Siêu tác nhân vượt trội trong các hệ thống động phát triển theo thời gian. Lợi ích chính là mức độ năng động bổ sung của chúng – chúng có thể tạo ra các tác nhân không được xác định trước, phát triển các công cụ mới cho các nhu cầu mới nổi, điều chỉnh các chiến lược điều phối của chúng dựa trên các điều kiện thay đổi và phát triển phương pháp giải quyết vấn đề của chúng khi chúng tìm hiểu thêm về lĩnh vực đó.

Không giống như các mẫu khác mà bạn xác định trước các tác nhân và công cụ, các siêu tác nhân có thể tạo ra các chuyên gia mới và tạo các công cụ tùy chỉnh theo yêu cầu. Phân tích một xu hướng công nghệ mới? Siêu tác nhân có thể tạo ra các chuyên gia về lĩnh vực cho các tác động pháp lý, động lực thị trường và tính khả thi kỹ thuật – các tác nhân không tồn tại cho đến khi nhu cầu cụ thể phát sinh. Nó cũng có thể phát triển các công cụ chuyên dụng để thu thập dữ liệu, các khung phân tích hoặc các định dạng báo cáo phù hợp với lĩnh vực cụ thể đó.

Việc tạo tác nhân và công cụ động này cho phép các hệ thống phát triển và thích ứng thay vì tuân theo các mẫu cố định.

## **Xây dựng niềm tin thông qua đánh giá**

Phương pháp tiếp cận theo mô hình đòi hỏi[ ](https://strandsagents.com/latest/documentation/docs/user-guide/observability-evaluation/evaluation/)[đánh giá](https://strandsagents.com/latest/documentation/docs/user-guide/observability-evaluation/evaluation/) mạnh mẽ để xây dựng niềm tin rằng các tác nhân đang hoạt động như mong đợi, đặc biệt là khi chúng đang đưa ra các quyết định tự chủ về việc sử dụng công cụ và điều phối tác vụ.

Vì các tác nhân theo mô hình đưa ra các quyết định động thay vì tuân theo các đường dẫn được xác định trước, việc đánh giá trở nên quan trọng hơn và cũng tinh tế hơn. Bạn cần đánh giá không chỉ liệu tác nhân có đưa ra câu trả lời đúng hay không, mà còn liệu nó có đưa ra các quyết định tốt về cách tiếp cận vấn đề hay không.

Phương pháp tiếp cận theo mô hình đã thay đổi cách chúng ta nghĩ về bản thân việc đánh giá. Việc kiểm thử truyền thống với các bộ dữ liệu tĩnh trở nên không đủ khi các tác nhân điều chỉnh hành vi của chúng một cách linh hoạt. Sự thay đổi này đòi hỏi các mô hình đánh giá mới phù hợp với trí thông minh của các hệ thống đang được thử nghiệm.

**Các giám khảo LLM** cung cấp một phương pháp mạnh mẽ để đánh giá các phản hồi của tác nhân trên quy mô lớn, nhưng chúng phải được hiệu chỉnh cẩn thận để phù hợp với mong đợi của người dùng cuối. Một giám khảo LLM ưu tiên độ chính xác kỹ thuật có thể bỏ qua các sắc thái quan trọng đối với người dùng thực tế, chẳng hạn như giọng điệu, tính hữu ích hoặc khả năng áp dụng thực tế.

**Người dùng mô phỏng được điều khiển bởi LLM** cho phép thử nghiệm động với các bộ dữ liệu đang phát triển, tạo ra các mẫu tương tác thực tế mà các trường hợp thử nghiệm tĩnh không thể nắm bắt được. Tuy nhiên, những người dùng mô phỏng này cũng phải được hiệu chỉnh để hành xử giống như người dùng cuối thực tế thay vì các kịch bản thử nghiệm lý tưởng hóa. Mục tiêu là hành vi người dùng đích thực, không phải hành vi người dùng hoàn hảo.

Các khía cạnh đánh giá chính cho các tác nhân theo mô hình bao gồm:

- **Sự phù hợp của việc lựa chọn công cụ** – Tác nhân có chọn đúng công cụ cho nhiệm vụ không?

- **Chất lượng suy luận** – Cách tiếp cận của tác nhân có hợp lý không?

- **Khả năng thích ứng** – Tác nhân xử lý các tình huống bất ngờ tốt đến mức nào?

- **Hiệu quả** – Tác nhân có hoàn thành nhiệm vụ mà không có các bước không cần thiết không?

Bản chất không xác định của các tác nhân dựa trên mô hình có nghĩa là bạn cần các đường cơ sở có ý nghĩa thống kê và đánh giá liên tục để theo dõi hiệu suất theo thời gian. Sự đầu tư vào việc đánh giá này cho phép bạn tự tin triển khai các tác nhân đưa ra quyết định tự chủ.

## **Sự thay đổi mô hình: Từ kiểm soát cứng nhắc đến thích ứng động**

Phương pháp tiếp cận theo mô hình đại diện cho một sự thay đổi cơ bản trong cách chúng ta nghĩ về các tác nhân AI. Thay vì cố gắng kiểm soát mọi khía cạnh của hành vi tác nhân thông qua việc điều phối phức tạp, chúng tôi cung cấp các công cụ, bối cảnh và mục tiêu phù hợp, sau đó để mô hình tự xác định cách tiếp cận tốt nhất một cách linh hoạt.

Sự thay đổi này giải quyết một vấn đề cốt lõi: logic được xác định trước gặp khó khăn trong việc xử lý một thế giới không thể đoán trước. Các khung truyền thống bị phá vỡ khi người dùng đặt câu hỏi theo những cách không ngờ tới, khi API trả về các phản hồi không mong muốn hoặc khi các yêu cầu kinh doanh thay đổi. Chúng thất bại vì chúng chỉ có thể xử lý các tình huống mà các nhà phát triển đã lường trước và lập trình.

Các tác nhân theo mô hình có thể thích ứng. Khi một lệnh gọi API không thành công, chúng sẽ suy luận về các giải pháp thay thế. Khi người dùng hỏi điều gì đó bất ngờ, chúng sẽ tìm cách giúp đỡ bằng cách sử dụng các công cụ có sẵn. Khi các yêu cầu thay đổi, chúng sẽ điều chỉnh cách tiếp cận của mình mà không cần thay đổi mã. Khả năng thích ứng này đến từ việc tận dụng khả năng suy luận của mô hình thay vì chống lại chúng.

Cách tiếp cận được áp dụng trong Strands cho phép các tác nhân xử lý các yêu cầu và dữ liệu thay đổi trong khi giảm bớt sự phức tạp mà các nhà phát triển cần quản lý. Bạn có thể có cả hai: sự đơn giản để bắt đầu nhanh chóng và sức mạnh để cấu hình mọi thứ khi sản xuất yêu cầu.

Phương pháp tiếp cận theo mô hình không phải là về việc xây dựng các khung điều phối tốt hơn. Đó là về việc nhận ra rằng các LLM hiện đại đã phát triển vượt xa sự cần thiết của sự hướng dẫn cứng nhắc như vậy. Bằng cách tận dụng khả năng suy luận của mô hình để điều phối, chúng ta có thể xây dựng các tác nhân vừa có khả năng hơn vừa dễ phát triển hơn. Triết lý này là nền tảng mà mọi thứ khác trong Strands được xây dựng dựa trên đó. Hãy truy cập trang web[ ](https://strandsagents.com/latest/)[Strands Agents](https://strandsagents.com/latest/) để dùng thử ngay hôm nay.

_Tìm kiếm thêm nội dung mã nguồn mở? Hãy chắc chắn theo dõi [AWS Open Source](https://www.linkedin.com/company/awsopen/posts/?feedView=all) trên LinkedIn!_

![Enter image alt description](/images/Blog/blog3/E015GUGD2V6-W0187GVFRG8-98d371d2068f-512.jpg)

### **Arron Bailiss**

Arron Bailiss là một Kỹ sư chính tập trung vào agent AI tại AWS, làm việc đa lĩnh vực của trí tuệ nhân tạo, học máy và robot. Anh ấy giúp định hình tương lai của các công cụ dành cho nhà phát triển cho phép các nhà xây dựng tạo ra các ứng dụng phức tạp dựa trên AI.
