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

Lưu ý rất quan trọng

AHI-O nên là Modular Monolith ở MVP, không phải Microservices.

Lý do:

Nhanh phát triển.
Dễ debug.
Dễ dùng Bolt.new, Replit, OpenCode.
Một repository, một deployment.
Sau này khi ổn định mới tách thành các service độc lập (AI, Knowledge, Memory, ERP Adapter, Workflow...).

Điều này phù hợp với mục tiêu ra sản phẩm nhanh, giảm chi phí và tránh gánh nặng vận hành sớm. Khi AHI-O trưởng thành, AHI-Factory có thể hỗ trợ tách module thành microservices mà không làm thay đổi kiến trúc nghiệp vụ. Điều này sẽ giúp bạn vừa có MVP sớm, vừa không khóa tương lai của hệ thống.
