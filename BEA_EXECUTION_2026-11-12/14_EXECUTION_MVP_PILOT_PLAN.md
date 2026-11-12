# 14 · Execution MVP: kế hoạch chạy thử 4 tuần

- Ngày lập: 12/11/2026. Người lập: Claude, phiên Claude Code đám mây.
- Trạng thái: **đề xuất, chờ anh duyệt.** Chưa sửa Master Plan, chưa ghi HO_SO, chưa sửa THUC_THI trong lần này.
- Căn cứ:
  - QD-L1-CHUNG-003 (Execution MVP ở P1, 2 dự án, 8 tuần);
  - QD-L1-CHUNG-004 (THUC_THI là nguồn chuẩn);
  - QD-L1-CHUNG-005 (IEC là tổ chức pilot);
  - BR & TOM v1.0 mục 4.1 Capability 4, mục 5.3, mục 10.3;
  - file 13 (ánh xạ Master Plan).
- Quy tắc giữ suốt pilot:
  - BEA không tự gán người phụ trách, không tự đặt hạn;
  - không chuyển Completed khi chưa có bằng chứng;
  - không ghi vào Master Plan;
  - không gửi gì ra ngoài;
  - không gọi model ngoài với dữ liệu dự án.

## 0. Quan hệ với lần chạy TASK 04 ngày 10/11/2026

Ngày 10/11, TASK 04 đã chạy trên máy: đề xuất 2 dự án dưới đây, tạo tab THUC_THI với 22 dòng, lập báo cáo tuần 0. Ngày 11/11, anh nhận phụ trách 4 dòng. Kế hoạch này **không tạo lại** THUC_THI. Nó dùng THUC_THI làm hiện trạng và bổ sung những gì đã thay đổi từ 10/11 đến 12/11:

- Bảng giá và đề xuất Kỳ 1 v2.1 đã phát hành với mốc mới.
- Nháp QD-IEC-DIALOGUES-008 chưa được duyệt.
- Có hợp đồng Gentech và MOU One AI.

## 1. Chọn hai dự án

### 1.1 Tiêu chí (chỉ dùng dữ kiện có nguồn, không chấm điểm cảm tính)

| Tiêu chí | Lý do |
|---|---|
| C1 · Là dự án IEC | QD-L1-CHUNG-005: IEC là tổ chức pilot |
| C2 · Có quyết định hoặc định hướng đã chốt sinh ra hành động | QD-L1-CHUNG-003: mọi QĐ có hành động phải có dòng theo dõi |
| C3 · Có mốc thời gian có nguồn trong 4 tuần tới (16/11 – 13/12) | Có việc thật để theo dõi |
| C4 · Có hoạt động trong BEA trong 7 ngày qua (05/11 – 12/11) | Có người đang làm, có dữ liệu cập nhật |
| C5 · Có dòng trong Master Plan (Project List) | Dẫn link sang bảng IEC được |

### 1.2 Đối chiếu năm ứng viên

| Ứng viên | C1 | C2 | C3 | C4 | C5 |
|---|---|---|---|---|---|
| **PRJ-IEC-DIALOGUES** | Có | Có: QD-IEC-DIALOGUES-001…007 Đã thống nhất; nháp 008 | Có: Bảng giá v2.1 ghi 16/11, 25/11; THUC_THI ghi 13/11, 20/11, 25/11, 27/11 | Có: 11/11, 12/11 | Có (STT 1) |
| **PRJ-IEC-WORKSHOP-ANM** | Có | Có: DINH_HUONG_v2 (07/11), **không có QĐ trong HO_SO** | Có: Benson Hunt xác nhận Hoa Sen 13/11, VIFC 20/11 (mốc dự kiến) | Có: 07/11; THUC_THI 11/11 | **Không** |
| PRJ-IEC-KE-HOACH-2027 | Có | Có: QD-IEC-KE-HOACH-2027-001, -002 | Không: chờ anh chọn Phương án A/B; chưa có mốc thực thi | Có: 06/11 | Không |
| PRJ-IEC-BEFORE-YOU-BUILD | Có | Có: QĐ-001…006 (19/10) | NOT AVAILABLE | Không (không có NHAT_KY sau 02/11) | Không |
| Talent to Business (Master Plan STT 2) | Có | NOT AVAILABLE | NOT AVAILABLE | Không có trong BEA | Có |

### 1.3 Kết quả đề xuất

| Mã | Tên | Lý do chọn | Điểm yếu đã biết |
|---|---|---|---|
| **PRJ-IEC-DIALOGUES** | IEC Dialogues, Kỳ 1 | Đạt cả 5 tiêu chí. Có nhiều QĐ nhất, có mốc ký và thanh toán gần nhất, chiếm 5/7 việc trong số đo cơ sở (file 11) | Mốc trong QĐ đang lệch với tài liệu đã phát hành (mục 2.3) |
| **PRJ-IEC-WORKSHOP-ANM** | Workshop an ninh mạng (Benson Hunt × Đại học Hoa Sen, VIFC Fintech Hub) | Đạt C1–C4. Có mốc gần (13/11, 20/11), có hành động rõ từ DINH_HUONG_v2, khác loại với Dialogues (dịch vụ tổ chức cho khách hàng, không phải tài trợ) | Không có trong Project List; quyết định chỉ nằm ở DINH_HUONG_v2, chưa thành QĐ, nên cả 11 dòng có Decision ID "—" |

Cặp này giống đề xuất ngày 10/11. Dữ liệu từ 10/11 đến 12/11 không làm đổi kết quả.

## 2. Các hành động hiện có

Nguồn: tab THUC_THI, BEA_DKB_INDEX, đọc 12/11/2026. Status: cả 22 dòng đang trống (chưa xác nhận). Evidence/Result: cả 22 dòng đang trống.

### 2.1 PRJ-IEC-DIALOGUES (11 dòng)

| Action ID | Action | Decision ID | Owner | Deadline |
|---|---|---|---|---|
| ACT-DIALOGUES-001 | Nhận phản hồi báo ý định của ACB | QD-IEC-DIALOGUES-002 | Anh Cường (11/11) | 13/11/2026 |
| ACT-DIALOGUES-002 | ACB ký thỏa thuận và thanh toán | QD-IEC-DIALOGUES-002 | CHƯA XÁC NHẬN | 20/11/2026 |
| ACT-DIALOGUES-003 | Thôi giữ ghế chuyên môn cho ACB nếu ACB không báo ý định trước 13/11 | QD-IEC-DIALOGUES-002 | Anh Cường (11/11) | 13/11/2026 |
| ACT-DIALOGUES-004 | Nhận phản hồi báo ý định của các ngân hàng nhận bộ đề xuất chung | QD-IEC-DIALOGUES-006 | Anh Cường (11/11) | 13/11/2026 |
| ACT-DIALOGUES-005 | Ngân hàng ký thỏa thuận và thanh toán | QD-IEC-DIALOGUES-006 | CHƯA XÁC NHẬN | 20/11/2026 |
| ACT-DIALOGUES-006 | Trình anh quyết từng trường hợp ngân hàng nhận bộ sau 13/11 | QD-IEC-DIALOGUES-006 | CHƯA XÁC NHẬN | Khi phát sinh |
| ACT-DIALOGUES-007 | Xếp ghế chuyên môn cho đơn vị đã ký theo mức liên quan; không giữ ghế cho ngân hàng chưa ký | QD-IEC-DIALOGUES-001, -006, -007 | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-DIALOGUES-008 | IEC duyệt nội dung demo và tài liệu có ghi tài trợ | — | CHƯA XÁC NHẬN | 25/11/2026 |
| ACT-DIALOGUES-009 | Duyệt nội dung diễn giả ghế chuyên môn | — | CHƯA XÁC NHẬN | 27/11/2026 |
| ACT-DIALOGUES-010 | Tính lại kế hoạch vận hành Kỳ 1 theo mục tiêu khoảng 100 doanh nghiệp | QD-IEC-DIALOGUES-003 | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-DIALOGUES-011 | Soạn Commercial Plan Kỳ 1 bản mới theo giá đã duyệt | QD-IEC-DIALOGUES-001 | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |

### 2.2 PRJ-IEC-WORKSHOP-ANM (11 dòng)

| Action ID | Action | Decision ID | Owner | Deadline |
|---|---|---|---|---|
| ACT-WORKSHOP-001 | Benson Hunt xác nhận chương trình tại Đại học Hoa Sen | — | Anh Cường (11/11) | 13/11/2026 |
| ACT-WORKSHOP-002 | Benson Hunt xác nhận chương trình tại VIFC Fintech Hub | — | CHƯA XÁC NHẬN | 20/11/2026 |
| ACT-WORKSHOP-003 | Dựng deck gửi Benson Hunt | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-004 | Tuỳ biến bản gửi VIFC Fintech Hub | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-005 | Tuỳ biến bản gửi Đại học Hoa Sen | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-006 | Tìm đầu mối VIFC Fintech Hub và đề nghị Hub nhận buổi | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-007 | Chốt cách xử lý thuế GTGT và chứng từ khi IEC xuất hoá đơn cho Benson Hunt | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-008 | Hỏi Benson Hunt: ngôn ngữ trình bày của Tony; buổi trao đổi sau phiên VIFC; nêu tên khách hàng | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-009 | Tony duyệt bộ câu hỏi và phương án của hai chương trình | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-010 | Kiểm tra concept CYBER TRUST TALK v2 đã gửi Vietnix, VNETWORK chưa | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| ACT-WORKSHOP-011 | Thu chi phí tổ chức (100%, một lần) sau khi Hoa Sen hoặc VIFC xác nhận ngày | — | CHƯA XÁC NHẬN | Sau khi có ngày tổ chức |

**Quan sát từ NHAT_KY, chưa ghi vào THUC_THI:**

- ACT-WORKSHOP-003, -004, -005 có đầu ra trong NHAT_KY ngày 07/11: deck gửi Benson Hunt v2; deck gửi Đại học Hoa Sen và VIFC v1, anh chốt "gửi ngay".
- Nhưng 6 file pptx không có trong KET_QUA, và không có bằng chứng đã gửi.
- Theo quy tắc, ba dòng này **chưa được chuyển Completed**. Anh xác nhận và cho biết nơi lưu file thì BEA mới cập nhật.

### 2.3 Lệch mốc cần anh quyết trước tuần 1

| Dòng | Mốc trong THUC_THI (theo QĐ) | Mốc trong tài liệu đã phát hành 12/11 (v2.1) | Căn cứ đổi |
|---|---|---|---|
| ACT-DIALOGUES-001, -003, -004 | 13/11 (báo ý định) | 16/11 | Nháp QD-IEC-DIALOGUES-008, chưa duyệt |
| ACT-DIALOGUES-002, -005 | 20/11 (ký, thanh toán) | 25/11 | Như trên |
| ACT-DIALOGUES-008 | 25/11 (duyệt nội dung demo) | 27/11 (gộp với duyệt nội dung diễn giả) | Như trên; NHAT_KY v2.1: anh chốt "không ghi mốc 27/11 vào QD" |

BEA giữ nguyên mốc cũ trong THUC_THI cho tới khi anh duyệt QĐ-008, hoặc chỉ đạo khác.

## 3. Hành động ứng viên mới (chưa ghi THUC_THI, chờ anh đồng ý)

| Dự án | Hành động ứng viên | Nguồn | Decision ID | Owner | Deadline |
|---|---|---|---|---|---|
| DIALOGUES | Duyệt hoặc không duyệt nháp QD-IEC-DIALOGUES-008 (dời hạn đồng hành Kỳ 1; tên tiếng Anh Kỳ 1) | NHAT_KY 12/11 PROPOSAL-KY1-v2.1, "Việc mở" | — | Anh (người quyết) | CHƯA XÁC NHẬN |
| DIALOGUES | Xem 5 điểm BEA tự đề xuất trong hợp đồng Gentech v2 (Điều 7.2, 7.5, 8.2, 13.2; Phụ lục 01 mục 4) | NHAT_KY 12/11 GENTECH v1, v2 | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| DIALOGUES | Chốt người ký phía Gentech (người đề xuất ký không phải đại diện theo pháp luật, không có giấy ủy quyền) | NHAT_KY 12/11 GENTECH, "Rủi ro đã báo anh" | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| DIALOGUES | Gentech ký hợp đồng và thanh toán | Hợp đồng v2 (KET_QUA 12/11) | (QĐ-008 nếu được duyệt) | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN; Bảng giá v2.1 ghi hạn chung 25/11, hợp đồng chưa ghi ngày |
| DIALOGUES | Gửi MOU và bộ mời đồng hành cho đầu mối One AI (BEA đã soạn email) | NHAT_KY 11/11 MOU-ONEAI | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| DIALOGUES | Lưu PDF hai deck Day 1 vào KET_QUA | NHAT_KY 06/11 VIEC-20261106-04, "Việc mở" | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| DIALOGUES | Lập DINH_HUONG_v3: 4 quyết định Day 1; SVF đã xác nhận tham dự | NHAT_KY 06/11 VIEC-20261106-04; NHAT_KY 12/11 v2.1 | — | CHƯA XÁC NHẬN | CHƯA XÁC NHẬN |
| WORKSHOP | Ghi các quyết định trong DINH_HUONG_v2 thành QĐ trong HO_SO, để 11 dòng có Decision ID | QD-L1-CHUNG-003; file 11, K6 | — | Anh (người duyệt) | CHƯA XÁC NHẬN |

Ghi chú: hợp đồng Gentech có ngày 12/11 và có giá trị lớn nhất trong các việc mới, nhưng chưa có trong THUC_THI. Việc này cho thấy cần quy tắc "mỗi việc mới có hành động thì thêm dòng ngay" (mục 6.3).

## 4. Dữ liệu còn thiếu

| Nhóm | Thiếu gì | Ai có | Ảnh hưởng |
|---|---|---|---|
| Owner | 18/22 dòng chưa có người phụ trách | Anh | Không biết ai báo tiến độ |
| Deadline | 13/22 dòng chưa có ngày cụ thể | Anh hoặc Owner | Không tính được sắp đến hạn hay quá hạn |
| Status | 22/22 dòng trống | Owner | Báo cáo tuần chỉ đếm được "chưa xác nhận" |
| Evidence | 22/22 dòng trống | Owner | Không dòng nào được chuyển Completed |
| DIALOGUES | Thư mời ACB đã gửi chưa, ngày gửi; danh sách ngân hàng đã nhận bộ đề xuất chung, ngày gửi | Anh | ACT-DIALOGUES-001…006 |
| DIALOGUES | Ngày diễn ra Day 1, Day 2 của Kỳ 1 | Anh | Mốc của ACT-DIALOGUES-007, -010 |
| DIALOGUES | Người phụ trách IEC Dialogues phía IEC (Project Owner) | Anh, IEC | Owner của nhiều dòng |
| WORKSHOP | Proposal v5 và deck đã gửi Benson Hunt, Hoa Sen, VIFC chưa; file pptx lưu ở đâu | Anh | ACT-WORKSHOP-001…005 |
| WORKSHOP | Đầu mối VIFC Fintech Hub; đầu mối Đại học Hoa Sen | Anh | ACT-WORKSHOP-006, -001 |
| WORKSHOP | Người xử lý thuế GTGT, chứng từ phía IEC | Anh, IEC | ACT-WORKSHOP-007, -011 |
| Master Plan | Danh mục mã giai đoạn dự án mà Tracking dùng ("1.*", "2.*", "4.*") | IEC | Chỉ cần nếu chọn phương án B |
| Quyền | Anh và IEC cho phép BEA đọc Master Plan (giả định của QD-L1-CHUNG-004, "chưa xác nhận") | Anh, IEC | Cơ sở để BEA đọc hằng tuần |

## 5. Những người cần được xác nhận vai trò

Chỉ liệt kê người hoặc vai trò có trong nguồn. BEA không gán vai trò.

| Người / vai trò | Có trong nguồn | Vai trò cần xác nhận | Theo BR & TOM 7.2 |
|---|---|---|---|
| Anh Cường | Mọi nguồn | (1) Owner của 4 dòng đã nhận 11/11; (2) người quyết các dòng còn lại; (3) người xác nhận báo cáo tuần có ích | BEA Owner; Executive / CEO |
| Tài khoản admin IEC (chủ sở hữu Master Plan) | Drive permissions | Đồng ý cho BEA đọc Master Plan; quyết phương án B nếu muốn | Organization Owner của IEC: NOT AVAILABLE (cần xác nhận người thật) |
| 3 tài khoản writer khác của Master Plan | Drive permissions | Ai trong số này cập nhật tiến độ IEC; có liên quan 2 dự án không | NOT AVAILABLE |
| Project Owner phía IEC của IEC Dialogues | Không có trong nguồn | Cần có để giao Owner cho ACT-DIALOGUES-002, -005, -007…-011 | Project Owner |
| Project Owner phía IEC của Workshop ANM | Không có trong nguồn | Như trên | Project Owner |
| Người điều phối Day 1 (founder Founder Circle); ghế trung lập Phiên 2 | NHAT_KY VIEC-20261106-03, -04 | Chỉ là người tham gia chương trình, không phải Owner hành động. Xác nhận có đưa vào tracker không | Ngoài tổ chức |
| Tony (Benson Hunt) | DINH_HUONG_v2 | Người duyệt ở ACT-WORKSHOP-009 (bên ngoài); BEA chỉ theo dõi phía IEC | Ngoài tổ chức |
| Đại diện ký phía Gentech | NHAT_KY Gentech | Thẩm quyền ký (rủi ro đã báo) | Ngoài tổ chức |
| Đầu mối One AI | NHAT_KY MOU-ONEAI | Người nhận MOU | Ngoài tổ chức |
| Kế toán / người xử lý hoá đơn của IEC | DINH_HUONG_v2 mục 4 (việc còn mở) | Owner của ACT-WORKSHOP-007, -011 | NOT AVAILABLE |

## 6. Cách chạy thử 4 tuần

### 6.1 Thời gian

- QD-L1-CHUNG-003 quy định chạy 8 tuần. TASK 04 yêu cầu 4 tuần.
- **Đề xuất:** 4 tuần là nửa đầu của 8 tuần. Cuối tuần 4 rà lại và quyết chạy tiếp, điều chỉnh hay dừng. Cần anh xác nhận cách hiểu này.
- Tuần chia Thứ Hai – Chủ Nhật, **khớp cột tuần của sheet Tracking trong Master Plan**.

| Tuần | Khoảng ngày | Báo cáo (mẫu file 12) | Mốc có nguồn trong tuần |
|---|---|---|---|
| Tuần 0 (chuẩn bị) | 12/11 – 15/11 | Bản điền thử ngày 12/11 (phụ lục file 12) | THUC_THI: 13/11 × 4 dòng. Hoa Sen: Benson Hunt xác nhận 13/11 (dự kiến) |
| Tuần 1 | 16/11 – 22/11 | Báo cáo #1, Thứ Hai 16/11 | v2.1: báo ý định 16/11. THUC_THI: 20/11 × 3 dòng. VIFC: Benson Hunt xác nhận 20/11 (dự kiến) |
| Tuần 2 | 23/11 – 29/11 | Báo cáo #2, Thứ Hai 23/11 | v2.1: ký và thanh toán 25/11. THUC_THI: 25/11, 27/11 |
| Tuần 3 | 30/11 – 06/12 | Báo cáo #3, Thứ Hai 30/11 | Theo dữ liệu mới |
| Tuần 4 | 07/12 – 13/12 | Báo cáo #4, Thứ Hai 07/12 | Theo dữ liệu mới |
| Rà pilot | Thứ Hai 14/12 | Báo cáo rà 4 tuần | Đo lại theo file 11, cùng định nghĩa |

### 6.2 Nhịp hằng tuần

| Bước | Khi nào | Ai | Làm gì | Ràng buộc |
|---|---|---|---|---|
| 1 | Trong tuần | Owner hoặc anh | Báo tiến độ cho BEA qua chat (trạng thái, việc đã làm, bằng chứng) | Bằng chứng: link file, email, biên bản, ảnh xác nhận |
| 2 | Trong tuần | BEA | Ghi vào THUC_THI đúng lời đã báo, kèm mã IN ở Progress Update; cập nhật Updated At | Chỉ ghi khi có lời của anh hoặc Owner; mỗi lượt ghi anh duyệt như hiện nay |
| 3 | Thứ Hai | BEA | Đọc THUC_THI, HO_SO, NHAT_KY tuần qua, Master Plan (chỉ đọc); lập báo cáo theo mẫu file 12 | Không suy diễn lý do trễ hay mức độ nghiêm trọng |
| 4 | Thứ Hai | Anh | Trả lời các quyết định chờ; xác nhận Owner, hạn; ghi báo cáo "có ích / không có ích" và một dòng lý do | Lời anh là bằng chứng nghiệm thu của QD-L1-CHUNG-003 |
| 5 | Thứ Hai | BEA | Ghi NHAT_KY tuần (số liệu, quyết định, thay đổi) | Theo khuôn NHAT_KY hiện hành |

### 6.3 Quy tắc dữ liệu trong pilot

1. Mỗi QĐ có hành động thì có ít nhất một dòng THUC_THI (gợi ý nguyên tắc trong QD-L1-CHUNG-003).
2. Việc mới phát sinh trong chat mà có hành động: BEA đề xuất dòng mới trong báo cáo tuần kế tiếp. Chỉ ghi khi anh đồng ý.
3. Owner chỉ ghi người đã nhận việc. Chưa có thì ghi "CHƯA XÁC NHẬN".
4. Deadline chỉ ghi ngày có nguồn (QĐ, tài liệu đã phát hành, lời anh). Không có thì ghi "CHƯA XÁC NHẬN" hoặc điều kiện ("Khi phát sinh").
5. Completed chỉ khi cột Evidence / Result có bằng chứng truy được.
6. Đổi hạn phải có nguồn (QĐ mới hoặc lời anh); dòng Progress Update ghi hạn cũ và căn cứ đổi.
7. Không chép dữ liệu nội bộ của Master Plan sang THUC_THI; chỉ dẫn link (QD-L1-CHUNG-004).

### 6.4 Chỉ số theo dõi pilot

Tên chỉ số lấy từ BR & TOM mục 10.3; điều kiện nghiệm thu lấy từ QD-L1-CHUNG-003.

| Chỉ số | Cách đo | Nguồn | Số đầu kỳ (12/11) |
|---|---|---|---|
| Tỷ lệ hoàn thành milestones | Số dòng có hạn trong tuần và Completed có bằng chứng ÷ số dòng có hạn trong tuần | THUC_THI | Chưa có kỳ nào kết thúc |
| Tỷ lệ dự án có KPI và owner rõ ràng (đo ở mức hành động) | Số dòng có Owner đã xác nhận ÷ tổng số dòng; số dòng có Deadline là ngày ÷ tổng | THUC_THI | Owner 4/22; Deadline 9/22 |
| Tỷ lệ phát hiện sớm vấn đề | Số dòng quá hạn hoặc Blocked đã xuất hiện trong mục "sắp đến hạn" hay "cần can thiệp" của báo cáo tuần trước ÷ tổng số dòng quá hạn hoặc Blocked | Báo cáo tuần | Chưa có kỳ |
| Tỷ lệ công việc có thể truy xuất lịch sử và trạng thái | Số dòng có Status không trống và Updated At trong 7 ngày ÷ tổng | THUC_THI | 0/22 có Status |
| Nghiệm thu QD-L1-CHUNG-003: mọi QĐ có hành động đều có dòng | Số QĐ L2 của 2 dự án có hành động mà có dòng ÷ số QĐ có hành động | HO_SO, THUC_THI | DIALOGUES: QĐ-001, 002, 003, 006, 007 có dòng; QĐ-004, 005 chưa xét có hành động không. WORKSHOP: chưa có QĐ |
| Nghiệm thu QD-L1-CHUNG-003: báo cáo tuần | Số báo cáo đã lập; số báo cáo anh ghi "có ích" | NHAT_KY | 0/4 |

### 6.5 Rà cuối tuần 4 (14/12/2026)

- Đo lại các chỉ số ở mục 6.4 và 7 chỉ số của file 11, cùng định nghĩa.
- **Câu hỏi để anh quyết:**
  - (1) chạy tiếp 4 tuần để đủ 8 tuần theo QD-L1-CHUNG-003;
  - (2) điều chỉnh (đổi dự án, đổi trường, đổi nhịp);
  - (3) dừng;
  - (4) có chuyển sang phương án B của file 13 không.
- Đề xuất tiêu chí cho buổi rà (cần anh duyệt):
  - có đủ 4 báo cáo tuần;
  - mọi dòng có hạn trong 4 tuần đều có Status;
  - anh ghi "có ích" cho ít nhất 3/4 báo cáo.

### 6.6 Chi phí và rủi ro

| Mục | Nội dung |
|---|---|
| Chi phí model | 0 đồng. Không gọi model ngoài với dữ liệu dự án (hợp đồng, giá, đối tác) |
| Công sức của anh | NOT AVAILABLE. Đo bằng cách anh ghi số phút mỗi lần cập nhật nếu anh đồng ý |
| R1 · Không có người báo tiến độ | 18/22 dòng chưa có Owner, nên báo cáo chỉ đếm được "chưa xác nhận". Cách giảm: tuần 0 xác nhận Owner trước |
| R2 · Hai nguồn mốc lệch nhau | QĐ cũ và tài liệu v2.1. Cách giảm: quyết QĐ-008 trong tuần 0 |
| R3 · Việc làm ở chat không về THUC_THI | Gentech, One AI là ví dụ. Cách giảm: quy tắc 6.3 mục 2 |
| R4 · Pilot dừng ở mức đếm | Nếu Status không được cập nhật, pilot chỉ chứng minh BEA đếm được, không chứng minh Execute. Cách giảm: buổi rà tuần 4 |

## 7. Những gì đã xác minh, còn thiếu, cần anh phê duyệt

| Đã xác minh (có nguồn) | Còn thiếu | Cần anh phê duyệt trước khi triển khai thật |
|---|---|---|
| Master Plan IEC 11.2026 đúng file trong Gap v1.1 B21; đọc được 7/7 sheet | Danh mục mã giai đoạn dự án IEC; người cập nhật Master Plan | Chọn phương án A (THUC_THI, khuyến nghị) hay B (bổ sung vào Master Plan) — file 13 mục 7 |
| Master Plan không có trường mức hành động; Tracking lỗi toàn bộ | Owner của 18/22 dòng | Hai dự án pilot: PRJ-IEC-DIALOGUES, PRJ-IEC-WORKSHOP-ANM |
| THUC_THI có 22 dòng; 4 Owner; 9 hạn là ngày; 0 Status | Hạn cụ thể của 13/22 dòng | 4 tuần là nửa đầu của 8 tuần theo QD-L1-CHUNG-003; rà ngày 14/12 |
| Mốc v2.1 (16/11, 25/11) khác QĐ-002, QĐ-006 (13/11, 20/11) | Trạng thái và bằng chứng của 4 dòng hạn 13/11 | Duyệt hoặc không duyệt nháp QD-IEC-DIALOGUES-008 trước khi BEA đổi hạn trong THUC_THI |
| Hợp đồng Gentech, MOU One AI chưa có dòng THUC_THI | Đã gửi gì cho ACB, ngân hàng, Benson Hunt, Hoa Sen, VIFC, One AI | Thêm 8 hành động ứng viên ở mục 3 (Owner, hạn để CHƯA XÁC NHẬN) |
| Quyền Drive: anh là writer của Master Plan; connector báo không sửa được | Anh và IEC đã cho phép BEA đọc Master Plan chưa | Nhịp báo cáo Thứ Hai và quy trình mục 6.2 |
| Cột mật khẩu trong sheet Social channel/ Community (BEA không đọc giá trị) | Project Owner phía IEC của 2 dự án | Bộ chỉ số pilot ở mục 6.4 và tiêu chí rà ở mục 6.5 |

**Dừng ở đây.** Không thay đổi Master Plan, THUC_THI, HO_SO cho tới khi anh duyệt.
