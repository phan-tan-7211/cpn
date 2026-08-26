# 80_TU_VAN_CHUYEN_GIA — NGUỒN TƯ VẤN BÊN NGOÀI

**TRẠNG THÁI:** REFERENCE  
**MỤC ĐÍCH:** lưu dấu vết tư vấn của công ty luật, kế toán, cơ quan hỗ trợ, nhà cung cấp dịch vụ hoặc chuyên gia để làm nguồn dữ liệu đầu vào.

> Đây là **nguồn chứng cứ về việc ai đã tư vấn gì, vào thời điểm nào**, không phải văn bản pháp luật và không tự động trở thành SOP hiện hành.

## Quy tắc lưu

1. Mỗi buổi/chuỗi tư vấn tạo một file theo mẫu `YYYY-MM-DD_DON_VI_CHU_DE.md`.
2. Ưu tiên bản **đã ẩn danh** nếu repo có khả năng được chia sẻ/public: không ghi số CCCD, điện thoại, địa chỉ, tài khoản, chữ ký, ảnh giấy tờ hoặc dữ liệu cá nhân không cần thiết.
3. Giữ đủ ngày giờ, bên tư vấn, câu hỏi, ý trả lời và bối cảnh để truy nguyên.
4. Không sửa câu tư vấn thành câu luật. Phần diễn giải phải tách riêng dưới nhãn `NHẬN ĐỊNH/CLAIM`.
5. Mọi claim có ảnh hưởng tuân thủ phải đi qua chu trình:

```text
SOURCE (tư vấn gốc)
  ↓
CLAIM (ý được trích xuất)
  ↓
VERIFY (đối chiếu luật/văn bản hiện hành)
  ↓
DECISION (quyết định của doanh nghiệp)
  ↓
SOP / CHECKLIST CURRENT
```

6. Claim chưa kiểm chứng chỉ được mang trạng thái `NEEDS_VERIFY`, `REFERENCE` hoặc `NEEDS_CONTEXT`.
7. Báo giá, gói dịch vụ, thương hiệu chữ ký số, số lượng hóa đơn... là dữ liệu thương mại tại thời điểm tư vấn; không đưa thành quy định pháp luật.

## Nơi chuyển hóa thành dữ liệu có cấu trúc

Dùng `00_MASTER/02_DATABASE_Y_KIEN_TU_VAN.md` để quản lý từng claim, trạng thái kiểm chứng, tác động và SOP đích.
