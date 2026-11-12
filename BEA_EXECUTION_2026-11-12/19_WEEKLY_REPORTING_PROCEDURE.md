# 19 · Quy trình báo cáo thực thi hằng tuần (Execution MVP)

- Hiệu lực: từ 12/11/2026, trong 4 tuần pilot (16/11 – 13/12/2026), là nửa đầu của 8 tuần theo QD-L1-CHUNG-003.
- Căn cứ:
  - QD-L1-CHUNG-003, -004 (Đã thống nhất);
  - file 14 (phương án pilot, anh duyệt trong TASK 05);
  - file 12 (mẫu báo cáo).
- Nguồn chuẩn: tab THUC_THI trong BEA_DKB_INDEX. Master Plan IEC chỉ đọc.

## 1. Kích hoạt

- Lịch báo cáo: **Thứ Hai** các ngày 16/11, 23/11, 30/11, 07/12/2026; rà pilot Thứ Hai 14/12/2026.
- **BEA không tự lên lịch, không tạo reminder, không gửi email, không thay đổi Calendar.**
- Báo cáo được lập khi anh mở phiên làm việc với BEA vào ngày báo cáo, hoặc nhắn "báo cáo tuần".
- Muốn nhắc tự động (Calendar, email nháp) thì cần anh phê duyệt riêng. Đó là sáng kiến P4-1 trong Gap v1.1.

## 2. Năm nội dung bắt buộc

| # | Nội dung | Định nghĩa | Lấy từ |
|---|---|---|---|
| 1 | Tiến độ | Số dòng theo 4 trạng thái và "chưa xác nhận"; dòng đổi trạng thái trong tuần, kèm bằng chứng | THUC_THI cột G, H, I, J; khối Tổng hợp N:O |
| 2 | Công việc trễ hạn | Deadline là ngày, nhỏ hơn ngày lập, Status ≠ Completed; kèm "sắp đến hạn" 7 ngày tới | THUC_THI cột F, G; ô O9, O10 |
| 3 | Công việc bị chặn | Status = Blocked, kèm điều đang chờ theo lời Owner. Phụ thuộc ghi trong Progress Update chỉ liệt kê, không tự chuyển Blocked | THUC_THI cột G, H |
| 4 | Quyết định chưa được thực thi | QĐ "Đã thống nhất" của 2 dự án có hành động liên kết nhưng chưa hành động nào In Progress hoặc Completed. Kèm QĐ hoặc nháp đang chờ anh duyệt | HO_SO; THUC_THI cột D, G; NHAT_KY |
| 5 | Vấn đề cần CEO/COO xử lý | Dòng thoả điều kiện khách quan: Blocked; quá hạn; sắp đến hạn mà thiếu Owner hoặc Status; Completed thiếu bằng chứng; hai nguồn ghi khác nhau; việc có hành động nhưng chưa có dòng | Toàn bộ nguồn trên |

## 3. Các bước mỗi tuần

| Bước | Ai | Làm gì | Ràng buộc |
|---|---|---|---|
| 1. Báo tiến độ | Owner hoặc anh | Nhắn BEA: trạng thái, việc đã làm, bằng chứng (link file, email, biên bản, ảnh xác nhận) | Không có lời báo thì dòng giữ nguyên |
| 2. Ghi THUC_THI | BEA | Ghi đúng lời đã báo. Thêm đoạn "dd/mm: …" vào **đầu** ô Progress Update, giữ nguyên nội dung cũ; cập nhật Updated At; ghi mã IN | Không tự gán Owner; không tự đặt Deadline; Completed chỉ khi cột I có bằng chứng; đổi hạn phải có nguồn (QĐ mới hoặc lời anh) |
| 3. Đọc dữ liệu | BEA (Thứ Hai) | Đọc THUC_THI, HO_SO, NHAT_KY tuần qua; đọc Master Plan ở chế độ chỉ đọc | Không ghi vào Master Plan |
| 4. Lập báo cáo | BEA | Theo mẫu file 12, đủ 5 nội dung ở mục 2; đối chiếu số đếm với khối Tổng hợp N:O | Không suy diễn lý do trễ hay mức độ nghiêm trọng |
| 5. Giao báo cáo | BEA | Trả báo cáo trong phiên chat; lưu một bản trong repo (BEA_EXECUTION_…); ghi NHAT_KY tuần trên Drive | Không gửi ra ngoài |
| 6. Phản hồi | Anh | Quyết các mục chờ; xác nhận Owner, hạn; ghi "có ích / không có ích" và một dòng lý do | Lời anh là bằng chứng nghiệm thu của QD-L1-CHUNG-003 |
| 7. Ghi nhật ký thay đổi | BEA | Mỗi lần sửa THUC_THI ghi: thời điểm, ô, trước và sau, lý do, Decision ID hoặc phê duyệt (như file 18) | Bắt buộc theo TASK 05 mục 4 |

## 4. Nhãn và quy tắc dữ liệu

- Owner chưa có người nhận việc: `PENDING OWNER CONFIRMATION`.
- Deadline chưa có nguồn: `PENDING DEADLINE CONFIRMATION`. Hạn có điều kiện từ nguồn ("Khi phát sinh", "Sau khi có ngày tổ chức") giữ nguyên.
- Status: Not Started / In Progress / Blocked / Completed. Để trống khi chưa có căn cứ.
- Decision ID: mã QĐ trong HO_SO. Nếu chỉ có nháp QĐ thì ghi kèm "(nháp, chờ duyệt)". Nếu không có QĐ thì ghi "Không có QĐ" và nguồn của hành động.
- Mọi QĐ có hành động phải có ít nhất một dòng. Việc mới phát sinh trong chat mà có hành động: BEA đề xuất dòng mới trong báo cáo tuần kế tiếp, và chỉ ghi khi anh đồng ý.

## 5. Chỉ số theo dõi pilot (đo ở mỗi báo cáo)

| Chỉ số (BR & TOM 10.3) | Cách đo | Đầu kỳ 12/11 |
|---|---|---|
| Tỷ lệ hoàn thành milestones | Số dòng có hạn trong tuần đã Completed có bằng chứng ÷ số dòng có hạn trong tuần | Chưa có tuần nào kết thúc |
| Tỷ lệ dự án có KPI và owner rõ ràng (mức hành động) | Số dòng có Owner đã xác nhận ÷ tổng; số dòng có hạn là ngày ÷ tổng | Owner 4/30; hạn 9/30 |
| Tỷ lệ phát hiện sớm vấn đề | Số dòng quá hạn hoặc Blocked đã nằm trong mục "sắp đến hạn" hay "cần xử lý" của báo cáo trước ÷ tổng số dòng quá hạn hoặc Blocked | Chưa có |
| Tỷ lệ công việc có thể truy xuất lịch sử và trạng thái | Số dòng có Status không trống và Updated At trong 7 ngày ÷ tổng | 3/30 |
| Nghiệm thu QD-L1-CHUNG-003 | Số báo cáo tuần đã lập; số báo cáo anh ghi "có ích" | Snapshot #1 đã lập; 0/4 báo cáo tuần |
