# DATABASE Ý KIẾN TƯ VẤN

**TRẠNG THÁI:** CURRENT — database quản trị nguồn; không phải văn bản pháp luật  
**CẬP NHẬT:** 2026-08-27  
**MỤC ĐÍCH:** chuyển nguồn tư vấn bên ngoài thành các claim có thể kiểm chứng, ra quyết định và đưa vào SOP khi đủ căn cứ.

## Quy ước trạng thái

- `NEEDS_CONTEXT`: thiếu bối cảnh/trường dữ liệu/hệ thống cụ thể.
- `NEEDS_VERIFY`: đã hiểu ý nhưng chưa đối chiếu pháp luật hiện hành.
- `NEEDS_VERIFY_HIGH`: claim có thể ảnh hưởng tuân thủ, không được dùng vận hành trước khi kiểm tra.
- `ACTION_RECHECK`: cần kiểm tra/sửa dữ liệu thực tế trước khi tiếp tục quy trình.
- `REFERENCE`: kinh nghiệm/quản trị thực tế có thể tham khảo.
- `VENDOR_PROCESS`: quy trình riêng của nhà cung cấp.
- `COMMERCIAL_REFERENCE`: báo giá/phạm vi dịch vụ.
- `VERIFIED`: đã đối chiếu văn bản hiện hành và có thể chuyển sang SOP.
- `REJECTED/OUTDATED`: claim sai, quá rộng hoặc hết hiệu lực.

## Nguồn TV-2026-08-26-WEFLY

Nguồn: `99_PHAP_LY_GOC/80_TU_VAN_CHUYEN_GIA/2026-08-26_Wefly_Lawfirm_DKKD_ke_toan_CKS_HDDT.md`

| ID | Chủ đề | Claim/ý tư vấn | Trạng thái | Cần kiểm tra gì | Đích sau khi xác minh |
|---|---|---|---|---|---|
| TV-2026-08-26-01 | Thông tin kế toán | Khi đã ghi nhận thông tin kế toán thì không nên để trống; cần thay bằng người phù hợp | NEEDS_VERIFY_HIGH | Trường/hệ thống nào; Luật Kế toán; TT58; đăng ký thuế | `02_KE_TOAN` / hồ sơ doanh nghiệp |
| TV-2026-08-26-02 | Người làm kế toán | DN nhỏ có thể để giám đốc kiêm kế toán; bên tư vấn nêu ngoại lệ TNHH 2 thành viên | NEEDS_VERIFY_HIGH | Đối tượng không được làm kế toán; quy định riêng DN siêu nhỏ TT58 | `02_KE_TOAN` decision tree nhân sự kế toán |
| TV-2026-08-26-03 | Quản trị | Chủ sở hữu và người đại diện pháp luật khác nhau vẫn có thể vận hành | NEEDS_VERIFY | Điều lệ, quyền đại diện, cơ chế ủy quyền, hồ sơ đăng ký | `09_QUAN_TRI` |
| TV-2026-08-26-04 | Ký hợp đồng | Giao dịch/hợp đồng chủ yếu do người đại diện theo pháp luật ký | NEEDS_VERIFY | Phân biệt đại diện theo pháp luật, đại diện theo ủy quyền và thẩm quyền nội bộ | `09_QUAN_TRI` SOP ký/ủy quyền |
| TV-2026-08-26-05 | Dữ liệu định danh | Tên người làm kế toán và thông tin định danh không khớp thì nên sửa cho đúng | ACTION_RECHECK | Đối chiếu dữ liệu thực tế trên hệ thống và hồ sơ gốc | `10_CHECKLIST` dữ liệu DN |
| TV-2026-08-26-06 | Thay đổi ĐKDN | Sau khoảng 15 ngày từ khi có GPKD vẫn có thể làm hồ sơ thay đổi | NEEDS_VERIFY_HIGH | Loại thay đổi; thời điểm phát sinh quyết định thay đổi; deadline pháp lý riêng | `01_BAT_DAU_DOANH_NGHIEP` / `09_QUAN_TRI` |
| TV-2026-08-26-07 | Chữ ký số | Nếu sắp đổi người đại diện thì nên đổi xong rồi mới mua chữ ký số | VENDOR_PROCESS | Quy trình CA cụ thể; có đổi/cấp lại chứng thư khi đổi người đại diện không | Checklist mua CKS |
| TV-2026-08-26-08 | Xác thực CKS | Nhà cung cấp yêu cầu người đại diện xác thực/sinh trắc học | VENDOR_PROCESS | Chính sách CA và quy định nhận biết khách hàng tại thời điểm mua | Checklist nhà cung cấp |
| TV-2026-08-26-09 | Báo giá | Gói 3 triệu: CKS 3 năm + 500 hóa đơn + hỗ trợ đăng ký thuế/HĐĐT | COMMERCIAL_REFERENCE | So sánh giá, phạm vi, gia hạn, phí phát sinh | CSDL nhà cung cấp, không vào SOP luật |
| TV-2026-08-26-10 | Thuế Q3/2026 | DN cần chuẩn bị nộp báo cáo thuế Quý 3/2026 | NEEDS_VERIFY | Sắc thuế, phương pháp, kỳ khai của chính DN, deadline pháp lý | `03_THUE_GTGT`, `04_THUE_TNDN`, `05_THUE_TNCN` |
| TV-2026-08-26-11 | TT58 | Dịch vụ hướng dẫn ghi sổ/vốn/nhập-xuất/báo cáo được tính phí theo số hóa đơn | COMMERCIAL_REFERENCE | Đây chỉ là phạm vi/báo giá dịch vụ | Không chuyển thành quy định |
| TV-2026-08-26-12 | Lao động dự kiến | Có thể giữ số lao động dự kiến là 2 dù hiện tại chưa có lao động | NEEDS_CONTEXT_HIGH | Ảnh chụp là biểu mẫu/hệ thống nào; trường này là dự kiến hay thực tế; nghĩa vụ cập nhật | `00_MASTER/01_HO_SO_DOANH_NGHIEP_CUA_TOI.md` sau khi xác minh |

## Backlog hành động rút ra từ nguồn này

1. **Xác minh ngay dữ liệu người làm kế toán/định danh đang lưu trên hệ thống** — đây là lỗi dữ liệu cụ thể, không nên để kéo sang các hồ sơ tiếp theo.
2. **Chưa quyết định mua chữ ký số trước khi chốt phương án người đại diện** nếu doanh nghiệp thực sự đang cân nhắc thay đổi và nhà cung cấp yêu cầu cấp theo người đại diện hiện tại.
3. **Tạo decision tree “ai được làm kế toán/phụ trách kế toán theo TT58”**; không dùng nguyên câu tư vấn “giám đốc được kiêm” cho tới khi kiểm chứng.
4. **Tạo SOP quyền ký/ủy quyền** để xử lý tình huống chủ sở hữu và người đại diện ở xa nhau thay vì mặc định bắt buộc phải gộp thành một người.
5. **Xác định chính xác trường “số lao động dự kiến = 2”** trước khi giữ hay sửa; ảnh/hệ thống là dữ liệu bắt buộc để kết luận.
6. **Tách kế hoạch Q3/2026 thành từng sắc thuế và kỳ khai thực tế**, không dùng câu “phải nộp báo cáo quý 3” như một nghĩa vụ chung cho mọi doanh nghiệp.

## Nguyên tắc chuyển claim sang SOP

Chỉ chuyển `VERIFIED` vào SOP khi đã ghi đủ:
- văn bản căn cứ;
- điều/khoản áp dụng;
- ngày hiệu lực;
- điều kiện áp dụng cho chính doanh nghiệp;
- deadline pháp lý nếu có;
- bằng chứng/chứng từ cần lưu;
- cách xử lý khi dữ liệu thực tế khác với claim tư vấn.
