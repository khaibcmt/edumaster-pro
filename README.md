# EduMaster Pro — 10 trong 1 (bản v3 — online + thời gian thực)

Nền tảng web giáo dục tổng hợp dành cho **GV Hồ Tấn Khải** — Sinh học & Công nghệ nông nghiệp — Trường THPT Mang Thít.

## Cách mở

Chỉ cần **double-click vào file `index.html`** là dùng được ngay trong trình duyệt. Toàn bộ CSS/JS nằm trong 1 file duy nhất — mở offline vẫn chạy đầy đủ các module cơ bản. Riêng **Phòng thi trực tuyến** (Module Game) cần có mạng: Firebase SDK và thư viện QR được nạp từ CDN chỉ khi dùng tính năng online, và cần Firebase config của chính người dùng (xem mục bên dưới). Khi đưa lên GitHub Pages cũng chỉ cần file này.

## 10 module + Trang chủ, Kho lưu trữ, Cài đặt

- **Trang chủ / Tổng quan:** lưới thẻ 10+ module, bấm để chuyển nhanh.
- **1. Tạo KHBD 5512:** nhập môn/lớp/tên bài/số tiết/mã NLS/chủ đề AI → sinh khung KHBD (3 dòng tiêu đề, I. Mục tiêu, II. Thiết bị, III. Tiến trình 4 hoạt động × 4 bước, Phụ lục) — có Sao chép và Tải .txt.
- **2. Ma trận đề:** nhập số câu theo 3 mức độ × 4 phần (Phần I 0,25đ / Phần II 1,0đ / Phần III 0,5đ mỗi câu; **Phần IV — Tự luận** có ô điểm mỗi câu riêng, mặc định 1,0đ, chỉnh 0,25–3đ), tự tính tổng câu + tổng điểm (tính cả Phần IV), cảnh báo khi khác 10 điểm.
- **3. Ngân hàng câu hỏi:** 16 câu trắc nghiệm Sinh học 10 sẵn có (Tế bào; Nguyên tố hoá học và nước; Phân tử sinh học; Hô hấp tế bào), lọc theo bài.
- **4. Trộn đề (tronde mini):** hai chế độ. (a) *Dán văn bản:* dán đề theo định dạng "Câu n. / A.–D. / Đáp án: X" (có sẵn đề mẫu 4 câu), xáo trộn câu + phương án bằng Fisher–Yates, xuất đề đã trộn kèm bảng đáp án dạng văn bản, sao chép hoặc **tải file .docx**. (b) *File Word (.docx):* nạp thẳng file đề Word — trộn ngay trên cấu trúc XML của tài liệu nên **hình ảnh và công thức (OMML) giữ nguyên vẹn**; nhận diện câu bắt đầu "Câu n."/"Câu n:"/"Câu n)", phương án A.–D. (hoặc A)–D)), đáp án "Đáp án: X"/"Đáp án X"/"Đ/A: X", và câu Đúng/Sai 4 ý a)–d) có ghi "(Đúng)"/"(Sai)" hoặc "— Đúng"/"— Sai" từng ý. Câu không đọc được đáp án sẽ **báo rõ và giữ nguyên vị trí, tuyệt đối không đoán đáp án**. Tạo 1–8 mã đề độc lập; trước khi tải phải xem **bảng đối chiếu đáp án** (câu mới → đáp án đúng mới → trích đoạn nội dung phương án đúng) và bấm xác nhận; file tải về đóng gói lại từ chính gói gốc (chỉ thay nội dung đã trộn, bỏ mọi dòng "Đáp án:"). Chế độ Word cần tải thư viện JSZip từ CDN khi dùng lần đầu.
- **5. Ôn tập trắc nghiệm:** học sinh chọn bài hoặc tất cả, làm từng câu, phản hồi đúng/sai ngay, tổng kết điểm cuối bài.
- **6. Game Rung chuông vàng:** game thi đấu kiểu game show quốc tế — 2 chế độ: **Chơi 1 người** và **Phòng thi trực tuyến** (cả lớp cùng thi, đồng bộ thời gian thực qua Firebase). Luật chơi đầy đủ ở mục "Luật chơi game" bên dưới.
- **7. Phiếu học tập:** trang thông tin kho 465 file phiếu (155 bài × 3 bản: Học sinh / Học sinh có đáp án / Giáo viên) của 6 bộ sách.
- **8. Tạo slide:** nhập tên bài + các mục (mỗi dòng 1 mục) → xem trước dàn ý (slide tiêu đề + từng mục + slide tổng kết) và **tải file PowerPoint .pptx thật**: slide bìa nền màu + tiêu đề lớn, slide mục tiêu, mỗi mục một slide (tiêu đề trên dải màu + gạch đầu dòng), slide "Cảm ơn thầy cô và các em"; font Arial, cỡ chữ tự giảm khi nội dung dài để chống tràn. Tính năng tải .pptx cần tải thư viện PptxGenJS từ CDN khi dùng lần đầu.
- **9. Sổ điểm:** bảng điểm (miệng, 15 phút, 1 tiết), tự tính ĐTB = (miệng + 15p + 1 tiết × 2)/4, xếp loại Giỏi/Khá/Trung bình/Yếu và tổng kết theo loại.
- **10. Thư viện tài liệu:** giới thiệu kho 227 KHBD, 465 phiếu học tập, ma trận & rubric, tài liệu tham chiếu.
- **11. Kho lưu trữ:** kho cục bộ chạy thật (lưu/tải lại/xoá bản nháp KHBD và ngân hàng câu hỏi trong localStorage) + khung kết nối Google Drive (thư mục gốc "EduMaster Pro") sẵn sàng nối Drive thật ở giai đoạn sau.
- **12. Cài đặt:** người dùng **tự nhập** Gemini API key (lưu localStorage, key `edumaster_gemini_key`), Google OAuth Client ID (key `edumaster_gclient_id`) và **Firebase config** cho phòng thi trực tuyến (key `edumaster_firebase_config`).

## Phòng thi trực tuyến (online, thời gian thực)

### Cách tạo project Firebase miễn phí và lấy config

1. Mở **console.firebase.google.com**, đăng nhập Google → **Add project** → đặt tên (ví dụ `edumaster`) → Create project.
2. Trong project: **Build → Realtime Database → Create Database** → chọn **Start in test mode**.
3. Bấm ⚙️ → **Project settings** → mục **Your apps** → chọn biểu tượng Web **&lt;/&gt;** → đặt tên app → Register app.
4. Sao chép đoạn **firebaseConfig** được hiển thị.
5. Mở EduMaster Pro → mục **Cài đặt** → dán vào ô **Firebase config (JSON)** → **Lưu**. Xong — config chỉ nằm trong trình duyệt của người dùng, mã nguồn web không chứa bất kỳ thông tin kết nối nào.

### Cách tạo phòng thi và cho học sinh vào phòng

1. Giáo viên vào **Module 6 → tab Phòng thi trực tuyến**, chỉnh **Panel Luật chơi** (luật sẽ đồng bộ xuống máy học sinh theo thời gian thực), bấm **Tạo phòng thi**.
2. Màn hình chờ hiện **mã QR thật to** + mã phòng 6 ký tự + link tham gia dạng `?room=MÃ`. Học sinh quét QR bằng điện thoại (hoặc mở link / nhập mã phòng trong Module Game), nhập tên → vào phòng. Danh sách học sinh đã vào hiện trực tiếp trên màn hình giáo viên.
3. Giáo viên bấm **Bắt đầu thi**: màn hình giáo viên hiện câu hỏi **chữ lớn** (hợp chiếu lên TV/màn hình lớp) cùng lúc với màn hình học sinh, kèm đồng hồ đếm ngược, số học sinh đã trả lời và **bảng xếp hạng trực tiếp**. Giáo viên bấm **Câu tiếp theo** để phát câu mới, **Mở câu hồi sinh** để mở đợt hồi sinh, **Kết thúc phòng** để chốt ván và vinh danh Top 3 (có pháo giấy).
4. Màn hình giáo viên còn có **Nhật ký ván đấu** (ghi lại cược điểm lớn, dùng kỹ năng, trộm điểm, hạ gục, hồi sinh, cứu trợ...) và **Danh sách bị loại** với nút **Cứu trợ** từng em / **Cứu trợ tất cả**.
5. Học sinh trả lời trên điện thoại bằng 4 nút đáp án lớn; sau khi trả lời sẽ thấy trạng thái chờ, điểm và thứ hạng của mình; cuối buổi thấy bảng xếp hạng chung cuộc.

> Lưu ý: mỗi thiết bị mở web (kể cả điện thoại học sinh) cần có Firebase config trong mục Cài đặt của trình duyệt đó mới kết nối được phòng — đây là hệ quả của nguyên tắc "không nhúng sẵn config vào mã nguồn" để tránh lộ thông tin kết nối.

## Luật chơi game (áp dụng cả 2 chế độ)

- **Điểm khởi đầu:** 100 điểm. Mỗi câu đúng cơ bản **+100 điểm** (câu Thách đố: 300 điểm), cộng thêm mức cược nếu có và thưởng chuỗi.
- **Trộn đáp án:** thứ tự 4 phương án được xáo trộn cho từng người chơi — trong phòng thi, **mỗi học sinh nhận một thứ tự khác nhau** (theo mã riêng của từng em), đáp án đúng tính theo nội dung, không theo vị trí.
- **Cược điểm:** chọn mức cược 10/20/50 điểm hoặc 25%/50% số điểm đang có, theo từng câu hoặc theo vòng (5 câu) — giáo viên chọn trong Panel Luật chơi. Đúng được cộng thêm mức cược.
- **Trừ điểm khi sai:** giáo viên bật/tắt được; mức trừ mặc định **50% giá trị câu** hoặc **trừ theo mức cược**.
- **Quyền trợ giúp (kiểu Ai là triệu phú):** **50:50** (ẩn 2 đáp án sai), **Đổi câu hỏi**, **Hỏi khán giả** (hiện % bình chọn mô phỏng, có trọng số nghiêng về đáp án đúng). **Mỗi người chơi chỉ dùng mỗi quyền đúng 1 lần trong cả ván** — dùng xong nút mờ đi kèm nhãn "Đã dùng"; số lượt đồng bộ thời gian thực trong phòng thi.
- **Chuỗi đúng liên tiếp (streak):** thưởng thêm tăng dần +10, +20, +30... theo độ dài chuỗi; sai là mất chuỗi.
- **Vòng Tăng tốc:** câu 4–6 nhân đôi điểm thưởng (x2) nếu được bật.
- **Câu Thách đố:** câu khó 300 điểm ở cuối ván; chỉ người chơi có điểm tối thiểu (giáo viên đặt, mặc định 200) mới được chơi.
- **🔮 Gương thần kỳ (kỹ năng đặc biệt):** trả lời **đúng liên tiếp 5 câu** (giáo viên chỉnh được) sẽ mở khoá Gương. Dùng Gương để **ăn trộm điểm của người đang Top 1**: trộm **100 điểm hoặc 10% điểm của Top 1 — lấy số nhỏ hơn**, đồng thời nhận **thưởng +50 điểm**. Gương dùng 1 lần cho mỗi lần mở khoá (đạt chuỗi lần nữa thì mở lại); nếu chính mình đang Top 1 thì Gương tạm khoá. Trong phòng thi, sự kiện dùng Gương được **phát thông báo lớn** lên màn hình giáo viên và mọi học sinh, bảng xếp hạng cập nhật ngay.
- **💀 Hạ gục (KILL):** điểm tụt xuống **0** (do trừ điểm, cược thua hoặc bị Gương ăn trộm) → bị hạ gục, tạm rời ván, bảng xếp hạng hiện 💀. Nếu cú về 0 do Gương của người khác gây ra → đó là một cú **KILL**: người ra tay nhận thêm **thưởng kill +100 điểm** và hệ thống phát thông báo lớn "⚔️ [A] đã HẠ GỤC [B] bằng Gương thần kỳ!".
- **🌟 Hồi sinh (tự cứu bằng câu hỏi):** sau mỗi vòng (5 câu) hoặc khi giáo viên bấm **Mở câu hồi sinh**, tất cả người chơi đang bị hạ gục/loại cùng nhận 1 câu hỏi hồi sinh: trả lời **đúng → hồi sinh** với điểm khởi động lại (mặc định 100) kèm thông báo "🌟 [Tên] đã HỒI SINH!"; sai → chờ đợt sau. Tối đa **2 lần hồi sinh/ván** (giáo viên chỉnh 0–3).
- **☠️ Loại vì sai liên tiếp:** đếm số câu sai liên tiếp của từng người (đúng 1 câu là đếm lại từ 0). Sai liên tiếp đủ **3 câu** (giáo viên chỉnh được hoặc tắt) → **bị loại ngay**, bảng xếp hạng hiện ☠️ kèm lý do "Sai 3 câu liên tiếp", có thông báo lớn. Đây là đường bị loại thứ hai, độc lập với điểm về 0.
- **🆘 Cứu trợ của giáo viên (khác với Hồi sinh):** trên màn hình giáo viên, mỗi học sinh bị loại/hạ gục có nút **Cứu trợ** riêng + nút **Cứu trợ tất cả**. Bấm là em đó quay lại ván **ngay, không cần trả lời câu hỏi**, với điểm cứu trợ do giáo viên đặt (mặc định 100) và bộ đếm sai liên tiếp về 0; có thông báo "🆘 Thầy/cô đã cứu trợ [Tên] quay lại ván đấu!". Quyền cứu trợ thuộc về giáo viên tuyệt đối, **không giới hạn số lần**. — *Hồi sinh là học sinh tự cứu mình bằng câu hỏi; Cứu trợ là giáo viên ra tay. Cả hai cùng tồn tại.*
- **🏅 Phần thưởng & huy hiệu:** theo mốc điểm — 🥉 **Đồng ≥ 300**, 🥈 **Bạc ≥ 500**, 🥇 **Vàng ≥ 1000**, 💎 **Kim cương ≥ 2000** — hiển thị ngay trên bảng xếp hạng. Cuối ván có màn hình **vinh danh Top 3** với hiệu ứng **pháo giấy (confetti)**.
- **Panel Luật chơi:** trước khi bắt đầu, giáo viên bật/tắt và chỉnh thông số tất cả luật trên (cược, trừ điểm, trợ giúp, tăng tốc, chuỗi, thách đố, Gương thần kỳ + số câu streak mở Gương, hạ gục/hồi sinh, loại vì sai liên tiếp, điểm cứu trợ, thời gian mỗi câu). Trong phòng thi, luật được đồng bộ xuống học sinh theo thời gian thực.

## Bảo mật API key (quan trọng)

- Web **không nhúng sẵn bất kỳ API key hay thông tin đăng nhập nào** trong mã nguồn.
- Key do từng người dùng tự nhập trong mục Cài đặt, chỉ lưu trong **trình duyệt của chính người đó** (localStorage), có nút Hiện/Ẩn và Xoá.
- Các module AI đọc key qua hàm dùng chung `getApiKey()`; nếu chưa có key sẽ hiện thông báo hướng dẫn vào Cài đặt. Khung kiểm tra key đã sẵn sàng — chưa gọi API thật.
- **Firebase config cũng theo cùng nguyên tắc:** không nhúng sẵn trong mã nguồn; người dùng tự dán config của project Firebase của mình trong mục Cài đặt (lưu localStorage, key `edumaster_firebase_config`). Chưa có config thì Phòng thi trực tuyến hiện hướng dẫn từng bước, các module offline vẫn chạy bình thường.

## Hệ màu chuẩn (áp dụng từ bản V4)

Nguyên tắc: **mỗi chức năng một màu riêng đặc trưng, xuyên suốt từ đầu đến cuối section của nó** — nút điều hướng đang chọn, thẻ Trang chủ, tiêu đề + gạch chân, nút chính, đầu bảng, viền trên thẻ con, badge, viền focus ô nhập, khối kết quả và các điểm nhấn đều dùng đúng màu của module đó, không lẫn màu giữa các module. Mọi tông màu thuộc cùng một "gia đình" độ bão hoà/độ sáng (chính ≈ tông 600, nhạt ≈ tông 400, đậm ≈ tông 800) để đứng cạnh nhau vẫn hài hoà. Mỗi section khai báo 3 biến `--mc` (chính) / `--mc2` (nhạt-sáng) / `--mcd` (đậm):

| Module | Màu đặc trưng | --mc | --mc2 | --mcd |
|---|---|---|---|---|
| Trang chủ | Tím thương hiệu | #6a11cb | #2575fc | #3a1c96 |
| 1. Tạo KHBD | Violet | #7c3aed | #a855f7 | #5b21b6 |
| 2. Ma trận đề | Xanh dương | #1d4ed8 | #0ea5e9 | #1e3a8a |
| 3. Ngân hàng câu hỏi | Xanh lá | #15803d | #22c55e | #14532d |
| 4. Trộn đề | Cam | #ea580c | #f59e0b | #9a3412 |
| 5. Ôn tập trắc nghiệm | Hồng | #db2777 | #f472b6 | #9d174d |
| 6. Game Rung chuông vàng | Đỏ | #dc2626 | #f59e0b (*) | #b91c1c |
| 7. Phiếu học tập | Ngọc teal | #0e7490 | #14b8a6 | #155e75 |
| 8. Tạo slide | Vàng amber | #d97706 | #fbbf24 | #92400e |
| 9. Sổ điểm | Xanh mint | #047857 | #10b981 | #064e3b |
| 10. Thư viện tài liệu | Nâu vàng | #92400e | #ca8a04 | #78350f |
| 11. Kho lưu trữ | Chàm indigo | #4f46e5 | #818cf8 | #312e81 |
| 12. Cài đặt | Xám slate | #475569 | #94a3b8 | #1e293b |
| 13. Hướng dẫn sử dụng | Xanh sky | #0284c7 | #38bdf8 | #075985 |

(*) Riêng Game: `--mc2` là vàng hổ phách — điểm nhấn "game show"; **4 nút đáp án giữ 4 màu theo vị trí kiểu Kahoot** (đỏ ▲ / xanh dương ◆ / vàng ● / xanh lá ■), không phải màu module.

**Ngoại lệ có chủ đích (giữ nguyên, không chuẩn hoá về màu module):**
- Màu ngữ nghĩa toàn trang: đúng = xanh lá, sai = đỏ, cảnh báo = vàng (ô báo lỗi, huy hiệu trạng thái...).
- Nhận diện thương hiệu tím: logo, khung thông tin giáo viên, thanh topbar đầu trang, nút/hộp thoại nhập key nhanh.
- Riêng Slide (vàng amber): chữ trắng trên các nền vàng chỉ đặt trên tông đậm (#b45309 trở xuống) ở nút chính và đầu bảng để dễ đọc.

**Nút nhập key nhanh (V4):** nút **"🔑 Nhập key Gemini"** luôn hiển thị ở thanh bên (dưới khung thông tin giáo viên) và ở đầu Trang chủ. Chưa có key thì nút hiện nhãn "Chưa có key" kèm viền sáng nhắc nhở; đã có key thì nhãn hiện "🔑 Key Gemini (N)". Bấm nút mở hộp thoại dán nhiều key (mỗi dòng 1 key, nạp sẵn key đã lưu) — lưu vào **đúng cùng kho** `localStorage 'edumaster_gemini_keys'` với mục Cài đặt (cùng khử trùng lặp, cùng xoay vòng), đồng bộ ngược lại ô nhập và trạng thái trong Cài đặt; không tạo kho key thứ hai.

## Giao diện (bản "lung linh, nhiều màu sắc")

- **Hiệu ứng:** nền pastel thuộc gia đình tím–xanh chuyển động chậm; thanh topbar đầu trang gradient tím thương hiệu kèm vệt sáng quét; sidebar gradient chuyển động + hộp thông tin giáo viên kính mờ (glassmorphism); thẻ kính mờ, bo tròn mềm, nhấc lên và phát sáng đúng màu module khi di chuột.
- **Màn hình Game kiểu game show:** 4 nút đáp án 4 màu Kahoot (đỏ ▲ / xanh dương ◆ / vàng ● / xanh lá ■), thanh đếm ngược chảy màu cầu vồng phát sáng, đồng hồ chữ gradient cam–đỏ đập nhịp, bảng xếp hạng có huy hiệu Vàng/Bạc/Đồng cho Top 1-2-3, bục vinh danh vàng–bạc–đồng, banner thông báo sự kiện (Gương thần kỳ, kill, hồi sinh, cứu trợ) cầu vồng nảy bật. Có hỗ trợ `prefers-reduced-motion` cho người dùng muốn tắt chuyển động.

## Mới trong bản v3

- **Parser đáp án đa kiểu + Bảng kiểm tra trực quan** (Module Trộn đề — chế độ dán văn bản, và nút "Nhập nhiều câu" mới trong Ngân hàng câu hỏi): tự nhận đáp án đúng theo 4 kiểu ghi — dòng "Đáp án: X"; dấu *** trước phương án đúng (***B. ... hoặc B. ***...); phương án đúng bọc trong [ ] ([B]. ...); bảng đáp án ở cuối văn bản ("1B 2A 3C 4D" sau dòng "Đáp án:", hoặc từng dòng "Câu 1: B"). Sau khi phân tích luôn hiện **bảng kiểm tra trực quan**: bấm vào phương án bất kỳ để đặt lại đáp án đúng; câu chưa có đáp án được viền đỏ gắn nhãn "Chưa có đáp án" và không cho trộn/dùng cho tới khi xử lý (hoặc bỏ chọn câu đó).
- **Thang điểm chuẩn Bộ có sẵn** (Module Ma trận đề): nút **Chuẩn 7991** (Phần I 12 câu × 0,25đ = 3đ; Phần II 4 câu Đúng/Sai tối đa 1,0đ/câu theo luỹ tiến 0,10/0,25/0,50/1,00 = 4đ; Phần III 6 câu × 0,5đ = 3đ; tổng đúng 10đ) và nút **Mẫu 24 câu (10 điểm)** (I: 16 câu 4đ; II: 4 câu 4đ; III: 4 câu 2đ). Module Ôn tập hiển thị ghi chú thang điểm này ở phần tổng kết.
- **Cài đặt đa key + chọn mô hình** (khung chuẩn bị cho đợt nối AI): dán nhiều Gemini key (mỗi dòng 1 key), hệ thống xoay vòng round-robin khi lấy key; key đơn cũ được tự gộp vào danh sách; chọn mô hình mặc định Nhanh nhất — Flash-Lite / Cân bằng — Flash / Chuyên sâu — Pro. Trạng thái hiện "Đang có N key sẵn sàng". *Chưa gọi API thật trong bản này.*
- **Slide thân thiện lớp học** (Module Tạo slide): nút chỉnh cỡ chữ A−/A+ (áp cho xem trước, trình chiếu và file .pptx); chế độ **Trình chiếu** toàn màn hình (phím ⬅️/➡️/Cách chuyển slide, Esc thoát); dòng "Đáp án: ..." sau một mục sẽ thành đáp án của slide đó — khi trình chiếu có nút Hiện/Ẩn đáp án; thêm công cụ **Quay số học sinh 1–50** và **Hẹn giờ thảo luận** (hết giờ nhấp nháy đỏ).
- **Game — mã phòng cố định + 2 chế độ mới** (giữ nguyên mọi luật v2): giáo viên đặt 1 mã phòng cố định dùng cho mọi buổi (QR/link không đổi), có nút **Dọn phòng** xoá ván cũ. Chế độ **Kéo co**: 2 đội Đỏ/Xanh, trả lời đúng kéo dây theo điểm câu, chạm 500 điểm kéo là thắng (phòng thi: chia đội cân bằng theo thứ tự vào phòng; 1 người: đấu với máy, chọn độ khó). Chế độ **Diệt Boss**: Boss có HP do giáo viên đặt (mặc định 1000), trả lời đúng gây sát thương = điểm câu, mỗi người chơi có 3 tim — sai mất 1 tim, hết tim thành khán giả cổ vũ; hạ Boss thì vinh danh Top Dũng Sĩ theo sát thương. Điểm cá nhân, cược, kỹ năng, Gương thần kỳ vẫn tính song song trong cả 2 chế độ mới.
- **Key sao lưu đa máy** (Module Kho lưu trữ): đóng gói kho lưu trữ + ngân hàng câu hỏi + sổ điểm + luật chơi game thành 1 đoạn mã văn bản để mang sang máy khác; khôi phục có bước xem tóm tắt rồi mới ghi đè. **Key sao lưu không bao giờ chứa API key / Client ID / Firebase config.**

## Sửa lỗi & bổ sung sau kiểm thử trực tiếp (đợt L1–L7)

- **L1 — Parser nhận thêm dãy đáp án đứng riêng ở cuối:** dãy "1A 2C 3B" (và biến thể "1.A 2.B", "1-A 2-B") ở cuối văn bản nay được nhận làm bảng đáp án **kể cả khi không có dòng "Đáp án:" đứng trước** (trước đây dãy này bị dính vào phương án D của câu cuối). Parser chỉ áp dụng khi cả dòng khớp mẫu nghiêm ngặt, đứng sau câu cuối và số cặp không vượt số câu — tránh nhận nhầm nội dung thường. Kiểm thử: bộ test parser mở rộng đạt **36/36** (gồm ca dãy riêng 3/3 đúng, phương án D câu cuối sạch, và 2 ca chống nhận nhầm).
- **L2 — Điểm trung bình Sổ điểm:** giữ nguyên làm tròn **1 chữ số thập phân** theo quy chế (quyết định của thầy Khải, không đổi).
- **L3 — Tiêu đề trạng thái cập nhật ngay:** điểm "Điểm đúng hiện tại" của Ôn tập, thanh Boss (HP + tổng sát thương) và hàng tim trong Diệt Boss (cả chế độ 1 người và phòng thi) nay cập nhật **ngay khi trả lời**, khớp với phản hồi dưới câu hỏi thay vì chậm một nhịp tới câu sau.
- **L4 — Đổi tên preset Ma trận:** "Gọn 10 câu" → **"Mẫu 24 câu (10 điểm)"** ở mọi nơi hiển thị.
- **L5 — Xem trước slide:** chuỗi đáp án trong khung xem trước chuẩn hoá thành "Đáp án: ..." (dấu cách rõ ràng sau dấu hai chấm).
- **L6 — Toast khi sao chép:** mọi nút Sao chép (khung KHBD, key sao lưu, link phòng...) nay hiện thông báo nhỏ "✅ Đã sao chép" tự ẩn sau ~1,5 giây; sao chép thất bại sẽ báo để copy thủ công, thay cho hộp thoại alert cũ.
- **L7 — Ma trận đề thêm Phần IV — Tự luận:** hàng mới đủ 3 cột mức độ + ô điểm mỗi câu riêng (mặc định 1,0đ, 0,25–3đ); tổng câu/tổng điểm và hộp Đạt chuẩn tính cả Phần IV; hai preset giữ nguyên cấu hình 3 phần và đặt Phần IV = 0 câu, kèm ghi chú "chưa gồm Tự luận". Kiểm thử logic bằng harness riêng đạt **15/15** (kịch bản I=8, II=4, III=4, IV=2×1,0đ → tổng đúng 10đ, Đạt chuẩn; IV 1 câu × 2đ cộng đúng 2đ).

## Kỹ thuật

- HTML/CSS/JavaScript thuần (vanilla), 1 file duy nhất, font hệ thống (Segoe UI/Arial), giao diện sidebar + thẻ bo góc, mỗi module một màu gradient riêng (xem mục Giao diện), responsive cơ bản.
- Dữ liệu (cài đặt, kho lưu trữ) lưu bằng localStorage của trình duyệt — xoá dữ liệu duyệt web sẽ mất các mục đã lưu trong kho cục bộ.
- Phòng thi trực tuyến dùng **Firebase Realtime Database** (cấu trúc `rooms/{code}/...`: meta/luật chơi, questions, players, current, answers, revive, events) với SDK nạp từ CDN gstatic chỉ khi cần; mã QR tham gia phòng sinh tại client bằng thư viện QR nạp từ CDN khi ở chế độ online.
