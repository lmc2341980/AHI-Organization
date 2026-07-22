Điều tôi muốn lưu ý

Tôi không khuyến nghị dùng Bolt.new làm công cụ chính để sinh toàn bộ hệ thống.

Bolt.new rất mạnh để tạo giao diện và prototype, nhưng AHI-O sẽ là một hệ thống lớn, cần khả năng refactor nhiều lần và kiểm soát kiến trúc.

Tôi đề xuất vai trò như sau:

OpenCode + Gemini: đọc và hiểu repository, ERPNext và các dự án nguồn mở; hỗ trợ phân tích và refactor.
Bolt.new: tạo nhanh giao diện và khung ứng dụng.
Replit: chạy thử và phát triển backend/API.
GitHub: nơi duy nhất lưu trữ mã nguồn, tài liệu và đặc tả.
AHI-Factory (sau này): thay thế dần Bolt.new để tự sinh giao diện, API, tài liệu và mã nguồn từ các Specification của AHI.

Như vậy, ngay từ MVP, kiến trúc đã hướng tới việc AHI-Factory sẽ dần thay thế các công cụ AI bên ngoài, thay vì phụ thuộc lâu dài vào chúng.
