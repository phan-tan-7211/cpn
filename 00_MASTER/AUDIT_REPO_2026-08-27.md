# PHASE 1 — AUDIT REPOSITORY 2026

**TRẠNG THÁI:** CURRENT  
**CẬP NHẬT:** 2026-08-27  
**PHẠM VI:** toàn bộ cây file trên nhánh `master` tại thời điểm audit  
**MỤC ĐÍCH:** xác định rủi ro cấu trúc, nội dung cũ, nguồn tham khảo, mâu thuẫn và các file cần ưu tiên kiểm tra trước khi chuyển repo thành hệ thống vận hành doanh nghiệp.

> Audit này **không phải** là tuyên bố rằng mọi nội dung trong repo đã được xác nhận đúng pháp luật. Ngược lại, file nào chưa được kiểm tra đủ điều kiện áp dụng được xếp `REVIEW` hoặc `REFERENCE`; tài liệu dựa trên văn bản hết hiệu lực được xếp `OBSOLETE`.

---

## 1. KẾT LUẬN NHANH

Repo hiện là một **kho tài liệu phẳng ở root**, chưa có README điều hướng và chưa có cấu trúc SOP/checklist theo nghiệp vụ. Văn bản pháp luật gốc, bài tổng hợp, transcript/video, biểu mẫu, dữ liệu doanh nghiệp và hướng dẫn nghiệp vụ đang nằm lẫn nhau.

### Rủi ro ưu tiên cao

1. **TT58/2026/TT-BTC đang bị diễn giải sai ở nhiều file.** Một số file mô tả TT58 như có một “hệ thống tài khoản kế toán giản lược” bắt buộc và khuyên không được tự thêm/bớt tài khoản. Hướng này cần viết lại: thông tin chính thức của Bộ Tài chính về TT58 nêu doanh nghiệp siêu nhỏ có thể chỉ mở các sổ kế toán cần thiết và **không cần sử dụng hệ thống tài khoản kế toán**; doanh nghiệp có quyền lựa chọn áp dụng chế độ kế toán doanh nghiệp nhỏ và vừa nếu phù hợp.
2. **Tên/mẫu BCTC TT58 cần sửa.** Một số file đang dùng cách gọi và cấu trúc giống chế độ cũ (“Bảng cân đối kế toán”, “thuyết minh BCTC” như một bộ bắt buộc). Cần đối chiếu đúng mẫu và phụ lục TT58 trước khi vận hành.
3. **Dữ liệu hồ sơ doanh nghiệp bị mâu thuẫn giữa các file.** Hồ sơ hiện trạng trong repo ghi chưa có lao động, trong khi một số hướng dẫn TT58 lại giả định khoảng 20 nhân sự. Từ PHASE 3 phải tạo một nguồn sự thật duy nhất và cấm tài liệu nghiệp vụ tự suy đoán dữ liệu doanh nghiệp.
4. **Nhóm hóa đơn theo Nghị định 70/2025 đã lỗi thời từ 01/07/2026.** Điều 43 Nghị định 254/2026/NĐ-CP quy định Nghị định 123/2020/NĐ-CP và Nghị định 70/2025/NĐ-CP hết hiệu lực từ khi NĐ254 có hiệu lực. Các file dùng NĐ70 làm quy trình hiện hành phải là `OBSOLETE`, chỉ giữ để tra cứu lịch sử/chuyển tiếp.
5. **Có nội dung biến transcript/video thành quy định pháp luật.** Ví dụ file xử lý sai sót hóa đơn ghi thời hạn “05 ngày làm việc” nhưng nguồn là video transcript. Không được dùng làm căn cứ vận hành nếu chưa truy được điều/khoản pháp lý hiện hành.
6. **Nhiều liên kết Obsidian cũ đang trỏ tới cấu trúc `ZINITEK_2026/zinitek/90_TAI_LIEU_THAM_KHAO/...` không tồn tại trong repo hiện tại.** Các link phải được sửa dần sang đường dẫn thật của repo.
7. **File thanh toán không dùng tiền mặt có lỗi liên kết căn cứ.** Link có tên file Luật TNDN 67/2025 nhưng nhãn hiển thị là “Luật Thuế GTGT 2024”. Nội dung ngưỡng 5 triệu phải luôn nêu rõ đang xét điều kiện nào (khấu trừ GTGT, chi phí TNDN...), đối tượng, thời kỳ và ngoại lệ.
8. **Ưu đãi TNDN 3 năm không được diễn đạt thành “DN mới nào cũng được miễn”.** NĐ20/2026 quy định ưu đãi cho doanh nghiệp nhỏ và vừa đăng ký kinh doanh lần đầu nhưng có các trường hợp loại trừ; SOP phải chạy decision tree trước khi kết luận.
9. **Khung xử phạt phải cập nhật NĐ291/2026/NĐ-CP.** Văn bản có hiệu lực 21/07/2026 và sửa hệ thống xử phạt thuế/hóa đơn; không được chép mức phạt từ tài liệu cũ mà không đối chiếu.
10. **TNCN 2026 cần bổ sung lớp hướng dẫn hiện hành.** Repo có NĐ253/2026 nhưng audit phát hiện cần đưa Thông tư 87/2026/TT-BTC vào danh mục cần kiểm tra/bổ sung ở PHASE 8 thay vì chỉ dựa vào bài tổng hợp.

---

## 2. VĂN BẢN 2026 ĐÃ XÁC MINH METADATA TỪ NGUỒN CHÍNH THỐNG

| Văn bản | Ngày ban hành | Hiệu lực | Vai trò trong repo | Trạng thái audit |
|---|---:|---:|---|---|
| TT58/2026/TT-BTC | 25/05/2026 | 01/07/2026 | Chế độ kế toán DN siêu nhỏ; áp dụng cho năm tài chính bắt đầu từ/ sau 01/07/2026 theo thông tin Bộ Tài chính | CURRENT (metadata), nội dung hướng dẫn repo: REVIEW |
| NĐ141/2026/NĐ-CP | 29/04/2026 | 01/01/2026 | sửa NĐ68/2026 và NĐ320/2025 về chính sách thuế/TNDN | CURRENT (metadata) |
| NĐ144/2026/NĐ-CP | 05/05/2026 | 20/06/2026 | sửa NĐ181/2025 (đã được NĐ359/2025 sửa) về GTGT | CURRENT (metadata) |
| NĐ20/2026/NĐ-CP | 15/01/2026 | 15/01/2026 | hướng dẫn NQ198/2025; có ưu đãi TNDN cho DNNVV đăng ký lần đầu với điều kiện/loại trừ | CURRENT (metadata) |
| NĐ252/2026/NĐ-CP | 30/06/2026 | 01/07/2026 | hướng dẫn Luật Quản lý thuế | CURRENT (metadata) |
| NĐ253/2026/NĐ-CP | 30/06/2026 | 01/07/2026 | hướng dẫn Luật Thuế TNCN | CURRENT (metadata) |
| NĐ254/2026/NĐ-CP | 30/06/2026 | 01/07/2026 | hóa đơn điện tử, chứng từ điện tử | CURRENT |
| TT89/2026/TT-BTC | 30/06/2026 | 01/07/2026 | khai thuế theo Luật QLT/NĐ252 | CURRENT (metadata) |
| TT91/2026/TT-BTC | 30/06/2026 | 01/07/2026 | hướng dẫn HĐĐT/chứng từ điện tử theo NĐ254 | CURRENT (metadata) |
| NĐ291/2026/NĐ-CP | 21/07/2026 | 21/07/2026 | sửa quy định xử phạt thuế/hóa đơn | CURRENT (metadata) |
| NĐ296/2026/NĐ-CP | 23/07/2026 | 23/07/2026 | sửa NĐ168/2025 về đăng ký doanh nghiệp | CURRENT (metadata) |

> `CURRENT (metadata)` chỉ có nghĩa số hiệu/ngày/hiệu lực/vai trò đã được đối chiếu nguồn chính thức. Trước khi trích điều khoản cụ thể vào SOP vẫn phải kiểm tra đúng điều, khoản, đối tượng và quy định chuyển tiếp.

---

## 3. PHÂN LOẠI FILE HIỆN CÓ

### 3.1. Nhóm pháp lý gốc — giữ lại, chuẩn hóa dần vào `99_PHAP_LY_GOC`

Các file sau là văn bản/copy pháp lý hoặc tài liệu gần nguồn gốc. **Không xóa.** Trạng thái mặc định trong audit là `REVIEW` cho đến khi đối chiếu bản chính thức và xác định phạm vi áp dụng:

- `Luat_108_2025_QH15_Luat_Quan_Ly_Thue.md`
- `Luat_41_2024_QH15_Luat_Bao_Hiem_Xa_Hoi.md`
- `Luat_67_2025_QH15_Luat_Thue_TNDN.md`
- `Luat_Doanh_Nghiep_67_VBHN.md`
- `Nghi_dinh_141_2026_Nd_Cp_Nguong_TNDN_1_Ty.md`
- `Nghi_dinh_144_2026_Nd_Cp_Sua_Doi_GTGT.md`
- `Nghi_dinh_158_2025_Nd_Cp_Huong_Dan_BHXH.md`
- `Nghi_dinh_168_2025_Nd_Cp_Dang_Ky_DN.md`
- `Nghi_dinh_181_2025_Nd_Cp_Huong_Dan_Thue_GTGT.md`
- `Nghi_dinh_20_2026_Nd_Cp_Mien_TNDN.md`
- `Nghi_dinh_252_2026_Nd_Cp_Huong_Dan_Quan_Ly_Thue.md`
- `Nghi_dinh_253_2026_Nd_Cp_Thue_TNCN.md`
- `Nghi_dinh_254_2026_Nd_Cp_Hoa_Don_Dien_Tu.md`
- `nghi_dinh_254_hoa_don_chung_tu_dien_tu.md` — trùng chủ đề; cần chọn một bản chuẩn và giữ bản còn lại làm duplicate/reference
- `Nghi_dinh_288_2026_Nd_Cp_Xu_Phat_Ke_Hoach_Dau_Tu.md`
- `Nghi_dinh_291_2026_Nd_Cp_Xu_Phat_Thue.md`
- `Nghi_dinh_296_2026_Nd_Cp_Sua_Doi_Dang_Ky_DN.md`
- `Nghi_dinh_320_2025_Nd_Cp_Huong_Dan_Thue_TNDN.md`
- `Nghi_quyet_198_2025_QH15_Bai_Bo_Le_Phi_Mon_Bai.md`
- `Thong_Tu_89_2026_Huong_Dan_Khai_Thue.md`
- `Thong_tu_21_2026_Sua_Doi_Huong_Dan_Thue.md`
- `Thong_tu_46_2025_Sua_Doi_Ke_Toan.md`
- `Thong_tu_58_2026_Ke_Toan_DN_Sieu_Nho.md`
- `Thong_tu_90_2026_Dang_Ky_Thue.md`
- `Thong_tu_91_2026_Sua_Doi_QL_Thue_Hoa_Don.md`
- `10_Nghi_Dinh_359_2025_Sua_Doi_GTGT.md`

### 3.2. Hướng dẫn/SOP tổng hợp — `REVIEW` trước khi vận hành

- `00_PHAP_LY_2026_MASTER.md` — khung tốt nhưng đang ở root, chưa có bảng trạng thái file và changelog; sẽ thay bằng MASTER mới ở PHASE 2.
- `checklist.md` — tài liệu quan trọng nhưng trộn hồ sơ DN, pháp lý, checklist và nhận định; có link Obsidian cũ và một số câu tuyệt đối cần sửa.
- `Cam_nang_Ke_toan_Full_Stack_ZINITEK_2026.md` — cần tách thành SOP theo nghiệp vụ, tránh trở thành “quyển sách” duy nhất.
- `01_Hoi_Dap_Thanh_Toan_Khong_Dung_Tien_Mat_GTGT.md` — nội dung có giá trị nhưng cần sửa căn cứ bị gắn nhầm và viết decision tree GTGT/TNDN riêng.
- `02_Huong_Dan_Khai_Thue_GTGT_TT89_2026_DN_Moi.md`
- `03_Hoi_Dap_Mien_Thue_TNDN_3_Nam_DN_Moi_ND20_2026.md`
- `04_Huong_Dan_Che_Do_Ke_Toan_DN_Sieu_Nho_TT58_2026.md` — **REVIEW PRIORITY** do sai cách mô tả hệ thống tài khoản/BCTC.
- `05_Huong_Dan_Tong_Hop_TT58_2026_DN_Sieu_Nho.md` — **REVIEW PRIORITY**; có giả định dữ liệu DN không khớp hồ sơ hiện trạng.
- `13_Lap_So_Sach_Ke_Toan_DN_Sieu_Nho_TT58_2026.md` — **REVIEW PRIORITY**; cùng lỗi hệ thống tài khoản.
- `2026-08-11_Quyet_dinh_ap_dung_che_do_ke_toan_TT58-2026 HƯƠNG DAN.md`
- `TT58_Mau_Bieu_Chi_Tiet.md`
- `09_He_Thong_Ke_Toan_VN_Thay_Doi_2025_2026.md`
- `07_Huong_Dan_Thay_Doi_Che_Do_HDQT_Luat_QL_Thue_Moi.md`
- `cap_nhat_10_diem_moi_thue_ke_toan_01072026.md`
- `tong_hop_12_van_ban_thue_ke_toan_2026.md`
- `Ke_Khai_Thue_Cong_Ty_Moi_Thanh_Lap.md`
- `Ke khai thue DN moi (VAT, TNDN, TSTN).md`
- `Cong_Viec_Ke_Toan_Cong_Ty_Moi_Thanh_Lap.md`
- `Ke toan DN moi thanh lap - Tong quat.md`
- `Quy trình kế toán chuẩn hóa cho Công ty TNHH 1 Thành viên mới thành lập (ngành thương mại, dịch vụ, sản xuất).md`
- `KHI NHẬN VIỆC Ở DOANH NGHIỆP MỚI KẾ TOÁN CẦN LÀM NHỮNG GÌ  - PHẦN 1.md`
- `Nhan viec o DN moi - Ban giao thong tin.md`
- `1 danh_muc_cong_viec_sau_thanh_lap_cong_ty.md`
- `danh_muc_cong_viec_sau_thanh_lap_cong_ty_2026.md`
- `Cac_Cong_Viec_Can_Lam_Cua_Doanh_Nghiep_Moi_Thanh_Lap_Phan_2.md`
- `Cac_Cong_Viec_Can_Lam_Cua_Doanh_Nghiep_Moi_Thanh_Lap_Phan_3.md`
- `DN moi thanh lap - 20 viec phai lam (P1).md`
- `DN moi thanh lap - Phan 2 (Cong viec 8-15).md`
- `DN moi thanh lap - Phan 3 (Cong viec 16-20, Quy che).md`
- `Luu_Y_Doanh_Nghiep_Moi_Thanh_Lap_2026_Tay_Nam_A.md`
- `Cach_Xac_Dinh_DN_Vua_Nho.md`
- `Huong_Dan_Phan_Loai_DN_Vua_Nho.md`
- `Lua chon phuong phap tinh thue GTGT - Truc tiep Khau tru.md`
- `Diem moi thue GTGT 01-07-2025 - Luat 48 - Nghi dinh 181.md`
- `Luat thue GTGT moi 01-07-2025 - Thanh toan khong tien mat.md`
- `Ke khai sai sot GTGT dau vao - Luat 48.md`
- `Chi tieu 34A to khai GTGT 01 - Thong tu 89.md`
- `Dan_Gia_Thue_Moi_Cho_DN_Nho.md`
- `Mien thue TNDN 3 nam - Nghi dinh 20-2026.md`
- `TNCN chua co MST - Giam tru ban than.md`
- `Thue TNCN moi 2026 - Bac thue va giam tru.md`
- `BHXH_An_Sinh_Xa_Hoi.md`
- `DKKD_Dat_Ten_Doanh_Nghiep.md`
- `Phat hoa don sai thoi diem - Nghi dinh 310.md`
- `Thoi diem lap hoa don - Ban day du.md`
- `Thoi diem lap hoa don - Tong hop.md`
- `Ke khai thue HĐ thay the dieu chinh - Ban ban.md`
- `Ke khai thue HĐ thay the dieu chinh - Ban mua.md`
- `Kiem tra file XML hoa don dien tu.md`
- `Uy quyen thanh toan qua tai khoan ca nhan - Rui ro.md`
- `Chi tieu vs Chi phi - Tinh gia thanh.md`
- `Nguyen tac ke toan - Tai san = Nguon von.md`
- `Phuong phap tinh gia xuat kho (BEP, FIFO, LIFO, TB).md`
- `DN xay dung he thong tai khoan rieng (Thay TT 200).md`
- `Co_So_Du_Lieu.md`
- `Tu_Dien_Phap_Ly.md`

### 3.3. Hóa đơn cũ theo NĐ70 — `OBSOLETE`

Các file sau **không được dùng làm SOP hiện hành từ 01/07/2026**:

- `Xu ly sai sot hoa don tu 01-06-2025 - Nghi dinh 70.md`
- `thoi_diem_ky_so_hoa_don_nghi_dinh_70_2025.md`
- `Bien ban xu ly sai sot hoa don.md`

Lý do: NĐ254/2026/NĐ-CP có hiệu lực 01/07/2026 và quy định NĐ123/2020/NĐ-CP, NĐ70/2025/NĐ-CP hết hiệu lực. Các nội dung cũ chỉ giữ để hiểu lịch sử hoặc xử lý giao dịch thuộc thời kỳ cũ/chuyển tiếp nếu có căn cứ.

### 3.4. Tài liệu không phải căn cứ pháp lý cuối cùng — `REFERENCE`

- `Ketoanhibay M.md`
- `Khánh An Ankhanglaw dv kế toán.md`
- `Lê Linh Misa.md`
- `Thanh Thư - Kt Thuận Thiên.md`
- `Trần Tuân.md`
- `kế toán lạc việt.md`
- `Luuvantuan https_thuequanghuy.vn_ BAO GIA DICH VU KT-XUẤT HĐ-BHXH 12.2024.docx (Converted - 2026-08-14 11_45).md`
- `Mẫu_Báo giá DV Kế Toán Công ty Sản Xuất, Xây Dựng, XNK _2026.md`
- `link.md`
- `Chinhsachonline_Doi_Chu_So_Huu_Mien_Thue.md` — có thể dùng để truy dấu câu hỏi/giải đáp, không thay thế điều khoản pháp luật.
- `MOF_Portal_Hoi_Dap_159416.md` — nguồn giải đáp cơ quan có thẩm quyền nhưng chỉ dùng đúng phạm vi câu hỏi, không nâng thành quy tắc chung.
- `MOF_So_Dinh_Danh_Thay_The_MST.md` — cần kiểm tra phạm vi/thời kỳ trước khi vận hành.

### 3.5. Hồ sơ doanh nghiệp — tách khỏi sách luật ở PHASE 3

- `thong_tin_doanh_nghiep.md`

File này là dữ liệu nghiệp vụ/hồ sơ nội bộ, không phải căn cứ pháp lý. PHASE 3 sẽ tạo hồ sơ doanh nghiệp tối giản, có trường `CHƯA XÁC ĐỊNH` cho dữ liệu chưa chốt và không để các file hướng dẫn tự suy đoán trạng thái công ty.

---

## 4. TRÙNG LẶP / CẦN HỢP NHẤT

### Thành lập doanh nghiệp
Có nhiều chuỗi P1/P2/P3 và checklist tổng quát cùng mô tả “việc phải làm sau thành lập”. PHASE 4 sẽ hợp nhất thành một SOP chính + checklist theo thời điểm, giữ các bản cũ làm REFERENCE/OBSOLETE tùy căn cứ.

### TT58/kế toán siêu nhỏ
Ít nhất các file `04_...TT58`, `05_...TT58`, `13_...TT58`, `TT58_Mau_Bieu_Chi_Tiet.md` và quyết định áp dụng đang lặp lại nội dung. PHASE 5 sẽ có một SOP kế toán siêu nhỏ chuẩn và các phụ lục/mẫu riêng.

### Hóa đơn
Có nhiều file về thời điểm lập, ký số, sai sót, điều chỉnh/thay thế, khai thuế bên mua/bên bán. PHASE 9 sẽ hợp nhất thành decision tree theo NĐ254/TT91 và chỉ giữ tài liệu NĐ70 ở khu vực lịch sử.

### GTGT
Các file “điểm mới 01/07/2025”, thanh toán 5 triệu, lựa chọn phương pháp, khai bổ sung và chỉ tiêu tờ khai cần được hợp nhất theo **mục đích sử dụng**: phương pháp tính → đầu vào → đầu ra → thanh toán → khai thuế → sai sót.

---

## 5. QUY TẮC ÁP DỤNG TỪ SAU AUDIT

1. Không file nào được coi là `CURRENT` chỉ vì tên có “2026”.
2. File nghiệp vụ mới phải có header:
   - `TRẠNG THÁI`
   - `CẬP NHẬT`
   - `ĐỐI TƯỢNG ÁP DỤNG`
   - `VĂN BẢN CĂN CỨ`
   - `NGÀY HIỆU LỰC`
3. Quy định có điều kiện phải viết dạng decision tree.
4. Deadline pháp lý phải dẫn điều/khoản; deadline nội bộ phải ghi rõ `DEADLINE NỘI BỘ`.
5. Mức phạt chỉ ghi khi đã kiểm tra văn bản xử phạt hiện hành; chưa chắc thì ghi `Chưa xác định — cần kiểm tra văn bản xử phạt hiện hành.`
6. Video/blog/bài dịch vụ chỉ `REFERENCE`.
7. Không xóa tài liệu cũ có giá trị lịch sử; đánh dấu `OBSOLETE` hoặc chuyển khu vực lịch sử ở phase phù hợp.
8. Khi có xung đột giữa file tổng hợp và văn bản hiện hành, ưu tiên văn bản hiện hành và ghi vào `00_MASTER/CHANGELOG_PHAP_LY.md`.

---

## 6. KẾ HOẠCH SAU AUDIT

- **PHASE 2:** tạo `00_MASTER/00_PHAP_LY_2026_MASTER.md` + `00_MASTER/CHANGELOG_PHAP_LY.md`, lập legal spine và bản đồ trạng thái tài liệu.
- **PHASE 3:** tạo “Hồ sơ doanh nghiệp của tôi” làm single source of truth, không lặp PII không cần thiết trong SOP.
- **PHASE 4–14:** chuyển từng mảng thành SOP/decision tree/checklist theo thứ tự đã thống nhất.

---

## 7. NGUỒN CHÍNH THỐNG ĐÃ DÙNG TRONG PHASE 1

- Cổng văn bản Chính phủ: NĐ20/2026, NĐ141/2026, NĐ144/2026, NĐ252/2026, NĐ253/2026, NĐ254/2026, NĐ291/2026, NĐ296/2026, TT89/2026, TT91/2026.
- Cổng Bộ Tài chính: thông tin chính thức về TT58/2026 và hỏi đáp chính sách về điều kiện thanh toán không dùng tiền mặt.

> Các URL nguồn chính thức sẽ được đưa vào MASTER/CHANGELOG theo từng chủ đề ở PHASE 2 để repo không phụ thuộc vào link video/blog.