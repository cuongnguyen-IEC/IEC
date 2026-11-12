# 12 · Mẫu báo cáo điều hành hằng tuần (BEA Weekly Execution Report)

- Phiên bản mẫu: v1, ngày 12/11/2026. Người lập: Claude.
- Trạng thái: **mẫu đề xuất, chờ anh duyệt.**
- Dùng cho: Execution MVP (QD-L1-CHUNG-003), 2 dự án pilot (file 14).
- Nguồn dữ liệu: tab THUC_THI (BEA_DKB_INDEX) là nguồn chuẩn (QD-L1-CHUNG-004). Đọc thêm HO_SO và NHAT_KY trong tuần. Master Plan IEC chỉ đọc để dẫn link.

## A. Quy tắc lập báo cáo

1. **Chỉ đếm và liệt kê dữ liệu có trong nguồn.** Không suy diễn lý do trễ. Không chấm mức độ nghiêm trọng hay rủi ro nếu nguồn không ghi.
2. **Trạng thái** dùng đúng 4 giá trị: Not Started, In Progress, Blocked, Completed. Dòng có Status trống được đếm riêng là **"Chưa xác nhận trạng thái"**, để tổng luôn khớp. Không gộp vào Not Started.
3. **Completed** chỉ được đếm khi cột Evidence / Result có bằng chứng. Dòng Completed mà thiếu bằng chứng đưa vào mục 9.
4. **Sắp đến hạn:** Deadline là ngày cụ thể, nằm trong [ngày lập; ngày lập + 7 ngày], và Status khác Completed.
5. **Quá hạn:** Deadline là ngày cụ thể, nhỏ hơn ngày lập, và Status khác Completed.
6. Deadline không phải ngày cụ thể ("CHƯA XÁC NHẬN", "Khi phát sinh") không vào mục 6, 7, mà được đếm ở mục "Dữ liệu thiếu".
7. **Lý do trễ** chỉ ghi khi Owner hoặc anh đã nói, kèm nguồn (mã IN, NHAT_KY). Không có thì ghi `NOT AVAILABLE`.
8. Tuần tính từ Thứ Hai đến Chủ Nhật, khớp cột tuần của sheet Tracking trong Master Plan IEC.
9. Báo cáo không gửi ra ngoài. BEA không sửa THUC_THI khi lập báo cáo. Đề xuất sửa nằm ở mục 9 và chờ anh duyệt.

## B. Mẫu (sao chép phần này mỗi tuần)

```markdown
# BÁO CÁO THỰC THI TUẦN [N] · [dd/mm] – [dd/mm/yyyy]

- Ngày lập: [Thứ Hai, dd/mm/yyyy] · Người lập: BEA (Claude)
- Phạm vi: [PRJ-…], [PRJ-…]
- Dữ liệu: THUC_THI đọc lúc [hh:mm dd/mm/yyyy]; HO_SO; NHAT_KY từ [dd/mm] đến [dd/mm]
- Báo cáo trước: [link NHAT_KY tuần N-1] · Thay đổi so với tuần trước: [số dòng mới / số dòng đổi trạng thái]

## 1–5. Tổng quan trạng thái

| Chỉ tiêu | [PRJ-1] | [PRJ-2] | Tổng |
|---|---|---|---|
| 1. Tổng số hành động | | | |
| 2. Chưa bắt đầu (Not Started) | | | |
| 3. Đang thực hiện (In Progress) | | | |
| 4. Bị chặn (Blocked) | | | |
| 5. Hoàn thành (Completed, có bằng chứng) | | | |
| Chưa xác nhận trạng thái (Status trống) | | | |
| Kiểm tra: 2+3+4+5+chưa xác nhận = 1 | | | Đúng / Sai |

## 6. Việc sắp đến hạn (7 ngày tới: [dd/mm] – [dd/mm])

| Action ID | Việc | Owner | Deadline | Status | Cập nhật gần nhất (ngày, nội dung) | Decision ID |
|---|---|---|---|---|---|---|
| | | | | | | |

(Không có: ghi "Không có dòng nào".)

## 7. Việc quá hạn

| Action ID | Việc | Owner | Deadline | Số ngày quá hạn | Status | Lý do (chỉ khi có nguồn) | Nguồn lý do |
|---|---|---|---|---|---|---|---|
| | | | | | | NOT AVAILABLE | |

## 8. Quyết định đang chờ xử lý

| Mã QĐ / nháp | Nội dung cần quyết | Người quyết | Phát sinh ngày | Hành động bị ảnh hưởng | Nguồn |
|---|---|---|---|---|---|
| | | | | | |

## 9. Vấn đề cần người điều hành can thiệp

Chỉ đưa vào mục này khi thoả ít nhất một điều kiện khách quan:

- (a) Status = Blocked;
- (b) quá hạn;
- (c) sắp đến hạn mà thiếu Owner hoặc Status;
- (d) Completed thiếu bằng chứng;
- (e) hai nguồn ghi khác nhau về cùng một mốc hay quyết định;
- (f) việc có hành động nhưng chưa có dòng THUC_THI.

| # | Điều kiện | Mô tả (theo dữ liệu) | Dòng / nguồn | Cần anh làm gì |
|---|---|---|---|---|
| 1 | | | | |

## 10. Dữ liệu thiếu

| Chỉ tiêu | [PRJ-1] | [PRJ-2] | Tổng |
|---|---|---|---|
| Owner "CHƯA XÁC NHẬN" | | | |
| Deadline không phải ngày cụ thể | | | |
| Status trống | | | |
| Updated At cũ hơn 7 ngày | | | |

## 11. Anh phản hồi (anh điền)

- Báo cáo có ích: Có / Không · Lý do (1 dòng):
- Quyết định ở mục 8:
- Xác nhận Owner / Deadline mới:
- Đồng ý ghi các đề xuất ở mục 9 vào THUC_THI: Có / Không / Một phần (ghi rõ):
```

## C. Cách tính từng mục từ THUC_THI

| Mục | Cột THUC_THI | Cách tính |
|---|---|---|
| 1 | A (Project ID) | Đếm dòng có Action ID, theo dự án |
| 2–5 | G (Status) | Đếm theo từng giá trị; 5 chỉ đếm khi I (Evidence / Result) không trống |
| Chưa xác nhận | G | Đếm dòng có G trống |
| 6 | F (Deadline), G | F là ngày, F ≥ ngày lập, F ≤ ngày lập + 7, G ≠ Completed |
| 7 | F, G | F là ngày, F < ngày lập, G ≠ Completed; số ngày quá hạn = ngày lập − F |
| 8 | D (Decision ID), HO_SO, NHAT_KY | QĐ ở trạng thái "Đề xuất" hoặc nháp chưa duyệt, và mục "Chờ anh" trong NHAT_KY tuần qua của 2 dự án |
| 9 | Toàn bảng, HO_SO, NHAT_KY | Theo điều kiện (a)–(f) |
| 10 | E, F, G, J | Đếm theo từng điều kiện |

Khối "Tổng hợp" ở cột N:O của THUC_THI đã có công thức cho các ô: tổng số, 4 trạng thái, sắp đến hạn, quá hạn, thiếu Owner, hạn chưa phải ngày, Completed chưa có bằng chứng. Báo cáo lấy số từ khối này rồi đối chiếu bằng cách đếm lại từng dòng.

---

## Phụ lục · Bản điền thử: Tuần 0, ngày lập 12/11/2026

> Điền từ THUC_THI đọc ngày 12/11/2026 (chỉ đọc), HO_SO, NHAT_KY từ 10/11 đến 12/11. Mục đích: thử mẫu trên dữ liệu thật. Đây **không** là báo cáo tuần chính thức số 1; báo cáo #1 dự kiến lập Thứ Hai 16/11/2026 nếu anh duyệt file 14. Lần chạy TASK 04 ngày 10/11 đã có báo cáo tuần 0 trên máy (15_BAO_CAO_THUC_THI_TUAN_0_2026-11-10.md); phiên này không đọc được file đó.

### BÁO CÁO THỰC THI TUẦN 0 · 09/11 – 15/11/2026 (điền thử)

- Ngày lập: Thứ Năm, 12/11/2026 · Người lập: BEA (Claude)
- Phạm vi: PRJ-IEC-DIALOGUES, PRJ-IEC-WORKSHOP-ANM
- Dữ liệu: THUC_THI (22 dòng; Updated At gần nhất 11/11/2026); HO_SO; NHAT_KY 10/11 – 12/11

#### 1–5. Tổng quan trạng thái

| Chỉ tiêu | DIALOGUES | WORKSHOP-ANM | Tổng |
|---|---|---|---|
| 1. Tổng số hành động | 11 | 11 | **22** |
| 2. Chưa bắt đầu (Not Started) | 0 | 0 | 0 |
| 3. Đang thực hiện (In Progress) | 0 | 0 | 0 |
| 4. Bị chặn (Blocked) | 0 | 0 | 0 |
| 5. Hoàn thành (Completed, có bằng chứng) | 0 | 0 | 0 |
| Chưa xác nhận trạng thái (Status trống) | 11 | 11 | **22** |
| Kiểm tra tổng | | | Đúng (0+0+0+0+22 = 22) |

Khối Tổng hợp của THUC_THI cũng ra: 22 chưa xác nhận, Not Started 0, In Progress 0, Blocked 0, Completed 0. Khớp.

#### 6. Việc sắp đến hạn (12/11 – 19/11)

| Action ID | Việc | Owner | Deadline | Status | Cập nhật gần nhất | Decision ID |
|---|---|---|---|---|---|---|
| ACT-DIALOGUES-001 | Nhận phản hồi báo ý định của ACB | Anh Cường | 13/11/2026 | (trống) | 11/11: anh nhận phụ trách. 10/11: BEA chưa biết thư mời ACB đã gửi chưa | QD-IEC-DIALOGUES-002 |
| ACT-DIALOGUES-003 | Thôi giữ ghế chuyên môn cho ACB nếu ACB không báo ý định trước 13/11 | Anh Cường | 13/11/2026 | (trống) | 11/11: anh nhận phụ trách. 10/11: chỉ làm khi điều kiện xảy ra | QD-IEC-DIALOGUES-002 |
| ACT-DIALOGUES-004 | Nhận phản hồi báo ý định của các ngân hàng nhận bộ đề xuất chung | Anh Cường | 13/11/2026 | (trống) | 11/11: anh nhận phụ trách. 10/11: BEA chưa có danh sách ngân hàng đã nhận bộ và ngày gửi | QD-IEC-DIALOGUES-006 |
| ACT-WORKSHOP-001 | Benson Hunt xác nhận chương trình tại Đại học Hoa Sen | Anh Cường | 13/11/2026 | (trống) | 11/11: anh nhận phụ trách. 10/11: mốc dự kiến; BEA chưa biết proposal v5 đã gửi chưa | — |

Khối Tổng hợp THUC_THI: "Sắp đến hạn (7 ngày tới)" = 4. Khớp.

Để chuẩn bị, các dòng có hạn trong 8–14 ngày tới (20/11 – 26/11):

- ACT-DIALOGUES-002 (20/11, CHƯA XÁC NHẬN Owner)
- ACT-DIALOGUES-005 (20/11, CHƯA XÁC NHẬN)
- ACT-WORKSHOP-002 (20/11, CHƯA XÁC NHẬN)
- ACT-DIALOGUES-008 (25/11, CHƯA XÁC NHẬN)

#### 7. Việc quá hạn

Không có dòng nào (ngày lập 12/11; hạn sớm nhất 13/11). Khối Tổng hợp: Quá hạn = 0.

#### 8. Quyết định đang chờ xử lý

| Mã QĐ / nháp | Nội dung cần quyết | Người quyết | Phát sinh ngày | Hành động bị ảnh hưởng | Nguồn |
|---|---|---|---|---|---|
| Nháp QD-IEC-DIALOGUES-008 | Dời hạn đồng hành Kỳ 1 cho mọi đơn vị theo gói (báo ý định 16/11; ký và thanh toán 25/11); chốt tên tiếng Anh Kỳ 1 | Anh | 12/11/2026 | ACT-DIALOGUES-001…005, -008 | NHAT_KY_2026-11-12_PROPOSAL-KY1-v2.1, "Việc mở" |
| (theo QD-IEC-DIALOGUES-006) | Quyết từng trường hợp ngân hàng nhận bộ sau mốc báo ý định | Anh | Khi phát sinh | ACT-DIALOGUES-006 | THUC_THI |
| (chưa có mã) | Hợp đồng Gentech v2: 5 điểm BEA tự đề xuất (Điều 7.2, 7.5, 8.2, 13.2; Phụ lục 01 mục 4); người ký phía Gentech | Anh | 12/11/2026 | Chưa có dòng (xem mục 9, dòng 4) | NHAT_KY Gentech v1, v2 |
| (chưa có mã) | Cách xử lý thuế GTGT và chứng từ khi IEC xuất hoá đơn cho Benson Hunt | Anh | 06/11/2026 | ACT-WORKSHOP-007, -011 | DINH_HUONG_v2 mục 4; NHAT_KY 07/11 v5 |

#### 9. Vấn đề cần người điều hành can thiệp

| # | Điều kiện | Mô tả (theo dữ liệu) | Dòng / nguồn | Cần anh làm gì |
|---|---|---|---|---|
| 1 | (c) sắp đến hạn, thiếu Status | 4 dòng hạn 13/11 chưa có Status, chưa có Evidence; cập nhật gần nhất 11/11 | ACT-DIALOGUES-001, -003, -004; ACT-WORKSHOP-001 | Cho biết trạng thái hiện tại, kèm bằng chứng nếu có |
| 2 | (e) hai nguồn ghi khác nhau | QĐ-002, QĐ-006 (Đã thống nhất) và THUC_THI ghi 13/11, 20/11. Bảng giá và đề xuất Kỳ 1 v2.1 đã phát hành 12/11 ghi 16/11, 25/11. ACT-DIALOGUES-008: THUC_THI 25/11, v2.1 27/11 | HO_SO; THUC_THI; IEC_Dialogues_Bang_gia_Ky_1_v2.1.pdf | Duyệt hoặc không duyệt nháp QĐ-008. BEA chỉ đổi hạn trong THUC_THI sau khi anh duyệt |
| 3 | (c) thiếu Owner | 18/22 dòng Owner "CHƯA XÁC NHẬN"; 3 trong số đó có hạn 20/11 | THUC_THI | Xác nhận người phụ trách. BEA không tự gán |
| 4 | (f) việc có hành động nhưng chưa có dòng | Hợp đồng Gentech (xem điều khoản, chốt người ký, ký và thanh toán); MOU One AI (gửi đầu mối) | NHAT_KY 11/11, 12/11 | Đồng ý thêm dòng (Owner, hạn để CHƯA XÁC NHẬN) |
| 5 | (e) hai nguồn ghi khác nhau | Hợp đồng Gentech v2: không hoàn tiền khi không xếp được ghế. Bảng giá v2.1 đã phát hành: "Nếu IEC không xếp được ghế, giá gói trọn kỳ là 40 triệu đồng" | NHAT_KY Gentech v2; Bảng giá v2.1 | Chọn bản nào áp dụng, hoặc ghi ngoại lệ cho Gentech |

#### 10. Dữ liệu thiếu

| Chỉ tiêu | DIALOGUES | WORKSHOP-ANM | Tổng |
|---|---|---|---|
| Owner "CHƯA XÁC NHẬN" | 8 | 10 | 18 |
| Deadline không phải ngày cụ thể | 4 | 9 | 13 |
| Status trống | 11 | 11 | 22 |
| Updated At cũ hơn 7 ngày (trước 05/11) | 0 | 0 | 0 |

Đối chiếu với khối Tổng hợp THUC_THI: Thiếu Owner = 18; Deadline chưa phải ngày cụ thể = 13. Khớp.

#### 11. Anh phản hồi

(để trống, anh điền)
