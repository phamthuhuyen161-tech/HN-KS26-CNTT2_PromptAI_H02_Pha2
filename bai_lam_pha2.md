# BÀI LÀM PHA 2 

- **Họ tên:**
- **Lớp:**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
{
"ma_goi": "SVT",
"ngay_su_kien": "2026-12-20",
"nguoi_lon": 2,
"tre_em": 1,
"loai_ve": "thuong",
"ghi_chu": null
},
{
"ma_goi": "FZ",
"ngay_su_kien": "2027-01-05",
"nguoi_lon": 3,
"tre_em": 0,
"loai_ve": null,
"ghi_chu": "hỗ trợ xe lăn"
},
{
"ma_goi": "VIP",
"ngay_su_kien": null,
"nguoi_lon": 4,
"tre_em": 0,
"loai_ve": "vip",
"ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
}
]
```

**Link trò chuyện:**https://gemini.google.com/app/68df69acd3a6dae4?pli=1

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn
Gói SVT có giá 1.200.000 đồng/người lớn. Nhóm có 5 người lớn:$$5 \times 1.200.000 = 6.000.000\text{ (đồng)
Tiền trẻ em2 trẻ em (8 tuổi và 10 tuổi) nằm trong độ tuổi từ 5 đến 11 tuổi nên tính 70% giá người lớn: $70\% \times 1.200.000 = 840.000\text{ (đồng/trẻ em)}$1 bé 3 tuổi (dưới 5 tuổi) được miễn phí: $0\text{ (đồng)}$
Tổng tiền trẻ em:$$(2 \times 840.000) + 0 = 1.680.000\text{ (đồng)}$$Tiền vé
Tổng tiền vé (tiền người lớn + tiền trẻ em):6.000.000 + 1.680.000 = 7.680.000\text{ (đồng)}$$Giảm giá nhóm
Nhóm có đủ 5 người lớn nên được giảm 5% trên tổng tiền vé:$$5\% \times 7.680.000 = 384.000\text{ (đồng)}$$Phụ thu
Có 1 người lớn chọn khu ghế ưu tiên với mức phụ thu 300.000 đồng/người:$$1 \times 300.000 = 300.000\text{ (đồng)}$$Tổng tiền
Tiền vé sau giảm giá: $7.680.000 - 384.000 = 7.296.000\text{ (đồng)}$
Tổng số tiền khách hàng cần thanh toán (tiền vé sau giảm + phụ thu):$$7.296.000 + 300.000 = 7.596.000\text{ (đồng)}$$[RESULT:7.596.000đồng]
```

**Link trò chuyện:**https://gemini.google.com/app/c16449d9968ea823?pli=1

### b) Kiểm tra kết quả AI

Kết luận:AI tính đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
"loai_su_co": "sai_khu_vuc",
"so_khach": 2,
"so_hiep_bi_anh_huong": 2,
"tom_tat": "Khán giả gói SVT bị xếp khu không mái che, ghế ướt dưới mưa suốt 2 hiệp đầu."
}
```

**Link trò chuyện:**https://gemini.google.com/app/e0d55fc601871e9e?pli=1

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
(Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
Đúng thông tin (50%)	0,5 / 5,0	
Lỗi 1 – Sai giá vé:


• Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."


• Lý do sai: Báo giá 1.000.000đ/người là sai so với thông tin chuẩn của ban tổ chức là 1.200.000 đồng/người lớn.


• Câu sửa đề xuất: "Vé gói Sân Vận Động có giá 1.200.000 đồng/người lớn ạ."



Lỗi 2 – Sai chính sách hoàn/huỷ vé:


• Câu bị lỗi: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."


• Lý do sai: Theo quy định chuẩn, huỷ từ 3 đến 6 ngày trước sự kiện chỉ được hoàn 50%, không phải hoàn tiền đầy đủ (100%).


• Câu sửa đề xuất: "Nếu anh huỷ vé trước trận từ 3 đến 6 ngày, ban tổ chức sẽ hoàn lại 50% giá trị vé ạ."

"Dạ, vé gói Sân Vận Động có giá 1.200.000 đồng/người lớn ạ. Về chính sách huỷ vé: nếu huỷ trước trận từ 7 ngày trở lên sẽ được hoàn 100%, huỷ từ 3 đến 6 ngày hoàn 50%, và dưới 3 ngày sẽ không hoàn tiền ạ."
Đầy đủ (30%)	1,0 / 3,0	
Lỗi 3 – Thiếu lời mời cung cấp thông tin đặt vé:


• Câu bị lỗi: "Anh cần gì cứ nhắn em nhé!" (toàn bộ phản hồi cũng không có lời mời cung cấp ngày trận đấu và số lượng vé).


• Lý do sai: Dù có trả lời giá vé và chính sách huỷ (dù sai thông tin), nhân viên chưa mời khán giả cung cấp ngày trận đấu và số lượng vé để đặt theo yêu cầu của rubric.


• Câu sửa đề xuất: "Để hỗ trợ mình đặt vé trận bán kết, anh/chị vui lòng cho em xin ngày trận đấu và số lượng vé cần đặt nhé ạ."

"Để em hỗ trợ mình đặt vé trận bán kết, anh/chị vui lòng cho em biết ngày trận đấu và số lượng vé mong muốn đặt ạ."
Giọng điệu (20%)	1,0 / 2,0	
Lỗi 4 – Dùng từ ngữ suồng sã, thiếu chuyên nghiệp:


• Câu bị lỗi: "Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ." và "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh. Anh cần gì cứ nhắn em nhé!"


• Lý do sai: Các cách dùng từ như "xem rất đã luôn", "nha anh", "cứ nhắn em nhé" mang sắc thái suồng sã, thân mật quá mức, chưa giữ được sự chuẩn mực và chuyên nghiệp của nhân viên tư vấn.


• Câu sửa đề xuất: "Dạ, gói Sân Vận Động mang đến trải nghiệm theo dõi trận đấu trực tiếp rất sôi động ạ. Nếu anh huỷ vé trước trận từ 3 ngày, mức hoàn tiền áp dụng là 50% ạ. Anh cần hỗ trợ thêm thông tin gì, xin vui lòng phản hồi để em phục vụ ạ."

"Dạ chào anh/chị! Gói Sân Vận Động mang đến trải nghiệm theo dõi trực tiếp rất sôi động ạ. Anh/chị cần hỗ trợ thêm thông tin gì, vui lòng cho em biết để em hỗ trợ mình chu đáo nhất ạ."
Tổng điểm	2,5 / 10	—	—
```

**Link trò chuyện:**https://gemini.google.com/app/8191cb8535cd28a1?pli=1
