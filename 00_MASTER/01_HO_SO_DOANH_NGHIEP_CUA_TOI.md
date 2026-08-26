# HỒ SƠ DOANH NGHIỆP CỦA TÔI — NGUỒN SỰ THẬT VẬN HÀNH

**TRẠNG THÁI:** CURRENT — hồ sơ kiểm soát trung tâm  
**CẬP NHẬT:** 2026-08-27  
**ĐỐI TƯỢNG ÁP DỤNG:** Công ty TNHH ZINITEK  
**VĂN BẢN CĂN CỨ CHÍNH CHO PHÂN LOẠI QUY MÔ:** Nghị định 80/2021/NĐ-CP, đặc biệt Điều 5–10; TT58/2026/TT-BTC chỉ áp dụng chế độ kế toán khi doanh nghiệp thực sự thuộc phạm vi  
**NGUYÊN TẮC:** file này là **single source of truth** cho dữ liệu vận hành; SOP không được tự bịa hoặc tự sửa dữ liệu doanh nghiệp.

> Không sao chép vào file này các dữ liệu cá nhân không cần thiết như số giấy tờ tùy thân, ngày sinh, địa chỉ nhà riêng, số điện thoại cá nhân. Nếu cần xử lý hồ sơ hành chính có PII, tra tài liệu gốc có kiểm soát thay vì phát tán dữ liệu sang mọi SOP.

---

# 1. CÁCH ĐỌC TRẠNG THÁI DỮ LIỆU

| Nhãn | Ý nghĩa |
|---|---|
| `CONFIRMED_REPO` | Có dữ liệu nhất quán trong hồ sơ/checklist repo tại lần audit. |
| `USER_DECLARED` | Mô hình/trạng thái được chủ doanh nghiệp xác nhận trong yêu cầu xây repo. |
| `SNAPSHOT` | Chỉ đúng tại ngày tài liệu nguồn; có thể đã thay đổi sau đó. |
| `NEEDS_RECHECK` | Chưa đủ bằng chứng hiện hành; không được suy đoán. |
| `TRIGGER_BASED` | Chỉ phát sinh nghĩa vụ khi một sự kiện tương ứng xảy ra. |

---

# 2. NHẬN DIỆN DOANH NGHIỆP — CHỈ GIỮ DỮ LIỆU CẦN CHO VẬN HÀNH

| Trường | Giá trị | Trạng thái / nguồn |
|---|---|---|
| Tên doanh nghiệp | CÔNG TY TNHH ZINITEK | `CONFIRMED_REPO` |
| Loại hình | Công ty TNHH một thành viên | `CONFIRMED_REPO` |
| Quốc gia hoạt động | Việt Nam | `CONFIRMED_REPO` + `USER_DECLARED` |
| Ngày đăng ký thành lập lần đầu | 11/08/2026 | `CONFIRMED_REPO` |
| Năm tài chính | 01/01–31/12 | `CONFIRMED_REPO`; cần đối chiếu khi áp dụng chuyển tiếp TT58 cho năm đầu |
| Ngành nghề chính đang ghi trong repo | 4659 — bán buôn máy móc, thiết bị và phụ tùng máy khác | `CONFIRMED_REPO` |
| Nhóm lĩnh vực để kiểm tra DNNVV | Thương mại/dịch vụ theo ngành nghề chính đã đăng ký | `WORKING_CLASSIFICATION`; Điều 6 NĐ80 yêu cầu dựa vào ngành, nghề kinh doanh chính đăng ký |

---

# 3. PHÂN LOẠI DOANH NGHIỆP SIÊU NHỎ — KHÔNG DÙNG DỰ BÁO ĐỂ KẾT LUẬN BỪA

## 3.1. Tiêu chí pháp lý đang dùng

Theo khoản 1 Điều 5 NĐ80/2021/NĐ-CP, doanh nghiệp siêu nhỏ trong **thương mại và dịch vụ** phải:

- có số lao động tham gia BHXH bình quân năm **không quá 10 người**; **và**
- có **tổng doanh thu năm không quá 10 tỷ đồng** **hoặc** **tổng nguồn vốn năm không quá 3 tỷ đồng**.

Điều 6 xác định lĩnh vực theo **ngành, nghề kinh doanh chính đã đăng ký**.

Đối với doanh nghiệp hoạt động dưới 01 năm:

- số lao động BHXH bình quân tính theo các tháng đã hoạt động;
- tổng nguồn vốn dùng số liệu tại **cuối quý liền kề** thời điểm cần xác định theo Điều 8;
- nếu hoạt động dưới 01 năm hoặc chưa có doanh thu, Điều 9 cho phép căn cứ tiêu chí **tổng nguồn vốn** để xác định quy mô DNNVV.

## 3.2. Tình trạng của ZINITEK tại lần audit

| Tiêu chí | Dữ liệu đang có | Kết luận được phép |
|---|---|---|
| Lĩnh vực | Ngành chính 4659 — bán buôn | Có cơ sở làm việc theo nhóm thương mại; kiểm tra lại nếu ngành chính thay đổi. |
| Lao động | Snapshot repo 20/08/2026: chưa có nhân viên | Đang dưới ngưỡng lao động tại snapshot; phải cập nhật hàng tháng khi phát sinh lao động BHXH. |
| Doanh thu | Repo ghi chưa có doanh thu; dự kiến 12 tháng đầu dưới 1 tỷ | **Dự kiến không phải số liệu pháp lý cuối cùng.** Khi chưa có doanh thu, dùng phương pháp Điều 8–9 NĐ80 để xác định. |
| Tổng nguồn vốn | Repo có dữ liệu vốn điều lệ nhưng không được tự đồng nhất với chỉ tiêu “tổng nguồn vốn” dùng cho Điều 8 | `NEEDS_RECHECK` tại số liệu cuối quý phù hợp. |
| Tự khai quy mô | Chủ doanh nghiệp xác nhận thuộc nhóm DN siêu nhỏ | `USER_DECLARED`; được dùng làm định hướng, nhưng phải lưu bằng chứng xác định theo NĐ80 khi áp dụng ưu đãi/chế độ có điều kiện. |

### Kết luận kiểm soát

**Không được viết:** “ZINITEK chắc chắn là DN siêu nhỏ vì doanh thu dự kiến dưới 1 tỷ.”

Cách đúng:

```text
Ngành chính đăng ký = thương mại/dịch vụ?
        ↓ CÓ
Lao động BHXH bình quân ≤ 10?
        ↓ CÓ / kiểm tra theo tháng hoạt động
DN dưới 1 năm hoặc chưa có doanh thu?
        ↓ CÓ
Dùng tổng nguồn vốn theo Điều 8 tại thời điểm xác định
        ↓
≤ 3 tỷ? → đủ tiêu chí quy mô siêu nhỏ theo nhánh này
> 3 tỷ? → không kết luận siêu nhỏ theo nhánh vốn; phải xét dữ liệu/doanh thu khi pháp luật cho phép
```

**Bằng chứng phải lưu khi cần chứng minh quy mô:**

- GCNĐKDN/đăng ký ngành nghề chính;
- chứng từ/danh sách lao động tham gia BHXH theo tháng;
- BCTC/số liệu tổng nguồn vốn theo đúng kỳ Điều 8;
- tờ khai tự xác định DNNVV nếu sử dụng chính sách hỗ trợ/ưu đãi yêu cầu;
- tài liệu xác định doanh thu năm khi đã có kỳ số liệu phù hợp.

---

# 4. TRẠNG THÁI VẬN HÀNH — SNAPSHOT, KHÔNG ĐƯỢC COI LÀ DỮ LIỆU SỐNG VĨNH VIỄN

Nguồn snapshot chính trong repo được cập nhật khoảng 20/08/2026. Các mục dưới đây phải được cập nhật khi có thay đổi thực tế.

| Hạng mục | Snapshot repo | Trạng thái kiểm soát |
|---|---|---|
| Doanh thu | Chưa phát sinh tại snapshot | `SNAPSHOT` |
| Mua bán thường xuyên | Chưa phát sinh tại snapshot | `SNAPSHOT` |
| Hàng tồn kho | Chưa có tại snapshot | `SNAPSHOT` |
| Nhân viên | Chưa có tại snapshot | `SNAPSHOT` |
| Trả lương | Chưa phát sinh tại snapshot | `SNAPSHOT` |
| Nhập khẩu | Chưa phát sinh tại snapshot | `SNAPSHOT`; mô hình tương lai đã xác định ở mục 6 |
| Phương pháp GTGT | Chưa chốt trong snapshot | `NEEDS_RECHECK` — PHASE 6 |
| Chữ ký số | Chưa có trong snapshot | `NEEDS_RECHECK` — PHASE 4 |
| HĐĐT | Chưa đăng ký/mua trong snapshot | `NEEDS_RECHECK` — PHASE 4/9 |
| Tài khoản ngân hàng DN | Chưa hoàn tất trong snapshot | `NEEDS_RECHECK` — PHASE 4 |
| Vốn góp | Snapshot ghi chưa góp | `NEEDS_RECHECK` — PHASE 4 phải kiểm tra hạn và chứng từ, không tự đặt deadline |

> Khi cập nhật một mục, thay **giá trị + ngày xác nhận + bằng chứng**, không chỉ đổi biểu tượng trạng thái.

---

# 5. VAI TRÒ / CON NGƯỜI — SOP CHỈ DÙNG CHỨC DANH, KHÔNG RẢI TÊN CÁ NHÂN

Các SOP nên dùng vai trò:

- **Chủ sở hữu**
- **Người đại diện theo pháp luật**
- **Người phụ trách kế toán / kế toán**
- **Người phê duyệt thanh toán**
- **Người mua hàng**
- **Người bán hàng**
- **Người quản lý kho**
- **Người phụ trách BHXH/lao động**

Nếu một người kiêm nhiều vai trò, quy trình vẫn phải thể hiện **hai bước kiểm soát logic** (ví dụ: lập → kiểm tra/phê duyệt) và ghi rõ trường hợp kiêm nhiệm để tránh “tự lập rồi tự duyệt” không có dấu vết kiểm soát.

Thông tin tên cá nhân/người đại diện thực tế phải tra hồ sơ đăng ký doanh nghiệp hiện hành khi cần ký/nộp; không lấy từ một file cũ nếu đang có thủ tục thay đổi chưa hoàn tất.

---

# 6. MÔ HÌNH MUA HÀNG TRUNG QUỐC / LOGISTICS — HAI LUỒNG BẮT BUỘC TÁCH

## LUỒNG A — ZINITEK TRỰC TIẾP NHẬP KHẨU

`USER_DECLARED` là tình huống có thể phát sinh.

Khi phát sinh, hồ sơ phải có decision tree riêng về:

- ai là người mua theo hợp đồng ngoại thương;
- ai đứng tên người nhập khẩu/tờ khai hải quan;
- Incoterms/điểm chuyển quyền, nếu áp dụng;
- chứng từ vận chuyển;
- tờ khai hải quan;
- thuế khâu nhập khẩu;
- thanh toán nước ngoài;
- chứng từ nhận hàng;
- xác định giá vốn;
- lưu hồ sơ nguồn gốc hàng.

**Không dùng hóa đơn mua hàng trong nước để thay thế hồ sơ nhập khẩu nếu ZINITEK chính là chủ thể nhập khẩu.**

## LUỒNG B — ZINITEK MUA TRONG NƯỚC TỪ LOGISTICS/NHÀ NHẬP KHẨU

`USER_DECLARED` là tình huống có thể phát sinh.

Khi đơn vị logistics/nhà nhập khẩu **đứng tên hàng hóa/nhập khẩu rồi bán lại cho ZINITEK**, SOP phải kiểm tra:

- quan hệ pháp lý thực sự là **mua bán trong nước** hay ủy thác/đại lý/dịch vụ khác;
- hợp đồng/đơn đặt hàng giữa ZINITEK và bên bán trong nước;
- hóa đơn đầu vào do bên bán trong nước lập;
- chứng từ giao nhận;
- chứng từ thanh toán;
- tài liệu chứng minh nguồn gốc nếu pháp luật/ngành hàng/giao dịch yêu cầu;
- quyền sở hữu và thời điểm ghi nhận hàng;
- giá vốn.

**Không tự yêu cầu ZINITEK phải có tờ khai hải quan đứng tên mình nếu thực tế ZINITEK chỉ là người mua trong nước — nhưng cũng không được bỏ qua hồ sơ nguồn gốc cần thiết cho hàng hóa cụ thể.** PHASE 11 sẽ xác định chi tiết theo luật hải quan/thuế/ngoại thương hiện hành.

---

# 7. TRIGGER MATRIX — KHI NÀO NGHĨA VỤ BẬT LÊN

| Sự kiện | SOP phải mở |
|---|---|
| Chuẩn bị mua hàng trong nước | Transaction check MUA HÀNG + GTGT + TNDN |
| Chuẩn bị mua từ Trung Quốc | PHASE 11: chọn Luồng A hay B **trước khi ký/thanh toán** |
| Chuẩn bị bán hàng | Hóa đơn + GTGT + giao nhận + thu tiền |
| Nhận hóa đơn đầu vào | Kiểm tra HĐĐT + điều kiện GTGT/TNDN + thanh toán |
| Tuyển người / ký HĐLĐ | Lao động + BHXH + TNCN + lương |
| Trả lương | TNCN + BHXH + thanh toán + chứng từ lương |
| Mua tài sản | Tài sản + hóa đơn + thanh toán + kế toán + TNDN |
| Phát hiện hóa đơn sai | PHASE 9 decision tree NĐ254/TT91 |
| Cuối tháng/quý/năm | Checklist kỳ hạn; deadline phải lấy từ luật hoặc ghi rõ nội bộ |
| Cơ quan thuế yêu cầu hồ sơ | PHASE 14: xử lý sự cố/kiểm tra hồ sơ |

---

# 8. DỮ LIỆU TUYỆT ĐỐI KHÔNG ĐƯỢC TỰ ĐIỀN

Nếu chưa có bằng chứng, ghi `CHƯA XÁC ĐỊNH` thay vì đoán:

- phương pháp tính GTGT;
- tài khoản ngân hàng đã kích hoạt hay chưa;
- trạng thái thay đổi người đại diện;
- tình trạng chữ ký số/HĐĐT;
- ngày thực tế góp đủ vốn;
- số lao động hiện tại sau ngày snapshot;
- doanh thu thực tế;
- phương thức nhập khẩu của từng lô;
- đối tượng được hưởng gia hạn/ưu đãi thuế;
- mức phạt.

---

# 9. CHECKLIST CẬP NHẬT HỒ SƠ NÀY

Cập nhật ngay khi có một trong các thay đổi:

- [ ] GCNĐKDN/đăng ký thay đổi được cấp mới.
- [ ] Thay ngành nghề kinh doanh chính.
- [ ] Mở/đóng/thay tài khoản ngân hàng dùng vận hành.
- [ ] Chốt phương pháp GTGT hoặc có thay đổi pháp lý liên quan.
- [ ] Kích hoạt/chuyển nhà cung cấp chữ ký số/HĐĐT.
- [ ] Góp vốn/phát sinh thay đổi vốn.
- [ ] Tuyển lao động đầu tiên hoặc thay đổi số lao động BHXH.
- [ ] Phát sinh doanh thu đầu tiên.
- [ ] Phát sinh lô nhập khẩu đầu tiên.
- [ ] Thay mô hình logistics.
- [ ] Đến cuối quý đầu tiên: lấy số liệu tổng nguồn vốn để **re-check quy mô DNNVV** nếu cần áp dụng chế độ/ưu đãi.
- [ ] Cuối năm: re-check phân loại siêu nhỏ theo NĐ80 cho kỳ tiếp theo.

---

# 10. NGUỒN TRONG REPO

- `thong_tin_doanh_nghiep.md` — dữ liệu đăng ký/hồ sơ gốc; có PII nên không sao chép lan rộng.
- `checklist.md` — snapshot vận hành khoảng 20/08/2026; không coi mọi trạng thái trong đó là hiện tại vĩnh viễn.
- `00_MASTER/AUDIT_REPO_2026-08-27.md` — ghi nhận mâu thuẫn dữ liệu và rủi ro tự suy đoán.
- `00_MASTER/00_PHAP_LY_2026_MASTER.md` — legal spine.

**Từ PHASE 3 trở đi, nếu một SOP cần biết “công ty hiện thuộc trường hợp nào”, phải tham chiếu file này trước.**