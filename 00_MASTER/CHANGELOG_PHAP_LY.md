# CHANGELOG PHÁP LÝ

**TRẠNG THÁI:** CURRENT  
**CẬP NHẬT:** 2026-08-27  
**MỤC ĐÍCH:** ghi lại **vì sao** nội dung vận hành trong repo thay đổi khi pháp luật thay đổi hoặc khi phát hiện hướng dẫn cũ/sai phạm vi.

> Changelog không thay thế việc đọc văn bản gốc. Mỗi entry phải chỉ ra văn bản, hiệu lực, tác động và file/SOP cần sửa.

---

## 2026-08-27 — PHASE 2: XÂY MASTER 2026

### 1. Bổ sung chuỗi sửa đổi thuế GTGT năm 2026

**Văn bản:** Luật 149/2025/QH15  
**Ban hành:** 11/12/2025  
**Hiệu lực:** 01/01/2026  
**Tác động:** sửa Luật Thuế GTGT 48/2024/QH15.  
**Repo bị ảnh hưởng:** toàn bộ file GTGT đang chỉ viện dẫn Luật 48/2024 + NĐ181 mà không kiểm tra luật sửa đổi.  
**SOP cần sửa:** PHASE 6 — GTGT.

### 2. Bổ sung Luật 09/2026/QH16 vào Legal Spine

**Văn bản:** Luật 09/2026/QH16  
**Ban hành:** 24/04/2026  
**Hiệu lực:** 24/04/2026  
**Tác động:** sửa một số điều của pháp luật về TNCN, GTGT, TNDN và TTĐB.  
**Repo bị ảnh hưởng:** GTGT, TNDN, TNCN; các bài tổng hợp chỉ nhìn văn bản gốc trước 24/04/2026 đều phải kiểm tra lại.  
**SOP cần sửa:** PHASE 6, 7, 8.

### 3. Phát hiện thiếu Thông tư hướng dẫn TNDN hiện hành

**Văn bản:** TT20/2026/TT-BTC  
**Ban hành:** 12/03/2026  
**Hiệu lực:** 12/03/2026  
**Tác động:** hướng dẫn chi tiết Luật TNDN 67/2025 và NĐ320/2025.  
**Repo bị ảnh hưởng:** nhóm TNDN hiện có Luật/NĐ nhưng chưa có file gốc TT20.  
**SOP cần sửa:** PHASE 7.  
**Việc cần làm:** bổ sung bản nguồn chính thức vào `99_PHAP_LY_GOC` khi chuẩn hóa kho pháp lý.

### 4. Phát hiện thiếu Thông tư hướng dẫn TNCN hiện hành

**Văn bản:** TT87/2026/TT-BTC  
**Ban hành:** 30/06/2026  
**Hiệu lực:** 01/07/2026  
**Tác động:** hướng dẫn Luật TNCN và NĐ253/2026.  
**Repo bị ảnh hưởng:** các file TNCN hiện không được coi là CURRENT cho tới khi đối chiếu TT87 + Luật 09/2026.  
**SOP cần sửa:** PHASE 8.  
**Việc cần làm:** bổ sung bản nguồn chính thức vào `99_PHAP_LY_GOC`.

### 5. Đưa NĐ245/2026 vào hệ thống dưới dạng chính sách có điều kiện

**Văn bản:** NĐ245/2026/NĐ-CP  
**Ban hành/hiệu lực:** 27/06/2026  
**Tác động:** gia hạn thời hạn nộp một số nghĩa vụ GTGT/TNDN/TNCN/tiền thuê đất trong năm 2026 cho đối tượng đáp ứng điều kiện.  
**Nguyên tắc repo:** không thay deadline chuẩn bằng deadline gia hạn nếu chưa xác định doanh nghiệp thuộc đối tượng.  
**SOP cần sửa:** PHASE 6, 7, 8 và checklist kỳ hạn PHASE 13.

### 6. Xác nhận BHXH backbone hiện hành

**Văn bản:** Luật 41/2024/QH15  
**Ban hành:** 29/06/2024  
**Hiệu lực:** 01/07/2025

**Văn bản:** NĐ158/2025/NĐ-CP  
**Ban hành:** 25/06/2025  
**Hiệu lực:** 01/07/2025

**Tác động:** PHASE 10 phải viết decision tree, không sử dụng câu tuyệt đối “giám đốc luôn phải đóng BHXH”.

---

## 2026-08-27 — PHASE 1: AUDIT REPO

### 1. NĐ254/2026 thay khung hóa đơn cũ

**Văn bản mới:** NĐ254/2026/NĐ-CP  
**Ban hành:** 30/06/2026  
**Hiệu lực:** 01/07/2026  
**Văn bản cũ hết hiệu lực theo Điều 43:** NĐ123/2020/NĐ-CP và NĐ70/2025/NĐ-CP (cần vẫn đọc điều khoản chuyển tiếp cho trường hợp tương ứng).  
**Repo bị ảnh hưởng:**

- `Xu ly sai sot hoa don tu 01-06-2025 - Nghi dinh 70.md`
- `thoi_diem_ky_so_hoa_don_nghi_dinh_70_2025.md`
- `Bien ban xu ly sai sot hoa don.md`
- các bài khác về thời điểm lập/ký/sai sót hóa đơn phải rà soát ở PHASE 9.

**Đã xử lý:** ba file trên đã được gắn `OBSOLETE`, giữ nguyên phần nội dung lịch sử; không xóa dữ liệu.

### 2. Hướng dẫn TT58 trong repo có lỗi khái niệm

**Văn bản:** TT58/2026/TT-BTC  
**Ban hành:** 25/05/2026  
**Hiệu lực:** 01/07/2026  
**Tác động:** một số file trong repo mô tả “hệ thống tài khoản kế toán giản lược” như hệ thống bắt buộc và dùng cấu trúc BCTC theo cách cần kiểm tra lại. Thông tin chính thức Bộ Tài chính nêu DN siêu nhỏ có thể chỉ mở sổ cần thiết và không cần sử dụng hệ thống tài khoản kế toán.

**Repo bị ảnh hưởng:**

- `04_Huong_Dan_Che_Do_Ke_Toan_DN_Sieu_Nho_TT58_2026.md`
- `05_Huong_Dan_Tong_Hop_TT58_2026_DN_Sieu_Nho.md`
- `13_Lap_So_Sach_Ke_Toan_DN_Sieu_Nho_TT58_2026.md`
- `TT58_Mau_Bieu_Chi_Tiet.md`
- `2026-08-11_Quyet_dinh_ap_dung_che_do_ke_toan_TT58-2026 HƯƠNG DAN.md`

**Trạng thái:** REVIEW PRIORITY.  
**SOP cần sửa:** PHASE 5.

### 3. Phát hiện mâu thuẫn dữ liệu doanh nghiệp

**Vấn đề:** hồ sơ/checklist hiện trạng trong repo ghi chưa có lao động, trong khi một số hướng dẫn TT58 tự giả định khoảng 20 nhân sự.  
**Tác động:** có thể dẫn tới phân loại doanh nghiệp sai và áp sai chế độ kế toán.  
**SOP cần sửa:** PHASE 3 tạo một nguồn sự thật duy nhất; PHASE 5 chỉ đọc dữ liệu từ hồ sơ đó.

### 4. Phát hiện biến nguồn tham khảo thành quy định

**Vấn đề:** một số file hóa đơn lấy video/transcript làm nguồn nhưng ghi thành deadline/nghĩa vụ pháp lý, ví dụ “05 ngày làm việc”.  
**Tác động:** nguy cơ vận hành theo một thời hạn không có căn cứ hiện hành.  
**Đã xử lý:** gắn cảnh báo `OBSOLETE`; mọi mức phạt/deadline sau này phải truy điều/khoản.

### 5. Phát hiện link nội bộ hỏng và sai nhãn căn cứ

**Vấn đề:** nhiều link Obsidian trỏ tới cấu trúc cũ `ZINITEK_2026/zinitek/...` không tồn tại trong repo.  
**Vấn đề cụ thể:** `01_Hoi_Dap_Thanh_Toan_Khong_Dung_Tien_Mat_GTGT.md` có link tên file Luật TNDN 67/2025 nhưng nhãn hiển thị “Luật Thuế GTGT 2024”.  
**Tác động:** người vận hành có thể tra nhầm căn cứ.  
**SOP cần sửa:** PHASE 6 và công việc chuẩn hóa link theo từng phase.

---

# TEMPLATE ENTRY MỚI

```markdown
## YYYY-MM-DD — [Tên thay đổi]

**Văn bản:** ...
**Số hiệu:** ...
**Ngày ban hành:** ...
**Ngày hiệu lực:** ...
**Văn bản sửa/thay thế:** ...
**Điều khoản ảnh hưởng:** ...
**Repo file bị ảnh hưởng:** ...
**SOP cần sửa:** ...
**Trạng thái xử lý:** PENDING / DONE
**Ghi chú chuyển tiếp/đối tượng:** ...
```

**Không ghi “đã cập nhật toàn bộ” nếu chưa thực sự rà soát toàn bộ file bị ảnh hưởng.**