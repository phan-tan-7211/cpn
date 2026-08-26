# 90_KIEN_THUC_CU — KHO LỊCH SỬ ĐÃ PHÂN LOẠI

**TRẠNG THÁI:** REFERENCE / OBSOLETE  
**CẬP NHẬT:** 2026-08-27  
**NGUYÊN TẮC:** đây là kho truy nguyên, **không phải danh sách tài liệu phải đọc để vận hành doanh nghiệp**.

> Muốn làm việc hiện hành: quay về `README.md`, `00_MASTER` và SOP CURRENT. Chỉ vào thư mục này khi cần xem nguồn cũ, cách hiểu cũ hoặc truy lại vì sao một SOP đã thay đổi.

## ĐỌC NHƯ THẾ NÀO

| Thư mục | Nội dung | Có nên đọc file thô? |
|---|---|---|
| `01_THANH_LAP_DN` | checklist/hướng dẫn doanh nghiệp mới cũ | Chỉ khi truy nguồn |
| `02_KE_TOAN_TT58` | các bản diễn giải TT58 cũ, nhiều bản trùng và có lỗi | Không; đọc README nhóm trước |
| `03_THUE_GTGT` | GTGT, thanh toán, khai bổ sung, phương pháp tính | Chỉ khi truy nguồn |
| `04_THUE_TNDN` | TNDN, miễn/ưu đãi, bài tổng hợp cũ | Chỉ khi truy nguồn |
| `05_THUE_TNCN` | TNCN cũ/transcript | Chỉ khi truy nguồn |
| `06_HOA_DON` | hóa đơn, NĐ70 cũ, bài thời điểm/sai sót | Không dùng trực tiếp |
| `07_BHXH_DKKD` | BHXH, đăng ký DN, phân loại DNNVV | Chỉ tham khảo |
| `08_KE_TOAN_NEN` | kiến thức kế toán nền/tài liệu học | Có thể đọc như REFERENCE |
| `09_NGUON_THAM_KHAO` | video, bài dịch vụ, báo giá, giải đáp, tổng hợp nguồn | Không coi là luật |
| `98_META_KHONG_PHAI_KIEN_THUC` | prompt, link rời, tài liệu meta | Không dùng nghiệp vụ |

## QUY TẮC DỌN KHO

1. **Không làm đẹp hàng loạt file nguyên bản.** File lịch sử được giữ gần nguyên trạng để bảo toàn nguồn/provenance.
2. Nhóm có nhiều bản trùng được **gộp ở cấp chỉ mục/README**, không ghép nội dung thô rồi vô tình hợp nhất cả lỗi.
3. File chứa nhận định sai hoặc quá rộng vẫn có thể giữ, nhưng phải nằm trong nhóm lịch sử và README nhóm phải nói rõ lỗi.
4. File không phải kiến thức (`link`, prompt, dữ liệu meta) bị tách khỏi luồng đọc.
5. Dữ liệu cá nhân chi tiết không được giữ trên cây public chỉ để “tham khảo”. Hồ sơ vận hành tối giản dùng `00_MASTER/01_HO_SO_DOANH_NGHIEP_CUA_TOI.md`.
6. Bất kỳ ý nào muốn tái sử dụng phải đi qua: **SOURCE → CLAIM → VERIFY → SOP**.

## LƯU Ý BẢO MẬT

Đợt dọn này gỡ các snapshot cũ có thông tin định danh cá nhân chi tiết khỏi **cây hiện tại** của repo public. Tuy nhiên, Git là hệ thống có lịch sử: blob cũ có thể vẫn tồn tại trong commit lịch sử. Nếu cần xóa triệt để khỏi lịch sử public thì phải thực hiện một đợt **history rewrite/purge riêng**, có kiểm soát.

## AUDIT

Xem `00_AUDIT_DON_DEP_2026-08-27.md` để biết file nào được gộp logic, file nào chuyển nhóm, file nào bị loại khỏi luồng đọc và vì sao.
