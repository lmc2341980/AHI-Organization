# CẨM NANG XÂY DỰNG MVP ỨNG DỤNG AI NHANH*Tài liệu tổng hợp hướng dẫn lựa chọn, so sánh và kết hợp các công cụ lập trình AI thế hệ mới (OpenBolt.dev, bolt.diy, OpenCode)*
---## 1. TỔNG QUAN TƯ VẤN LỰA CHỌN BAN ĐẦU### Bối cảnh dự án*   **Mục tiêu:** Xây dựng Sản phẩm Khả dụng Tối thiểu (MVP) trong thời gian ngắn nhất.*   **Hạn chế kỹ thuật:** Không thành thạo sử dụng dòng lệnh (Terminal), Git, Node.js hoặc Docker.
### Khuyến nghị cốt lõiBạn nên ưu tiên lựa chọn **OpenBolt.dev** để bắt đầu. Bản chất OpenBolt.dev là một dịch vụ lưu trữ đám mây (Cloud hosting) chạy trên nền tảng mã nguồn của bolt.diy nhưng đã được tối ưu giao diện web để người dùng không cần cài đặt.

**Lý do lựa chọn:***   **Bỏ qua cài đặt phức tạp:** Không cần cấu hình môi trường máy tính cá nhân. Chỉ cần mở trình duyệt, đăng nhập là có thể sử dụng ngay.*   **Tốc độ ra MVP tối đa:** Giao diện trực quan giúp tập trung hoàn toàn vào việc mô tả ý tưởng bằng ngôn ngữ tự nhiên để AI tự động tạo giao diện và logic.*   **Chia sẻ dễ dàng:** Hỗ trợ xem trước (Preview) ứng dụng theo thời gian thực và dễ dàng xuất bản để gửi cho người dùng thử nghiệm hoặc nhà đầu tư.
---## 2. BẢNG SO SÁNH: OPENBOLT.DEV vs BOLT.DIY vs OPENCODE
Để hiểu rõ hơn về hệ sinh thái bạn đang tiếp cận, dưới đây là bảng đối chiếu chi tiết tính năng và bản chất của từng công cụ:

| Tiêu chí | OpenBolt.dev | Bolt.diy | OpenCode |
| :--- | :--- | :--- | :--- |
| **Bản chất công cụ** | Trình soạn thảo full-stack chạy trên Cloud (mây). | Trình soạn thảo full-stack chạy Cục bộ (local). | **Tác nhân AI (AI Agent)** chạy độc lập để chỉnh sửa mã nguồn hiện có. |
| **Môi trường vận hành** | Trình duyệt web trực tuyến, không tốn tài nguyên máy. | Máy tính cá nhân (qua Node.js/pnpm, Docker hoặc App Desktop). | Ứng dụng máy tính (Desktop App) độc lập hoặc tích hợp trong VS Code. |
| **Giao diện làm việc** | Giao diện Web, tích hợp sẵn cửa sổ xem trước (Preview) ứng dụng. | Giao diện Web local, tích hợp sẵn cửa sổ xem trước (Preview) ứng dụng. | Không có cửa sổ preview riêng; tập trung vào việc đọc/ghi file và tương tác qua chat. |
| **Cách thức hoạt động** | Tự động tạo khung dự án, cài đặt thư viện và chạy ứng dụng trực tiếp trên đám mây từ số 0. | Tự tạo khung dự án, cài thư viện và chạy ứng dụng dựa trên tài nguyên phần cứng của bạn. | Cần có sẵn một thư mục mã nguồn (ví dụ từ GitHub). AI sẽ quét thư mục, **tự động sửa file và chạy lệnh Terminal thay cho bạn**. |
| **Mức độ kiểm soát** | Phụ thuộc vào nền tảng bên thứ ba để lưu trữ lịch sử và mã nguồn. | Kiểm soát tuyệt đối 100% dữ liệu, mã nguồn và lịch sử chat trên máy cá nhân. | Kiểm soát tốt vì chỉnh sửa trực tiếp trên thư mục dự án cục bộ của bạn. |
| **Tích hợp Mô hình AI** | Hỗ trợ mang khóa API riêng (BYOK) từ OpenAI, Anthropic, Gemini, DeepSeek,... | Hỗ trợ BYOK và có khả năng chạy mô hình local (Ollama, LM Studio) hoàn toàn ngoại tuyến. | Hỗ trợ nạp API Key cá nhân để điều khiển AI Agent sửa lỗi, tối ưu cấu trúc. |
---## 3. QUY TRÌNH PHÁT TRIỂN MVP TỐI ƯU (KHÔNG DÙNG DÒNG LỆNH)
Khi kết hợp cả 3 công cụ này cùng với GitHub, bạn sẽ tạo ra một chu trình khép kín giúp xây dựng MVP cực nhanh mà không vấp phải rào cản kỹ thuật:


[Bước 1: OpenBolt.dev] ──(Tạo app nhanh)──> [Giao diện & Logic Cơ bản]
│
(Đồng bộ qua Extension)
▼
[Bước 2: GitHub Repository] <────────────────────────┘
│
(Kết nối/Tải về)
▼
[Bước 3: OpenCode Desktop] ──(Chat bằng tiếng Việt)──> [Tự động nâng cấp & Sửa code sâu]


### Bước 1: Dựng khung và tạo giao diện cơ bản trên OpenBolt.dev
*   Truy cập OpenBolt.dev và nhập mô tả ý tưởng của bạn (Prompt) bằng tiếng Việt hoặc tiếng Anh.
*   Theo dõi AI tự động viết code, cài đặt các gói giao diện và hiển thị thành phẩm ở cửa sổ **Preview**.
*   Chỉnh sửa trực tiếp bằng cách chat cho đến khi đạt được bộ khung MVP ưng ý.

### Bước 2: Lưu trữ mã nguồn an toàn lên GitHub không dùng Terminal
Vì bạn không thạo dòng lệnh, hãy sử dụng tiện ích mở rộng trình duyệt để đồng bộ tự động:
1.  Đăng ký tài khoản miễn phí tại [GitHub](https://github.com).
2.  Cài đặt tiện ích mở rộng **[Bolt to GitHub](https://google.com)** trên các trình duyệt lõi Chromium (Chrome, Edge, Brave).
3.  Truy cập cài đặt GitHub, tạo một **Personal Access Token (Classic)** và tích chọn quyền `repo`.
4.  Copy đoạn mã Token vừa tạo dán vào phần cấu hình của extension *Bolt to GitHub*.
5.  Tại giao diện OpenBolt.dev đang làm việc, bấm vào biểu tượng extension, đặt tên cho dự án và nhấn **Push**. Toàn bộ mã nguồn sẽ tự động được đóng gói và đẩy lên kho lưu trữ GitHub của bạn.

### Bước 3: Nâng cấp tính năng nâng cao bằng OpenCode
Khi ứng dụng của bạn phình to, các trình duyệt web như OpenBolt có thể bị giới hạn bộ nhớ hoặc không xử lý được các logic hệ thống phức tạp:
1.  Tải và cài đặt ứng dụng **[OpenCode Desktop](https://opencode.ai)** về máy tính.
2.  Kết nối OpenCode với tài khoản GitHub của bạn và chọn kho lưu trữ (repository) chứa dự án đã đẩy lên ở Bước 2.
3.  Lúc này, OpenCode đóng vai trò như một **Lập trình viên ảo (AI Agent)** trên máy tính của bạn. Bạn chỉ cần chat yêu cầu tính năng mới (ví dụ: *"Tích hợp thêm cổng thanh toán"* hoặc *"Sửa lỗi không lưu được dữ liệu"*). 
4.  OpenCode sẽ tự động mở file, viết lại mã nguồn, tự gõ các câu lệnh Terminal cần thiết để cài đặt phần mềm bổ sung mà bạn không cần trực tiếp can thiệp vào dòng lệnh.

---

## 4. HƯỚNG DẪN CHUẨN BỊ TRƯỚC KHI BẮT ĐẦU
Để các công cụ trên có thể hoạt động, chúng cần một "bộ não" (Mô hình ngôn ngữ lớn). Bạn cần chuẩn bị sẵn ít nhất một loại mã khóa kết nối (API Key):

1.  **Lựa chọn tối ưu nhất cho Lập trình:** **Anthropic Claude 3.5 Sonnet** (Khả năng viết code cấu trúc lớn cực tốt) hoặc **OpenAI GPT-4o**.
2.  **Lựa chọn tiết kiệm/Ngon-Bổ-Rẻ:** **DeepSeek-V3 / DeepSeek-R1** (Chi phí API cực thấp nhưng năng lực lập trình và hiểu tiếng Việt rất mạnh).
3.  **Cách nạp:** Copy đoạn mã API Key nhận được từ nhà cung cấp, nhấn vào biểu tượng bánh răng cài đặt (Settings) hoặc biểu tượng chìa khóa trên giao diện OpenBolt.dev / OpenCode và dán vào để kích hoạt.

------------------------------
