---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

- Triển khai và tối ưu kỹ thuật Re-ranking cho pipeline RAG: nghiên cứu Cross-Encoder và triển khai cơ chế xếp hạng lại sau bước Vector Search để cải thiện chất lượng ngữ cảnh đưa vào mô hình.
- Hoàn thiện chức năng đăng nhập bằng Google: triển khai hoàn chỉnh luồng OAuth 2.0 với Amazon Cognito và Google Identity Provider, bổ sung cơ chế liên kết tài khoản và xử lý trùng email giữa đăng nhập Google và email/password.
- Hoàn thiện backend trang thông tin cá nhân người dùng: hoàn tất API quản lý hồ sơ, avatar và thay đổi mật khẩu; tối ưu đồng bộ dữ liệu giữa Cognito, DynamoDB và S3.
- Kiểm thử và đánh giá hiệu quả các kỹ thuật RAG: so sánh Standard RAG, Self-RAG và Re-ranking trên bộ dữ liệu thực tế để đưa ra kết luận và hướng tối ưu.
- Họp nhóm rà soát tiến độ dự án và tham gia sự kiện "FCAJ x Agentic AI Build Week powered by GenAI Fund" (25/07/2026).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                      | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                    |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------------------------------------------------------------------------------- |
| 2   | - Triển khai và tối ưu Re-ranking cho pipeline RAG: <br>&emsp;+ Nghiên cứu mô hình Cross-Encoder để xếp hạng lại kết quả sau Vector Search; thiết kế API xếp hạng lại (inputs: query, retrieved_passages) và lựa chọn mô hình/weights thử nghiệm. <br>&emsp;+ Triển khai PoC re-ranking, đo thời gian xử lý và ảnh hưởng tới throughput; lưu ý tối ưu batch/FP16 nếu dùng GPU để giảm latency. | 20/07/2026   | 20/07/2026      | [Cross-Encoder paper / SentenceTransformers Cross-encoders](https://www.sbert.net/docs/usage/cross-encoders.html) |
| 3   | - Tích hợp Re-ranking vào hệ thống và cấu hình feature flag: <br>&emsp;+ Đóng gói re-ranker thành module có thể bật/tắt độc lập; thêm metadata vào response (ranking score, normalized_score). <br>&emsp;+ Tối ưu chất lượng ngữ cảnh đưa vào model AI (top-k selection sau re-ranking, context window trimming).                                                                              | 21/07/2026   | 21/07/2026      |                                                                                                                   |
| 4   | - Hoàn thiện chức năng đăng nhập bằng Google: <br>&emsp;+ Triển khai hoàn chỉnh luồng OAuth 2.0 với Amazon Cognito và Google Identity Provider; xử lý link callback, exchange code, và persist session. <br>&emsp;+ Bổ sung cơ chế liên kết tài khoản khi email trùng giữa đăng nhập Google và email/password (merge account flow).                                                            | 22/07/2026   | 22/07/2026      |                                                                                                                   |
| 5   | - Hoàn thiện backend trang thông tin cá nhân: <br>&emsp;+ Hoàn tất các API quản lý hồ sơ cá nhân, avatar và thay đổi mật khẩu; tối ưu cơ chế đồng bộ dữ liệu giữa Amazon Cognito, DynamoDB và Amazon S3.                                                                                                                                                                                       | 23/07/2026   | 23/07/2026      |                                                                                                                   |
| 6   | - Kiểm thử và đánh giá hiệu quả các kỹ thuật RAG: <br>&emsp;+ So sánh Standard RAG, Self-RAG và Re-ranking trên bộ dữ liệu thực tế; thu thập metrics: retrieval precision@k, answer exact match / F1, latency, and confidence calibration. <br>&emsp;+ Tổ chức buổi A/B test nội bộ và tổng hợp kết quả để báo cáo hướng tối ưu tiếp theo.                                                     | 24/07/2026   | 24/07/2026      |                                                                                                                   |
| 7   | - Họp nhóm rà soát tiến độ dự án và trao đổi, góp ý hoàn thiện báo cáo giữa các thành viên. <br> - Tham gia sự kiện "FCAJ x Agentic AI Build Week powered by GenAI Fund" (25/07/2026).                                                                                                                                                                                                         | 25/07/2026   | 25/07/2026      |                                                                                                                   |

### Kết quả đạt được tuần 5:

- Triển khai PoC Re-ranking (Cross-Encoder) và đo được ảnh hưởng bước đầu lên chất lượng truy xuất và latency; xác định các điểm cần tối ưu (batching, precision/FP16) để giảm độ trễ.
- Tích hợp Re-ranking vào pipeline như module có thể bật/tắt, trả về metadata xếp hạng (ranking score, normalized_score) để hỗ trợ chọn ngữ cảnh tốt hơn cho mô hình AI.
- Hoàn thiện luồng đăng nhập bằng Google: OAuth 2.0 với Cognito + Google hoạt động ổn định; bổ sung cơ chế liên kết tài khoản và xử lý trường hợp trùng email.
- Hoàn thiện backend trang thông tin cá nhân: API quản lý hồ sơ, avatar và thay đổi mật khẩu đã ổn định; tối ưu cơ chế đồng bộ giữa Cognito, DynamoDB và S3.
- Thực hiện kiểm thử so sánh Standard RAG, Self-RAG và Re-ranking trên bộ dữ liệu mẫu; thu thập các chỉ số retrieval precision@k, answer F1, latency, và confidence calibration để làm cơ sở cho tối ưu tiếp theo.
- Tổ chức họp nhóm rà soát tiến độ và tham gia sự kiện "FCAJ x Agentic AI Build Week powered by GenAI Fund" (25/07/2026).
