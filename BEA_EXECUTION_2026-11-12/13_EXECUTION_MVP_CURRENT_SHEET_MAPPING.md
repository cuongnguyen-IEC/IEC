# 13 · Execution MVP: ánh xạ vào bảng Master Plan IEC hiện tại

- Ngày lập: 12/11/2026. Người lập: Claude, phiên Claude Code đám mây.
- Cách đọc Master Plan: **chỉ đọc** qua connector Google Sheets. Không tạo bản sao, không sửa ô nào.
- Trạng thái: **đề xuất, chờ anh duyệt.** Chưa thay đổi Master Plan, chưa ghi HO_SO.
- Dữ kiện không có trong nguồn ghi `NOT AVAILABLE`.

## 0. Tóm tắt

1. Đã tìm đúng bảng **"Master Plan IEC 11.2026"**, khớp mục B21 của báo cáo Gap v1.1 r2. BEA đọc được toàn bộ 7 sheet.
2. Master Plan **không có trường nào ở mức hành động**. Trong 10 trường của Execution Tracker, chỉ "Project" khớp được (theo tên dự án ở sheet Project List). Không có người phụ trách, hạn, trạng thái, cập nhật tiến độ hay bằng chứng.
3. Sheet Tracking được thiết kế để theo dõi theo tuần (Thứ Hai – Chủ Nhật, 02/11/2026 đến 31/01/2027), nhưng mọi ô tính đều báo `#ERROR!`. Ô không lỗi duy nhất ("Liên hệ trong Master Data" = 5) đang đếm sai: thực tế chỉ có 1 liên hệ, 4 ô còn lại là nhãn.
4. Chưa có dữ liệu tiến độ nào được ghi. Social Log chỉ có dòng tiêu đề; cột "Mục tiêu" ở Tracking để trống.
5. Có **xung đột cần anh quyết.** TASK 04 muốn ưu tiên ánh xạ và bổ sung trường vào workbook Master Plan. QD-L1-CHUNG-004 (Đã thống nhất 10/11/2026) chọn tab THUC_THI trong BEA_DKB_INDEX làm nguồn chuẩn và ghi rõ "BEA không ghi vào bảng của IEC". Mục 7 nêu hai phương án.
6. Tab THUC_THI đã có từ 10/11/2026 (lần chạy TASK 04 trước), gồm 22 dòng của hai dự án. Mục 8 tóm tắt hiện trạng.

## 1. Tài liệu đã xác định

| Mục | Giá trị | Nguồn |
|---|---|---|
| Tên | Master Plan IEC 11.2026 (tên file có dấu cách ở cuối) | Drive metadata |
| Mã Drive | `14EsFUdAKz__zOm1ze3HEoDnCm3_Jgh1ReLp8ZaTeBoU` | Drive metadata |
| Chủ sở hữu | Tài khoản admin IEC | Drive permissions |
| Ngày tạo | 31/10/2026 10:00 (giờ VN) | Drive metadata |
| Sửa lần cuối | 09/11/2026 13:22 (giờ VN), bởi một tài khoản writer khác, không phải anh | Drive metadata |
| Locale, múi giờ | vi_VN, Asia/Saigon | Sheets API |
| Khớp báo cáo v1.1 | B21: "Sheet 'Master Plan IEC 11.2026' (chủ sở hữu admin IEC, sửa 08/11)…" | Gap v1.1 r2 |
| Bảng cùng loại khác (không dùng) | "Master Plan Nhân Sự - 072026", "Master Plan Event 092026" | Drive search |

## 2. Quyền truy cập

| Dữ kiện | Giá trị |
|---|---|
| Danh sách quyền | 1 owner (admin IEC); 4 writer: tài khoản của anh (cuong_nguyen@thdvietnam.com) và 3 tài khoản cá nhân khác |
| Chia sẻ công khai | Không (visibility: PRIVATE) |
| Connector báo quyền sửa cho phiên này | `canEdit = false` |
| Ghi nhận trước đây | NHAT_KY 10/11/2026: "Anh chỉ có quyền xem Master Plan" |

**Điểm lệch cần anh xác nhận.** Danh sách quyền ghi tài khoản của anh là *writer*, nhưng connector báo phiên này không sửa được. Với các file khác, connector cũng báo `canEdit = false` cho file không do connector tạo, nên con số này có thể chỉ phản ánh phạm vi quyền của connector, không phải quyền của anh. Dù đúng trường hợp nào, BEA cũng **không sửa** Master Plan khi chưa có phê duyệt.

## 3. Các sheet và cấu trúc dữ liệu

| # | Sheet | Kích thước lưới | Cấu trúc (tiêu đề cột) | Dữ liệu hiện có | Ghi chú |
|---|---|---|---|---|---|
| 1 | Master | 1009 × 27 | Ma trận đối tác × hạng mục. Cột: MÔ TẢ, HẠNG MỤC, IEC, GOE, Maxrall, Neox, OneAi, Marvelous (Game - VGG), Net Impact. Hàng: TA, KHÁCH HÀNG, SẢN PHẨM, REV MODEL (5 loại doanh thu), SOCIAL CHANNELS, Community, Action (Online/Offline), Data nắm giữ | 22 hàng; hầu hết chỉ điền ở cột IEC | Mô hình kinh doanh, không phải bảng việc |
| 2 | Project List | 1000 × 26 | STT, TÊN PROJECT, MÔ TẢ, BẢN QUYỀN | 5 dự án; STT 6–10 để trống | Không có trạng thái, người phụ trách, hạn |
| 3 | Social channel/ Community | 1001 × 27 | (tiêu đề ở hàng 2) STT, Kênh, Tên trang/Tên group, Link, **Tài khoản/Mật khẩu**, Admin/PIC, Ngày lập, Mục tiêu member/follower, Hiện tại, % đạt mục tiêu, Trạng thái, Ghi chú | BEA **chỉ đọc hàng tiêu đề**, không đọc giá trị | Có cột mật khẩu trong bảng chia sẻ cho 5 tài khoản (xem mục 6) |
| 4 | Partner | 1008 × 26 | STT, PARTNER, PHÂN LOẠI, SẢN PHẨM, PHÂN LOẠI, PROGRAM, TRADE-OFF | 23 đối tác | Có Benson Hunt (#19), DH Hoa Sen (#14), VIFC - Fintech Hub (#23), SIHUB và Startup Vietnam Foundation (PROGRAM = IEC Dialogues) |
| 5 | Master Data | 1000 × 26 | STT, Họ tên, Xưng hô, Tổ chức, Chức vụ, Nhóm data, Dự án liên quan, Nguồn/Kênh, Khu vực, Lĩnh vực, SĐT, Email, Zalo/LinkedIn, Ngày thêm, Tháng thêm, Ghi chú | 1 liên hệ (STT 0); hàng 4–7 cột B là nhãn | Dữ liệu cá nhân; BEA không chép |
| 6 | Tracking | 994 × 26 | Nhóm, Chỉ số, Dòng (Mục tiêu / Thực tế / % hoàn thành), Nguồn dữ liệu, 13 tuần (02/11 → 31/01) | Mọi ô tính `#ERROR!`; cột Mục tiêu trống | Xem mục 5 |
| 7 | Social Log | 1000 × 26 | Ngày ghi nhận, Tên kênh, Dự án, Member/Follower, Số bài đăng trong tuần, Reach, Lượt tương tác, Người ghi, Ghi chú | Chỉ có tiêu đề | Nguồn tiến độ của Tracking, chưa có dòng nào |

## 4. Danh sách dự án / chương trình

### 4.1 Trong Master Plan (sheet Project List)

| STT | TÊN PROJECT | BẢN QUYỀN | Mã BEA tương ứng | Ghi chú |
|---|---|---|---|---|
| 1 | IEC Dialogues | IEC | PRJ-IEC-DIALOGUES | MÔ TẢ trống |
| 2 | Talent to Business | IEC | Không có trong DU_AN | BEA chưa có dữ liệu |
| 3 | Sáng Đèn Program | GOE Alliance | — | Thuộc GOE Alliance, ngoài phạm vi IEC (BR-13) |
| 4 | RE:FORM BUSINESS COMMUNITY | GOE Alliance | — | Như trên |
| 5 | Nền tảng CFN | GOE Alliance | — | Như trên |

**Không xác định được dự án nào "đang hoạt động" từ Master Plan**, vì bảng không có cột trạng thái. Sheet Tracking có công thức `COUNTIF('Project List'!C7:C7,"4.*")` cho "Dự án đang triển khai" và `"1.*"`, `"2.*"` cho "đang trao đổi/đề xuất". Như vậy người thiết kế định dùng mã giai đoạn ở cột C, nhưng cột C hiện là MÔ TẢ. Danh mục mã giai đoạn: NOT AVAILABLE.

### 4.2 Trong BEA (DU_AN và hoạt động gần nhất, đọc 12/11/2026)

| Mã BEA | Có trong Project List? | Hoạt động gần nhất có bằng chứng | Mốc sắp tới có nguồn |
|---|---|---|---|
| PRJ-IEC-DIALOGUES | Có (STT 1) | 12/11: proposal Kỳ 1 v2.1, hợp đồng Gentech | Bảng giá v2.1 đã phát hành: báo ý định 16/11, ký và thanh toán 25/11/2026. QĐ-002, QĐ-006 (Đã thống nhất) còn ghi 13/11 và 20/11 |
| PRJ-IEC-WORKSHOP-ANM | **Không** (Benson Hunt, Hoa Sen, VIFC có ở sheet Partner) | 07/11: deck gửi Hoa Sen và VIFC; 11/11: anh nhận phụ trách ACT-WORKSHOP-001 | DINH_HUONG_v2: Benson Hunt xác nhận Hoa Sen 13/11, VIFC 20/11 (mốc dự kiến) |
| PRJ-IEC-KE-HOACH-2027 | Không | 06/11: concept v2.1 | Chưa có mốc thực thi; chờ anh chọn Phương án A/B |
| PRJ-IEC-BEFORE-YOU-BUILD | Không | QĐ ngày 19/10; không có NHAT_KY sau 02/11 | NOT AVAILABLE |

## 5. Cách cập nhật tiến độ (theo cấu trúc quan sát được)

- **Theo thiết kế.** Người dùng nhập dữ liệu nguồn (ngày chốt hợp tác ở Partner; số member, bài đăng, reach mỗi tuần ở Social Log; ngày thêm liên hệ ở Master Data). Sheet Tracking dùng công thức `COUNTIFS` gom theo tuần Thứ Hai – Chủ Nhật và so với hàng "Mục tiêu" nhập tay.
- **Thực tế (12/11/2026).** Chưa có dữ liệu tiến độ: Social Log trống; cột Mục tiêu trống; mọi ô tính lỗi.
- **Lịch sử sửa.** API chỉ trả 1 bản gộp (31/10/2026), nên không xác định được nhịp cập nhật: NOT AVAILABLE.
- **Quan sát về công thức lỗi.** BEA chỉ ghi nhận, không sửa:
  - công thức trộn kiểu tham chiếu R1C1 (`R7C[0]`) vào công thức A1;
  - tham chiếu tới ô không có dữ liệu tương ứng (`Partner!C18:C18` cho "Ngày chốt hợp tác"; `Partner!C3:C3` cho phân loại "Đối tác hệ sinh thái");
  - tên sheet trong công thức là `'Social channel Community'`, thiếu ký tự "/" so với tên thật;
  - "Liên hệ trong Master Data" dùng `COUNTA('Master Data'!$B$2:$B$1000)`, đếm cả 4 ô nhãn (Partner, Community, Media, Master Data) nên ra 5 thay vì 1.
- **Chiều thời gian.** Tracking chia tuần Thứ Hai – Chủ Nhật. File 14 dùng cùng cách chia tuần để báo cáo BEA khớp với bảng IEC.

## 6. Dữ liệu đã đọc và dữ liệu cố ý không đọc

| Sheet | Đã đọc | Không đọc |
|---|---|---|
| Master, Project List, Partner, Tracking, Social Log | Toàn bộ giá trị; công thức của 8 ô Tracking để tìm nguyên nhân lỗi | — |
| Master Data | Hàng tiêu đề và cột A–B (đếm số liệu) | Không chép SĐT, email vào sản phẩm |
| Social channel/ Community | Chỉ hàng tiêu đề | **Toàn bộ giá trị** (có cột Tài khoản/Mật khẩu) |

**Lưu ý cho anh, ngoài phạm vi Execution MVP:** bảng chia sẻ cho 5 tài khoản có cột "Tài khoản/Mật khẩu". Anh cân nhắc báo IEC chuyển mật khẩu sang công cụ quản lý mật khẩu. BEA không đọc giá trị và không làm gì thêm.

## 7. Ánh xạ 10 trường Execution Tracker

| Trường | Mô tả | Có trong Master Plan? | Vị trí gần nhất trong Master Plan | Có trong THUC_THI? |
|---|---|---|---|---|
| Project ID | Mã dự án | **Không có mã.** Chỉ có tên | `'Project List'!B` (TÊN PROJECT) + `A` (STT) | Có (cột A; cột K "Link bảng IEC") |
| Action ID | Mã hành động | Không | — | Có (B) |
| Action | Việc cần thực hiện | Không | Master hàng "Action" chỉ liệt kê loại hoạt động (Webinar, Workshop…) | Có (C) |
| Decision ID | Quyết định tạo ra hành động | Không | — | Có (D), trỏ HO_SO |
| Owner | Người chịu trách nhiệm | Không ở mức dự án/hành động | Chỉ có "Admin/PIC" ở cấp kênh social | Có (E) |
| Deadline | Hạn hoàn thành | Không | — | Có (F) |
| Status | Not Started / In Progress / Blocked / Completed | Không | Tracking ngầm định mã giai đoạn ở `'Project List'!C`, cột này chưa có | Có (G, có danh sách chọn) |
| Progress Update | Cập nhật tiến độ | Không | — | Có (H) |
| Evidence / Result | Bằng chứng hoặc kết quả | Không | — | Có (I) |
| Updated At | Ngày cập nhật | Không | — | Có (J) |

**Kết luận:** 0/10 trường có ở mức hành động trong Master Plan; 10/10 trường đã có trong THUC_THI. Theo nguyên tắc "ưu tiên cấu trúc hiện tại", hai phương án sau đều không tạo hệ thống mới. A dùng workbook BEA đã có; B bổ sung vào workbook Master Plan.

### 7.1 Phương án A — giữ QD-L1-CHUNG-004 (BEA khuyến nghị cho 4 tuần pilot)

- THUC_THI (BEA_DKB_INDEX) là nguồn chuẩn của hành động phát sinh từ QĐ.
- Master Plan chỉ đọc. Mỗi dòng THUC_THI có cột "Link bảng IEC" trỏ tới dòng tương ứng ở Project List.
- **Không đổi Master Plan, không cần IEC cho phép ghi.**
- Ưu điểm: đúng QĐ đã duyệt; đúng BR-13 (không ghi vào dữ liệu của tổ chức khác); đã chạy từ 10/11.
- Nhược điểm:
  - đội IEC không thấy hành động trong bảng của họ;
  - PRJ-IEC-WORKSHOP-ANM chưa có dòng trong Project List nên không dẫn link được;
  - lệch với ưu tiên của TASK 04.

### 7.2 Phương án B — bổ sung vào workbook Master Plan (theo hướng TASK 04)

**Điều kiện trước khi làm:**

- (1) Anh duyệt.
- (2) Chủ sở hữu (admin IEC) đồng ý.
- (3) Có QĐ mới thay một phần QD-L1-CHUNG-004 ("BEA không ghi vào bảng của IEC").
- (4) Chốt ai ghi vào bảng: đội IEC hay BEA.

**B1 — Tối thiểu: thêm 3 cột vào sheet Project List** (sau cột D):

| Cột mới | Nội dung | Ràng buộc |
|---|---|---|
| E · Mã dự án BEA | PRJ-IEC-… | Chỉ dự án IEC |
| F · Trạng thái dự án | Theo mã giai đoạn mà Tracking đang dùng ("1.", "2.", "4."…) | IEC cung cấp danh mục mã; nếu đặt ở F thì công thức Tracking phải trỏ lại (việc của IEC) |
| G · Người phụ trách dự án | Họ tên | Người được IEC xác nhận; BEA không tự điền |

Thêm 1 dòng "Workshop an ninh mạng – Benson Hunt" nếu IEC coi đây là dự án của IEC.

**B2 — Đầy đủ: thêm sheet mới "Action Tracker" trong Master Plan:**

| Cột | Trường | Kiểu / kiểm tra dữ liệu |
|---|---|---|
| A | Project ID | Chọn từ danh sách mã ở Project List cột E |
| B | Action ID | Văn bản, duy nhất (ACT-…) |
| C | Action | Văn bản |
| D | Decision ID | Văn bản (QD-…), có thể trống nếu hành động không từ QĐ |
| E | Owner | Văn bản; chỉ ghi người đã xác nhận nhận việc |
| F | Deadline | Ngày (dd/mm/yyyy); trống nếu chưa chốt |
| G | Status | Danh sách: Not Started / In Progress / Blocked / Completed |
| H | Progress Update | Văn bản, ghi kèm ngày |
| I | Evidence / Result | Link hoặc mô tả bằng chứng |
| J | Updated At | Ngày |

- Định dạng có điều kiện: tô đỏ khi `G = "Completed"` mà `I` trống.
- Định dạng có điều kiện: tô cam khi `F` đã qua và `G ≠ "Completed"`.

**Rủi ro của B:**

- dữ liệu nằm ở 2 nơi nếu THUC_THI vẫn giữ;
- mã QĐ của BEA xuất hiện trong bảng của IEC (cần anh xác nhận QĐ L2 của dự án IEC được phép hiển thị cho đội IEC);
- bảng đang chia sẻ cho 4 writer, nên ai cũng sửa được trạng thái.

### 7.3 Khuyến nghị

Chạy pilot 4 tuần theo **A**. Xét **B1** ở buổi rà tuần 4 nếu IEC muốn đội IEC cùng thấy và cùng cập nhật. Chỉ làm **B2** khi IEC đồng ý giao người cập nhật. Lý do: A không cần ai thêm phê duyệt ngoài anh và đúng QĐ đã thống nhất; B cần IEC đồng ý và một QĐ mới.

## 8. Hiện trạng tab THUC_THI (đọc 12/11/2026, chỉ đọc)

| Chỉ tiêu | Giá trị | Ghi chú |
|---|---|---|
| Số dòng | 22 (PRJ-IEC-DIALOGUES 11; PRJ-IEC-WORKSHOP-ANM 11) | Tạo 10/11/2026 |
| Owner đã xác nhận | 4 dòng "Anh Cường" (ACT-DIALOGUES-001, -003, -004; ACT-WORKSHOP-001), nhận ngày 11/11 (IN-20261110-0019) | 18 dòng "CHƯA XÁC NHẬN" |
| Deadline là ngày cụ thể | 9 dòng (13/11 × 4; 20/11 × 3; 25/11; 27/11) | 13 dòng chưa phải ngày cụ thể |
| Status | 22 dòng trống (khối Tổng hợp đếm 22 "Chưa xác nhận trạng thái") | BEA không tự đặt trạng thái |
| Evidence / Result | 22 dòng trống | Không có dòng Completed |
| Link bảng IEC | 11 dòng "Project List: IEC Dialogues"; 11 dòng "Không có trong bảng IEC" | Đúng QD-L1-CHUNG-004 |
| Khối Tổng hợp (N:O) | Sắp đến hạn (7 ngày) = 4; Quá hạn = 0; Thiếu Owner = 18; Completed chưa có bằng chứng = 0 | Công thức trong sheet |

**Điểm cần xử lý trước tuần 1 (chưa sửa, chờ anh):**

1. Hạn của ACT-DIALOGUES-001 đến -005 và -008 đang theo QĐ-002, QĐ-006 (13/11, 20/11, 25/11). Bảng giá và đề xuất Kỳ 1 v2.1 đã phát hành ngày 12/11 ghi 16/11, 25/11, 27/11. Nháp QD-IEC-DIALOGUES-008 chưa duyệt. Khi anh duyệt QĐ-008, BEA mới đổi hạn trong THUC_THI.
2. Có việc mới từ 11–12/11 chưa có dòng: ký hợp đồng Gentech; gửi MOU và email cho One AI. Xem file 14, mục 3. BEA không tự gán người phụ trách hay hạn.

## 9. Nguồn

- Master Plan IEC 11.2026 (`14EsFUdAKz__zOm1ze3HEoDnCm3_Jgh1ReLp8ZaTeBoU`): 7 sheet, metadata, danh sách quyền, lịch sử sửa, công thức Tracking.
- BEA_DKB_INDEX (`1JDRgM7BusKt908uSfHHkx5A0Wk1UQ-JxRhJ9dhyJaS4`): THUC_THI, DU_AN, HO_SO.
- QD-L1-CHUNG-003 (`1QbxFqA6QOwbjf1wduueWQ007RXb8h-609vEqB_6q3aQ`), QD-L1-CHUNG-004 (`1QSqUyyz9kYKM_FVsFs6hPr8boIk71x1rvxkRPTGJx74`).
- Gap v1.1 r2 (`1jvgKbFvQg2ULLJ8NEeGsNqNlKtoRI3OflJ_kHQtsHQM`): B21, P1-2.
- IEC_Dialogues_Bang_gia_Ky_1_v2.1.pdf (`1K1iMD0-3LIirt11Ut_r45TEfzdCh-Xun`); NHAT_KY_2026-11-12_PROPOSAL-KY1-v2.1.
- DINH_HUONG_v2 của PRJ-IEC-WORKSHOP-ANM (`1MP8bNMQPYbJ0x5L9Ompb4sSRbEhmf4BUdAwfr3t2TTc`).
