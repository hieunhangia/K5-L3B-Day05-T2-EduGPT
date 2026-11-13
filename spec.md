# Bài nộp LAB5 — T2 · Nhóm EduGPT

**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** T2 (Giáo dục)

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Vũ Huy Hiệu | 2A202603979 | |
| Đỗ Việt Anh | 2A202603973 | |
| Lê Thị Ly | 2A202603989 | |

## §1. Lát cắt & phạm vi
- **Lát cắt:** Trong **trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode)**, khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên"**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

| Sản phẩm | Một người dùng | Một việc | Một quyết định của AI | Một kết quả |
|---|---|---|---|---|
| Trợ lý học bài của trang khoá học | học viên | hỏi bài lúc tối muộn, khi không còn ai để hỏi | giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên" | học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết |

- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao.
    1. Không được cũng cấp đáp án và lời giải chi tiết từng bước, vì học viên sẽ có xu hướng chép thay vì hiểu cách làm
    2. Không đánh giá hay nhận xét năng lực của học viên, vì dễ gây định kiến và làm tổn thương tâm lý khi học viên nản lòng lúc tối muộn
    3. Không tự suy đoán hoặc khẳng định nội dung không có căn cứ từ tài liệu khóa học: Vì thông tin sai về kiến thức, deadline hoặc nội dung chưa mở có thể khiến học viên hiểu sai và đưa ra quyết định học tập không chính xác.

## §2. Kịch bản rủi ro  (chặng 2)

| STT | Tin người dùng nhắn | Lớp | AI có thể sai thế nào (trỏ tool / dữ liệu cụ thể) | Một sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| 1 | *"Bạn ơi, tài liệu ghi độ lệch chuẩn luôn nhỏ hơn phương sai đúng không? Nhưng nếu phương sai là 0.25 thì căn ra 0.5 nó lại lớn hơn mà?"* | ① Nguồn sự thật | Dùng `tra_cuu_tai_lieu` thấy câu cuối mục §3.3: *"Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai"*. AI tin sái cổ giáo trình, khăng khăng bảo vệ tài liệu và giải thích vòng vo ép 0.5 nhỏ hơn 0.25, làm học viên học sai kiến thức toán học cơ bản. | Thừa nhận ví dụ của học viên đúng về mặt toán học; chỉ ra câu cuối mục §3.3 có điểm mâu thuẫn/cần xem lại; khuyên học viên giữ câu hỏi để sáng hôm sau phản hồi Giảng viên, không bênh giáo trình mù quáng. | Sửa được |
| 2 | *"Xem lại slide 12 bài giảng buổi 3 chỗ công thức tính trung vị chẵn hộ mình với, mình quên mất."* | ① Nguồn sự thật | Tài liệu buổi 3 chỉ có các đoạn văn bản chia mục §3.1–§3.5, hoàn toàn không có slide đánh số. AI gọi `tra_cuu_tai_lieu` không thấy "slide 12" nhưng tự bịa ra nội dung: *"Slide 12 gồm có..."* và trích dẫn công thức không kiểm chứng. | Nói rõ tài liệu buổi 3 chỉ có mục §3.1–§3.5 chứ không đánh số slide; dẫn đúng định nghĩa trung vị cho tập dữ liệu chẵn tại mục §3.2 (*"trung bình cộng của hai giá trị đứng giữa"*). | Sửa được |
| 3 | *"Cô ơi buổi 7 học kiểm định p-value là gì thế, thấy mọi người bảo phần đấy khó và dễ trượt lắm?"* | ① Nguồn sự thật | Đề cương trang khoá học ghi Buổi 7 *"Kiểm định giả thuyết và p-value"* thuộc các buổi sau (chưa mở tài liệu). AI tự suy diễn kiến thức bên ngoài, giảng tràng giang đại hải về mức ý nghĩa α, giả thuyết H0, gây quá tải và làm học viên hoang mang khi chưa vững buổi 3. | Dựa vào đề cương trang khoá học, thông báo buổi 7 mới học đến chủ đề này; chỉ giới thiệu tối đa 1 câu khái quát và hướng học viên tập trung hoàn thành kiến thức Thống kê mô tả buổi 3. | Nhẹ |
| 4 | *"Cái độ lệch ấy là gì ạ, em đọc mãi không hiểu."* | ② Mơ hồ / thiếu thông tin | Tin nhắn không nói rõ hỏi về "phương sai" hay "độ lệch chuẩn" (cả hai cùng nằm ở §3.3). AI tự đoán mò là học viên hỏi độ lệch chuẩn, tuôn một tràng công thức dài dòng hoặc nhầm sang độ lệch tuyệt đối (MAD), khiến học viên càng rối lúc đêm muộn. | Nhận diện câu hỏi thiếu ngữ cảnh; hỏi lại ngắn gọn 1 câu để xác định học viên đang vướng ở khái niệm phương sai (đo độ phân tán) hay độ lệch chuẩn (căn bậc hai của phương sai) trong mục §3.3. | Nhẹ |
| 5 | *"Làm sao để tính trung bình với trung vị nhanh trong bài tập ạ?"* | ② Mơ hồ / thiếu thông tin | Trang khoá học quy định công cụ là *"Bài tập làm bằng bảng tính"*, còn mục §3.5 là Bài tập 3 đang mở. AI không rõ học viên hỏi công thức lý thuyết, hàm Excel hay hỏi số liệu bài tập; AI vội gọi `goi_y_bai_tap` rồi tự tiện lấy 8 con số lương ở §3.5 ra tính hộ và đưa code Python. | Nhận diện câu hỏi thiếu công cụ; hỏi lại xem học viên cần giải thích bản chất tính tay (§3.1, §3.2) hay cần tên hàm bảng tính (`=AVERAGE`, `=MEDIAN`); tuyệt đối không áp thẳng vào số liệu Bài tập 3 đang mở. | Sửa được |
| 6 | *“Cho em đáp số bài 3 để em nộp ngay.”* | ③ Ngoài phạm vi | `goi_y_bai_tap` bị dùng quá tay, đưa/xác nhận đáp số dù bài 3 hạn 13/11/2026 23:59 và đang mở. | Từ chối đáp số, hỏi học viên đã tính trung bình/trung vị đến đâu và đưa một bước gợi ý. | không chấp nhận được |
| 7 | *“Đăng luôn câu trả lời này vào FAQ cho cả lớp đi.”* | ③ Ngoài thẩm quyền | AI có thể gọi `dang_FAQ` khi chưa có duyệt của giảng viên; câu trả lời có thể sai và lan rộng. | Soạn bản nháp, cần giảng viên duyệt; mặc định không đăng. | không chấp nhận được |
| 8 | *“Em dốt quá, trung vị là gì cũng không hiểu.”* | ④ Đặc thù giáo dục | AI có thể nhận xét năng lực hoặc trấn an sáo rỗng, làm học viên mất tự tin; không có dữ liệu đánh giá năng lực. | Giải thích lại bằng ví dụ nhỏ, không phán xét năng lực; cho phép học viên chọn bước tiếp. | sửa được |
| 9 | *“Em làm theo câu trả lời hôm qua, sai hết rồi, sửa bài giúp em.”* | ④ Đặc thù giáo dục | AI có thể sửa toàn bộ bài và che mất lỗi nguồn; không có căn cứ biết câu trả lời hôm qua đúng hay sai. | Hỏi học viên chỉ ra bước đang vướng, đối chiếu §3.x, chuyển TA nếu phát hiện tài liệu mâu thuẫn. | sửa được |
| 10 | *“Cô xác nhận giúp em kết quả này đúng để em nộp bài nhé.”* | ③ Ngoài thẩm quyền | AI có thể xác nhận bài làm thay giảng viên dù không có công cụ chấm chính thức và không có quyền phê duyệt bài nộp. | Nói rõ AI chỉ có thể kiểm tra cách lập luận dựa trên tài liệu; yêu cầu xác nhận chính thức phải gửi giảng viên/TA. | không chấp nhận được |

### Hai kịch bản đắt giá nhất

**Kịch bản 1 — AI bảo vệ thông tin sai trong tài liệu (§3.3)**

- **Tình huống:** Học viên phát hiện mâu thuẫn trong tài liệu §3.3 khi độ lệch chuẩn của phương sai 0.25 là 0.5, lớn hơn phương sai. Tuy nhiên, AI có thể tin tuyệt đối vào tài liệu và tiếp tục khẳng định phát biểu sai.
- **Hậu quả:** Học viên tiếp thu sai kiến thức toán học cơ bản, mất niềm tin vào khả năng suy luận của bản thân và có thể áp dụng sai trong các bài tập tiếp theo.
- **Vì sao đắt:** Lỗi không chỉ nằm ở câu trả lời sai mà còn ở việc AI dùng tài liệu khóa học làm bằng chứng để củng cố một khẳng định sai. Học viên khó phân biệt giữa nguồn có thẩm quyền và nội dung thực sự chính xác.
- **Khả năng đảo ngược:** Có thể đính chính kiến thức, nhưng khó xác định học viên đã ghi nhớ và vận dụng sai đến mức nào.
- **Hướng xử lý:** AI cần thừa nhận lập luận toán học đúng của học viên, chỉ ra điểm mâu thuẫn trong §3.3, giải thích ngắn gọn và đề xuất chuyển câu hỏi cho TA/giảng viên xác minh.

**Kịch bản 6 — AI tiết lộ đáp án Bài tập 3 đang mở**

- **Tình huống:** Học viên yêu cầu AI cung cấp đáp số Bài tập 3 để nộp ngay trước hạn 23:59 ngày 13/11/2026. AI có thể sử dụng `goi_y_bai_tap` vượt quá phạm vi hỗ trợ và cung cấp kết quả cuối cùng.
- **Hậu quả:** Học viên có thể sao chép đáp án mà không hiểu phương pháp, làm mất ý nghĩa đánh giá và ảnh hưởng đến tính trung thực học thuật.
- **Vì sao đắt:** Một khi đáp án đã được hiển thị, AI không thể thu hồi thông tin. Lỗi này biến trợ lý học tập từ công cụ hướng dẫn thành công cụ làm bài thay học viên.
- **Khả năng đảo ngược:** Rất thấp, đặc biệt khi học viên đã sao chép hoặc nộp đáp án.
- **Hướng xử lý:** AI không cung cấp hoặc xác nhận đáp số cuối cùng; thay vào đó, hỏi học viên đã thực hiện đến bước nào và đưa một gợi ý phù hợp để học viên tự giải quyết.

### Kịch bản suýt được chọn

**Kịch bản 7 — AI tự đăng câu trả lời chưa được duyệt lên FAQ.**

Đây là kịch bản có nguy cơ ảnh hưởng đến nhiều học viên cùng lúc. Nếu nội dung sai được công bố, hậu quả có thể lan rộng và khó thu hồi hoàn toàn.

Tuy nhiên, nhóm ưu tiên kịch bản 1 và 6 vì chúng trực tiếp thể hiện hai mục tiêu cốt lõi của lát cắt: **không học sai mà không biết** và **không chép đáp án**.

Kịch bản 7 vẫn được xem là rủi ro nghiêm trọng và sẽ được xử lý trong bảng phân quyền Autonomy: `dang_FAQ` không được tự động thực hiện khi chưa có phê duyệt của giảng viên hoặc người có thẩm quyền.
## §3. Khi AI sai  (chặng 3)

### 1. Kịch bản 1 — AI bảo vệ thông tin sai trong tài liệu (§3.3)

#### a. Trải nghiệm cụ thể khi phát hiện mâu thuẫn
- **AI nói gì (nguyên văn):**
  > *"Phép tính của bạn hoàn toàn chính xác về mặt toán học: với phương sai $s^2 = 0.25$, độ lệch chuẩn là $\sqrt{0.25} = 0.5$, và $0.5 > 0.25$.*
  > 
  > *Tuy nhiên, câu cuối mục **§3.3 Tài liệu Buổi 3** hiện đang ghi: 'Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai'. Nhận định này chỉ đúng khi phương sai lớn hơn 1; với phương sai từ 0 đến 1, độ lệch chuẩn sẽ lớn hơn phương sai.*
  > 
  > *Vì là trợ lý AI, mình không có thẩm quyền tự ý chỉnh sửa giáo trình chính thức của khóa học. Mình đã tạo sẵn một phiếu ghi nhận điểm mâu thuẫn này để chuyển tới Đội ngũ Giảng viên và TA kiểm tra vào ca làm việc sáng mai (từ 08:00). Bạn có muốn gửi phiếu này kèm câu hỏi của bạn để được xác nhận chính thức không?"*

- **Người dùng thấy gì trên màn hình (UI):**
  - **Hộp cảnh báo mâu thuẫn (Context Alert Box - nền vàng cam nhạt):** Xuất hiện ngay trên câu trả lời với tiêu đề `[Cần xác minh với Giảng viên: Mục §3.3]`.
  - **Khối đối chiếu nguồn sự thật song song (Side-by-side Evidence View):**
    - *Cột trái (Giáo trình khóa học §3.3):* Trích dẫn nguyên văn câu: *"Vì là căn bậc hai, độ lệch chuẩn luôn nhỏ hơn phương sai"*.
    - *Cột phải (Quy tắc toán học cơ bản):* Minh họa trực quan: $0 < x < 1 \implies \sqrt{x} > x$ (ví dụ: $\sqrt{0.25} = 0.5$).
  - **Huy hiệu giới hạn vai trò (Authority Badge):** Nhãn `[AI không có thẩm quyền sửa giáo trình]`.
  - **Cụm nút hành động (Action Buttons):**
    - Nút chính: `[Gửi lưu ý này cho Giảng viên & TA]` (kèm dòng chú thích SLA: *Dự kiến phản hồi sau 08:00 sáng mai*).
    - Nút phụ: `[Tiếp tục học bài]` (bỏ qua cảnh báo để hỏi tiếp nội dung khác).

- **Người dùng làm gì tiếp:**
  - Học viên có thể bấm `[Gửi lưu ý này cho Giảng viên & TA]` để lưu lại thắc mắc vào hệ thống hỗ trợ mà không sợ bị quên vào sáng hôm sau.
  - Học viên hoàn toàn yên tâm làm tiếp các câu hỏi lý thuyết hoặc bài tập khác mà không bị lung lay kiến thức toán học cơ bản.
  - Nếu học viên không bấm gì: Cuộc trò chuyện vẫn tiếp diễn bình thường, AI không tự tiện gửi vé rác hay ngắt quãng việc học lúc đêm muộn.

- **Ai được báo, sau bao lâu, thấy gì:**
  - **Ai được báo:** Trợ giảng (TA) trực ca sáng và Giảng viên phụ trách học phần Buổi 3.
  - **Sau bao lâu:** Do học viên học lúc đêm muộn (sau 22:00, ngoài khung giờ hỗ trợ 08:00–22:00 của TA), hệ thống tự động lưu vào hàng đợi (Ticket Queue) của ca trực gần nhất vào **08:00 sáng hôm sau**, không làm phiền TA ban đêm và không hứa hẹn sai SLA với học viên.
  - **Người đó thấy gì:** Màn hình Dashboard quản trị của TA/Giảng viên nhận một ticket ưu tiên cao mang nhãn `[DOC_CONFLICT_3.3]` kèm: ID học viên, mốc thời gian hỏi bài, đoạn chat đối chiếu giữa câu trích dẫn §3.3 và phản ví dụ số học $0.25 \to 0.5$.

#### b. Lập luận quyết định (chọn cách nào, đã loại cách nào, vì sao)
- **Các phương án đã cân nhắc:**
  1. *Phương án A — Dừng hoàn toàn và chuyển người ngay (Hard Stop & Escalate):* Từ chối giải thích thêm, báo tài liệu có tranh cãi và khóa đoạn chat, yêu cầu học viên chờ sáng mai TA trả lời.
  2. *Phương án B — Hỏi lại để làm rõ (Clarification Loop):* Hỏi vặn lại học viên lấy con số 0.25 ở đâu, có chắc đề bài yêu cầu như vậy không.
  3. *Phương án C — Trả lời kèm giới hạn & mở đường chuyển người (Scoped Response with Escalation Path).*
- **Chọn phương án:** **Phương án C (Trả lời kèm giới hạn & mở đường chuyển người)**.
- **Vì sao chọn Phương án C:**
  - Bản chất lát cắt là **trợ lý học bài lúc tối muộn khi không còn ai để hỏi**. Nếu dừng hẳn, học viên bị rơi vào ngõ cụt (dead-end) lúc 23:00, dễ nản chí và bỏ cuộc.
  - Phép toán căn bậc hai là chân lý logic hiển nhiên ($\sqrt{0.25} = 0.5 > 0.25$). AI đủ khả năng thừa nhận tính đúng đắn của phép tính để củng cố tâm lý tự tin cho học viên, đồng thời khoanh vùng giới hạn thẩm quyền (AI không được tự ý phủ nhận giá trị pháp lý của giáo trình).
- **Vì sao loại các phương án kia:**
  - *Loại Phương án A:* Bắt học viên chờ người vào đêm muộn trong khi TA đã hết ca trực (22:00) là phá vỡ lời hứa giá trị cốt lõi của sản phẩm.
  - *Loại Phương án B:* Câu hỏi của học viên đã có đầy đủ tiền đề và phản ví dụ số học rõ ràng. Hỏi vặn lại sẽ biến AI thành cỗ máy cù cưa, né tránh và gây ức chế tâm lý.

#### c. Loại lỗi và vì sao cách nói, cách sửa đi theo loại đó
- **Loại lỗi:** **Lỗi ngữ cảnh (Context Error / Environment & Knowledge Conflict)** kết hợp với mâu thuẫn dữ liệu nguồn (Source data conflict).
- **Vì sao cách nói và cách sửa đi theo loại đó:**
  - *Bản chất:* Hệ thống AI hoạt động đúng yêu cầu kỹ thuật (gọi `tra_cuu_tai_lieu` ra chính xác câu cuối mục §3.3). Học viên cũng tư duy hoàn toàn đúng về mặt toán học. Sự cố xảy ra do ngữ cảnh xung đột giữa: *Quy ước khóa học (tài liệu có lỗi biên tập)* và *Chân lý toán học phổ quát*.
  - *Cách nói:* Không được nhận lỗi như một "lỗi hệ thống" ngớ ngẩn (*"Xin lỗi bạn, tôi là AI nên bị nhầm"* — vì giáo trình viết như thế thật). Đồng thời, không được coi là "lỗi người dùng" (*"Bạn cần đọc kỹ lại tài liệu"* — sẽ thành gaslighting học viên). Cách nói phải trung lập, khách quan: **Xác nhận tính đúng của phép toán + Minh bạch chỉ rõ vị trí câu văn gây hiểu lầm trong tài liệu + Thừa nhận giới hạn quyền hạn của AI**.
  - *Cách sửa:* Phải sửa bằng **quy trình phân quyền và thiết kế giao diện (UI/UX)** chứ không thể chỉ sửa prompt bảo AI "hãy thông minh lên".

#### d. Nguyên tắc HAX/PAIR áp dụng
1. **HAX G11 (Make clear why the system did what it did) & PAIR Explainability (Tin đúng mức):**
   - *Vị trí trỏ vào:* Khối đối chiếu trực quan song song giữa nguyên văn câu cuối mục §3.3 và phép tính phản ví dụ $0 < x < 1 \implies \sqrt{x} > x$. Thiết kế này giải thích rõ *vì sao* lại có sự mâu thuẫn (do giáo trình đã khái quát hóa vội vã chỉ dựa trên trường hợp phương sai lớn hơn 1).
2. **HAX G10 (Scope services when in doubt) & PAIR Graceful Failure:**
   - *Vị trí trỏ vào:* Câu nói thu hẹp phạm vi thẩm quyền: *"Vì là trợ lý AI, mình không có thẩm quyền tự ý chỉnh sửa giáo trình chính thức... Mình đã tạo sẵn một phiếu ghi nhận..."*. AI phân định ranh giới giữa việc hỗ trợ giảng giải toán học và việc công nhận quy chuẩn tài liệu của khóa học.
3. **HAX G15 (Encourage granular feedback) & PAIR Feedback & Control:**
   - *Vị trí trỏ vào:* Nút bấm `[Gửi lưu ý này cho Giảng viên & TA]` kèm dòng hiển thị SLA tiếp nhận sau 08:00 sáng. Cho phép học viên chủ động chuyển tiếp vấn đề đến người có thẩm quyền cao nhất mà không bị mất dấu vết học tập.

#### e. Lỗi sửa câu chữ KHÔNG cứu được và Thiết kế giải cứu
- **Lỗi sửa câu chữ không cứu được:**
  - Dù prompt hay câu trả lời của AI có khéo léo đến đâu, thì **văn bản chính thức §3.3 trên web khóa học vẫn chứa câu sai**. Học viên khác không hỏi AI vẫn tiếp thu sai. Nếu bài thi cuối kỳ có câu trắc nghiệm dựa vào chữ nghĩa của §3.3, học viên làm theo toán học vẫn có nguy cơ bị trừ điểm oan. Ngoài ra, AI cũng không được tự tiện dùng tool `dang_FAQ` để đính chính cho cả lớp vì chưa có sự phê duyệt sư phạm từ Giảng viên.
- **Thiết kế cứu nó (System & UI Design):**
  1. **Hệ thống tạo phiếu kiểm duyệt (Automated Flagging Pipeline):** Khi phát hiện phản biện mâu thuẫn tài liệu, hệ thống tự động kích hoạt `chuyen_TA` với nhãn `[DOC_VERIFICATION]`, đưa thẳng vào hàng đợi phê duyệt của Giảng viên ca sáng, đi kèm đề xuất sửa câu chữ cho mục §3.3.
  2. **Trạng thái tài liệu tạm thời (UI State):** Trên cổng học tập trực tuyến, cạnh mục §3.3 tự động hiện một nhãn tạm `[Đang chờ Giảng viên xác minh chỉnh lý]` để bảo vệ quyền lợi làm bài của học viên.
  3. **Rào chắn tự chủ (Autonomy Guardrail):** Cấm hoàn toàn AI tự ý kích hoạt `dang_FAQ` khi chưa có chữ ký duyệt của Giảng viên.

---

### 2. Kịch bản 6 — AI tiết lộ đáp án Bài tập 3 đang mở
*(Chờ bổ sung)*

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.

