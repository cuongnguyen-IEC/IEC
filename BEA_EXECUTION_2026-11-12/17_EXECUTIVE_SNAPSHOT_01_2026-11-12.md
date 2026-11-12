# BÁO CÁO SNAPSHOT ĐIỀU HÀNH #1 · Execution MVP · 12/11/2026

- Ngày lập: Thứ Năm, 12/11/2026, sau khi cập nhật THUC_THI (revision 46, 21:51 giờ VN). Người lập: BEA (Claude).
- Loại báo cáo: **snapshot tình trạng ban đầu** của pilot. Báo cáo tuần #1 lập Thứ Hai 16/11/2026 theo quy trình ở file 19.
- Phạm vi: PRJ-IEC-DIALOGUES, PRJ-IEC-WORKSHOP-ANM (hai dự án pilot đã duyệt).
- Dữ liệu:
  - THUC_THI (BEA_DKB_INDEX) đọc lại sau cập nhật: 30 dòng;
  - HO_SO;
  - NHAT_KY từ 10/11 đến 12/11;
  - Bảng giá Kỳ 1 v2.1.
- Quy tắc:
  - chỉ ghi dữ kiện có nguồn;
  - không suy diễn lý do trễ hay mức độ nghiêm trọng;
  - dòng Status trống được đếm riêng là "chưa xác nhận trạng thái".

## 1. Tiến độ

| Chỉ tiêu | DIALOGUES | WORKSHOP-ANM | Tổng | Ô tổng hợp THUC_THI |
|---|---|---|---|---|
| Tổng số hành động | 18 | 12 | **30** | O3 = 30 |
| Not Started | 0 | 0 | 0 | O5 = 0 |
| In Progress | 0 | 3 | **3** | O6 = 3 |
| Blocked | 0 | 0 | 0 | O7 = 0 |
| Completed (có bằng chứng) | 0 | 0 | 0 | O8 = 0 |
| Chưa xác nhận trạng thái | 18 | 9 | **27** | O4 = 27 |
| Kiểm tra tổng | | | 0+3+0+0+27 = 30, đúng | |

**Tiến độ có bằng chứng trong kỳ (06–12/11):**

- ACT-WORKSHOP-003, -004, -005 → In Progress. NHAT_KY 07/11 ghi đã dựng deck gửi Benson Hunt (v2), deck gửi VIFC Fintech Hub (v1) và Đại học Hoa Sen (v1); anh chốt "gửi ngay" hai deck sau. File pptx chưa có trong KET_QUA; chưa có bằng chứng đã gửi.
- ACT-DIALOGUES-007 (xếp ghế): hợp đồng Gentech v2 (12/11) ghi ghế Phiên 1 cho Gentech; Gentech chưa ký.
- Đầu ra mới 11–12/11 chưa có hành động theo dõi trước đó, nay đã thêm dòng:
  - Bảng giá và Đề xuất Kỳ 1 v2.1 (4 PDF trong KET_QUA);
  - hợp đồng Gentech v1, v2;
  - MOU ONEAI.

## 2. Công việc trễ hạn

Không có dòng quá hạn (ngày lập 12/11; hạn sớm nhất là 13/11). Ô O10 = 0.

**Sắp đến hạn (12/11 – 19/11): 4 dòng, đều hạn 13/11/2026 (ngày mai), Owner là anh Cường, Status trống:**

| Action ID | Việc | Decision ID | Cập nhật gần nhất |
|---|---|---|---|
| ACT-DIALOGUES-001 | Nhận phản hồi báo ý định của ACB | QD-IEC-DIALOGUES-002 | 12/11: không thấy phản hồi trong nguồn đã tra |
| ACT-DIALOGUES-003 | Thôi giữ ghế cho ACB nếu ACB không báo ý định trước 13/11 | QD-IEC-DIALOGUES-002 | 12/11: phụ thuộc ACT-DIALOGUES-001 |
| ACT-DIALOGUES-004 | Nhận phản hồi báo ý định của các ngân hàng nhận bộ chung | QD-IEC-DIALOGUES-006 | 12/11: chưa có danh sách ngân hàng đã nhận bộ |
| ACT-WORKSHOP-001 | Benson Hunt xác nhận chương trình tại Đại học Hoa Sen | (nháp QD-IEC-WORKSHOP-ANM-003) | 12/11: không có bằng chứng proposal v5 đã gửi |

**Trong 8–14 ngày tới (20/11 – 26/11):** ACT-DIALOGUES-002, -005 (20/11), ACT-WORKSHOP-002 (20/11), ACT-DIALOGUES-008 (25/11). Cả 4 dòng Owner đều là PENDING OWNER CONFIRMATION.

## 3. Công việc bị chặn

Không có dòng nào Status = Blocked (O7 = 0). Các phụ thuộc ghi trong Progress Update (không tự chuyển thành Blocked):

| Dòng | Phụ thuộc vào | Nguồn |
|---|---|---|
| ACT-DIALOGUES-003 | Kết quả ACT-DIALOGUES-001 | QĐ-002, mục Điều kiện áp dụng |
| ACT-WORKSHOP-011 | ACT-WORKSHOP-007 (thuế GTGT) và ngày tổ chức | DINH_HUONG_v2 |
| ACT-DIALOGUES-001…005, -008 | Mốc có thể đổi nếu anh duyệt nháp QĐ-008 (ACT-DIALOGUES-012) | NHAT_KY 12/11 v2.1 |
| ACT-DIALOGUES-015 | ACT-DIALOGUES-013, -014 (điều khoản, người ký) | NHAT_KY Gentech |

## 4. Quyết định chưa được thực thi

Định nghĩa: QĐ "Đã thống nhất" của 2 dự án có hành động liên kết trong THUC_THI, nhưng chưa hành động nào có Status In Progress hoặc Completed. Tức là **chưa có bằng chứng thực thi được ghi nhận**, không có nghĩa là chắc chắn chưa làm.

| QĐ | Hành động liên kết | Hành động đã có tiến độ ghi nhận | Ghi chú |
|---|---|---|---|
| QD-IEC-DIALOGUES-001 (giá, gói) | ACT-DIALOGUES-007, -011, -013, -014, -015 | 0/5 | QĐ ghi hiệu lực đến 06/11, đã qua (file 16, mục E1) |
| QD-IEC-DIALOGUES-002 (mốc ACB) | ACT-DIALOGUES-001, -002, -003 (và -008, -009 qua Tiêu chí) | 0/5 | Hạn 13/11 ngày mai |
| QD-IEC-DIALOGUES-003 (quy mô theo doanh nghiệp) | ACT-DIALOGUES-010 | 0/1 | Không tìm thấy kế hoạch vận hành tính lại |
| QD-IEC-DIALOGUES-006 (mốc nhóm ngân hàng) | ACT-DIALOGUES-004, -005, -006, -007 (và -008, -009) | 0/6 | — |
| QD-IEC-DIALOGUES-007 (nhiều ngân hàng) | ACT-DIALOGUES-007 | 0/1 | — |
| QD-IEC-DIALOGUES-004, -005 | Không có dòng mở | — | Đầu ra theo QĐ đã có (bộ ACB, PDF trong KET_QUA 04/11); kết quả với ACB: NOT AVAILABLE |

**Quyết định đang chờ anh (chưa duyệt, BEA không tự thực hiện phần phụ thuộc):**

| Mã / nháp | Nội dung | Hành động bị ảnh hưởng | Nguồn |
|---|---|---|---|
| Nháp QD-IEC-DIALOGUES-008 | Dời hạn đồng hành Kỳ 1 (16/11, 25/11); tên tiếng Anh Kỳ 1 | ACT-DIALOGUES-001…005, -008, -012 | NHAT_KY 12/11 v2.1 |
| Nháp QD-IEC-KE-HOACH-2027-001 v2 | Cập nhật danh sách chương trình 2027 (ngoài 2 dự án pilot) | — | File 16, mục B2 |
| Nháp QD-IEC-WORKSHOP-ANM-001…003 | Hồ sơ QĐ cho quyết định trong DINH_HUONG_v2 | 11 dòng WORKSHOP; ACT-WORKSHOP-012 | File 16, mục C |
| Hợp đồng Gentech v2 | 5 điều khoản BEA tự đề xuất; người ký; mâu thuẫn với QĐ-001 (40 triệu) | ACT-DIALOGUES-013, -014, -015 | NHAT_KY Gentech v1, v2 |
| Thuế GTGT khi xuất hoá đơn cho Benson Hunt | Còn mở từ 06/11 | ACT-WORKSHOP-007, -011 | DINH_HUONG_v2 mục 4 |

## 5. Vấn đề cần CEO/COO xử lý

Chỉ liệt kê vấn đề thoả điều kiện khách quan của mẫu (file 12, mục 9). Không xếp mức độ.

| # | Điều kiện | Vấn đề (theo dữ liệu) | Cần anh làm gì |
|---|---|---|---|
| 1 | Sắp đến hạn, thiếu Status | 4 dòng hạn 13/11 chưa có Status, Evidence | Cho biết trạng thái và bằng chứng nếu có, hoặc quyết mốc mới qua QĐ-008 |
| 2 | Hai nguồn ghi khác nhau | QĐ-002, QĐ-006 và THUC_THI ghi 13/11, 20/11; tài liệu v2.1 đã phát hành ghi 16/11, 25/11 | Duyệt hoặc không duyệt nháp QĐ-008 |
| 3 | Hai nguồn ghi khác nhau | Hợp đồng Gentech v2 "không hoàn tiền khi không xếp được ghế"; QĐ-001 và Bảng giá v2.1 "40 triệu khi không xếp được ghế" | Chọn điều khoản áp dụng cho Gentech |
| 4 | Hai nguồn ghi khác nhau | QĐ-001 ghi bảng giá hiệu lực đến 06/11; tài liệu 12/11 vẫn chào giá với hạn 25/11 | Xác nhận gia hạn, có thể gộp vào QĐ-008 |
| 5 | Thiếu Owner | 26/30 dòng PENDING OWNER CONFIRMATION, trong đó 4 dòng có hạn 20/11 và 25/11 | Xác nhận người phụ trách; chưa có Project Owner phía IEC cho cả 2 dự án |
| 6 | Hạn chưa phải ngày | 21/30 dòng (19 dòng PENDING DEADLINE CONFIRMATION, 2 dòng hạn có điều kiện) | Xác nhận hạn cho dòng nào cần hạn |
| 7 | In Progress chờ xác nhận hoàn thành | 3 deck Workshop đã dựng nhưng chưa có trên Drive, chưa có bằng chứng gửi | Cho biết đã gửi chưa và lưu file ở đâu, để chuyển Completed |

## 6. Dữ liệu thiếu

| Chỉ tiêu | DIALOGUES | WORKSHOP-ANM | Tổng | Ô tổng hợp |
|---|---|---|---|---|
| Owner chưa xác nhận | 15 | 11 | 26 | O11 = 26 |
| Deadline không phải ngày cụ thể | 11 | 10 | 21 | O12 = 21 |
| Status trống | 18 | 9 | 27 | O4 = 27 |
| Updated At cũ hơn 7 ngày | 0 | 0 | 0 | — |

## 7. Anh phản hồi (anh điền)

- Báo cáo có ích: Có / Không · Lý do (1 dòng):
- Quyết định ở mục 4:
- Xác nhận Owner / Deadline:
