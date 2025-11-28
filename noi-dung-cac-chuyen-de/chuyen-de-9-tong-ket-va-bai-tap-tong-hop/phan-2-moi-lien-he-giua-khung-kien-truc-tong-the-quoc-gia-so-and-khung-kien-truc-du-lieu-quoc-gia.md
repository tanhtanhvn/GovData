# Phần 2 - Mối liên hệ giữa Khung Kiến trúc Tổng thể Quốc gia Số & Khung Kiến trúc Dữ liệu Quốc gia

#### **1.** **Khung Kiến trúc Tổng thể Quốc gia Số**

a) Mục tiêu

* Tạo ra bức tranh tổng thể cho chuyển đổi số quốc gia.
* Định hướng phát triển hạ tầng – nền tảng – ứng dụng – dịch vụ thống nhất trên toàn quốc.
* Là căn cứ để các Bộ/Tỉnh xây dựng kiến trúc số cấp ngành/địa phương.

b) Cấu trúc 4 lớp

* Lớp Hạ tầng số và An toàn mạng: Trung tâm dữ liệu quốc gia, đám mây chính phủ, mạng truyền số liệu chuyên dùng.
* Lớp Dữ liệu & Nền tảng lõi: Cơ sở dữ liệu quốc gia (dân cư, đất đai, doanh nghiệp...), NDOP, nền tảng số dùng chung.
* Lớp Ứng dụng & Nghiệp vụ dùng chung: Hệ thống điều hành, dịch vụ công, các ứng dụng tác nghiệp của Bộ/Ngành/Tỉnh.
* Lớp Kênh tương tác & Đo lường hiệu quả: Cổng dịch vụ công quốc gia, Ứng dụng di động, API mở phục vụ doanh nghiệp, Dashboards.

c) Đặc trưng

* Là “kiến trúc tổng thể” cho toàn bộ Chính phủ số.
* Định hình không gian số cho tất cả cơ quan nhà nước.

#### **2.** **Khung Kiến trúc Dữ liệu Quốc gia**

a) Mục tiêu

* Chuẩn hóa cách tổ chức, quản trị và khai thác dữ liệu ở cấp quốc gia.
* Đảm bảo dữ liệu đúng – đủ – sạch – sống – thống nhất – dùng chung.

b) Thành phần chính

1. Phân tầng dữ liệu
   1. Dữ liệu chủ / dữ liệu giao dịch
   2. Dữ liệu dùng chung
   3. Dữ liệu phân tích, tổng hợp
   4. Dữ liệu mở
   5. Dữ liệu quốc gia / dữ liệu chuyên ngành (miền)
2. Mô hình chia sẻ – liên thông dữ liệu
   1. CSDL tổng hợp quốc gia, CSDL quốc gia (theo lĩnh vực), CSDL dùng chung Bộ/Ngành/Địa phương
   2. NDOP (Nền tảng tích hợp, chia sẻ dữ liệu quốc gia)
   3. Cơ chế ủy quyền truy cập dữ liệu
3. Khung quản trị dữ liệu quốc gia
   1. Vai trò: Ban chỉ đạo dữ liệu quốc gia – Ban chỉ đạo dữ liệu cấp bộ/cấp tỉnh – Cơ quan chủ quản dữ liệu
   2. Chính sách chất lượng: KPI/KQI, Từ điển dữ liệu dùng chung
   3. Kiểm soát sự tuân thủ và Kiểm toán dữ liệu
4. An toàn dữ liệu
   1. Mô hình 8 lớp: Bảo mật – Quyền riêng tư – Giám sát dữ liệu

c) Đặc trưng

* Tập trung vào dữ liệu như một tài nguyên chiến lược.
* Là “bộ khung vận hành” cho toàn bộ dòng chảy dữ liệu công.

#### **3.** **Mối liên hệ giữa hai khung kiến trúc**

a) Quan hệ bố cục

* Khung Kiến trúc Tổng thể Quốc gia Số = _không gian tổng thể_
* Khung Kiến trúc Dữ liệu Quốc gia = _một kiến trúc con quan trọng trong không gian đó_

b) Quan hệ chức năng

* Tổng thể quốc gia số định hướng cách:
  * kết nối hệ thống,
  * triển khai hạ tầng,
  * tổ chức nền tảng & ứng dụng.
* Khung kiến trúc dữ liệu định hướng cách:
  * tổ chức và mô hình hóa dữ liệu,
  * đảm bảo liên thông và dùng chung,
  * quản trị & chất lượng dữ liệu,
  * chia sẻ & an toàn dữ liệu.

c) Vai trò “xương sống” của kiến trúc dữ liệu

* Mọi ứng dụng số → không có dữ liệu chuẩn → hoạt động không hiệu quả.
* Mọi tích hợp hệ thống → không có liên thông dữ liệu → bị chia cắt (silo).
* Mọi phân tích AI/BI → không có kho dữ liệu sạch → sai lệch.

\=> Kiến trúc dữ liệu chính là trục xương sống (backbone) giúp Chính phủ số vận hành thống nhất.

#### **4.** **Ý nghĩa đối với triển khai thực tế**

a) Bảo đảm đồng bộ trên toàn quốc

* Kiến trúc số cấp ngành/tỉnh → phù hợp Khung Kiến trúc Tổng thể.
* Kiến trúc dữ liệu ngành/tỉnh → phù hợp Khung Kiến trúc Dữ liệu Quốc gia.

b) Tránh trùng lặp – lãng phí – mâu thuẫn

* Không lặp lại nhiều kho dữ liệu cùng một loại.
* Không dùng tiêu chuẩn dữ liệu khác nhau theo từng ngành.
* Không phát triển hệ thống số “độc lập”, thiếu tích hợp.

c) Tạo nền tảng cho Liên thông dữ liệu quốc gia

* Liên thông kỹ thuật (API, nền tảng tích hợp).
* Liên thông ngữ nghĩa (ontology, từ điển dữ liệu).
* Liên thông nghiệp vụ (quy trình chia sẻ dữ liệu).

d) Đảm bảo chính phủ vận hành dựa trên dữ liệu

* Dữ liệu sạch → chất lượng ra quyết định nâng cao.
* Dữ liệu liên thông → giảm yêu cầu giấy tờ (Once-Only).
* Dữ liệu chuẩn hóa → hỗ trợ AI, BI, phân tích chính sách.
