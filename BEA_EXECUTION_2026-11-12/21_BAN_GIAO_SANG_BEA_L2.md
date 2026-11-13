# BÀN GIAO: phiên Claude Code đám mây → phiên bea-l2 trên máy anh Cường

- Ngày bàn giao: 13/11/2026. Người lập: Claude (phiên đám mây, repo cuongnguyen-IEC/IEC, nhánh `ccr-594510c6-l92km9`).
- Người nhận: phiên Claude Code mở trong thư mục `bea-l2` trên máy anh.
- Phiên nhận làm theo CLAUDE.md của bea-l2. Tài liệu này chỉ nêu trạng thái và việc dở dang.

## 1. Lý do bàn giao

Phiên đám mây không đọc được sổ input, sổ việc, check.js trong bea-l2. Các việc cần những thứ đó phải làm ở phiên trên máy.

## 2. Trạng thái tới 12/11/2026, 23:00 giờ VN

| Hạng mục | Trạng thái | Vị trí |
|---|---|---|
| Tab THUC_THI (BEA_DKB_INDEX) | 30 hành động của PRJ-IEC-DIALOGUES (18) và PRJ-IEC-WORKSHOP-ANM (12). 1 Completed, 4 In Progress, 25 chưa xác nhận trạng thái. 24 Owner ghi `PENDING OWNER CONFIRMATION`; 20 hạn chưa phải ngày | `1JDRgM7BusKt908uSfHHkx5A0Wk1UQ-JxRhJ9dhyJaS4`, sheetId 3 |
| HO_SO | Ghi thêm dòng 104–110 ngày 12/11: QD-IEC-DIALOGUES-008 (Đã thống nhất); QĐ-002, QĐ-006 "Đã thay đổi" phần mốc; QD-IEC-DIALOGUES-001 v2 (Đã thống nhất), v1 "Đã thay đổi" | cùng file, tab HO_SO |
| QD-IEC-DIALOGUES-008 | Mọi đơn vị báo ý định trước 16/11, ký và thanh toán trước 25/11/2026; mốc cập nhật theo tiến độ thực | Doc `13HOvGCcnFQp6uiT9jkG8jT15CpNPApxhGkBaw5a-DOk` |
| QD-IEC-DIALOGUES-001 v2 | Bảng giá dùng để tính, không khấu trừ trên giá gói; nếu có thì thương lượng trade-off dịch vụ giá trị tương đương. Cách hiểu "trade-off" chờ anh xác nhận | Doc `1K_SPPktoBxWeolHbsEssgfd9VYic43fQz7_3E-i8Bsc` |
| NHAT_KY | NHAT_KY_2026-11-12_TASK05_execution-mvp; NHAT_KY_2026-11-12_TASK05_phan-hoi-anh | PRJ-GLOBAL/NHAT_KY; Doc `1B_kaKlR0N2FaQ-cZdBRkNLQkzc2W8OrlBkwgL5UUZiM`, `1u3eg7vWElud1KRSUOROhSYtvGa3zizh8ggWW5olVj0c` |
| File 11–21 | Đo cơ sở (xlsx); mẫu báo cáo tuần; ánh xạ Master Plan; kế hoạch pilot; báo cáo TASK 05; Decision Record v2 (nháp); snapshot #1; nhật ký thay đổi; quy trình tuần; phản hồi và cơ chế đề xuất; tài liệu này | GitHub cuongnguyen-IEC/IEC, nhánh `ccr-594510c6-l92km9`, thư mục `BEA_EXECUTION_2026-11-12/` |

Không đổi trong phiên đám mây:

- Master Plan IEC (theo QD-L1-CHUNG-004);
- CLAUDE.md, code, cấu hình, ask.js, check.js, models.json.

## 3. Việc cần làm ở phiên bea-l2 (theo thứ tự)

**Việc 1 — Đối chiếu nguyên văn IN-20261106-0016, 0017, 0018** (chỉ đọc).

- Đọc sổ input, trích nguyên văn ba mục kèm thời điểm.
- So với bản nháp QD-IEC-KE-HOACH-2027-001 v2 do phiên đám mây soạn từ NHAT_KY và concept v2.1. Bản nháp có 3 thay đổi so với v1:
  1. Bỏ nhánh hướng nghiệp THPT; trường THPT giữ trong danh sách inventory (IN-0016).
  2. Gộp mọi hoạt động ở trường đại học thành "IEC Campus" (tên tạm), gồm Talents to Business 3 tầng; bỏ "định hướng lộ trình nghề nghiệp" riêng vì trùng tầng 1 (IN-0017, IN-0018).
  3. Thêm content channel của IEC; thêm inventory: cộng đồng doanh nghiệp khởi nghiệp, quỹ tài chính, người theo dõi content channel (IN-0017, IN-0018).
- Hướng IEC Market Access, sản phẩm, gói Khởi động, điều kiện chỉ tiêu giữ nguyên v1.
- Báo anh: khớp hay khác ở điểm nào.
- Chưa ghi HO_SO cho QĐ này khi anh chưa trả lời câu 1 ở mục 4.

**Việc 2 — Kiểm sổ việc về mã VIEC-20261106-03 và -04.**

- Trên Drive có hai NHAT_KY cùng mang mã VIEC-20261106-03 (concept v2 kế hoạch 2027; khung nội dung Day 1).
- Gap v1.1 (B12) lại dẫn thay đổi IN-0016…0018 từ `viec/VIEC-20261106-04.json`.
- Báo anh mã nào đúng cho việc nào. Không sửa sổ việc khi anh chưa duyệt.

**Việc 3 — Ghi bù việc làm ở phiên đám mây vào bea-l2**, theo cách CLAUDE.md quy định cho việc làm ngoài lớp 2:

- Proposal Kỳ 1 v2.1 (12/11): NHAT_KY_2026-11-12_PROPOSAL-KY1-v2.1 ghi "Khi có máy: chép 4 PDF và nhật ký này vào bea-l2, điền mã VIEC và mã IN của chat 12/11". 4 PDF đang ở KET_QUA của PRJ-IEC-DIALOGUES.
- Hợp đồng Gentech v1, v2 (12/11); MOU ONEAI (11/11, đã có VIEC-20261111-01).
- TASK 04 lần 2, TASK 05 và phản hồi của anh 12/11 (việc về chính BEA). TASK 04 lần 2 chưa có NHAT_KY trên Drive.

**Việc 4 — Chờ anh trả lời 3 câu** (file 20, mục 7):

1. Có áp cơ chế theo dõi việc mới ngay không (mục 5)?
2. "Trade-off dịch vụ giá trị tương đương" nghĩa là (a) IEC bù cho đơn vị bằng dịch vụ khác trong chương trình, hay (b) đơn vị đóng góp dịch vụ cho chương trình thay một phần tiền?
3. Có sửa Bảng giá Kỳ 1 v2.1 (bỏ câu "40 triệu khi không xếp được ghế") thành v2.2 và thêm điều khoản trade-off vào hợp đồng Gentech (v3) không?

**Việc 5 — Báo cáo tuần #1, Thứ Hai 16/11/2026.**

- Theo quy trình ở file 19: tiến độ; trễ hạn; bị chặn; QĐ chưa được thực thi; vấn đề cần CEO/COO xử lý.
- Nếu anh đồng ý câu 1 thì báo theo 3 nhóm, nói bằng lời thường, không dùng mã.
- Không tự lên lịch, không tạo reminder, không gửi email.

## 4. Lời anh đã nói (12/11), cần giữ

- "tôi còn không nắm rõ là việc gì thì duyệt kiểu nào? BEA hoàn toàn không có cơ chế tracking task" → không hỏi anh bằng mã; không hỏi duyệt những gì anh đã nói rõ.
- "đổi mốc quyết định để cập nhật theo tiến độ thực của các task" → đã ghi QĐ-008.
- "price list để tính toán chứ không cho phép khấu trừ trên giá gói. nếu có thì cho phép thương lượng trade off cho những service giá trị tương đương cho chương trình." → đã ghi QĐ-001 v2.

## 5. Cơ chế theo dõi việc đề xuất (chờ anh trả lời câu 1)

1. Cuối mỗi việc, BEA nêu "bước tiếp theo" trong 1–3 dòng (việc gì, ai làm, khi nào); anh trả lời một lần; chỉ tạo dòng THUC_THI từ đó.
2. Ba nhóm:
   - **A** chờ bên ngoài trả lời — hỏi "đã ai trả lời chưa";
   - **B** việc anh hoặc IEC làm — hỏi "xong chưa";
   - **C** việc BEA làm — BEA tự báo.
3. Nói bằng lời thường; mã để trong ngoặc.
4. BEA tự tìm bằng chứng (Drive, Gmail, NHAT_KY) trước khi hỏi.
5. Quyết định anh đã nói rõ thì ghi thẳng thành QĐ "Đã thống nhất" kèm nguyên văn.
6. 30 dòng hiện có đã xếp sẵn theo 3 nhóm: A 8, B 17, C 4, đã xong 1 (file 20, mục 5).

Muốn BEA lớp 2 tự làm điểm 1 sau mỗi việc thì phải sửa CLAUDE.md. Việc đó cần anh duyệt riêng (QD-L1-CHUNG-006).

## 6. Ràng buộc

- Không sửa CLAUDE.md, code, cấu hình, hook khi anh chưa duyệt.
- Không ghi vào Master Plan IEC (QD-L1-CHUNG-004).
- HO_SO chỉ ghi thêm dòng, không sửa dòng cũ.
- THUC_THI: không tự gán người phụ trách, không tự đặt hạn; Completed phải có bằng chứng; mỗi lần sửa ghi trước và sau.
- Hợp đồng, giá, nội dung đối tác: không gửi cho model ngoài (NT-CHUNG-016).
