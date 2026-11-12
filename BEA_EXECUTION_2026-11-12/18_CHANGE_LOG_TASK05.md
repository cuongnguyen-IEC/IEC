# 18 · Nhật ký thay đổi — TASK 05 (Execution MVP & Decision Record v2)

- Người thực hiện: Claude (BEA), phiên Claude Code đám mây.
- Phạm vi được sửa: **chỉ tab THUC_THI** trong BEA_DKB_INDEX (`1JDRgM7BusKt908uSfHHkx5A0Wk1UQ-JxRhJ9dhyJaS4`, sheetId 3).
- Không sửa:
  - Master Plan IEC (theo QD-L1-CHUNG-004);
  - HO_SO, DU_AN, LIEN_KET;
  - mọi hồ sơ QĐ trên Drive;
  - code, cấu hình, CLAUDE.md, ask.js, check.js, models.json.
- Thời điểm: 12/11/2026, khoảng 21:45–21:51 (giờ Việt Nam).
- Điểm khôi phục:
  - Trước: revision Drive `32` (11/11/2026 12:01 giờ VN).
  - Sau: revision `46` (12/11/2026 21:51 giờ VN).
  - Khôi phục được bằng Lịch sử phiên bản của Google Sheets.
- Căn cứ phê duyệt chung:
  - TASK 05 (anh: "Tôi đã xem xét và phê duyệt phương án triển khai Execution MVP"; mục 1 yêu cầu liên kết QĐ, ghi PENDING…, ghi tiến độ);
  - QD-L1-CHUNG-003 (Execution MVP, Đã thống nhất 10/11);
  - QD-L1-CHUNG-004 (THUC_THI là nguồn chuẩn, Đã thống nhất 10/11);
  - file 14 mục 3 (8 hành động ứng viên, nằm trong phương án anh duyệt).

## Bảng thay đổi

| Mã | Ô / vùng | Trước | Sau | Lý do | Căn cứ |
|---|---|---|---|---|---|
| CL-01 | D9, D10 (ACT-DIALOGUES-008, -009) | `—` | `QD-IEC-DIALOGUES-002, -006 (Tiêu chí)` | Liên kết hành động với QĐ có nêu mốc này ở mục Tiêu chí | TASK 05 mục 1; QĐ-002, QĐ-006 mục Tiêu chí |
| CL-02 | D13:D23 (ACT-WORKSHOP-001…011) | `—` (11 ô) | Nguồn quyết định DINH_HUONG_v2 kèm nháp QĐ: -001, -002 → `…→ nháp QD-IEC-WORKSHOP-ANM-003 (chờ duyệt)`; -003, -004, -005, -006, -008, -009 → `…→ nháp QD-IEC-WORKSHOP-ANM-001 (chờ duyệt)`; -007, -011 → `…→ nháp QD-IEC-WORKSHOP-ANM-002 (chờ duyệt)`; -010 → `Không có QĐ: việc còn mở, DINH_HUONG_v2 mục 4` | Dự án chưa có QĐ trong HO_SO. Dẫn tới nơi chứa quyết định (DINH_HUONG_v2) và nháp QĐ trong file 16. Không ghi mã QĐ như thể đã duyệt | TASK 05 mục 1, 2 |
| CL-03 | E3, E6–E12, E14–E23 (18 ô) | `CHƯA XÁC NHẬN` | `PENDING OWNER CONFIRMATION` | TASK 05 yêu cầu nhãn này. 4 ô "Anh Cường" (E2, E4, E5, E13) giữ nguyên | TASK 05 mục 1 |
| CL-04 | F8, F11, F12, F15–F22 (11 ô) | `CHƯA XÁC NHẬN` | `PENDING DEADLINE CONFIRMATION` | Như trên. Giữ nguyên hạn có điều kiện từ nguồn (F7 "Khi phát sinh", F23 "Sau khi có ngày tổ chức") và mọi hạn là ngày | TASK 05 mục 1 |
| CL-05 | O11 (công thức "Thiếu Owner") | `=COUNTIF(E2:E,"CHƯA XÁC NHẬN")` | `=COUNTIF(E2:E,"PENDING OWNER CONFIRMATION")+COUNTIF(E2:E,"CHƯA XÁC NHẬN")` | Nếu không sửa, CL-03 làm ô này về 0 (sai). Công thức liên quan trực tiếp; vẫn đếm nhãn cũ nếu còn | TASK 05 mục 1, 4 |
| CL-06 | G15, G16, G17 (ACT-WORKSHOP-003, -004, -005) | trống | `In Progress` | NHAT_KY 07/11 ghi đã dựng các deck. File chưa có trên Drive, chưa có bằng chứng gửi nên **không** chuyển Completed | TASK 05 "ghi nhận tiến độ"; quy tắc Completed cần bằng chứng |
| CL-07 | I15, I16, I17 | trống | Dẫn NHAT_KY_2026-11-07_deck_Benson_Hunt_IEC_v2 / NHAT_KY_2026-11-07_deck_gui_HoaSen_VIFC, kèm "(file pptx chưa có trên Drive)" | Bằng chứng một phần cho CL-06 | như trên |
| CL-08 | H2:H23 (22 ô) | Nội dung cũ (mục dưới) | Thêm một đoạn "12/11: …" ở **đầu** ô; nội dung cũ giữ nguyên nguyên văn ở sau | Ghi tiến độ tại 12/11 theo nguồn đã tra; không xoá lịch sử cập nhật | TASK 05 mục 1 |
| CL-09 | J2:J23 (22 ô) | 10/11/2026 (18 ô) hoặc 11/11/2026 (J2, J4, J5, J13) | 12/11/2026 | Ngày cập nhật theo CL-08 | — |
| CL-10 | A24:L31 (8 dòng mới) | trống | ACT-DIALOGUES-012…018, ACT-WORKSHOP-012 (chi tiết ở file 15 mục 1.3); Owner, Deadline = PENDING…; Status trống; K24:K30 là công thức HYPERLINK giống các dòng cũ | Hành động phát sinh từ QĐ hoặc quyết định của anh 11–12/11 chưa có dòng (QD-L1-CHUNG-003: mọi QĐ có hành động đều có dòng) | File 14 mục 3 (đã duyệt cùng phương án) |
| CL-11 | Ghi chú tiêu đề E1, F1 | E1: "Chỉ điền khi anh xác nhận. Chưa có thì ghi CHƯA XÁC NHẬN." F1: "Chỉ điền khi có nguồn (QĐ, DINH_HUONG, lời anh). Chưa có thì ghi CHƯA XÁC NHẬN." | Đổi sang hướng dẫn ghi PENDING OWNER / DEADLINE CONFIRMATION, có ghi "từ 12/11/2026, TASK 05; trước đó ghi CHƯA XÁC NHẬN"; F1 thêm "Hạn có điều kiện từ nguồn giữ nguyên" | Ghi chú phải khớp quy tắc mới | TASK 05 mục 1 |

Không xoá dòng hay cột nào. Không đổi cột A, B, C, K, L của 22 dòng cũ. Không đổi khối Tổng hợp N1:O13, trừ O11 (CL-05). Không đổi kiểm tra dữ liệu (danh sách chọn Status).

## Đoạn thêm vào Progress Update (CL-08)

Nội dung cũ đứng sau đoạn mới, giữ nguyên nguyên văn.

| Dòng | Action ID | Đoạn thêm (12/11) | Nội dung cũ (giữ nguyên) |
|---|---|---|---|
| 2 | ACT-DIALOGUES-001 | Không thấy phản hồi của ACB trong NHAT_KY, KET_QUA và hộp thư đã tra; Status chờ anh xác nhận. Bảng giá v2.1 phát hành 12/11 ghi báo ý định 16/11; hạn giữ 13/11 theo QĐ-002 cho tới khi anh duyệt nháp QĐ-008. | 11/11: anh Cường nhận phụ trách (IN-20261110-0019). 10/11: BEA chưa biết thư mời ACB đã gửi hay chưa |
| 3 | ACT-DIALOGUES-002 | Không có bằng chứng ký hoặc thanh toán. v2.1 ghi 25/11; giữ 20/11 theo QĐ-002 cho tới khi duyệt QĐ-008. | (trống) |
| 4 | ACT-DIALOGUES-003 | Chưa xác định được điều kiện; phụ thuộc ACT-DIALOGUES-001. | 11/11: anh Cường nhận phụ trách… 10/11: chỉ làm khi điều kiện xảy ra |
| 5 | ACT-DIALOGUES-004 | Vẫn chưa có danh sách ngân hàng đã nhận bộ và ngày gửi; v2.1 ghi 16/11; giữ 13/11 theo QĐ-006. | 11/11: anh Cường nhận phụ trách… 10/11: BEA chưa có danh sách ngân hàng… |
| 6 | ACT-DIALOGUES-005 | Không có bằng chứng ký hoặc thanh toán; v2.1 ghi 25/11; giữ 20/11 theo QĐ-006. | (trống) |
| 7 | ACT-DIALOGUES-006 | Chưa phát sinh trường hợp nào trong nguồn đã tra. | (trống) |
| 8 | ACT-DIALOGUES-007 | Hợp đồng Gentech v2 ghi ghế chuyên môn Phiên 1 cho Gentech; Gentech chưa ký nên chưa xếp ghế chính thức. | 10/11: tối đa 2 ghế mỗi phiên, 6 ghế cả kỳ |
| 9 | ACT-DIALOGUES-008 | v2.1 dời mốc duyệt demo sang 27/11; giữ 25/11 cho tới khi duyệt QĐ-008. Decision ID liên kết QĐ-002, QĐ-006. | (trống) |
| 10 | ACT-DIALOGUES-009 | Không có cập nhật. Decision ID liên kết QĐ-002, QĐ-006. | (trống) |
| 11 | ACT-DIALOGUES-010 | Không tìm thấy kế hoạch vận hành tính lại sau 04/11 (bản mới nhất: E01_Plan_Operating_v0.3, 05/10). | (trống) |
| 12 | ACT-DIALOGUES-011 | Không tìm thấy Commercial Plan Kỳ 1 bản sau 18/10 (bản mới nhất: E01_Plan_Commercial_v0.3, 05/10). | 10/11: BEA chưa kiểm đã có bản mới chưa |
| 13 | ACT-WORKSHOP-001 | Không có bằng chứng Benson Hunt đã xác nhận, cũng không có bằng chứng proposal v5 đã gửi. | 11/11: anh Cường nhận phụ trách… 10/11: mốc dự kiến; BEA chưa biết proposal v5… |
| 14 | ACT-WORKSHOP-002 | Không có cập nhật; Hub chưa đồng ý nhận buổi. | 10/11: mốc dự kiến |
| 15 | ACT-WORKSHOP-003 | NHAT_KY 07/11 ghi đã dựng 2 deck v2 gửi Benson Hunt; file chưa có trong KET_QUA. Chuyển In Progress. | (trống) |
| 16 | ACT-WORKSHOP-004 | NHAT_KY 07/11 ghi đã dựng deck gửi VIFC, anh chốt "gửi ngay"; chưa có bằng chứng đã gửi. Chuyển In Progress. | 10/11: làm sau deck gửi Benson Hunt |
| 17 | ACT-WORKSHOP-005 | Như trên, deck gửi Đại học Hoa Sen. | 10/11: làm sau deck gửi Benson Hunt |
| 18 | ACT-WORKSHOP-006 | Chưa có đầu mối VIFC Fintech Hub trong nguồn đã tra. | 10/11: Hub chưa đồng ý nhận buổi, chưa có đầu mối |
| 19 | ACT-WORKSHOP-007 | Vẫn còn mở (DINH_HUONG_v2 mục 4). | (trống) |
| 20 | ACT-WORKSHOP-008 | Không có bằng chứng đã hỏi Benson Hunt. | (trống) |
| 21 | ACT-WORKSHOP-009 | Không có cập nhật. | (trống) |
| 22 | ACT-WORKSHOP-010 | Không có cập nhật. | (trống) |
| 23 | ACT-WORKSHOP-011 | Chưa có ngày tổ chức nên chưa đến bước thu. | 10/11: phụ thuộc ACT-WORKSHOP-007 |

Nguyên văn đầy đủ của từng ô sau thay đổi: đọc lại THUC_THI!H2:H23, hoặc so revision 32 với revision 46.

## Kiểm tra sau thay đổi (đọc lại THUC_THI!A1:O32, 12/11/2026)

| Ô tổng hợp | Trước | Sau | Khớp dự kiến |
|---|---|---|---|
| Tổng số hành động (O3) | 22 | 30 | Có (22 + 8) |
| Chưa xác nhận trạng thái (O4) | 22 | 27 | Có (30 − 3 In Progress) |
| In Progress (O6) | 0 | 3 | Có |
| Not Started, Blocked, Completed | 0 | 0 | Có |
| Sắp đến hạn 7 ngày (O9) | 4 | 4 | Có (4 dòng hạn 13/11) |
| Quá hạn (O10) | 0 | 0 | Có |
| Thiếu Owner (O11) | 18 | 26 | Có (18 + 8 dòng mới) |
| Deadline chưa phải ngày cụ thể (O12) | 13 | 21 | Có (13 + 8) |
| Completed chưa có bằng chứng (O13) | 0 | 0 | Có |

## Thay đổi khác trong nhiệm vụ (không phải bảng vận hành)

| Mã | Đối tượng | Thay đổi | Ghi chú |
|---|---|---|---|
| CL-12 | Drive: PRJ-GLOBAL/NHAT_KY | Tạo mới NHAT_KY_2026-11-12_TASK05_execution-mvp (Google Doc `1B_kaKlR0N2FaQ-cZdBRkNLQkzc2W8OrlBkwgL5UUZiM`, 12/11/2026 21:57 giờ VN); đã đọc lại, nội dung đầy đủ | Nhật ký theo khuôn BEA; không sửa NHAT_KY cũ |
| CL-13 | Repo GitHub, nhánh `ccr-594510c6-l92km9` | Thêm file 15–19 | Không sửa file 11–14 |
