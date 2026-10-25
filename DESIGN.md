# DESIGN.md — Landing page studio yoga Thả Lỏng (MSR-42)

> Tài liệu thiết kế chốt cho sprint TEC-318. Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ mô tả task TEC-319 và đối chiếu trực tiếp DESIGN.md của cả 3 project gần nhất trên GitHub (đọc qua raw.githubusercontent.com ngày 2026-10-25):

1. **Thời Khắc** (m-software-thoi-khac, TEC-312) — archetype ghi rõ trong file: **A7 Typography-first**; cặp font: **Noto Serif Display + Be Vietnam Pro**; nhiệt màu: **tối-trung tính** (nền than chì, chữ kem, nhấn vàng đồng).
2. **An Lạc** (m-software-an-lac, TEC-305) — archetype ghi rõ trong file: **A2 Split (chia đôi)**; cặp font: **Lora + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền kem giấy, chữ xanh rừng, nhấn vàng nghệ).
3. **Lửa Ấm** (m-software-lua-am, TEC-297) — archetype ghi rõ trong file: **A5 Theo chương**; cặp font: **Fraunces + Be Vietnam Pro**; nhiệt màu: **tối-ấm** (nền nâu sẫm, chữ kem, nhấn đất nung).

Lựa chọn cho Thả Lỏng (đối chiếu trực tiếp với 3 project trên):

- **Archetype: A3 Lệch tâm (off-center)** — KHÁC A7 của project liền trước (Thời Khắc) và KHÁC A2 của project liền trước nữa (An Lạc), thỏa luật "không dùng lại archetype của 2 project liền trước"; cũng khác A5 của Lửa Ấm và khác A1 Editorial dọc của các project trước đó (Lá Xanh, Tĩnh Trà). Cách lệch tâm thể hiện ở: hero ảnh lệch phải, chữ lệch trái; các khối xen kẽ lệch trục (khối chẵn lệch trái, khối lẻ lệch phải); lưới lớp học 3 cột nhưng thẻ giữa nhô cao hơn 2 thẻ bên.
- **Cặp font: Playfair Display + Be Vietnam Pro** — KHÁC nguyên cặp của project liền trước Thời Khắc (Noto Serif Display + Be Vietnam Pro): font tiêu đề đổi sang Playfair Display; cũng khác Lora + Be Vietnam Pro của An Lạc và Fraunces + Be Vietnam Pro của Lửa Ấm.
- **Nhiệt màu: sáng-ấm** — KHÔNG tạo chuỗi 3 project liên tiếp cùng nhiệt màu: chuỗi gần nhất là Lửa Ấm tối-ấm → An Lạc sáng-ấm → Thời Khắc tối-trung tính (đã đứt quãng), nên Thả Lỏng sáng-ấm chỉ đứng sau 1 project tối-trung tính, không tạo chuỗi 3 sáng-ấm liên tiếp.
- **Điểm nhấn đặc sắc riêng:** "đường thở" — một đường kẻ mảnh màu tím oải hương chạy dọc trục lệch của trang, dài dần qua từng khối như một hơi thở chậm (mô tả cụ thể ở mục 7).
- **Giữ nguyên so với công thức gợi ý trong yêu cầu:** bảng màu (nền #F4F1EA, chữ #2E2A33, nhấn #7C6A9E), cặp font (Playfair Display + Be Vietnam Pro) và không khí (Japandi tối giản, tĩnh lặng) đều giữ nguyên, vì không vi phạm luật chống trùng nào — chỉ mở rộng bảng màu từ 3 mã gợi ý thành 6 mã đủ vai trò (thêm nền khối phụ, chữ phụ, nhấn phụ).

## 1. Tổng quan và phong cách tham chiếu (duy nhất)

- Sản phẩm: landing page 1 trang cho studio yoga nhỏ Thả Lỏng — dành cho người mới bắt đầu và dân văn phòng muốn chậm lại sau giờ làm; lớp hatha nhẹ nhàng, vinyasa buổi sáng, yin thư giãn buổi tối; không gian ấm, yên tĩnh, nhiều cây xanh.
- Phong cách tham chiếu duy nhất: **Japandi tối giản, tĩnh lặng** — ít đồ, nhiều khoảng trống, gỗ sáng + vải lanh + cây xanh; ảnh lớp yoga buổi sáng ngập nắng dịu; chữ serif thanh mảnh, không ồn ào kiểu quảng cáo giảm giá.
- CẤM: template bán hàng (giỏ hàng, nút mua ngay, banner khuyến mãi), icon stock đủ màu, ảnh sáng phẳng ban ngày kiểu sàn thương mại điện tử, lưới thẻ đều tăm tắp không có lệch trục.

## 2. Bảng màu (chỉ dùng đúng 6 mã dưới đây, không dùng màu ngoài bảng)

| Mã | Vai trò |
|---|---|
| `#F4F1EA` | Nền chính toàn trang (kem giấy sáng-ấm) |
| `#E9E2D4` | Nền khối phụ, nền thẻ lớp học, nền form |
| `#2E2A33` | Chữ chính (tiêu đề + nội dung), nền chân trang |
| `#6B6572` | Chữ phụ: mô tả, ghi chú, nhãn nhỏ, placeholder trong form |
| `#7C6A9E` | Nhấn chính (tím oải hương): nút CTA, giá mẫu, đường thở, chấm độ khó |
| `#C9BBA8` | Nhấn phụ (be đất): đường kẻ mảnh ngăn khối, viền thẻ, nền khối ảnh khi ảnh lỗi/chưa tải |

Quy tắc dùng màu:

- Nền sáng chiếm đa số diện tích; chữ chàm tím than trên nền kem phải đọc rõ, không dùng chữ phụ cho đoạn văn chính.
- Tím oải hương chỉ dùng cho điểm nhấn (CTA, giá, đường thở, chấm độ khó), không tô nền cả khối bằng màu nhấn.

## 3. Font chữ

- Tiêu đề: **Playfair Display** (serif cao, thanh mảnh, hỗ trợ tiếng Việt) — cỡ hero 64px desktop / 40px mobile, tiêu đề khối 36px / 28px.
- Nội dung: **Be Vietnam Pro** — cỡ 16px, giãn dòng 1.7, đoạn mô tả ngắn, không viết đoạn dài quá 3 dòng trên desktop.
- Nút CTA: Be Vietnam Pro đậm, chữ hoa nhỏ, không dùng font tiêu đề cho nút.

## 4. Bố cục — Archetype A3 Lệch tâm (off-center)

- Trang là một cột dọc 9 khối, nhưng trục thị giác LỆCH: khối chẵn dồn nội dung sang trái (lề trái 8%, lề phải 20%), khối lẻ dồn sang phải (lề trái 20%, lề phải 8%). Trên mobile (< 768px) mọi khối về một cột thẳng, không lệch.
- Hero: ảnh lớn toàn màn hình (100vh), lệch phải — ảnh chiếm 62% chiều rộng bên phải, khối chữ (tên studio + 1 câu triết lý + nút CTA "Đặt lịch học thử") nằm chồng lên phần trái của ảnh, nền kem mờ sau chữ.
- Lưới lớp học: 3 thẻ trên một hàng, thẻ giữa (vinyasa buổi sáng) nhô cao hơn 2 thẻ bên 32px, tạo nhịp lệch.
- Lịch học theo tuần: bảng 7 cột (thứ 2–Chủ nhật), mỗi ô chỉ tên lớp + giờ, không ảnh; ô lớp yin buổi tối tô nền khối phụ.
- Huấn luyện viên: 3 thẻ ngang, ảnh tròn 1:1 lệch trái, chữ lệch phải trong thẻ.
- Bảng giá: 2 cột (theo tháng / theo buổi), cột theo tháng có viền nhấn chính dày hơn, lệch cao hơn 16px.
- Cảm nhận học viên: 3 trích dẫn, mỗi trích dẫn bắt đầu bằng dấu ngoặc kép lớn màu nhấn, xếp so le (trích dẫn giữa thụt vào 48px).
- Form học thử: 4 trường (họ tên, điện thoại, lớp muốn thử, khung giờ) + nút gửi, CHỈ giao diện (preventDefault, không gửi đi đâu); chỉ ghi nhãn trường và nút, không ghi câu xác nhận gửi thành công hay hứa hẹn liên hệ (tránh hứa hẹn xử lý thật).
- Chân trang: nền chữ chính, chữ kem, 3 cột (tên studio + triết lý ngắn, liên hệ placeholder, giờ mở cửa placeholder).

## 5. Thứ tự các khối (từ trên xuống)

1. Hero (100vh, ảnh lớp yoga buổi sáng ngập nắng, lệch phải).
2. Triết lý chậm rãi (1 đoạn ngắn + 3 từ khóa: Chậm — Thở — Lắng nghe).
3. Các lớp học (3 thẻ: Hatha nhẹ nhàng, Vinyasa buổi sáng, Yin thư giãn buổi tối; mỗi thẻ có mô tả ngắn + độ khó cho người mới bằng 1–3 chấm tím).
4. Lịch học theo tuần (bảng 7 cột).
5. Huấn luyện viên (3 người, tên + dòng giới thiệu ngắn — tên thật để placeholder [CẦN BỔ SUNG] nếu chưa có).
6. Bảng giá mẫu (theo tháng + theo buổi, mọi giá ghi rõ "Giá mẫu").
7. Cảm nhận học viên (3 trích dẫn, tên người nói để placeholder [CẦN BỔ SUNG]).
8. Form đặt lịch học thử (CHỈ giao diện).
9. Chân trang (địa chỉ, điện thoại, giờ mở cửa đều là placeholder [CẦN BỔ SUNG], không bịa số liệu thật).

## 6. Quy tắc ảnh (ảnh mẫu Unsplash, Dev kiểm tra từng ảnh trả HTTP 200 trước khi dùng)

- Tông chung: ánh sáng tự nhiên dịu buổi sáng, tông ấm nhạt, nhiều cây xanh, không gian yên tĩnh; ảnh người tập yoga thật, tư thế rõ ràng, không ảnh studio rực rỡ kiểu quảng cáo phòng gym.
- Tỉ lệ: hero 16:9 (toàn màn hình, cắt vừa 100vh); thẻ lớp học 4:5 dọc; ảnh huấn luyện viên 1:1 vuông (hiển thị tròn); khối triết lý 3:2 ngang; cảm nhận học viên không dùng ảnh.
- Ảnh lỗi/chưa tải: nền khối màu nhấn phụ #C9BBA8, không để vỡ layout.
- Tất cả ảnh đều là ảnh mẫu, không ghi chú thích kiểu "ảnh thật của studio".

## 7. Điểm nhấn đặc sắc riêng — "Đường thở"

- Một đường kẻ mảnh 2px màu nhấn chính #7C6A9E chạy dọc theo trục lệch của trang (bên trái ở khối chẵn, bên phải ở khối lẻ), nối từ cuối hero xuống trước chân trang.
- Độ dài đường kẻ tăng dần qua từng khối như một hơi thở chậm: ở khối triết lý chỉ dài 40px, mỗi khối sau dài thêm 40px, đến khối cảm nhận thì thành đường dài nối liền sang khối form.
- Trên đường thở, tại đầu mỗi khối có một chấm tròn nhỏ màu nhấn (6px) đánh dấu "một nhịp thở".
- Độ khó lớp học cũng dùng cùng ngôn ngữ chấm: 1 chấm = rất nhẹ (hatha), 2 chấm = vừa (vinyasa), 3 chấm = sâu lắng nhưng vẫn cho người mới (yin) — kèm chữ giải thích, không để chấm đứng một mình.
- Không dùng thêm họa tiết trang trí nào khác ngoài đường thở và chấm tròn (giữ đúng tinh thần Japandi: ít mà đủ).

## 8. Responsive

- Breakpoint 768px: mọi khối về một cột thẳng, hero ảnh toàn chiều rộng (chữ nằm dưới ảnh, không chồng lên ảnh), lưới lớp học xếp dọc, thẻ giữa không nhô cao nữa, bảng lịch tuần cuộn ngang.
- Breakpoint 480px: tiêu đề hero 32px, bảng giá xếp dọc, form 1 cột.
- Nút CTA luôn đủ lớn để bấm trên điện thoại (cao tối thiểu 48px).

## 9. Placeholder và ghi chú cho Dev

- Mọi thông tin thật chưa có (địa chỉ, điện thoại, giờ mở cửa, tên huấn luyện viên, tên người cảm nhận) đều để nguyên dạng [CẦN BỔ SUNG], không bịa.
- Mọi giá đều ghi rõ "Giá mẫu" ngay cạnh con số.
- Form học thử CHỈ giao diện: submit thì preventDefault, không fetch, không action, không mailto, không tel:.
- Không giỏ hàng, không thanh toán, không tài khoản, không backend.
