# Phần 5 - Từ điển dữ liệu dùng chung

#### **1.** **Mục tiêu và phạm vi**

* Chuẩn hóa ngữ nghĩa và cấu trúc dữ liệu thống nhất toàn quốc.
* Đảm bảo tương thích – liên thông – đồng bộ giữa các cơ sở dữ liệu và hệ thống thông tin.
* Áp dụng chung cho các cơ quan trong toàn hệ thống chính trị.

#### **2.** **Nguyên tắc xây dựng**

* Chuẩn hóa: Dùng thuật ngữ, định nghĩa, cấu trúc thống nhất; tránh trùng lặp.
* Nhất quán: Áp dụng đồng bộ trên toàn quốc, mọi cấp hành chính và lĩnh vực.
* Tương thích & Liên thông: Hỗ trợ kết nối, trao đổi dữ liệu giữa các hệ thống trong và ngoài nước.
* Mở & Mở rộng: Linh hoạt, dễ cập nhật theo thay đổi chính sách, công nghệ; hỗ trợ đa ngôn ngữ.
* Quản lý tập trung: Phân cấp rõ vai trò giữa cơ quan quản lý, cơ quan ngành, đơn vị chủ sở hữu dữ liệu.
* Bảo mật & Tuân thủ: Phân loại truy cập, bảo vệ dữ liệu cá nhân, tuân thủ Luật Dữ liệu và các quy định an toàn thông tin.

#### **3.** **Sơ đồ tổng quát hệ thống từ điển**

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

**(1) Lớp nội dung**

* Bộ từ vựng cốt lõi: Thuật ngữ dùng chung xuyên ngành, cấp quốc gia.
* Từ vựng theo lĩnh vực: Chuyên biệt từng ngành (y tế, giáo dục, tài chính…).
* Cấu trúc dữ liệu: Mô tả thực thể – mối quan hệ – định dạng kỹ thuật.
* Phân loại (taxonomy): Theo chủ đề, ngành, loại thực thể, độ nhạy cảm.
* Tương tác quốc tế: Ánh xạ với chuẩn quốc tế để đảm bảo liên thông xuyên biên giới.

**(2) Lớp quản trị**

* Quản lý vòng đời từ vựng: (1) Đề xuất → (2) Rà soát → (3) Tham vấn → (4) Phê duyệt & Đăng ký.
* Phiên bản hóa:
  * _Major Release:_ 3 năm/lần, cập nhật toàn diện.
  * _Minor Release:_ 12 tháng/lần, cập nhật theo lĩnh vực.
  * Ghi nhật ký thay đổi và duy trì phiên bản cũ để tương thích.
* Giám sát & đánh giá:
  * Giám sát liên tục việc sử dụng, phản hồi và lỗi thuật ngữ.
  * Đánh giá định kỳ hàng năm để cập nhật và cải tiến.

**(3) Công cụ & Tài liệu hỗ trợ**

* Công cụ số: Nền tảng quản lý từ vựng, Cổng Dữ liệu quốc gia, Công cụ kiểm tra tương thích, mô hình hóa dữ liệu.
* Tài liệu & hỗ trợ kỹ thuật: Hướng dẫn sử dụng, cẩm nang, đào tạo trực tuyến, diễn đàn cộng đồng, trung tâm hỗ trợ kỹ thuật.

**4.** **Cấu trúc mô tả thuật ngữ**

* Mô tả nghiệp vụ: mã định danh, tên, định nghĩa, ngữ cảnh, đơn vị quản lý, ngôn ngữ, phiên bản, tài liệu liên quan.
* Mô tả kỹ thuật: Tên trường, kiểu dữ liệu, độ dài, quan hệ, giá trị hợp lệ, API, quy tắc chuẩn hóa, tương thích quốc tế.

**5. Chuẩn đăng ký metadata (ISO 11179)**

* Tên đầy đủ: _ISO/IEC 11179 – Information Technology — Metadata Registries (MDR)_
* Cơ quan ban hành: Tổ chức Tiêu chuẩn hóa Quốc tế (ISO) và Ủy ban Kỹ thuật Điện Quốc tế (IEC).
* Mục đích: Chuẩn hóa cách mô tả, quản lý và đăng ký siêu dữ liệu (metadata) để đảm bảo dữ liệu được hiểu và sử dụng thống nhất.
* Ứng dụng: Là nền tảng cho việc xây dựng Từ điển dữ liệu dùng chung và liên thông dữ liệu giữa các hệ thống khác nhau.
* Nội dung: Gồm 6 phần mô tả toàn bộ vòng đời và cấu trúc quản lý metadata

**6.** **Chuẩn metadata dữ liệu mở (DCAT-AP)**

* Tên đầy đủ: _DCAT-AP (Data Catalog Vocabulary – Application Profile for data portals in Europe)_
* Cơ quan ban hành: Ủy ban Châu Âu (European Commission) và Tổ chức W3C (World Wide Web Consortium).
* Mục tiêu: Chuẩn hóa mô tả siêu dữ liệu (metadata) của bộ dữ liệu mở (open data) để các cổng dữ liệu quốc gia và quốc tế có thể trao đổi, tìm kiếm, liên thông và chia sẻ dữ liệu dễ dàng.
* Bản chất: DCAT-AP là “hồ sơ ứng dụng” (Application Profile) mở rộng từ chuẩn DCAT (Data Catalog Vocabulary) do W3C phát triển, được tùy chỉnh cho ngữ cảnh châu Âu và quốc gia.
* Ứng dụng: Xây dựng Cổng dữ liệu quốc gia (data.gov.vn) và các cổng dữ liệu của bộ, ngành, địa phương phục vụ công bố dữ liệu mở.
