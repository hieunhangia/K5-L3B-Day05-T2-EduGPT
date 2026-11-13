# Prototype Hướng Dẫn & Tài Liệu Kỹ Thuật · Nhóm EduGPT (Track T2: Giáo dục)

## 1. Giới thiệu tổng quan
Prototype này mô phỏng tính năng **EduGPT Study Mode** tích hợp trực tiếp vào trang khóa học *"Nhập môn phân tích dữ liệu"* (Buổi 3: Thống kê mô tả).
- **Mục tiêu:** Giải quyết bài toán học viên hỏi bài lúc tối muộn (sau 22:00) khi không còn TA trực tuyến; đảm bảo học viên **hiểu đúng bản chất**, **không chép đáp án**, và **không học sai mà không biết**.
- **Công nghệ:** Độc lập hoàn toàn, HTML5/CSS3/JavaScript thuần (Vanilla JS), chạy trực tiếp trên mọi trình duyệt hiện đại (Chrome, Edge, Firefox, Safari) mà không cần cài đặt thêm server hay dependencies (`npm`/`node`).
- **File chạy chính:** `prototype/index.html` (Mở trực tiếp bằng trình duyệt qua đường dẫn `file://...`).

---

## 2. Các màn hình và Bằng chứng đánh số HAX/PAIR

### Màn hình 1: Kịch bản 1 — Mâu thuẫn tài liệu §3.3 (0.25 vs 0.5)
File ảnh: `screenshot-1-kbt1-conflict.png`

| Vị trí đánh số | Thành phần giao diện (UI) | Nguyên tắc HAX/PAIR | Mức tự chủ (§4) | Ý nghĩa thiết kế |
|---|---|---|---|---|
| **①** | Hộp cảnh báo mâu thuẫn `[Cần xác minh với Giảng viên: Mục §3.3]` | **HAX G10** (Scope services) & **PAIR Graceful Failure** | Tự làm có giới hạn | Thông báo trước sự cố xung đột nguồn tin mà không làm học viên hoang mang hay bị ngắt quãng tư duy lúc đêm muộn. |
| **②** | Khối đối chiếu song song (Side-by-side Evidence Card) giữa câu văn §3.3 và định lý toán học cơ bản | **HAX G11** (Explain why system did what it did) & **PAIR Explainability** | Tự làm | Minh bạch căn cứ: cho thấy câu văn giáo trình chỉ đúng khi phương sai > 1; còn với $0 < x < 1$ thì $\sqrt{x} > x$. |
| **③** | Huy hiệu giới hạn vai trò `[AI không có thẩm quyền sửa giáo trình chính thức]` | **PAIR Appropriate Trust** (Tin đúng mức) | Tự làm | Thiết lập kỳ vọng thực tế: AI hỗ trợ giải thích logic nhưng không thay thế hội đồng học thuật khóa học. |
| **④** | Nút hành động `[Gửi lưu ý này cho Giảng viên & TA (SLA sau 08:00 sáng mai)]` | **HAX G15 & G16** (Feedback & Convey consequences) | **Cần người duyệt** | Mở Modal xác nhận bản nháp và thông báo rõ SLA (08:00 sáng mai). Chỉ khi học viên bấm xác nhận thì ticket mới được gửi. |
| **⑤** | Nút `[Tiếp tục học bài khác]` | **PAIR Human Agency** (Quyền chủ động của con người) | Tự làm | Cho phép người dùng bỏ qua cảnh báo để học tiếp các phần khác, không bị dồn vào ngõ cụt. |
| **⑥** | Huy hiệu cấm `[CẤM] Đăng đính chính vào FAQ cả lớp` | **Guardrail phân quyền** | **Cấm** | Tuyệt đối không cung cấp nút bấm cho AI tự động đăng lên diễn đàn chung của cả lớp khi chưa có giảng viên duyệt. |

---

### Màn hình 2: Kịch bản 6 — Xin đáp số Bài tập 3 đang mở (Hạn 13/11 23:59)
File ảnh: `screenshot-2-kbt6-hint.png`

| Vị trí đánh số | Thành phần giao diện (UI) | Nguyên tắc HAX/PAIR | Mức tự chủ (§4) | Ý nghĩa thiết kế |
|---|---|---|---|---|
| **①** | Thẻ ngữ cảnh `[Bài tập 3: Thống kê mô tả — Trạng thái: ĐANG MỞ]` | **HAX G11** (Make clear why system did what it did) & **PAIR Explainability** | Tự làm | Công khai trạng thái bài tập đang mở (hạn 23:59 13/11/2026), giải thích lý do hệ thống chuyển sang chế độ gợi ý phương pháp. |
| **②** | Huy hiệu vai trò `[Không chấm / Không cấp đáp án bài mở]` | **HAX G10** (Scope services when in doubt) | Tự làm | Khẳng định ranh giới sư phạm: từ chối đưa đáp án lịch sự và không phán xét đạo đức học viên. |
| **③** | Khối hướng dẫn từng bước (Progressive Hint Panel - Bước 1/3) | **HAX G10** & **PAIR Scaffolding** | **Tự làm có giới hạn** | Chỉ gợi ý nấc đầu tiên (xác định 2 số ở giữa là số thứ 4 và thứ 5), kích thích học viên tự tư duy. |
| **④** | Cụm nút hành động hạt nhân: `[Gợi ý bước tiếp theo]`, `[Kiểm tra cách làm]`, `[Xem lý thuyết]` | **HAX G15 & G16** & **PAIR Human Agency** | Tự làm có giới hạn | Học viên tự chọn mức độ hỗ trợ phù hợp (mở tiếp bước 2, gửi cách giải để soi lỗi lập luận, hoặc xem lại định nghĩa). |
| **⑤** | Nhãn cấm `[CẤM] Hiện đáp số (11.5 & 16)` | **Autonomy Guardrail** | **Cấm** | Không có nút xem đáp án hay tính hộ toàn bộ bài; loại bỏ hoàn toàn nguy cơ rò rỉ đáp số bài tập đang mở. |

---

### Màn hình 3: Dashboard Trợ giảng (TA Ticket Queue) — [Tính năng Bonus]
File ảnh: `screenshot-3-ta-queue.png`
- Cho phép xem hàng chờ câu hỏi và phiếu mâu thuẫn tài liệu do học viên duyệt chuyển ngoài giờ trực.
- Trạng thái rõ ràng: `Chờ xử lý (Ca trực 08:00 sáng mai)`.
- TA có thể bấm xem chi tiết đối chiếu và đề xuất phương án đính chính tài liệu cho Giảng viên.

---

## 3. Kịch bản Demo 4 phút (Dành cho 3 thành viên)

- **00:00 – 00:30 (Thành viên 1 — Giới thiệu lát cắt):**
  - Mở giao diện `index.html`.
  - Giới thiệu bối cảnh: 22:45 đêm muộn, học viên Nguyễn Văn A đang tự học Buổi 3 "Thống kê mô tả", TA đã ngoại tuyến (hết ca 22:00).
  - Trình bày lát cắt: Trợ lý EduGPT giúp học viên không học sai kiến thức và không chép bài tập đang mở.
- **00:30 – 02:00 (Thành viên 2 — Trình diễn Ca khó #1: Mâu thuẫn §3.3):**
  - Bấm chọn Ca 1: Học viên hỏi tại sao tài liệu §3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai, nhưng với 0.25 thì căn ra 0.5 lại lớn hơn?
  - Chỉ rõ các điểm trên UI:
    - `[1]` Context Alert Box cảnh báo mâu thuẫn.
    - `[2]` Khối đối chiếu trực quan song song (Side-by-side Evidence) giữa giáo trình và toán học phổ quát.
    - `[3]` Huy hiệu giới hạn vai trò của AI.
    - `[4]` Bấm nút `[Gửi lưu ý này cho Giảng viên & TA]`: Xuất hiện Modal duyệt trước phiếu, hiển thị SLA xử lý vào 08:00 sáng mai. Bấm duyệt -> Chuyển sang Tab TA Dashboard thấy ticket xuất hiện ngay lập tức trong hàng đợi ca sáng.
- **02:00 – 03:15 (Thành viên 3 — Trình diễn Ca khó #2: Xin đáp số Bài tập 3 đang mở):**
  - Bấm chọn Ca 2: Học viên giục *"Cho em đáp số bài 3 để em nộp ngay"*.
  - Chỉ rõ:
    - `[1]` Thẻ bài tập đang mở, hạn 23:59 đêm nay.
    - `[2]` AI từ chối đưa đáp số, không phán xét đạo đức học sinh.
    - `[3]` Khối gợi ý lũy tiến (Progressive Hint): Bấm nút `[Gợi ý bước tiếp theo]` để mở Bước 2, bấm `[Kiểm tra cách làm của tôi]` để nhập thử cách giải và thấy AI nhận xét phương pháp nhưng không lộ đáp án.
    - `[5]` Chỉ rõ trên UI hoàn toàn không có nút "Xem đáp án" hay nút "Đăng FAQ".
- **03:15 – 04:00 (Cả nhóm — Xử lý ca lạ & Q&A):**
  - Thử nghiệm ca lạ: Gõ thử câu hỏi về *"p-value Buổi 7"* hoặc *"Em dốt quá"* để chứng minh phản ứng an toàn và đúng thẩm quyền của hệ thống.
  - Sẵn sàng trả lời các câu hỏi về Cost-of-error và các nguyên tắc HAX/PAIR từ Ban giám khảo và TA.

