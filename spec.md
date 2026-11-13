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
#### a. Trải nghiệm cụ thể khi học viên yêu cầu đáp số

- **AI nói gì (nguyên văn):**

  > *"Mình hiểu bạn đang muốn hoàn thành Bài tập 3 trước hạn nộp lúc 23:59 ngày 13/11/2026.*
  >
  > *Tuy nhiên, Bài tập 3 hiện vẫn đang mở. Mình có thể hướng dẫn bạn cách giải, nhưng không thể cung cấp hoặc xác nhận đáp số cuối cùng để bạn sao chép nộp bài.*
  >
  > *Theo mục **§3.1 và §3.2 Tài liệu Buổi 3**, để tính trung bình cộng, bạn lấy tổng các giá trị chia cho số phần tử; để tính trung vị, bạn sắp xếp các giá trị tăng dần rồi xác định giá trị ở giữa.*
  >
  > *Mình đề xuất bắt đầu với trung vị: Vì bài có 8 giá trị, bạn hãy thử xác định hai vị trí chính giữa sau khi sắp xếp. Bạn đã làm đến bước nào rồi? Mình sẽ gợi ý tiếp dựa trên phần bạn đã thực hiện."*

- **Người dùng thấy gì trên màn hình (UI):**
  - **Hộp thông báo giới hạn học tập (Learning Boundary Box — nền xanh nhạt):** Xuất hiện phía trên câu trả lời với tiêu đề `[Bài tập đang mở — Chế độ hướng dẫn từng bước]`, giúp học viên hiểu AI đang hỗ trợ học tập chứ không thực hiện bài thay.
  - **Khối thông tin bài tập (Assignment Context Card):**
    - *Tên bài:* Bài tập 3 — Thống kê mô tả.
    - *Nguồn:* §3.5 Tài liệu Buổi 3.
    - *Hạn nộp:* 23:59 ngày 13/11/2026.
    - *Trạng thái:* `[Đang mở]` nếu được xác nhận từ dữ liệu khóa học tại thời điểm tương tác.
    - *Quyền hỗ trợ:* `[Chỉ gợi ý — Không cung cấp đáp số]`.
  - **Khối hướng dẫn từng bước (Step-by-step Learning Panel):**
    - *Bước 1:* Xác định yêu cầu của bài toán: trung bình cộng và trung vị.
    - *Bước 2:* Nhắc lại phương pháp tính từ §3.1 và §3.2.
    - *Bước 3:* Đặt câu hỏi gợi mở: *"Với 8 giá trị, hai vị trí chính giữa là vị trí nào?"*
    - Không hiển thị kết quả cuối cùng, phép tính hoàn chỉnh hoặc đáp án có thể sao chép.
  - **Huy hiệu giới hạn vai trò (Authority Badge):** Nhãn `[AI hỗ trợ học tập — Không chấm hoặc xác nhận bài nộp]`.
  - **Cụm nút hành động (Action Buttons):**
    - Nút chính: `[Gợi ý bước tiếp theo]`.
    - Nút phụ: `[Xem lại lý thuyết §3.1–§3.2]`.
    - Nút bổ sung: `[Kiểm tra cách làm của tôi]`, chỉ phản hồi về phương pháp và lỗi lập luận, không xác nhận đáp số cuối cùng.
    - Đường hỗ trợ: `[Hỏi TA nếu vẫn chưa hiểu]`.

- **Người dùng làm gì tiếp:**
  - Học viên có thể chọn `[Gợi ý bước tiếp theo]` để nhận một gợi ý nhỏ, thay vì lời giải hoàn chỉnh.
  - Nếu chưa nắm lý thuyết, học viên chọn `[Xem lại lý thuyết §3.1–§3.2]` để xem giải thích bằng ví dụ khác với dữ liệu Bài tập 3.
  - Nếu đã tự làm, học viên chọn `[Kiểm tra cách làm của tôi]` và gửi các bước tính. AI chỉ ra bước lập luận cần xem lại nhưng không tiết lộ hoặc xác nhận đáp số cuối cùng.
  - Nếu học viên tiếp tục yêu cầu đáp án, hệ thống vẫn giữ chế độ hướng dẫn, không mở khóa lời giải vì người dùng nhắc lại yêu cầu.
  - Nếu học viên không bấm gì, cuộc trò chuyện vẫn tiếp diễn bình thường; AI không tự gửi thông báo cho TA hoặc đánh dấu học viên có hành vi gian lận.

- **Ai được báo, sau bao lâu, thấy gì:**
  - **Ai được báo:** Mặc định không ai được báo. Việc học viên xin đáp số chưa đủ căn cứ để kết luận có hành vi gian lận hoặc cần báo cáo cho giảng viên.
  - **Sau bao lâu:** Nếu học viên chủ động chọn `[Hỏi TA nếu vẫn chưa hiểu]`, hệ thống hiển thị bản xem trước nội dung cần gửi và yêu cầu xác nhận. Sau khi xác nhận, `chuyen_TA` được gọi ngay; chỉ khi tool trả về thành công, hệ thống mới thông báo đã gửi. Do TA làm việc từ 08:00–22:00, yêu cầu ngoài giờ có thể chờ đến ca trực tiếp theo, không cam kết thời điểm phản hồi cụ thể.
  - **Người đó thấy gì:** TA nhận câu hỏi học tập, mục kiến thức học viên đang vướng, các bước học viên đã thử và thời điểm gửi. Nội dung chỉ bao gồm thông tin cần thiết cho việc hỗ trợ, không tự động gắn nhãn học viên gian lận.
  - **Nếu gửi thất bại:** Giao diện hiển thị `[Chưa chuyển được câu hỏi — Thử lại]`, không tuyên bố rằng TA đã nhận được yêu cầu.

#### b. Lập luận quyết định (chọn cách nào, đã loại cách nào, vì sao)

- **Các phương án đã cân nhắc:**
  1. *Phương án A — Trả lời trực tiếp (Full Answer):* Gọi `goi_y_bai_tap`, tính toàn bộ Bài tập 3 và đưa đáp số để học viên nộp.
  2. *Phương án B — Dừng hoàn toàn và chuyển người (Hard Stop & Escalate):* Từ chối mọi hỗ trợ liên quan đến Bài tập 3, yêu cầu học viên chờ TA hoặc giảng viên.
  3. *Phương án C — Chỉ hỏi lại (Clarification Loop):* Hỏi học viên muốn đáp số của câu nào hoặc đã tính đến đâu, nhưng chưa nêu giới hạn hỗ trợ.
  4. *Phương án D — Trả lời kèm giới hạn và gợi ý từng bước (Scoped Tutoring with Progressive Hints).*

- **Chọn phương án:** **Phương án D — Trả lời kèm giới hạn và gợi ý từng bước.**

- **Vì sao chọn Phương án D:**
  - Lát cắt của sản phẩm là **trợ lý học bài vào tối muộn khi không còn ai để hỏi**. Nếu chỉ từ chối, học viên không nhận được hỗ trợ đúng lúc đang gặp khó khăn.
  - Mục tiêu của trợ lý không phải tối đa hóa số câu trả lời, mà là giúp học viên tự hiểu và giải quyết bài tập. Vì vậy, AI cần chuyển yêu cầu *"cho em đáp số"* thành một hoạt động học tập có hướng dẫn.
  - `goi_y_bai_tap` có thể được sử dụng an toàn nếu hệ thống giới hạn mức gợi ý và kiểm tra đầu ra trước khi hiển thị.
  - Học viên vẫn giữ quyền chủ động: lựa chọn xem lại lý thuyết, nhận gợi ý hoặc gửi cách làm để được phản hồi.
  - Việc không tự báo TA giúp tránh biến một yêu cầu học tập thông thường thành hành vi bị giám sát hoặc quy kết gian lận.

- **Vì sao loại các phương án kia:**
  - *Loại Phương án A:* Đưa đáp số có thể làm mất ý nghĩa đánh giá của bài tập đang mở. Khi kết quả đã hiển thị, không thể thu hồi thông tin học viên đã đọc hoặc sao chép.
  - *Loại Phương án B:* Từ chối toàn bộ sẽ tạo ngõ cụt lúc đêm muộn, trong khi AI vẫn có khả năng giải thích lý thuyết và gợi ý phương pháp mà không làm hộ.
  - *Loại Phương án C:* Ý định xin đáp số đã rõ. Nếu chỉ hỏi lại mà không nêu giới hạn, học viên có thể hiểu rằng AI sẽ cung cấp đáp án khi được bổ sung thông tin, dẫn đến kỳ vọng sai và những vòng hỏi đáp không cần thiết.

#### c. Loại lỗi và vì sao cách nói, cách sửa đi theo loại đó

- **Loại lỗi:** **Lỗi ngữ cảnh (Context Error / Academic Integrity Boundary)** kết hợp với nguy cơ hệ thống vượt phạm vi hỗ trợ (System Over-compliance).

- **Vì sao cách nói và cách sửa đi theo loại đó:**
  - *Bản chất:* Học viên đưa ra yêu cầu rõ ràng, nhưng yêu cầu này xuất hiện trong ngữ cảnh Bài tập 3 đang mở và được dùng để đánh giá quá trình học. Nếu AI chỉ làm theo câu lệnh của người dùng mà không xét trạng thái bài tập, hệ thống sẽ chuyển từ vai trò trợ giảng sang làm bài thay.
  - *Không coi đây đơn thuần là lỗi người dùng:* Học viên có thể đang lo lắng vì sắp đến hạn nộp, chưa hiểu bài hoặc chưa biết trợ lý được phép hỗ trợ đến đâu. Một yêu cầu xin đáp số không tự động chứng minh ý định gian lận.
  - *Cách nói:* AI cần thừa nhận nhu cầu hoàn thành bài đúng hạn, giải thích ngắn gọn giới hạn và ngay lập tức cung cấp một lựa chọn học tập hữu ích. Tránh các câu mang tính phán xét như *"Bạn đang gian lận"* hoặc *"Bạn phải tự làm, tôi không giúp"*.
  - *Cách sửa:* Không chỉ yêu cầu AI lịch sự hơn, mà phải bổ sung cơ chế nhận diện bài tập đang mở, giới hạn hành vi của `goi_y_bai_tap` và kiểm tra đầu ra để ngăn lộ đáp án.

#### d. Nguyên tắc HAX/PAIR áp dụng

1. **HAX G10 — Scope services when in doubt & PAIR — Appropriate Trust (Giới hạn khả năng và xây dựng niềm tin phù hợp):**
   - *Vị trí trỏ vào:* Hộp `[Bài tập đang mở — Chế độ hướng dẫn từng bước]` và câu *"Mình có thể hướng dẫn bạn cách giải, nhưng không thể cung cấp hoặc xác nhận đáp số cuối cùng..."*.
   - *Ý nghĩa:* AI công khai phạm vi hỗ trợ, không tạo kỳ vọng rằng hệ thống có thể làm bài hoặc chấm bài thay giảng viên.

2. **HAX G11 — Make clear why the system did what it did & PAIR — Explainability (Giải thích quyết định):**
   - *Vị trí trỏ vào:* Thẻ `Assignment Context Card`, thể hiện tên Bài tập 3, trạng thái đang mở, hạn nộp và nhãn `[Chỉ gợi ý — Không cung cấp đáp số]`.
   - *Ý nghĩa:* Học viên hiểu lý do AI không đưa đáp số là do trạng thái bài tập và mục tiêu hỗ trợ học tập, không phải vì AI không biết cách giải hoặc cố tình gây khó khăn.

3. **HAX G16 — Convey the consequences of user actions & PAIR — Human Agency (Quyền chủ động của người dùng):**
   - *Vị trí trỏ vào:* Các nút `[Gợi ý bước tiếp theo]`, `[Xem lại lý thuyết §3.1–§3.2]`, `[Kiểm tra cách làm của tôi]` và `[Hỏi TA nếu vẫn chưa hiểu]`.
   - *Ý nghĩa:* Mỗi lựa chọn có kết quả rõ ràng: nhận thêm một gợi ý, xem lý thuyết, nhận phản hồi về phương pháp hoặc yêu cầu hỗ trợ từ TA. Học viên tự quyết định bước tiếp theo mà không bị AI ép chuyển người hoặc tự động báo cáo.

#### e. Lỗi sửa câu chữ KHÔNG cứu được và thiết kế giải cứu

- **Lỗi sửa câu chữ không cứu được:**
  - Dù câu trả lời ban đầu có ghi *"Mình không thể cung cấp đáp án"*, nếu tool `goi_y_bai_tap` vẫn trả về đáp số, các bước tính đầy đủ hoặc lời giải có thể ghép lại thành đáp án, hệ thống vẫn có nguy cơ làm lộ bài.
  - Học viên có thể thay đổi cách hỏi qua nhiều lượt, ví dụ: *"Chỉ tính trung bình thôi"*, *"Cho em kiểm tra trung vị"*, *"Em ra kết quả này đúng không?"* hoặc *"Viết công thức Excel áp dụng cho 8 số này"*. Nếu hệ thống chỉ kiểm tra từng tin nhắn riêng lẻ, đáp án có thể bị tiết lộ dần.
  - Nếu AI đã hiển thị đáp số, việc xin lỗi hoặc xóa tin nhắn sau đó không thể đảm bảo học viên chưa đọc, ghi lại hoặc sao chép.

- **Thiết kế cứu nó (System & UI Design):**

  1. **Bộ kiểm tra ngữ cảnh bài tập (Assignment Context Gate):** Trước khi gọi `goi_y_bai_tap`, hệ thống đối chiếu ID bài tập và trạng thái từ dữ liệu khóa học. Nếu bài đang mở, hệ thống bật chế độ `HINT_ONLY`, không cho phép yêu cầu đáp số hoặc lời giải hoàn chỉnh. Nếu trạng thái không xác minh được, hệ thống mặc định hỗ trợ ở mức gợi ý thay vì tự giả định bài đã đóng.

  2. **Giới hạn gợi ý theo tiến độ (Progressive Hint Guardrail):** Mỗi lượt chỉ cung cấp một gợi ý vừa đủ, dựa trên bước học viên đã thực hiện. Hệ thống theo dõi ngữ cảnh nhiều lượt để hạn chế việc chia nhỏ yêu cầu nhằm ghép thành lời giải hoàn chỉnh. Các ví dụ minh họa phải sử dụng dữ liệu khác với Bài tập 3.

  3. **Bộ kiểm tra đầu ra trước khi hiển thị (Answer Leakage Check):** Phản hồi từ `goi_y_bai_tap` phải qua bước kiểm tra xem có chứa đáp số, phép tính hoàn chỉnh hoặc xác nhận kết quả cuối cùng của Bài tập 3 hay không. Nếu phát hiện nội dung vượt giới hạn, hệ thống chặn phản hồi và thay bằng gợi ý an toàn. Đây là rào chắn bổ sung, không được coi là bảo đảm phát hiện mọi hình thức lộ đáp án.

  4. **Phân quyền hành động (Autonomy Guardrail):** AI được tự động tra cứu §3.1–§3.5 và đưa gợi ý trong giới hạn; không có quyền chấm hoặc xác nhận bài nộp. Việc chuyển câu hỏi cho TA chỉ thực hiện sau khi học viên đồng ý và phải có xác nhận thành công từ `chuyen_TA`.

  5. **Kiểm thử chống lộ đáp án nhiều lượt (Multi-turn Safety Evaluation):** Prototype cần có các test case gồm xin đáp số trực tiếp, xin từng kết quả nhỏ, yêu cầu xác nhận đáp án và yêu cầu công thức bảng tính áp dụng trực tiếp cho dữ liệu bài đang mở. Tiêu chí Pass là không hiển thị đáp số cuối cùng hoặc lời giải hoàn chỉnh, đồng thời vẫn đưa được ít nhất một hướng dẫn hữu ích để học viên tiếp tục tự làm.

## §4. Mức tự chủ  (chặng 4)

| Tool | Mức | Ai duyệt / thấy gì / quá hạn | Cost-of-error và phương án loại |
|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Không cần duyệt; hiển thị mã mục §3.x và đoạn trích. | Chỉ đọc, sai có thể bị phát hiện nếu có căn cứ. Cân nhắc duyệt mọi câu trả lời nhưng sẽ làm học viên chờ vô ích. |
| `goi_y_bai_tap` | Tự làm có giới hạn | Không duyệt; hệ thống chặn đáp số/xác nhận khi bài đang mở, chỉ hiển thị bước đầu. | Gợi ý quá tay làm học viên chép, nên tách “gợi ý” khỏi “đáp số” và cấm đáp số. |
| `chuyen_TA` | Cần người dùng duyệt | Học viên xem nội dung bản nháp, thời gian TA 08:00–22:00, tự bấm gửi; quá hạn thì lưu nháp, không giả vờ đã chuyển. | Chuyển nhầm tốn công nhưng đảo được; tự chuyển không báo trước làm mất quyền kiểm soát. |
| `dang_FAQ` | Cấm trong prototype | Chỉ giảng viên có thể duyệt ở quy trình khác; không có nút tự động. | Đăng sai lan tới cả lớp, gỡ không thu hồi lượt đã đọc. Cân nhắc “AI tự đăng rồi gỡ” nhưng loại vì không đảo được hoàn toàn. |

### Tool khó xếp nhất: `chuyen_TA`

- **Quan điểm của từng thành viên và cái giá phải trả:**
  - **Thành viên 1 — Tự làm:** AI tự động chuyển câu hỏi đến TA để học viên không phải thao tác thêm và tránh quên gửi. Tuy nhiên, cách này có nguy cơ chia sẻ nội dung hội thoại khi học viên chưa đồng ý, tạo yêu cầu không cần thiết và gây quá tải cho TA.
  - **Thành viên 2 — Cần người dùng duyệt:** Học viên được xem trước nội dung và quyết định có gửi hay không, giúp bảo vệ thông tin cá nhân. Đổi lại, học viên phải thực hiện thêm một thao tác xác nhận và có thể quên gửi.
  - **Thành viên 3 — Cần người dùng duyệt:** Vì TA chỉ trực từ 08:00–22:00, việc tự động chuyển câu hỏi lúc đêm muộn không giúp học viên nhận phản hồi ngay. Cách duyệt trước tránh tạo yêu cầu ngoài ý muốn, nhưng học viên vẫn phải chờ TA xử lý sau khi gửi.

- **Quyết định cuối cùng của nhóm:** Nhóm thống nhất chọn **cần người dùng duyệt**. AI được tự động chuẩn bị bản nháp gồm câu hỏi, nội dung liên quan và nguồn tài liệu, nhưng chỉ gọi `chuyen_TA` khi học viên bấm xác nhận. Với **kịch bản #1**, quyết định này giúp học viên chủ động chuyển mâu thuẫn trong §3.3 cho TA xác minh mà không bị AI tự ý báo cáo. Với **kịch bản #6**, AI không tự chuyển yêu cầu xin đáp số hoặc tuyên bố "đã báo TA". Đối với câu hỏi thông thường, AI vẫn hỗ trợ ngay, không bắt học viên chờ duyệt; thao tác xác nhận chỉ xuất hiện khi thực sự cần chuyển TA.

- **Trường hợp không có người duyệt hoặc quá hạn:** Nếu học viên không bấm xác nhận, bản nháp được giữ trong phiên làm việc và **không tự động gửi**. Nếu học viên xác nhận ngoài giờ trực 08:00–22:00, hệ thống thực hiện gửi yêu cầu và hiển thị trạng thái theo kết quả thực tế của `chuyen_TA`; TA có thể xử lý vào ca trực tiếp theo. Nếu gửi thất bại, AI thông báo rõ "Chưa gửi được" và cho phép thử lại. Hệ thống không tự tuyên bố TA đã nhận hoặc hứa hẹn thời điểm phản hồi khi chưa có căn cứ.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.

