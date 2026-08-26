# 00 — PHÁP LÝ 2026 MASTER

**TRẠNG THÁI:** CURRENT  
**CẬP NHẬT:** 2026-08-27  
**ĐỐI TƯỢNG ÁP DỤNG:** doanh nghiệp tại Việt Nam; hồ sơ vận hành hiện khai báo thuộc nhóm doanh nghiệp siêu nhỏ, nhưng tiêu chí phân loại phải được kiểm tra lại khi dữ liệu doanh thu/lao động thay đổi  
**VĂN BẢN CĂN CỨ:** xem Legal Spine bên dưới  
**NGÀY HIỆU LỰC:** theo từng văn bản; không dùng một ngày chung cho toàn bộ hệ thống

> Đây là **bản đồ điều hành pháp lý**, không phải một “cuốn sách luật”. Mỗi SOP phải đi từ: **luật → điều kiện áp dụng → việc phải làm → người làm → thời hạn → chứng từ → nơi lưu → kiểm tra → xử lý sai sót**.
>
> Repo này nhằm giảm rủi ro tuân thủ; **không tuyên bố và không thể bảo đảm 100% doanh nghiệp sẽ không bị xử phạt**.

---

## 1. CÁCH DÙNG MASTER

Khi cần trả lời một câu hỏi vận hành, làm theo thứ tự:

1. Xác định **giao dịch/sự kiện** đang xảy ra.
2. Xác định **thời điểm** phát sinh.
3. Xác định **đối tượng** và điều kiện áp dụng.
4. Tra **Legal Spine** để biết văn bản gốc + văn bản sửa đổi hiện hành.
5. Mở SOP tương ứng.
6. Nếu SOP là `REVIEW`, **không dùng như kết luận pháp lý cuối cùng**.
7. Nếu có xung đột giữa SOP và văn bản hiện hành: **ưu tiên văn bản hiện hành** và ghi thay đổi vào `CHANGELOG_PHAP_LY.md`.

---

## 2. TRẠNG THÁI TÀI LIỆU

| Trạng thái | Dùng thế nào |
|---|---|
| 🟢 `CURRENT` | Đã kiểm tra đủ để dùng trong phạm vi ghi rõ tại file. |
| 🟡 `REVIEW` | Có giá trị tham khảo nhưng còn điểm phải đối chiếu/cập nhật trước khi vận hành. |
| 🔴 `OBSOLETE` | Không dùng làm căn cứ nghiệp vụ hiện tại; chỉ giữ lịch sử/chuyển tiếp. |
| ⚪ `REFERENCE` | Video, bài viết, transcript, báo giá, kinh nghiệm, giải đáp có phạm vi hẹp; không phải căn cứ pháp lý cuối cùng. |

**Không được gắn `CURRENT` chỉ vì tên file có “2026”.**

---

## 3. HỒ SƠ VẬN HÀNH CỦA DOANH NGHIỆP — CÁC GIẢ ĐỊNH ĐƯỢC PHÉP

Từ dữ liệu đã có trong repo và yêu cầu vận hành:

- Doanh nghiệp được thành lập và hoạt động tại Việt Nam.
- Hồ sơ hiện khai báo doanh nghiệp thuộc nhóm **doanh nghiệp siêu nhỏ**.
- Có hoạt động mua hàng từ Trung Quốc hoặc dự kiến phát sinh.
- Có thể phát sinh hai mô hình logistics hoàn toàn khác nhau:
  - **A — Doanh nghiệp trực tiếp nhập khẩu.**
  - **B — Đơn vị logistics/nhà nhập khẩu đứng tên nhập khẩu, sau đó bán hàng trong nước cho doanh nghiệp.**
- Doanh nghiệp bán hàng trong nước.

**Cấm suy diễn:** A và B không được dùng chung một bộ chứng từ/hải quan/thuế/giá vốn nếu pháp lý và quyền sở hữu khác nhau.

Các dữ liệu có thể thay đổi như người đại diện, nhân sự, ngân hàng, phương pháp GTGT, trạng thái chữ ký số, HĐĐT… phải lấy từ **Hồ sơ doanh nghiệp của tôi** ở PHASE 3, không sao chép rải rác vào SOP.

---

# 4. LEGAL SPINE — HỆ THỐNG VĂN BẢN HIỆN HÀNH CẦN TRA

`CURRENT` trong bảng này có nghĩa văn bản đang là một mắt xích hiện hành/đã được xác minh metadata tại ngày cập nhật. Khi áp dụng một điều khoản cụ thể vẫn phải kiểm tra điều, khoản, chuyển tiếp, đối tượng và kỳ tương ứng.

## 4.1. Kế toán doanh nghiệp siêu nhỏ

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **TT58/2026/TT-BTC** — ban hành 25/05/2026, hiệu lực 01/07/2026 | Chế độ kế toán DN siêu nhỏ; áp dụng cho năm tài chính bắt đầu từ hoặc sau 01/07/2026 theo thông tin chính thức của Bộ Tài chính | 🟢 CURRENT |
| TT132/2018/TT-BTC | Chế độ cũ cho DN siêu nhỏ | 🔴 HISTORICAL/OBSOLETE cho kỳ thuộc phạm vi TT58 |

### Điểm kiểm soát bắt buộc

- TT58 **không được diễn giải thành “hệ thống tài khoản giản lược bắt buộc”**. Thông tin chính thức Bộ Tài chính nêu DN siêu nhỏ có thể chỉ mở các sổ cần thiết và **không cần sử dụng hệ thống tài khoản kế toán**.
- DN siêu nhỏ có thể lựa chọn chế độ kế toán DN nhỏ và vừa nếu phù hợp theo quy định.
- Các file `04_...TT58`, `05_...TT58`, `13_...TT58` hiện là **REVIEW PRIORITY** cho đến PHASE 5.
- Phải tách **chế độ kế toán** khỏi **nghĩa vụ thuế**.

---

## 4.2. Quản lý thuế / khai thuế / đăng ký thuế

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **Luật 108/2025/QH15** | Luật Quản lý thuế mới; hiệu lực 01/07/2026 | 🟢 CURRENT |
| **NĐ252/2026/NĐ-CP** | Hướng dẫn Luật Quản lý thuế; hiệu lực 01/07/2026 | 🟢 CURRENT |
| **TT89/2026/TT-BTC** | Khai thuế; hiệu lực 01/07/2026 | 🟢 CURRENT |
| **TT90/2026/TT-BTC** | Đăng ký thuế; ban hành 30/06/2026, hiệu lực 01/07/2026 | 🟢 CURRENT |

### Kiểm soát

Không viết “mọi DN khai quý” hoặc “mọi DN khai tháng”. Kỳ khai phải xác định theo sắc thuế, đối tượng, điều kiện và kỳ thực tế.

---

## 4.3. Thuế GTGT

### Chuỗi luật phải đọc theo thứ tự sửa đổi

1. **Luật 48/2024/QH15 — Thuế GTGT** (nền tảng, hiệu lực 01/07/2025).
2. **Luật 149/2025/QH15** — sửa Luật GTGT, ban hành 11/12/2025, hiệu lực 01/01/2026.
3. **Luật 09/2026/QH16** — sửa đồng thời TNCN, GTGT, TNDN, TTĐB; ban hành và hiệu lực 24/04/2026.
4. **NĐ181/2025/NĐ-CP** — hướng dẫn GTGT.
5. **NĐ359/2025/NĐ-CP** — sửa NĐ181.
6. **NĐ144/2026/NĐ-CP** — tiếp tục sửa NĐ181; ban hành 05/05/2026, hiệu lực 20/06/2026.

### Cổng quyết định bắt buộc

**Khi thấy con số “5 triệu” không được kết luận ngay.** Phải hỏi:

```text
Đang kiểm tra điều kiện gì?
        ↓
Khấu trừ GTGT đầu vào? ──→ kiểm tra Luật GTGT + NĐ181 và các sửa đổi
        │
        └─ Chi phí được trừ TNDN? ──→ kiểm tra Luật TNDN + NĐ320 và các sửa đổi
```

Sau đó mới xác định:

- tổng giá thanh toán nào được xét;
- hình thức thanh toán;
- trường hợp trả chậm/trả góp;
- bù trừ/cấn trừ/ủy quyền;
- nhập khẩu;
- ngoại lệ;
- thời điểm phải có chứng từ thanh toán.

**Không được viết:** “Trên 5 triệu bắt buộc chuyển khoản” như một quy tắc chung cho mọi mục đích.

---

## 4.4. Thuế TNDN

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **Luật 67/2025/QH15** | Luật TNDN nền tảng; hiệu lực 01/10/2025 | 🟢 CURRENT, đọc cùng luật sửa đổi |
| **Luật 09/2026/QH16** | Sửa một số quy định TNDN; hiệu lực 24/04/2026 | 🟢 CURRENT amendment |
| **NĐ320/2025/NĐ-CP** | Hướng dẫn Luật TNDN | 🟢 CURRENT, đọc cùng sửa đổi |
| **NĐ141/2026/NĐ-CP** | Sửa NĐ320 và chính sách liên quan năm 2026 | 🟢 CURRENT |
| **TT20/2026/TT-BTC** | Hướng dẫn chi tiết Luật TNDN/NĐ320; ban hành + hiệu lực 12/03/2026 | 🟢 CURRENT — **repo đang thiếu file gốc** |
| **NĐ20/2026/NĐ-CP** | Chính sách theo NQ198/2025; có ưu đãi TNDN cho DNNVV đăng ký lần đầu nhưng có điều kiện/loại trừ | 🟢 CURRENT, CONDITIONAL |

### Cổng quyết định miễn TNDN 3 năm

Không kết luận “DN mới = miễn 3 năm”. Phải xác định ít nhất:

```text
Có thuộc DNNVV theo tiêu chí pháp luật?
        ↓
Có phải đăng ký kinh doanh lần đầu?
        ↓
Có rơi vào trường hợp loại trừ tại NĐ20/2026?
        ↓
Khoản thu nhập đang xét có thuộc diện được hưởng?
        ↓
Xác định kỳ bắt đầu ưu đãi và chứng từ chứng minh
```

PHASE 7 phải dẫn đúng điều/khoản trước khi biến thành checklist.

---

## 4.5. Thuế TNCN

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **Luật 109/2025/QH15 — Thuế TNCN** | Luật mới, hiệu lực 01/07/2026 | 🟢 CURRENT, đọc cùng sửa đổi |
| **Luật 09/2026/QH16** | Sửa một số quy định TNCN trước thời điểm Luật 109 có hiệu lực | 🟢 CURRENT amendment |
| **NĐ253/2026/NĐ-CP** | Hướng dẫn Luật TNCN; hiệu lực 01/07/2026 | 🟢 CURRENT |
| **TT87/2026/TT-BTC** | Hướng dẫn chi tiết Luật TNCN/NĐ253; ban hành 30/06/2026, hiệu lực 01/07/2026 | 🟢 CURRENT — **repo đang thiếu file gốc** |

**Không dùng biểu thuế/giảm trừ cũ cho kỳ 2026 nếu pháp luật mới đã áp dụng cho kỳ đó.**

---

## 4.6. Hóa đơn điện tử / chứng từ điện tử

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **NĐ254/2026/NĐ-CP** | Khung HĐĐT/chứng từ điện tử mới; hiệu lực 01/07/2026 | 🟢 CURRENT |
| **TT91/2026/TT-BTC** | Hướng dẫn NĐ254; hiệu lực 01/07/2026 | 🟢 CURRENT |
| NĐ123/2020/NĐ-CP | Khung cũ | 🔴 OBSOLETE từ 01/07/2026, trừ nội dung chuyển tiếp mà NĐ254 cho phép |
| NĐ70/2025/NĐ-CP | Sửa khung cũ | 🔴 OBSOLETE từ 01/07/2026, trừ việc tra cứu giao dịch/thời kỳ lịch sử và chuyển tiếp nếu có |

### Quy tắc vận hành

- Không dùng quy trình “thông báo phát hành rồi chờ duyệt” nếu quy định hiện hành không yêu cầu như vậy.
- Xử lý sai sót, điều chỉnh, thay thế, thời điểm lập, ký số, truyền dữ liệu phải viết lại theo NĐ254 + TT91 ở PHASE 9.
- Ba file NĐ70/video đã được gắn `OBSOLETE` trong PHASE 1.

---

## 4.7. BHXH / lao động

| Văn bản | Vai trò | Trạng thái |
|---|---|---|
| **Luật 41/2024/QH15 — BHXH** | Nền tảng BHXH; ban hành 29/06/2024, hiệu lực 01/07/2025 | 🟢 CURRENT |
| **NĐ158/2025/NĐ-CP** | Hướng dẫn BHXH bắt buộc; ban hành 25/06/2025, hiệu lực 01/07/2025 | 🟢 CURRENT |

**Không viết:** “Giám đốc luôn phải đóng BHXH”. PHASE 10 phải dựng decision tree theo vai trò quản lý, hưởng lương/không hưởng lương, HĐLĐ, đồng thời thuộc nhiều nhóm và trường hợp tham gia nơi khác.

---

## 4.8. Xử phạt thuế / hóa đơn

Legal spine phải đọc **văn bản nền + chuỗi sửa đổi**, đặc biệt **NĐ291/2026/NĐ-CP**, có hiệu lực 21/07/2026, sửa hệ thống xử phạt thuế/hóa đơn.

**Quy tắc:** không chép mức phạt từ blog/video/file cũ. Nếu chưa xác định chắc điều khoản hiện hành, ghi:

> **Chưa xác định — cần kiểm tra văn bản xử phạt hiện hành.**

---

## 4.9. Đăng ký doanh nghiệp

- **NĐ168/2025/NĐ-CP** — khung đăng ký doanh nghiệp.
- **NĐ296/2026/NĐ-CP** — sửa NĐ168, ban hành và hiệu lực 23/07/2026.

Mọi SOP thay đổi đăng ký doanh nghiệp phải kiểm tra mẫu biểu và quy trình hiện hành tại thời điểm nộp.

---

## 4.10. Chính sách gia hạn năm 2026

**NĐ245/2026/NĐ-CP** — ban hành và hiệu lực 27/06/2026, gia hạn thời hạn nộp GTGT, TNDN, TNCN và tiền thuê đất **cho các đối tượng/kỳ đáp ứng điều kiện**.

**TRẠNG THÁI:** 🟢 CURRENT nhưng **TEMPORARY + CONDITIONAL**.

Không tự động thay deadline chuẩn trong checklist. Checklist phải ghi:

1. deadline luật chung;
2. sau đó mới hỏi DN có thuộc NĐ245 hay không;
3. nếu có, ghi deadline gia hạn và hồ sơ/chứng cứ áp dụng.

---

## 4.11. Nhập khẩu / logistics

**TRẠNG THÁI PHASE 2:** 🟡 REVIEW — chưa khóa Legal Spine đầy đủ.

PHASE 11 phải tách:

### A. Doanh nghiệp trực tiếp nhập khẩu

Kiểm tra riêng: hợp đồng ngoại thương, chủ thể nhập khẩu, khai hải quan, trị giá, thuế nhập khẩu/GTGT khâu nhập khẩu, chứng từ nộp thuế, vận chuyển, thanh toán ngoại thương, quyền sở hữu, giá vốn.

### B. Doanh nghiệp mua trong nước từ logistics/nhà nhập khẩu

Kiểm tra riêng: chủ thể đứng tên nhập khẩu, hợp đồng mua bán trong nước, hóa đơn đầu vào, chứng từ giao nhận, thanh toán, nguồn gốc hàng hóa, quyền sở hữu và giá vốn.

**Không suy đoán hai trường hợp giống nhau.**

---

# 5. BẢN ĐỒ TRẠNG THÁI REPO SAU PHASE 1

## 🟢 CURRENT

- `00_MASTER/AUDIT_REPO_2026-08-27.md` — kết quả audit, không phải SOP chi tiết.
- `00_MASTER/00_PHAP_LY_2026_MASTER.md` — file này.
- `00_MASTER/CHANGELOG_PHAP_LY.md` — lịch sử thay đổi pháp lý.

## 🟡 REVIEW PRIORITY

- `00_PHAP_LY_2026_MASTER.md` ở root — bản khung cũ, được MASTER mới thay thế vai trò trung tâm.
- `checklist.md`
- `Cam_nang_Ke_toan_Full_Stack_ZINITEK_2026.md`
- `04_Huong_Dan_Che_Do_Ke_Toan_DN_Sieu_Nho_TT58_2026.md`
- `05_Huong_Dan_Tong_Hop_TT58_2026_DN_Sieu_Nho.md`
- `13_Lap_So_Sach_Ke_Toan_DN_Sieu_Nho_TT58_2026.md`
- các bài hướng dẫn GTGT/TNDN/TNCN/HĐĐT còn lại cho đến khi phase tương ứng kiểm tra xong.

## 🔴 OBSOLETE đã gắn trực tiếp

- `Xu ly sai sot hoa don tu 01-06-2025 - Nghi dinh 70.md`
- `thoi_diem_ky_so_hoa_don_nghi_dinh_70_2025.md`
- `Bien ban xu ly sai sot hoa don.md`

## ⚪ REFERENCE

Video/transcript, bài dịch vụ kế toán, báo giá, chia sẻ kinh nghiệm, nội dung mạng xã hội và giải đáp có phạm vi hẹp không được dùng làm căn cứ pháp lý cuối cùng. Danh sách chi tiết xem `AUDIT_REPO_2026-08-27.md`.

---

# 6. CÁC VĂN BẢN HIỆN HÀNH ĐANG THIẾU FILE GỐC TRONG REPO

Ưu tiên bổ sung/đối chiếu ở phase chuyên đề:

1. **Luật 149/2025/QH15** — sửa Luật GTGT, hiệu lực 01/01/2026.
2. **Luật 09/2026/QH16** — sửa TNCN, GTGT, TNDN, TTĐB; hiệu lực 24/04/2026.
3. **Luật 109/2025/QH15** — Thuế TNCN, hiệu lực 01/07/2026.
4. **TT20/2026/TT-BTC** — hướng dẫn TNDN, hiệu lực 12/03/2026.
5. **TT87/2026/TT-BTC** — hướng dẫn TNCN, hiệu lực 01/07/2026.
6. **NĐ245/2026/NĐ-CP** — gia hạn nghĩa vụ thuế/tiền thuê đất năm 2026 có điều kiện.

> “Thiếu file gốc” không có nghĩa repo không được nhắc đến văn bản; nghĩa là chưa có bản nguồn được lưu/chuẩn hóa trong kho để đối chiếu nội bộ.

---

# 7. TEMPLATE HEADER BẮT BUỘC CHO SOP MỚI

```text
TRẠNG THÁI: CURRENT / REVIEW / OBSOLETE / REFERENCE
CẬP NHẬT: YYYY-MM-DD
ĐỐI TƯỢNG ÁP DỤNG: ...
VĂN BẢN CĂN CỨ: ...
NGÀY HIỆU LỰC: ...
PHẠM VI/ĐIỀU KIỆN: ...
```

Nếu có deadline:

```text
HẠN PHÁP LÝ: ... (Điều ... Khoản ... văn bản ...)
```

hoặc:

```text
DEADLINE NỘI BỘ: ... (do doanh nghiệp tự đặt, không phải hạn luật)
```

---

# 8. TEMPLATE SOP VẬN HÀNH

Mỗi SOP chính nên có:

1. **Khi nào dùng SOP này?**
2. **Decision tree xác định trường hợp.**
3. **Ai chịu trách nhiệm?**
4. **Các bước phải làm.**
5. **Hồ sơ/chứng từ phải có.**
6. **Nơi lưu hồ sơ.**
7. **Hạn thực hiện.**
8. **Điểm kiểm soát trước khi hoàn tất.**
9. **Không được làm.**
10. **Nếu đã làm sai.**
11. **Rủi ro/xử phạt.**
12. **Căn cứ pháp lý + ngày hiệu lực + sửa đổi/thay thế.**

---

# 9. CÁC CÂU TUYỆT ĐỐI BỊ CẤM

Không dùng các câu sau nếu chưa qua decision tree:

- “Trên 5 triệu bắt buộc chuyển khoản.”
- “Có đầu vào mới được có đầu ra.”
- “Giám đốc luôn phải đóng BHXH.”
- “Tất cả DN khai thuế quý.”
- “DN mới luôn được miễn TNDN 3 năm.”
- “NĐ70/2025 là quy trình hóa đơn hiện hành.”

---

# 10. TRẠNG THÁI CÁC PHASE

| Phase | Nội dung | Trạng thái |
|---:|---|---|
| 1 | Audit toàn repo | ✅ DONE — 2026-08-27 |
| 2 | MASTER + changelog | ✅ DONE — 2026-08-27 |
| 3 | Hồ sơ doanh nghiệp của tôi | ⏭ NEXT |
| 4 | Công việc sau thành lập | PENDING |
| 5 | Kế toán / TT58 | PENDING |
| 6 | GTGT | PENDING |
| 7 | TNDN | PENDING |
| 8 | TNCN | PENDING |
| 9 | Hóa đơn | PENDING |
| 10 | BHXH/lao động | PENDING |
| 11 | Nhập khẩu/logistics | PENDING |
| 12 | Quản trị | PENDING |
| 13 | Checklist vận hành | PENDING |
| 14 | Xử lý sự cố | PENDING |

---

# 11. NGUYÊN TẮC CẬP NHẬT MASTER

Mỗi lần có văn bản mới:

1. ghi số hiệu, ngày ban hành, ngày hiệu lực;
2. xác định văn bản bị sửa/thay thế;
3. đọc điều khoản chuyển tiếp;
4. xác định đối tượng/kỳ áp dụng;
5. liệt kê file repo bị ảnh hưởng;
6. sửa SOP;
7. đánh dấu tài liệu cũ `OBSOLETE` nếu cần;
8. ghi lý do thay đổi vào `CHANGELOG_PHAP_LY.md`;
9. commit với message mô tả đúng phạm vi.

**Không được chỉ đổi năm trong tiêu đề rồi coi là cập nhật pháp luật.**