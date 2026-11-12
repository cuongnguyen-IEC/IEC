# 15 · Báo cáo triển khai Execution MVP và Decision Record v2 (TASK 05)

- Ngày: 12/11/2026. Người thực hiện: Claude (BEA), phiên Claude Code đám mây.
- Kết quả nhanh:
  - Execution Tracker đã chạy thật trên tab **THUC_THI** cho 2 dự án pilot: 30 hành động, cập nhật 12/11.
  - Decision Record v2 đã lập cho 8 QĐ, kèm bản cập nhật QD-IEC-KE-HOACH-2027-001 và 3 nháp QĐ Workshop. Tất cả **chờ anh duyệt**, chưa ghi HO_SO.
  - Đã có snapshot điều hành #1.
  - Không ghi vào Master Plan IEC.

## 0. Quyết định nào đã được duyệt, và BEA áp dụng ra sao

| Quyết định | Trạng thái | BEA làm |
|---|---|---|
| ND-2 · Nguồn chuẩn theo dõi thực thi | **Đã duyệt** ngày 10/11/2026, thành QD-L1-CHUNG-004: "Tab THUC_THI trong BEA_DKB_INDEX là nguồn chuẩn … BEA không ghi vào bảng của IEC" | Triển khai trên THUC_THI. **Không** dùng Master Plan làm nơi ghi, vì nội dung ND-2 đã duyệt chọn THUC_THI, không chọn Master Plan |
| RC-3 · Execution MVP ở P1 | Đã duyệt, QD-L1-CHUNG-003 | Triển khai |
| Phương án pilot (file 13 phương án A; file 14) | Anh duyệt trong TASK 05 | Hai dự án PRJ-IEC-DIALOGUES, PRJ-IEC-WORKSHOP-ANM; 8 hành động ứng viên ở file 14 mục 3 |
| Khuôn Decision Record v2 (12 trường) | Anh yêu cầu áp dụng trong TASK 05 | Lập bản trình bày v2 |
| Cập nhật HO_SO theo khuôn v2 | **Chưa duyệt.** TASK 05 chỉ cho ghi khi "việc cập nhật đã được phê duyệt" | Chưa ghi; đã chuẩn bị đúng các dòng sẽ ghi thêm (file 16, mục D) |
| Nháp QD-IEC-DIALOGUES-008 (dời mốc 16/11, 25/11) | **Chưa duyệt** | Không đổi hạn trong THUC_THI; chỉ ghi chú và thêm hành động "Quyết nháp QĐ-008" |

Nếu anh muốn dùng Master Plan IEC làm nơi theo dõi (phương án B của file 13), cần hai thứ:

- một QĐ mới thay một phần QD-L1-CHUNG-004;
- chủ sở hữu bảng (tài khoản admin IEC) đồng ý.

Đây là quyết định của anh, không phải vấn đề quyền truy cập.

## 1. Execution Tracker (THUC_THI)

### 1.1 Hai dự án pilot có thông tin theo dõi

| Dự án | Số hành động | Có Decision ID hoặc ghi rõ không có QĐ | Owner đã xác nhận | Hạn là ngày | Status đã ghi | Updated At |
|---|---|---|---|---|---|---|
| PRJ-IEC-DIALOGUES | 18 (11 cũ + 7 mới) | 18/18 | 3 | 7 | 0 | 12/11/2026 cho cả 18 dòng |
| PRJ-IEC-WORKSHOP-ANM | 12 (11 cũ + 1 mới) | 12/12 | 1 | 2 | 3 (In Progress) | 12/11/2026 cho cả 12 dòng |
| **Tổng** | **30** | **30/30** | **4** | **9** | **3** | — |

Nguồn: đọc lại THUC_THI!A1:O32 sau khi sửa (revision Drive 46). Khối tổng hợp của sheet ra cùng số: O3 = 30, O6 = 3, O11 = 26, O12 = 21.

### 1.2 Liên kết hành động với quyết định

| Nhóm liên kết | Số dòng | Dòng |
|---|---|---|
| Liên kết QĐ "Đã thống nhất" trong HO_SO | 14 | ACT-DIALOGUES-001…011 (QĐ-001, -002, -003, -006, -007), -013, -014, -015 (QĐ-001) |
| Liên kết quyết định chưa có hồ sơ được duyệt (nháp hoặc chưa ghi) | 13 | ACT-DIALOGUES-012 (nháp QĐ-008), -018 (4 điểm Day 1 chưa ghi); ACT-WORKSHOP-001…009, -011, -012 (DINH_HUONG_v2 → nháp QD-IEC-WORKSHOP-ANM-001…003) |
| Ghi rõ "Không có QĐ" kèm nguồn hành động | 3 | ACT-DIALOGUES-016, -017; ACT-WORKSHOP-010 |

Các thay đổi trong lần này:

- 2 dòng trước để "—" nay liên kết QĐ-002, QĐ-006 (mục Tiêu chí nêu mốc 25/11, 27/11).
- 11 dòng WORKSHOP trước để "—" nay dẫn tới nơi chứa quyết định và nháp QĐ.

### 1.3 Tám hành động mới (theo file 14 mục 3)

| Action ID | Việc | Decision ID |
|---|---|---|
| ACT-DIALOGUES-012 | Quyết nháp QD-IEC-DIALOGUES-008 (dời hạn đồng hành; tên tiếng Anh Kỳ 1) | QD-IEC-DIALOGUES-008 (nháp, chưa duyệt) |
| ACT-DIALOGUES-013 | Xem 5 điểm BEA tự đề xuất trong hợp đồng Gentech v2; chọn "không hoàn tiền" hay "40 triệu khi không xếp được ghế" | QD-IEC-DIALOGUES-001; chốt chat 12/11 chưa có QĐ |
| ACT-DIALOGUES-014 | Chốt người ký phía Gentech và giấy ủy quyền | như trên |
| ACT-DIALOGUES-015 | Gentech ký hợp đồng và thanh toán | như trên |
| ACT-DIALOGUES-016 | Gửi MOU ONEAI x ISTED và bộ mời đồng hành cho đầu mối One AI | Không có QĐ |
| ACT-DIALOGUES-017 | Lưu PDF hai deck Day 1 vào KET_QUA | Không có QĐ |
| ACT-DIALOGUES-018 | Lập DINH_HUONG_v3 (4 quyết định Day 1; SVF đã xác nhận) | Chưa có QĐ |
| ACT-WORKSHOP-012 | Duyệt nháp QD-IEC-WORKSHOP-ANM-001…003 | Nháp, chờ duyệt |

Cả 8 dòng: Owner = PENDING OWNER CONFIRMATION, Deadline = PENDING DEADLINE CONFIRMATION, Status trống.

### 1.4 Người phụ trách và hạn

- **Owner lấy từ dữ liệu đã có:** chỉ 4 dòng có người đã nhận việc (anh Cường, 11/11, IN-20261110-0019). 26 dòng ghi `PENDING OWNER CONFIRMATION`.
  - Với các dòng mà NHAT_KY nêu anh là người làm (gửi MOU One AI, tải PDF Day 1, duyệt nháp QĐ-008), BEA chỉ ghi điều đó vào Progress Update và chờ anh xác nhận. BEA không tự gán, vì ghi chú cột Owner yêu cầu "chỉ điền khi anh xác nhận".
- **Deadline:**
  - 9 dòng có ngày từ nguồn (giữ nguyên);
  - 2 dòng có hạn điều kiện từ nguồn ("Khi phát sinh", "Sau khi có ngày tổ chức") giữ nguyên;
  - 19 dòng ghi `PENDING DEADLINE CONFIRMATION`.
  - Không đổi hạn theo Bảng giá v2.1, vì nháp QĐ-008 chưa duyệt.
- **Tiến độ hiện tại:**
  - 22 dòng cũ có đoạn "12/11: …" theo nguồn đã tra (NHAT_KY, KET_QUA, hộp thư, Drive).
  - 3 dòng chuyển In Progress, có bằng chứng ở cột Evidence/Result.
  - Không dòng nào chuyển Completed.

## 2. Decision Record v2

| Hồ sơ | Kết quả | Vị trí |
|---|---|---|
| QD-IEC-DIALOGUES-001…007 | Đã đọc toàn văn; trình bày theo khuôn 12 trường. Decision, Options, Assumptions chép nguyên văn từ v1; Actual Outcomes chỉ ghi dữ kiện có nguồn; Lessons Learned = NOT AVAILABLE | File 16, mục A |
| QD-IEC-KE-HOACH-2027-001 v1 | Trình bày lại; trạng thái "Đã thống nhất, lỗi thời một phần" | File 16, mục B1 |
| **QD-IEC-KE-HOACH-2027-001 v2** | **Bản cập nhật chờ duyệt**, gồm 3 thay đổi theo IN-20261106-0016…0018: (1) bỏ nhánh hướng nghiệp THPT; (2) IEC Campus gộp Talents to Business; (3) thêm content channel và nguồn inventory. Giữ nguyên hướng, sản phẩm, điều kiện chỉ tiêu. Quan hệ với v1: v1 sẽ ghi "Đã thay đổi", v2 "Đã thống nhất", đều bằng dòng mới. Bằng chứng là thứ cấp (NHAT_KY, concept v2.1), nên đánh dấu **CẦN XÁC NHẬN**. Actual Outcomes, Lessons Learned = NOT AVAILABLE | File 16, mục B2, B3 |
| QD-IEC-WORKSHOP-ANM-001…003 | 3 nháp mới từ DINH_HUONG_v2 và NHAT_KY 06–07/11; chỗ nguồn không có ghi NOT AVAILABLE | File 16, mục C |
| HO_SO | **Chưa ghi** (việc cập nhật chưa được duyệt). Đã liệt kê đúng các dòng sẽ ghi thêm | File 16, mục D |

Phát hiện khi đọc hồ sơ (file 16, mục E):

- QD-IEC-DIALOGUES-001 ghi bảng giá hiệu lực đến 06/11, nhưng tài liệu 12/11 vẫn chào giá.
- Hợp đồng Gentech v2 trái QD-IEC-DIALOGUES-001 ở điều kiện 40 triệu.
- Tên "Phương án A/B" bị dùng cho hai nghĩa khác nhau.
- Mốc rà lại 06/11 của QĐ-003 đã qua.

## 3. Chạy thử hoạt động

| Hạng mục | Kết quả | Vị trí |
|---|---|---|
| Báo cáo tình trạng ban đầu | Snapshot #1 ngày 12/11 có đủ: tiến độ, trễ hạn (0; 4 dòng hạn 13/11), bị chặn (0; 4 nhóm phụ thuộc), QĐ chưa được thực thi (5 QĐ có hành động, chưa hành động nào có tiến độ ghi nhận), 7 vấn đề cần CEO/COO xử lý. Số đếm khớp khối tổng hợp của sheet | File 17 |
| Quy trình báo cáo hằng tuần | Thứ Hai 16/11, 23/11, 30/11, 07/12; rà 14/12. Gồm 5 nội dung bắt buộc, 7 bước, quy tắc nhãn, chỉ số pilot. Không tự lên lịch, không tạo reminder, không gửi email, không đổi Calendar | File 19 |

## 4. Kiểm soát thay đổi

- Mọi thay đổi trên THUC_THI có trong file 18: 11 mục CL-01 đến CL-11, mỗi mục ghi ô, trước, sau, lý do, căn cứ. Kèm kiểm tra khối tổng hợp trước và sau.
- Thời điểm: 12/11/2026, khoảng 21:45–21:51 giờ VN.
- Khôi phục được: revision 32 (trước) và 46 (sau) trong Lịch sử phiên bản.
- Ghi thêm NHAT_KY_2026-11-12_TASK05_execution-mvp vào PRJ-GLOBAL/NHAT_KY (Doc `1B_kaKlR0N2FaQ-cZdBRkNLQkzc2W8OrlBkwgL5UUZiM`).
- **Không sửa:** Master Plan IEC, HO_SO, DU_AN, LIEN_KET, hồ sơ QĐ trên Drive, code, cấu hình, CLAUDE.md, ask.js, check.js, models.json.
- Không xoá dòng, cột hay tab nào. Không thêm tab.

## 5. Nghiệm thu

| Tiêu chí | Trạng thái | Bằng chứng |
|---|---|---|
| Hai dự án pilot đã có thông tin theo dõi | **COMPLETED** | THUC_THI: 30 dòng (18 DIALOGUES, 12 WORKSHOP-ANM), cả 30 có Updated At 12/11/2026 và Progress Update có nguồn. Đọc lại A1:O32 sau sửa; khối tổng hợp O3 = 30. Revision 46 |
| Mọi hành động có quyết định liên quan đã được liên kết | **PARTIALLY COMPLETED** | 30/30 dòng có Decision ID hoặc ghi rõ "Không có QĐ". 14 dòng liên kết QĐ đã thống nhất. 13 dòng liên kết tới quyết định chưa có hồ sơ được duyệt (nháp QĐ-008; nháp QD-IEC-WORKSHOP-ANM-001…003; 4 điểm Day 1). Hoàn tất khi anh duyệt các nháp ở file 16 mục C và QĐ-008 |
| Các trường thiếu người phụ trách hoặc deadline được nêu rõ | **COMPLETED** | 26 ô `PENDING OWNER CONFIRMATION`; 19 ô `PENDING DEADLINE CONFIRMATION`; 2 hạn có điều kiện giữ nguyên nguồn. Ô O11 (công thức đã sửa) = 26; O12 = 21 |
| Hồ sơ QD-IEC-KE-HOACH-2027-001 được cập nhật hoặc có bản cập nhật chờ duyệt | **COMPLETED** (bản cập nhật chờ duyệt) | File 16, mục B2: nội dung v2 đầy đủ 12 trường; B3: đối chiếu IN-20261106-0016…0018, đánh dấu CẦN XÁC NHẬN; mục D: dòng HO_SO sẽ ghi thêm. HO_SO chưa ghi vì chưa có phê duyệt |
| Có báo cáo snapshot điều hành đầu tiên | **COMPLETED** | File 17, lập từ THUC_THI sau cập nhật; 5 nội dung bắt buộc; số đếm khớp O3–O13 |
| Không có lịch sử hoặc dữ liệu gốc bị ghi đè | **COMPLETED** | Progress Update cũ giữ nguyên văn (đoạn mới thêm vào đầu ô). Không xoá dòng hay cột. Các ô bị thay là nhãn giữ chỗ hoặc dữ liệu quản lý, theo yêu cầu TASK 05, đều có bản trước và sau trong file 18: 29 ô "CHƯA XÁC NHẬN", 13 ô "—", 22 ô Updated At, công thức O11, ghi chú E1, F1. Điểm khôi phục: revision 32. HO_SO, Master Plan, hồ sơ QĐ không bị chạm |
| (Bổ sung) Áp khuôn Decision Record v2 cho các QĐ liên quan | **PARTIALLY COMPLETED** | Đã lập cho QĐ-DIALOGUES-001…007, QĐ-2027-001 (v1 và v2) và 3 nháp WORKSHOP (file 16). Chưa thành hồ sơ chính thức trên Drive và HO_SO; chờ anh duyệt |
| (Bổ sung) Quy trình báo cáo hằng tuần | **PARTIALLY COMPLETED** | Quy trình đã viết (file 19) và đã chạy một lần ở dạng snapshot (file 17). Báo cáo tuần #1 đến hạn 16/11, chưa chạy |
| (Bổ sung) Ghi vào Master Plan IEC | **BLOCKED** | Bị chặn bởi QD-L1-CHUNG-004 (Đã thống nhất): "BEA không ghi vào bảng của IEC". Cần QĐ mới và sự đồng ý của chủ sở hữu bảng. Không phải vấn đề quyền truy cập |
| (Bổ sung) Không sửa code, cấu hình, CLAUDE.md, ask.js, check.js, models.json | **COMPLETED** | Phiên này không truy cập bea-l2. Chỉ ghi vào THUC_THI, 1 Doc NHAT_KY trên Drive và các file .md trong repo |

## 6. Yêu cầu quyền truy cập (một yêu cầu)

**Cần anh cung cấp:** nguyên văn ba dòng **IN-20261106-0016, IN-20261106-0017, IN-20261106-0018** trong sổ input (thư mục `bea-l2` trên máy anh). Anh có thể chép file sổ input của ngày 06/11 lên thư mục BEA_KNOWLEDGE trên Drive, hoặc dán ba dòng vào chat.

**Để làm gì:** đối chiếu nguyên văn trước khi anh duyệt QD-IEC-KE-HOACH-2027-001 v2. Hiện bằng chứng chỉ là bản BEA ghi lại trong NHAT_KY và concept v2.1. Phiên đám mây không đọc được sổ input trên máy.

## 7. Việc chờ anh quyết (không phải quyền truy cập)

1. Trạng thái 4 dòng hạn **13/11** (ACT-DIALOGUES-001, -003, -004; ACT-WORKSHOP-001).
2. Duyệt hoặc không duyệt nháp QD-IEC-DIALOGUES-008. Nếu duyệt, BEA đổi hạn 6 dòng trong THUC_THI và ghi nhật ký thay đổi.
3. Hợp đồng Gentech: điều khoản ghế (không hoàn tiền hay 40 triệu theo QĐ-001); người ký.
4. Duyệt QD-IEC-KE-HOACH-2027-001 v2 và 3 nháp QD-IEC-WORKSHOP-ANM. Sau đó BEA tạo Doc và ghi thêm dòng HO_SO.
5. Owner cho 26 dòng; Project Owner phía IEC của 2 dự án.
6. Xác nhận 3 deck Workshop đã gửi chưa, file lưu ở đâu, để chuyển Completed.
