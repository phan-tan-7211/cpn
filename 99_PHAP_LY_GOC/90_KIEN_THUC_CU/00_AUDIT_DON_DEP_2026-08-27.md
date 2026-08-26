# AUDIT DỌN `90_KIEN_THUC_CU` — 2026-08-27

**TRẠNG THÁI:** CURRENT cho mục đích quản trị kho lịch sử  
**PHẠM VI:** chỉ đánh giá cách lưu/đọc tài liệu cũ; không nâng các tài liệu này thành căn cứ pháp lý hiện hành.

## 1. KẾT LUẬN

Kho cũ có giá trị truy nguyên nhưng đang có 4 vấn đề:

1. **Trùng chủ đề rất nhiều:** doanh nghiệp mới, TT58, GTGT và hóa đơn có nhiều file nói gần cùng một việc.
2. **Nhiều file chứa lỗi/nhận định quá rộng:** đặc biệt transcript video và các bản TT58 cũ.
3. **Định dạng không đồng nhất:** Obsidian link cũ, DOCX-converted, transcript không dấu, bảng/callout lẫn lộn.
4. **Có file không phải kiến thức hoặc không nên public:** prompt, link rời, snapshot hồ sơ có PII.

Vì vậy không nên sửa đẹp từng file. Giải pháp là **phân loại + chỉ mục sạch + giữ nguyên bản thô để truy nguồn**.

---

## 2. NHÓM NÊN GỘP LOGIC, KHÔNG ĐỌC TỪNG FILE

### A. Doanh nghiệp mới thành lập

Các chuỗi P1/P2/P3, checklist, `Cong_Viec_Ke_Toan_...`, `Ke toan DN moi...`, `KHI NHẬN VIỆC...`, `Nhan viec...`, `danh_muc...` lặp nhau rất nhiều. Một số transcript có deadline/mẫu khai mang tính khái quát hoặc sai thời kỳ.

**Xử lý:** gom vào `01_THANH_LAP_DN`; đọc SOP hiện hành ở `01_BAT_DAU_DOANH_NGHIEP`, không cố hợp nhất nguyên văn các bản cũ.

### B. TT58/2026

Các file `04_...TT58`, `05_...TT58`, `13_...TT58`, `TT58_Mau_Bieu_Chi_Tiet.md` và `2026-08-11_Quyet_dinh...` trùng đáng kể.

Các lỗi đã xác định:
- mô tả TT58 như có “hệ thống tài khoản giản lược” và giới hạn thêm/bớt tài khoản;
- gọi BCTC theo cấu trúc không đúng TT58;
- một số file tự giả định số nhân sự không khớp snapshot doanh nghiệp;
- `TT58_Mau_Bieu_Chi_Tiet.md` ghi sai bộ sổ ở trường hợp GTGT khấu trừ + TNDN trên thu nhập tính thuế;
- bản hướng dẫn quyết định áp dụng dùng tiêu chí ngành/qui mô và nguồn blog chưa đủ chặt.

**Xử lý:** gom vào `02_KE_TOAN_TT58`; README nhóm nêu lỗi và trỏ sang SOP đã kiểm chứng tại `02_KE_TOAN`.

### C. Thuế GTGT

Các file về lựa chọn phương pháp, thanh toán không tiền mặt, điểm mới 01/07/2025, khai sai sót, chỉ tiêu tờ khai và khai thuế DN mới không nên ghép thành một “luật” vì chúng thuộc nhiều thời kỳ/chức năng khác nhau.

**Xử lý:** gom vào `03_THUE_GTGT`; chỉ gộp ở cấp chỉ mục theo luồng: phương pháp → đầu vào → thanh toán → khai → sửa sai.

### D. Hóa đơn

Nhóm NĐ70, thời điểm lập/ký, bên mua/bên bán điều chỉnh, XML và bài xử phạt đang lẫn cả nội dung hết hiệu lực, transcript và nhận định chưa kiểm chứng.

**Xử lý:** gom vào `06_HOA_DON`; NĐ70 giữ lịch sử nhưng không dùng hiện hành. Các bài mức phạt không được tái dùng nếu chưa đối chiếu văn bản xử phạt hiện hành.

---

## 3. FILE NÊN LOẠI KHỎI LUỒNG ĐỌC

### Gỡ khỏi cây public hiện tại

- `thong_tin_doanh_nghiep.md`
- `Co_So_Du_Lieu.md`

**Lý do:** chứa dữ liệu cá nhân/định danh chi tiết và trạng thái cũ. Không cần thiết cho kho kiến thức public. Dữ liệu vận hành tối thiểu đã có ở `00_MASTER/01_HO_SO_DOANH_NGHIEP_CUA_TOI.md` với nguyên tắc không phát tán PII.

> Lưu ý: việc gỡ khỏi cây hiện tại không tự xóa blob khỏi lịch sử Git.

### Chuyển sang `98_META_KHONG_PHAI_KIEN_THUC`

- `master pormpt lần đầu` — là chỉ dẫn xây repo, không phải kiến thức pháp lý/kế toán.
- `link.md` — chỉ chứa một liên kết rời, không có nội dung đủ để lập luận.
- `00_PHAP_LY_2026_MASTER.md` — master cũ đã được thay bằng `00_MASTER/00_PHAP_LY_2026_MASTER.md`; chỉ giữ để truy lịch sử thiết kế.

---

## 4. FILE NÊN GIỮ NHƯ NGUỒN THAM KHẢO, KHÔNG CẦN “LÀM ĐẸP”

- Transcript/video và ghi chú của các kênh kế toán.
- Báo giá/phạm vi dịch vụ kế toán.
- Bài giải đáp/portal của cơ quan nhà nước, nhưng chỉ dùng đúng phạm vi câu hỏi.
- Từ điển pháp lý cũ.
- Cẩm nang kế toán tổng hợp cũ: giữ để khai thác ý, không coi là SOP CURRENT.

Các file này được chuyển vào `09_NGUON_THAM_KHAO` hoặc nhóm nghiệp vụ tương ứng. Nếu cần tái sử dụng, trích claim rồi kiểm chứng.

---

## 5. CHUẨN ĐỊNH DẠNG TỪ NAY

Chỉ các **README/tóm tắt đã biên tập** trong kho lịch sử mới cần chuẩn hóa theo mẫu:

```text
# TÊN NHÓM
TRẠNG THÁI
MỤC ĐÍCH
KHÔNG DÙNG CHO

## Kết luận nhanh
## Các file nguồn
## Ý còn giá trị
## Lỗi/điểm đã lỗi thời
## Tài liệu CURRENT thay thế
```

File nguyên bản không cần chuyển toàn bộ sang mẫu này; giữ nguyên sẽ giúp phân biệt rõ **nguồn thô** và **bản đã biên tập**.

---

## 6. KẾT LUẬN QUẢN TRỊ

`90_KIEN_THUC_CU` từ nay là **archive có chỉ mục**, không phải “thùng tài liệu”. Người dùng bình thường chỉ cần đọc README ở cấp thư mục. File thô chỉ mở khi cần truy nguyên một claim cụ thể.
