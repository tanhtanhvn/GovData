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

#### **4.** **Cấu trúc mô tả thuật ngữ**

* Mô tả nghiệp vụ
  * (1) Mã định danh duy nhất (ID), ví dụ: ndg:ID-001
  * (2) Tên nghiệp vụ, ví dụ: HoVaTen (tiếng Việt), FullName (tiếng Anh).
  * (3) Định nghĩa nghiệp vụ, ví dụ: HoVaTen: tên đầy đủ của cá nhân, bao gồm họ, tên đệm, và tên chính, dùng để xác định danh tính.
  * (4) Mô tả ngữ cảnh sử dụng, ví dụ: HoVaTen được dùng trong đăng ký dịch vụ công, xác minh danh tính, và quản lý hồ sơ dân cư.
  * (5) Nhóm dữ liệu/Phân loại, ví dụ: nhóm dữ liệu: Dân cư; Phân loại: Thông tin cá nhân.
  * (6) Mối quan hệ với thực thể, ví dụ: HoVaTen là thuộc tính của thực thể CaNhan; liên kết với DiaChiThuongTru qua mối quan hệ hasAddress.
  * (7) Đơn vị tạo ra dữ liệu, ví dụ: Bộ Công an (tạo dữ liệu HoVaTen từ Cơ sở dữ liệu quốc gia về Dân cư).
  * (8) Đơn vị sở hữu dữ liệu.
  * (9) Ngôn ngữ, ví dụ: Tiếng Việt (HoVaTen), tiếng Anh (FullName).
  * (10) Phiên bản/Trạng thái, ví dụ: Phiên bản 1.0, trạng thái: Đang sử dụng, cập nhật: 2025-07-21.
  * (11) Tài liệu liên quan, ví dụ: Luật Căn cước 2023.
  * (12) Từ đồng nghĩa/gần nghĩa, ví dụ: HoVaTen → TenDayDu, TenCaNhan.
  * (13) Thuật ngữ liên quan (Related Terms), ví dụ: HoVaTen liên quan đến CCCD, NgaySinh, GioiTinh.
  * (14) Thuộc tính mô tả nghiệp vụ, ví dụ: đối với thực thể CaNhan, các thuộc tính nghiệp vụ bao gồm HoVaTen, NgaySinh, GioiTinh, DiaChiThuongTru, QuocTich,…
* Mô tả kỹ thuật:&#x20;
  * (15) Tên trường kỹ thuật (Technical Name), ví dụ: CaNhan.full\_name.
  * (16) Loại dữ liệu, ví dụ: String (cho HoVaTen).
  * (17) Độ dài/Định dạng, ví dụ: HoVaTen: Độ dài tối đa 50 ký tự; NgaySinh: Định dạng YYYY-MM-DD.
  * (18) Kiểu dữ liệu mô hình (RDF/OWL), ví dụ: xsd:string (cho HoVaTen), xsd: date (cho NgaySinh).
  * (19) Quan hệ với trường khác, ví dụ: HoVaTen thuộc CaNhan, DiaChiThuongTru có quan hệ hasAddress với CaNhan.
  * (20) Thuộc tính kỹ thuật (Attributes), ví dụ: Đối với CaNhan, các thuộc tính kỹ thuật bao gồm HoVaTen, NgaySinh, GioiTinh, DiaChiThuongTru, QuocTich,…
  * (21) Danh sách giá trị, ví dụ: GioiTinh: \[Nam, Nữ, Khác].
  * (22) Quy tắc chuẩn hóa, ví dụ: HoVaTen: In hoa chữ cái đầu (Nguyen Van A).
  * (23) API mô tả truy cập, ví dụ: GET/api/CaNhan/{id}, định dạng JSON.
  * (24) Tương thích chuẩn quốc tế (Mapping quốc tế), ví dụ: HoVaTen → schema:name, CCCD → nc: PersonIdentification, NgaySinh → schema:birthDate, GioiTinh → nc: PersonSexCode,...
  * (25) Miền giá trị hợp lệ (Validation Rules), ví dụ: CCCD: 12 ký tự số, bắt buộc.

#### 5. Quy trình xây dựng từ điển dữ liệu

* Phân tích ⇒ anh sách từ vựng thô (bao gồm thuật ngữ, mô tả, ngữ cảnh sử dụng).
  * Đánh giá nhu cầu dữ liệu dùng chung
  * Rà soát tài liệu, biểu mẫu, quy trình nghiệp vụ và hệ thống công nghệ thông tin hiện có.
  * Thu thập danh sách thuật ngữ, trường dữ liệu từ các cơ sở dữ liệu chuyên ngành.
  * Gom nhóm các thuật ngữ tương tự nhưng khác tên, xác định từ vựng cần chuẩn hóa.
* Chuẩn hóa ⇒ Danh mục từ vựng chuẩn hóa, có định nghĩa và phân loại rõ ràng.
  * Chuẩn hóa tên, định nghĩa, loại bỏ từ đồng nghĩa hoặc gây nhầm lẫn.
  * Phân loại từ vựng: từ vựng cốt lõi (dùng chung, ví dụ: thông tin cá nhân), từ vựng chuyên ngành (y tế, giáo dục, tài chính...).
  * Gắn thuật ngữ với ngữ cảnh nghiệp vụ và cơ quan chịu trách nhiệm.
  * Ánh xạ với các chuẩn quốc tế chuyên ngành (nếu có)
* Mô hình hóa ⇒ Mô hình từ vựng có cấu trúc thống nhất.
  * Thiết kế cấu trúc kỹ thuật: tên, mô tả, kiểu dữ liệu, định dạng, mã hóa,…
  * Thiết lập quan hệ phân cấp
  * Mô hình hóa bằng chuẩn kỹ thuật
* Xác thực ⇒ Danh mục từ vựng đã xác thực.
  * Thẩm định kỹ thuật: kiểm tra logic, định dạng, kiểu dữ liệu.
  * Thẩm định ngữ nghĩa: bảo đảm phù hợp pháp lý và hành chính.
  * Tham vấn chuyên ngành: gửi từ vựng đến các đơn vị liên quan để xác nhận.
* Công bố ⇒ Đăng tải trên cổng Từ điển dữ liệu dùng chung để sử dụng chung, bảo đảm khả năng truy cập mở và tái sử dụng.
* Quản trị ⇒ Thiết lập quy trình quản lý vòng đời, cơ chế phiên bản hóa, cập nhật định kỳ, gắn mã định danh duy nhất cho từng thuật ngữ; giám sát áp dụng.

#### 6. Chuẩn dữ liệu metadata

**a) Chuẩn đăng ký metadata (ISO 11179)**

* Tên đầy đủ: _ISO/IEC 11179 – Information Technology — Metadata Registries (MDR)_
* Cơ quan ban hành: Tổ chức Tiêu chuẩn hóa Quốc tế (ISO) và Ủy ban Kỹ thuật Điện Quốc tế (IEC).
* Mục đích: Chuẩn hóa cách mô tả, quản lý và đăng ký siêu dữ liệu (metadata) để đảm bảo dữ liệu được hiểu và sử dụng thống nhất.
* Ứng dụng: Là nền tảng cho việc xây dựng Từ điển dữ liệu dùng chung và liên thông dữ liệu giữa các hệ thống khác nhau.
* Nội dung: Gồm 6 phần mô tả toàn bộ vòng đời và cấu trúc quản lý metadata

b) **Chuẩn metadata dữ liệu mở (DCAT-AP)**

* Tên đầy đủ: _DCAT-AP (Data Catalog Vocabulary – Application Profile for data portals in Europe)_
* Cơ quan ban hành: Ủy ban Châu Âu (European Commission) và Tổ chức W3C (World Wide Web Consortium).
* Mục tiêu: Chuẩn hóa mô tả siêu dữ liệu (metadata) của bộ dữ liệu mở (open data) để các cổng dữ liệu quốc gia và quốc tế có thể trao đổi, tìm kiếm, liên thông và chia sẻ dữ liệu dễ dàng.
* Bản chất: DCAT-AP là “hồ sơ ứng dụng” (Application Profile) mở rộng từ chuẩn DCAT (Data Catalog Vocabulary) do W3C phát triển, được tùy chỉnh cho ngữ cảnh châu Âu và quốc gia.
* Ứng dụng: Xây dựng Cổng dữ liệu quốc gia (data.gov.vn) và các cổng dữ liệu của bộ, ngành, địa phương phục vụ công bố dữ liệu mở.
