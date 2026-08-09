---
title: "Event 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# AWS First Cloud AI Journey — Agent Forge Deep Dive

### Mục đích của sự kiện

- Cập nhật kiến thức chuyên sâu về **Amazon Bedrock AgentCore** — nền tảng của AWS dành riêng cho việc xây dựng và vận hành AI Agent ở quy mô production.
- Mang tới góc nhìn thực tế từ chuyên gia AWS về xu hướng ngành IT và định hướng phát triển sự nghiệp cho sinh viên/kỹ sư trẻ.
- Tạo cơ hội thực hành trực tiếp (hands-on), giúp học viên tự tay xây dựng một AI Agent đơn giản ngay trong buổi học.

### Nội dung nổi bật

#### Chia sẻ mở đầu — Góc nhìn ngành IT (anh Hiếu)

- Chia sẻ góc nhìn tổng quan về thị trường công nghệ hiện tại, đặc biệt là làn sóng chuyển dịch sang GenAI và Agentic AI đang tác động tới cách các doanh nghiệp xây dựng phần mềm.
- Đưa ra lời khuyên thực tế cho sinh viên/kỹ sư trẻ ngành IT: tập trung xây dựng nền tảng vững (hiểu bản chất hệ thống, không chỉ chạy theo công cụ mới), đồng thời chủ động thích nghi với tốc độ thay đổi nhanh của công nghệ AI.
- Nhấn mạnh rằng công cụ AI hỗ trợ lập trình sẽ ngày càng phổ biến, nhưng tư duy giải quyết vấn đề và hiểu đúng bài toán nghiệp vụ mới là yếu tố quyết định sự khác biệt của một kỹ sư giỏi.

#### Amazon Bedrock AgentCore (anh Nghĩa Trần)

Phần trình bày trọng tâm của buổi Deep Dive, giới thiệu các thành phần cốt lõi giúp đưa AI Agent từ bản demo lên hệ thống production thật sự đáng tin cậy.

**3 nhóm tính năng chính:**

- **Memory** — cơ chế giúp Agent lưu giữ và truy xuất lại ngữ cảnh qua nhiều lượt tương tác, thay vì mỗi lần hỏi đáp đều là một phiên độc lập không có "trí nhớ". Đây là nền tảng để Agent duy trì được ngữ cảnh hội thoại dài và cá nhân hoá trải nghiệm theo từng người dùng.
- **Evaluations** — bộ công cụ đánh giá chất lượng phản hồi của Agent một cách có hệ thống, giúp đội ngũ phát triển đo lường được độ chính xác, mức độ hữu ích và phát hiện các trường hợp Agent trả lời sai lệch trước khi đưa vào production.
- **Observability** — khả năng quan sát và truy vết toàn bộ quá trình suy luận/hành động của Agent (từng bước gọi tool, từng quyết định trung gian), giúp đội vận hành dễ dàng debug khi Agent hoạt động không như mong đợi, tương tự cách CloudWatch/X-Ray theo dõi hệ thống truyền thống nhưng áp dụng riêng cho đặc thù của Agent.

**Các tính năng bổ trợ khác:** Harness (khung chạy thử/đóng gói Agent), Policy (thiết lập ràng buộc hành vi cho Agent), Identity (quản lý danh tính và quyền hạn khi Agent thay mặt người dùng thao tác với hệ thống khác)... — đóng vai trò hỗ trợ, giúp AgentCore trở thành một nền tảng đầy đủ vòng đời cho việc xây dựng Agent, từ phát triển tới vận hành an toàn.

#### Hands-on Lab — Xây dựng Agent với Bedrock AgentCore (anh Hải Anh)

- Thực hành trực tiếp xây dựng một AI Agent đơn giản trên nền Amazon Bedrock AgentCore, áp dụng ngay các khái niệm Memory/Observability vừa được giới thiệu ở phần trước.
- Sử dụng **Kiro** (công cụ lập trình hỗ trợ AI của AWS) để "vibe code" — viết code chủ yếu bằng cách mô tả yêu cầu bằng ngôn ngữ tự nhiên, để AI sinh code khung sườn, sau đó tinh chỉnh lại theo đúng nhu cầu thực tế.
- Trải nghiệm trực tiếp quy trình từ ý tưởng → prompt → code chạy được, giúp hình dung rõ ràng hơn cách AgentCore và các công cụ AI-assisted coding rút ngắn thời gian phát triển Agent so với cách viết thủ công truyền thống.

### Những điều học được

- Amazon Bedrock AgentCore cung cấp bộ công cụ khá đầy đủ để đưa Agent từ ý tưởng thử nghiệm lên hệ thống production, thay vì phải tự xây dựng riêng lẻ từng phần (memory, logging, đánh giá chất lượng...).
- Observability và Evaluations là 2 yếu tố dễ bị bỏ qua khi mới làm quen với Agentic AI, nhưng lại quan trọng không kém phần logic chính của Agent — vì Agent hoạt động không xác định (non-deterministic) hơn phần mềm truyền thống rất nhiều.
- Công cụ AI-assisted coding như Kiro có thể rút ngắn đáng kể thời gian từ ý tưởng tới bản demo chạy được, nhưng vẫn cần người kỹ sư hiểu rõ hệ thống để chỉnh sửa/kiểm soát đúng hướng.

### Ứng dụng vào công việc

- Nghiên cứu cơ chế Memory của Amazon Bedrock AgentCore và cân nhắc khả năng áp dụng trong các phiên bản phát triển tiếp theo của chatbot RAG SmartDocAI, nhằm cải thiện khả năng duy trì ngữ cảnh hội thoại qua nhiều lượt tương tác.
- Tìm hiểu cơ chế Observability của Amazon Bedrock AgentCore và cân nhắc khả năng áp dụng trong tương lai để nâng cao khả năng theo dõi, truy vết từng bước xử lý trong các pipeline RAG phức tạp, trên nền tảng cơ chế giám sát CloudWatch Logs/Alarms hiện tại.
- Đánh giá Kiro như một công cụ hỗ trợ phát triển trong các giai đoạn tiếp theo của dự án, đặc biệt đối với việc viết kiểm thử, xây dựng các script nhỏ và tự động hóa những tác vụ lập trình lặp lại nhằm nâng cao hiệu quả phát triển.

### Cảm nhận sau sự kiện

Buổi Deep Dive lần này giúp em có cái nhìn rõ ràng hơn về khoảng cách giữa việc "làm demo AI Agent chạy được" và "xây dựng AI Agent đủ tin cậy để đưa vào production" — mà Amazon Bedrock AgentCore chính là câu trả lời của AWS cho khoảng cách đó. Phần chia sẻ của anh Hiếu ở đầu buổi cũng cho em thêm động lực và một góc nhìn thực tế hơn về con đường phát triển sự nghiệp trong ngành, giữa bối cảnh công nghệ AI thay đổi rất nhanh. Phần hands-on lab với Kiro là trải nghiệm thú vị nhất buổi, giúp em hình dung cụ thể cách AI-assisted coding có thể hỗ trợ công việc thực tế, không chỉ dừng ở lý thuyết.

#### Một số hình ảnh khi tham gia sự kiện

![Ảnh sự kiện Agent Forge Deep Dive](/images/4-EventParticipated/Event-08-08-2026.jpg)
