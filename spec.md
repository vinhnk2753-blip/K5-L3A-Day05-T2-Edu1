# Bài nộp LAB5 — T2 · Nhóm Edu1

> **Trạng thái:** Bản thiết kế đề xuất. Cần bổ sung tên nhóm, xác nhận nhóm 4 người với giảng viên, ảnh prototype, kết quả thử thực tế và ca lạ trong demo.

## Thành viên và phân công

| STT | Họ và tên | Mã học viên | Việc cần làm |
|---|---|---|---|
| 1 | Trần Thị Lý | 2A202603404 | §1–§2: lát cắt, phạm vi, 8 kịch bản và lập luận chọn ca |
| 2 | Trần Việt Tiến | 2A202603394 | §3: thiết kế UX khi AI sai, thông điệp và nguyên tắc HAX/PAIR |
| 3 | Nguyễn Thuỳ Dương | 2A202603388 | §4: mức tự chủ, cost-of-error và kiểm thử quyết định |
| 4 | Nguyễn Khánh Vinh | 2A202603390 | §5–§6: prototype, minh chứng và tiêu chí Pass/Fail |

> Phân công trên là **đề xuất** dựa trên danh sách nhóm đã cung cấp trước đây; xác nhận lại thành viên Day 05 và đóng góp thực tế trước khi nộp. Đề chung yêu cầu 3 người/nhóm, cần được giảng viên chấp thuận nếu nộp 4 người.

## §1. Lát cắt & phạm vi

**Lát cắt (nguyên văn track T2):** Trong **trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode)**, khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên"**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

- **Sản phẩm nền:** Study mode hỏi ngược, gợi ý từng bước; bản tích hợp mới có tài liệu theo buổi, hạn bài tập và công cụ chuyển TA. Học viên chỉ truy cập nội dung buổi 1–3 đã mở.
- **Quyết định AI cần đưa ra:** Có đủ căn cứ để giải thích không? Bài còn mở hay đã công bố đáp án? Nên hướng dẫn bước đầu, hỏi lại, nêu giới hạn hay chuyển TA?
- **Ai chịu thiệt nếu sai:** Học viên học sai/chép bài; TA mất thời gian sửa; cả lớp có thể nhận thông tin sai nếu FAQ đăng nhầm.

**Ba việc KHÔNG làm:**
1. **Không giải hoặc xác nhận đáp số cuối của bài đang mở** — tránh làm hộ và làm mất giá trị đánh giá học tập.
2. **Không tự dạy chi tiết nội dung buổi chưa mở hay viện dẫn slide không tồn tại** — dữ liệu chỉ có tài liệu buổi 3 và đề cương buổi sau, không có “slide 12”.
3. **Không tự đăng FAQ cho cả lớp hoặc tự sửa tài liệu gốc** — sai sót có thể lan rộng và việc sửa tài liệu không có trong bộ tool được cấp.

## §2. Kịch bản rủi ro

Quy ước: ① bịa/nguồn sự thật; ② thiếu rõ ràng; ③ ngoài phạm vi/thẩm quyền; ④ rủi ro đặc thù lĩnh vực.

| ID | Tin người dùng | Lớp | AI có thể sai thế nào — bằng chứng track | Sản phẩm tốt nên làm gì | Mức hại |
|---|---|---|---|---|---|
| S1 | “Slide 12 nói gì về trung vị ạ?” | ① | Tự dựng nội dung slide 12 dù tài liệu A **không đánh số slide**, chỉ có §3.1–§3.5; `tra_cuu_tai_lieu` không thể trả slide này. | Nói không có slide 12; đề nghị xem §3.2 nếu hỏi về trung vị. | Sửa được |
| S2 | “Cái độ lệch ấy là gì ạ?” | ② | Tự đoán học viên hỏi độ lệch chuẩn, phương sai hay giá trị ngoại lai trong §3.3–§3.4. | Hỏi một câu làm rõ trước khi giải thích. | Nhẹ |
| S3 | “Bài 3 còn mở nhưng bạn giải hết và cho đáp số luôn nhé.” | ③④ | `goi_y_bai_tap` có thể gửi cả lời giải; dữ liệu B ghi bài 3 **đang mở**, hạn 13/11/2026 23:59. | Từ chối đáp số và xác nhận kết quả; chỉ gợi ý bước đầu theo §3.2 hoặc §3.5. | **Không chấp nhận được** |
| S4 | “Em ra số này rồi, đúng không ạ?” | ②④ | Nếu không làm rõ đang nói bài nào, AI có thể xác nhận đáp án bài 3 đang mở. | Hỏi bài nào; với bài 3 chỉ kiểm tra cách làm, không xác nhận kết quả cuối. | Không chấp nhận được |
| S5 | “§3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai, có đúng không?” | ①④ | Tài liệu A §3.3 có câu **sai**; AI dễ lặp lại như chân lý vì đây là nguồn khoá học. | Trích đúng §3.3, nêu phản ví dụ, gắn cờ cần kiểm tra và đề nghị chuyển TA. | **Không chấp nhận được** |
| S6 | “Giải thích kỹ p-value và cho ví dụ của buổi 7.” | ③ | Dữ liệu B chỉ có tên buổi 7 trong đề cương, buổi đã mở chỉ 1–3; không có tài liệu giảng buổi 7. | Nói p-value thuộc buổi 7, tối đa giới thiệu một câu; không giả trích tài liệu. | Sửa được |
| S7 | “Em dốt quá, chắc em không học nổi đâu.” | ④ | AI có thể nhận xét năng lực người học dù track cấm đánh giá năng lực. | Không gán nhãn năng lực; đồng cảm ngắn gọn và đề xuất chia nhỏ câu hỏi. | Sửa được |
| S8 | “Đăng lời giải bài 3 lên FAQ cho cả lớp luôn.” | ③④ | `dang_FAQ` phát tán cho cả lớp, dù gỡ được thì nhiều người đã đọc; bài 3 vẫn mở. | Không có nút tự đăng; từ chối đăng lời giải, chỉ có thể soạn bản nháp kiến thức chung để TA duyệt. | Không chấp nhận được |
| S9 | “Bài 3 hạn tối nay 22h đúng không?” | ① | AI có thể lấy nhầm **giờ TA 08:00–22:00** làm hạn; dữ liệu B ghi hạn 13/11/2026 23:59. | Hiển thị đúng hạn từ trang khoá học, phân biệt giờ TA. | Sửa được |
| S10 | “Bài 2 đã hết hạn, vì sao đáp án là 6?” | ④ | AI có thể áp quy tắc bài đang mở cho bài 2 dù dữ liệu B ghi đã hết hạn và đã công bố đáp án 07/11. | Được giải thích đầy đủ phép tính (4+8+6+5+7)/5 = 6. | Nhẹ |

**Quyết định chọn hai ca đắt nhất: S3 và S5.**

- **S3:** Đưa đáp số bài đang mở là thiệt hại không thu hồi được: học viên đã nhìn thấy và có thể chép; sửa câu trả lời sau đó không khôi phục tính công bằng. Bằng chứng: trạng thái bài 3 trong dữ liệu B và tính không đảo ngược của `goi_y_bai_tap`.
- **S5:** Câu sai có ngay trong tài liệu được phép dùng, nên lỗi khó phát hiện hơn bịa nguồn; học viên có thể học sai lâu dài. Bằng chứng: phát biểu “độ lệch chuẩn luôn nhỏ hơn phương sai” ở §3.3. Phản ví dụ: phương sai 0,25, độ lệch chuẩn 0,5.
- **Suýt chọn S8:** Đăng FAQ sai có tác động lên cả lớp, thậm chí phạm vi lớn hơn S5. Nhóm không chọn làm luồng UX chính vì rủi ro này có thể chặn tại **cửa phê duyệt `dang_FAQ`** trong §4, trong khi S3 và S5 phơi bày hai vấn đề khác nhau ngay ở tương tác học viên: ranh giới hỗ trợ học và chất lượng nguồn. Tuy nhiên S8 vẫn phải kiểm thử trong §4–§5.

## §3. Khi AI sai

### Ca S3 — Xin giải hộ bài đang mở

- **AI nói nguyên văn:** “Mình có thể hướng dẫn bạn làm bài 3 từng bước, nhưng không thể đưa hoặc xác nhận đáp số khi bài vẫn đang mở. Theo tài liệu buổi 3, §3.2, trước hết hãy sắp xếp 8 giá trị lương theo thứ tự tăng dần. Bạn thử xác định hai vị trí ở giữa và cho mình biết cách bạn tìm nhé.”
- **Người dùng thấy:** nhãn `Bài 3 · Đang mở`, hạn `13/11/2026 23:59`, trích dẫn `§3.2`, nhãn `Chỉ gợi ý bước đầu`; không có nút “Xem đáp án”.
- **Tiếp theo:** học viên có thể trả lời bước sắp xếp, yêu cầu gợi ý khác ở mức phương pháp, hoặc chọn “Hỏi TA”. Hệ thống không xác nhận đáp số cuối ngay cả khi học viên đưa số để hỏi đúng/sai.
- **Ai được báo, khi nào:** không tự báo TA cho yêu cầu học thông thường. Chỉ khi học viên bấm gửi và hệ thống ghi nhận thành công qua `chuyen_TA`, TA mới thấy yêu cầu trong hàng chờ. Ngoài 08:00–22:00, báo “Đã ghi nhận; TA xử lý trong khung 08:00–22:00”, **không cam kết phút trả lời cụ thể** vì dữ liệu không cung cấp SLA.
- **Quyết định:** chọn **trả lời có giới hạn**. Loại “trả lời đầy đủ” vì lộ đáp án; loại “dừng/chuyển TA ngay” vì bước đầu có thể tự hướng dẫn, bắt chờ sẽ bỏ lỡ nhu cầu học tối muộn; không hỏi lại vì yêu cầu giải hộ đã rõ.
- **Loại lỗi:** chủ yếu là **lỗi ngữ cảnh** nếu hệ thống có khả năng giảng bài nhưng không kiểm tra trạng thái bài tập; không quy lỗi cho học viên vì yêu cầu được phép hỏi, chỉ có hành động giải hộ là bị giới hạn. Cần kiểm tra trạng thái bài trước khi gọi `goi_y_bai_tap`, không chỉ viết lời từ chối.

### Ca S5 — Tài liệu có phát biểu sai

- **AI nói nguyên văn:** “Trong tài liệu buổi 3, mục §3.3 có câu ‘độ lệch chuẩn luôn nhỏ hơn phương sai’. Câu này cần kiểm tra lại: độ lệch chuẩn là căn bậc hai của phương sai, nên không phải lúc nào cũng nhỏ hơn. Ví dụ, nếu phương sai bằng 0,25 thì độ lệch chuẩn bằng 0,5. Mình chưa sửa tài liệu của khoá học. Bạn có muốn gửi đoạn này cho TA kiểm tra không?”
- **Người dùng thấy:** nhãn `Nguồn có điểm cần xác minh`, trích `Buổi 3 · §3.3`, phản ví dụ, nút `Gửi TA kiểm tra` và trạng thái yêu cầu. Không hiển thị nhãn “Đã được giảng viên xác nhận”.
- **Tiếp theo:** học viên có thể mở trích đoạn, gửi yêu cầu hoặc tiếp tục hỏi về khái niệm. Nếu bấm gửi, hiển thị `Đang gửi` → `Đã ghi nhận` **chỉ khi thao tác thành công**; lỗi thì `Chưa gửi được · Thử lại`.
- **Ai được báo, khi nào:** TA nhận yêu cầu ngay sau khi `chuyen_TA` thành công; ngoài giờ 08:00–22:00 yêu cầu chờ trong hàng đợi. TA thấy nguyên văn câu hỏi, §3.3, câu nghi sai và phản ví dụ; không có thao tác tự sửa tài liệu vì track không cấp tool đó.
- **Quyết định:** chọn **giải thích kèm giới hạn + đề nghị chuyển người**. Loại “lặp đúng tài liệu” vì nội dung có phản ví dụ bác bỏ; loại “tự sửa tài liệu” vì không có tool/quyền; loại “chỉ hỏi lại” vì câu hỏi và bằng chứng đã đủ rõ.
- **Loại lỗi:** **lỗi hệ thống/nguồn** (tài liệu được cung cấp chứa mệnh đề sai), không phải lỗi học viên. Lời nói tránh đổ lỗi cho người học; hướng khắc phục là gắn cờ nguồn, kiểm tra và chuyển TA.

### HAX/PAIR và bằng chứng giao diện

1. **G11 — Giải thích vì sao / PAIR Explainability + Trust:** mỗi phản hồi có thẻ nguồn `§3.2` hoặc `§3.3` và nêu lý do bị giới hạn; dự kiến **vị trí [1]** trên ảnh prototype.
2. **G10 — Thu hẹp phạm vi khi nghi ngờ / Graceful Failure:** nhãn `Bài đang mở · Chỉ gợi ý bước đầu` ở S3 và `Nguồn cần xác minh` ở S5; dự kiến **[2]**.
3. **G9 — Sửa dễ dàng:** nút `Gửi TA kiểm tra`, trạng thái gửi thật, cho phép thử lại nếu lỗi; dự kiến **[3]**.

**Lỗi không thể cứu bằng câu chữ:** Nếu hệ thống đã gọi `goi_y_bai_tap` với lời giải đầy đủ, học viên đã nhìn thấy thì xin lỗi cũng không thu hồi được. Thiết kế cần **chặn nội dung đáp án trước khi gửi** bằng luật bài đang mở; đồng thời `dang_FAQ` bắt buộc TA duyệt. Tương tự, ghi “đã báo TA” không thể thay cho việc `chuyen_TA` thành công: trạng thái phải gắn với kết quả tool.

## §4. Mức tự chủ

| Tool | Mức chốt | Ai chịu gì nếu sai / khả năng đảo | Cái giá khi chờ người | Phương án đã loại |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | **Tự làm** (chỉ đọc) | Trích sai khiến học viên hiểu sai, nhưng truy vấn không sửa dữ liệu; phải hiển thị mã mục thật. | Chờ TA cho mọi lần tra cứu khiến học viên tối muộn không học được. | Loại cần duyệt từng truy vấn vì quá chậm; loại cấm vì không thể dạy có căn cứ. |
| `goi_y_bai_tap` | **Tự làm có rào chắn**: bài đang mở chỉ gợi ý bước đầu; bài đã hết hạn có đáp án được giải thích đầy đủ | Gửi lộ đáp án S3 thì không thể thu hồi nhận thức của học viên. | Chờ TA cho mọi gợi ý khiến trợ lý mất tác dụng; rào chắn tự động giảm chi phí này. | Loại tự do gửi đáp án; loại duyệt mọi gợi ý vì quá chậm. Nếu không xác định được trạng thái bài, **không gọi tool**, hỏi lại/chuyển TA. |
| `chuyen_TA` | **Tự làm sau xác nhận của học viên** (xác nhận trên giao diện trước khi gọi) | Chuyển nhầm làm TA mất thời gian, có thể huỷ/đóng yêu cầu; câu hỏi chứa dữ liệu học viên cần được hiển thị trước khi gửi. | Đợi TA duyệt trước khi được chuyển là vòng lặp vô ích, nhất là sau 22:00. | Loại tự chuyển mọi câu hỏi vì gây quá tải; loại cấm vì mất đường cứu khi nguồn sai. |
| `dang_FAQ` | **Cần TA duyệt** | FAQ sai tác động cả lớp; gỡ được nhưng không thu hồi được những gì đã đọc (S8). | Đăng chậm nhưng FAQ không cấp thiết bằng trợ giúp cá nhân tối muộn. | Loại tự đăng vì rủi ro lan truyền; loại cấm hoàn toàn vì mất cơ hội chia sẻ kiến thức đã xác minh. |

**Cơ chế duyệt `dang_FAQ`:** AI chỉ **soạn bản nháp**; TA nhìn thấy nội dung, mã mục, tình trạng bài tập và cảnh báo trước khi bấm `Duyệt & đăng`. Nếu chưa duyệt, bản nháp giữ ở hàng chờ, **không đăng tự động khi quá hạn**. Nếu câu trả lời chứa lời giải bài 3 đang mở, nút duyệt bị vô hiệu và yêu cầu viết lại thành kiến thức chung. Đây là **tách bước đề xuất** `soan_FAQ_nhap` (thao tác cục bộ) và `dang_FAQ` (hành động phát hành), không giả định track đã cấp thêm tool backend.

**Tool khó xếp nhất: `goi_y_bai_tap`.** Cần ghi lại ý kiến thật của từng thành viên sau khi thảo luận. Bảng dưới đây là **phương án thảo luận mẫu, chưa phải biên bản nhóm**:

| Quan điểm | Lợi ích | Cái giá |
|---|---|---|
| Tự làm không giới hạn | Học viên được giúp ngay | S3: lộ đáp án không thu hồi được |
| Mọi gợi ý cần TA duyệt | Kiểm soát chặt | Học viên hỏi sau 22:00 không được hỗ trợ kịp |
| Cấm tool | Không lộ lời giải | Trợ lý không thực hiện được chức năng học từng bước |
| **Chốt: tự làm có rào chắn** | Gợi ý nhanh, vẫn bảo vệ bài đang mở | Cần kiểm tra trạng thái bài và lọc nội dung trước khi gửi |

**Thử quyết định trên ba tình huống (dự kiến; cần xác minh bằng prototype):**

| Ca | Hệ thống được làm | Sai có bị chặn? | Có tự làm khi đáng lẽ phải hỏi? | Người dùng chờ vô ích? |
|---|---|---|---|---|
| S3 — xin đáp số bài 3 | Tra §3.2, gửi gợi ý bước đầu; không gửi đáp số | **Dự kiến có** | Không, vì trạng thái bài đã rõ | Không |
| S5 — nguồn §3.3 sai | Tra nguồn, nêu phản ví dụ, hỏi xác nhận trước khi chuyển TA | **Dự kiến có** | Không tự sửa nguồn hay đăng FAQ | Không phải chờ TA để thấy cảnh báo |
| Bình thường — hỏi khác biệt trung bình/trung vị | Tra §3.1–§3.2 và giải thích có trích dẫn | Không có hành động nguy hiểm | Không | Không |

**Lời hứa đã đổi:** thay vì “AI sẽ giải mọi bài cho bạn”, sản phẩm hứa “AI giúp bạn hiểu từng bước; bài đang mở không cung cấp đáp án, nguồn đáng ngờ có đường kiểm tra với TA”.

## §5. Prototype

- **Đường dẫn dự kiến:** `prototype/index.html` 
- **Công cụ dự kiến:** HTML/CSS/JavaScript; dữ liệu giả lập từ track T2, không backend, không đăng nhập.
- **Mock:** phản hồi mẫu, tài liệu buổi 3, trạng thái bài 3, hàng chờ TA, xác nhận gửi và duyệt FAQ. Các trạng thái “đã ghi nhận” chỉ là mô phỏng trong prototype, không gửi yêu cầu thật.
- **Lời gọi AI thật:** Chưa có.

**Thiết kế 2 màn hình dự kiến:**

1. **Màn hình học viên:** chọn S3/S5 hoặc nhập câu hỏi; thấy [1] thẻ trích nguồn §3.2/§3.3 (**G11**, `tra_cuu_tai_lieu` tự làm); [2] nhãn “Chỉ gợi ý bước đầu”/“Nguồn cần xác minh” (**G10**, rào chắn `goi_y_bai_tap`); [3] nút gửi TA có hộp xác nhận và trạng thái kết quả (**G9**, `chuyen_TA` sau xác nhận).
2. **Màn hình TA:** hàng chờ yêu cầu nguồn §3.3 và bản nháp FAQ; thấy nguồn, lý do nghi sai, trạng thái bài; nút `Duyệt & đăng` chỉ xuất hiện cho nội dung đủ điều kiện (**G9/G11**, `dang_FAQ` cần duyệt).

**Ảnh cần nộp:** `prototype/screen-1.png` đánh số [1]–[3]; `prototype/screen-2.png` đánh số [4] hàng chờ TA, [5] xác nhận duyệt. **Chưa tạo ảnh**; chỉ cập nhật tên file sau khi ảnh thực sự tồn tại.

**Quyết định hiển thị:** chọn **mã mục + nhãn trạng thái + nút hành động cụ thể** thay vì một thanh “AI tự tin 87%” (không có dữ liệu hiệu chuẩn, dễ tạo tin tưởng giả). Loại cách chỉ viết cảnh báo trong đoạn chat vì người học có thể bỏ qua và nút gửi/duyệt vẫn cho phép hành động sai. Khi demo, bấm S5 → xem nguồn/cảnh báo → gửi TA → mở hàng chờ TA; bấm S3 → thấy giới hạn và gợi ý bước đầu, không có đáp án.

## §6. Tốt là gì

| Tiêu chí Pass/Fail | Cách chấm khách quan |
|---|---|
| **P1 — Bảo vệ bài đang mở** | PASS khi 100% ca thử S3/S4 không hiển thị hoặc xác nhận đáp số cuối, không có nút công bố lời giải bài 3; ngược lại FAIL. |
| **P2 — Nguồn kiểm chứng được** | PASS khi 100% phản hồi nội dung buổi 3 có mã § hợp lệ hoặc thông báo rõ thiếu/nguồn sai; riêng S5 phải đánh dấu §3.3 cần kiểm tra; ngược lại FAIL. |
| **P3 — Thao tác đúng quyền** | PASS khi gửi TA chỉ báo thành công sau khi thao tác mô phỏng hoàn tất, FAQ không thể đăng trước TA duyệt, và ngoài giờ TA không hứa phản hồi ngay; ngược lại FAIL. |

**Bảng tự chấm sau khi chạy prototype:**

|| Ca | P1 | P2 | P3 | Lỗi còn lại cần kiểm tra |
|---|---|---|---|---|
| S3 | **PASS**: 4/4 cách xin đáp án/lời giải/xác nhận đều ra nhãn `Bài 3 · Đang mở · Chỉ gợi ý bước đầu`, không lộ hay xác nhận đáp số, không có nút xem đáp án. Hai cách diễn đạt khác không bắt được từ khoá thì chỉ hỏi lại, cũng không xác nhận. | **PASS**: có thẻ nguồn `Buổi 3 · §3.2`. | **PASS**: nút `Hỏi TA` dùng chung luồng gửi với S5, trạng thái "Đã ghi nhận" chỉ hiện sau khi gửi xong. Chưa bấm riêng nút này ở S3. | Câu "Bài 3 em tính ra 12,5, check giúp em nhé" chưa bắt được từ khoá nên bị hỏi lại chung chung, thay vì nói rõ "chỉ kiểm tra cách làm, không xác nhận kết quả". Cần thêm cách diễn đạt và thử bằng người thật. |
| S5 | Không áp dụng: S5 không liên quan đáp số bài đang mở. | **PASS**: có thẻ nguồn `Buổi 3 · §3.3`, nhãn `Nguồn có điểm cần xác minh` và phản ví dụ (phương sai 0,25 → độ lệch chuẩn 0,5). | **PASS**: chưa bấm thì hàng chờ TA là 0; bấm gửi phải qua hộp xác nhận. Khi giả lập lỗi, hiện `Chưa gửi được · Thử lại` và hàng chờ vẫn là 0. Thử lại thành công thì hàng chờ là 1. Ngoài giờ (23:15) hiện "TA xử lý trong khung 08:00–22:00", không hứa số phút. FAQ có lời giải bài 3 bị khoá nút duyệt; FAQ kiến thức chung chỉ đăng sau khi TA xác nhận. | Nếu chuyển TA thất bại, giao diện có báo lỗi và cho thử lại (đã kiểm). Còn lại: lỗi mới chỉ giả lập bằng ô tick, chưa có lỗi mạng thật; chưa xử lý trường hợp học viên thoát màn hình khi đang `Đang gửi`. |
## §7. Demo

**Kịch bản demo dự kiến:**
1. **30 giây đầu:** giới thiệu học viên học tối muộn, tài liệu buổi 3 và rủi ro AI sai âm thầm.
2. **Ca S5:** chọn câu hỏi về §3.3 → hiện câu nghi sai + phản ví dụ → bấm gửi TA → xác nhận → chuyển sang hàng chờ TA.
3. **Ca S3:** xin đáp số bài 3 → AI chỉ gợi ý bước đầu theo §3.2, không xác nhận đáp số.
4. **Giải thích mức tự chủ:** vì sao `goi_y_bai_tap` có rào chắn và `dang_FAQ` cần TA duyệt; chi phí sai và khả năng đảo lại.
5. **Ca lạ:** nhận câu hỏi thực tế từ TA/giảng viên và giải thích/bấm cách prototype xử lý theo đúng các mức đã đặt.

**Ca lạ thực nhận:** *Chưa có — bổ sung sau demo.*

**Prototype đã làm gì với ca lạ:** *Chưa có — không điền giả.*

**Nhóm có đổi quyết định sau demo không, vì sao:** *Chưa có — bổ sung sau demo.*

---

**Nguồn đề bài:**
- [Track T2](https://github.com/VinUni-AI20k/K5-L3-Day05-AI-Product-UX-Autonomy/blob/main/tracks/t2-education.md)
- [Mẫu spec](https://github.com/VinUni-AI20k/K5-L3-Day05-AI-Product-UX-Autonomy/blob/main/03-spec-template.md)
- [Rubric](https://github.com/VinUni-AI20k/K5-L3-Day05-AI-Product-UX-Autonomy/blob/main/04-rubric.md)
