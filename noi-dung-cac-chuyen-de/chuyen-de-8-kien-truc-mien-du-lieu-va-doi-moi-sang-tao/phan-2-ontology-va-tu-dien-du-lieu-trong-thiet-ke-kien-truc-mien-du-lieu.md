# Phần 2 - Ontology và Từ điển dữ liệu trong thiết kế kiến trúc miền dữ liệu

#### **1.** **Khái niệm Ontology và Từ điển Dữ liệu**

**a) Ontology (Mô hình ngữ nghĩa)**

* Là mô hình mô tả các khái niệm, mối quan hệ giữa các khái niệm và quy tắc nghiệp vụ trong một miền dữ liệu.
* Cấu trúc gồm:
  * Lớp (Class) – đại diện nhóm đối tượng (Bệnh nhân, Cơ sở y tế, Dịch vụ khám chữa bệnh...).
  * Thuộc tính (Property) – đặc trưng hoặc mối quan hệ giữa các đối tượng.
  * Cá thể (Instance) – giá trị cụ thể của đối tượng (Bệnh nhân Nguyễn Văn A...).
  * Luật suy luận (Rules) – quy tắc logic cho phép hệ thống suy diễn tri thức mới.
* Ví dụ:
  * “Bệnh nhân” được “điều trị tại” “Cơ sở y tế”.
  * “Bệnh nhân” “mắc” “Bệnh lý”.
  * “Dịch vụ y tế” “tuân theo” “Danh mục ICD-10”.
* Vai trò:
  * Chuẩn hóa ý nghĩa dữ liệu để con người và máy cùng hiểu thống nhất.
  * Tạo nền tảng cho liên thông ngữ nghĩa và phân tích thông minh (AI/ML).
  * Là cốt lõi của hệ thống dữ liệu có khả năng “hiểu” và “suy luận” tri thức.

**b) Từ điển Dữ liệu**

* Là bộ mô tả kỹ thuật các phần tử dữ liệu được sử dụng trong hệ thống thông tin.
* Mỗi phần tử gồm: tên, kiểu dữ liệu, độ dài, đơn vị, mô tả, nguồn và quy tắc mã hóa.
* Ví dụ:
  * “Patient\_ID”: mã bênh nhân, 10 ký tự, nguồn HIS.
  * “Disease\_Code”: mã bệnh chuẩn ICD-10.
* Vai trò:
  * Chuẩn hóa cấu trúc dữ liệu để các hệ thống có thể trao đổi, xử lý và tích hợp.
  * Đảm bảo thống nhất về định dạng, kiểu và quy tắc kỹ thuật trong toàn bộ kho dữ liệu.

**c) Mối quan hệ giữa Ontology và Từ điển Dữ liệu**

* Từ điển dữ liệu mô tả _“dữ liệu có gì và được định nghĩa ra sao”_.
* Ontology mô tả _“dữ liệu có ý nghĩa gì và liên hệ thế nào trong thực tiễn”_.
* Khi kết hợp:
  * Dữ liệu vừa có cấu trúc rõ ràng, vừa có ngữ nghĩa logic.
  * Tạo thành hệ thống dữ liệu có thể hiểu được và suy luận được (machine-understandable data).

#### **2.** **Hệ thống Từ điển Dữ liệu Dùng Chung Quốc Gia**

**a) Vai trò và mục tiêu**

* Là thành phần cốt lõi trong Khung Kiến trúc Dữ liệu Quốc gia (QĐ 2439/QĐ-TTg, 2025).
* Đảm bảo mọi cơ quan, bộ, ngành, địa phương hiểu và sử dụng dữ liệu theo cùng chuẩn.
* Tích hợp hai lớp chuẩn hóa:
  * Chuẩn kỹ thuật (Technical Standardization).
  * Chuẩn ngữ nghĩa (Semantic Standardization).

**b) Cấu trúc hệ thống từ điển dữ liệu dùng chung**

* Từ điển dữ liệu cấp quốc gia: dữ liệu chủ quốc gia, dữ liệu danh mục chuẩn hóa dùng chung liên ngành.
* Từ điển dữ liệu chuyên ngành: dữ liệu chủ chuyên ngành, dữ liệu danh mục chuyên ngành.

**c) Chức năng của hệ thống**

* Chuẩn hóa định danh dữ liệu công.
* Đảm bảo liên thông và chia sẻ dữ liệu xuyên ngành qua NDOP (Nền tảng chia sẻ và mở dữ liệu quốc gia).
* Cung cấp nền tảng cho việc xây dựng các kho dữ liệu dùng chung, dữ liệu mở và kho dữ liệu chủ.
* Hỗ trợ triển khai AI và phân tích thông minh trên dữ liệu công.

#### **3.** **Mối quan hệ giữa Ontology, Từ điển Dữ liệu và Kiến trúc Miền Dữ liệu**

**a) Từ điển dữ liệu trong kiến trúc miền dữ liệu**

* Xác định cấu trúc, định danh, đơn vị đo, mã hóa cho từng phần tử trong miền.
* Đảm bảo dữ liệu của miền tương thích kỹ thuật với kiến trúc dữ liệu tổng thể.

**b) Ontology trong kiến trúc miền dữ liệu**

* Mô hình hóa các khái niệm nghiệp vụ cốt lõi và mối quan hệ giữa chúng.
* Giúp hệ thống hiểu được logic hoạt động của miền (ai – làm gì – với cái gì).
* Cho phép phân tích và truy vấn thông minh: ví dụ “tất cả bệnh nhân được điều trị bởi bệnh viện tuyến tỉnh có mã bệnh thuộc nhóm truyền nhiễm”.

**c) Khi kết hợp ontology và từ điển dữ liệu**

* Tạo ra kiến trúc miền dữ liệu “ba lớp”:
  * Lớp kỹ thuật: cấu trúc dữ liệu.
  * Lớp ngữ nghĩa: ý nghĩa và mối quan hệ.
  * Lớp nghiệp vụ: quy trình và logic hoạt động.
* Kết quả là một miền dữ liệu có thể tích hợp, liên thông và khai thác hiệu quả trong toàn bộ kiến trúc quốc gia.

#### **4.** **Ứng dụng và minh họa thực tiễn**

**a) Ví dụ miền Y tế**

* Ontology: FHIR, SNOMED CT, ICD-10.
* Kết nối khái niệm Bệnh nhân – Bệnh viện – Dịch vụ – Chẩn đoán – Kết quả.
* Từ điển dữ liệu: mô tả mã bệnh, mã xét nghiệm, kiểu dữ liệu thống nhất.
* Kết quả: dữ liệu bệnh nhân từ nhiều bệnh viện được đồng bộ, hỗ trợ phân tích dịch tễ.

**b). Ví dụ miền Giáo dục**

* Ontology: Người học – Cơ sở giáo dục – Nhà giáo – Hồ sơ học tập suốt đời.
* Từ điển dữ liệu: số định danh cá nhân, mã số hồ sơ học tập suốt đời, mã trường, mã môn học.
* Khi liên thông với dữ liệu dân cư và y tế: phân tích mối tương quan giữa sức khỏe, địa lý và kết quả học tập.

**c). Ví dụ miền Kinh tế – Tài chính**

* Ontology: Doanh nghiệp – Ngành nghề – Thuế – Hoạt động sản xuất.
* Từ điển dữ liệu: mã doanh nghiệp, mã ngành VSIC, mã thuế.
* Ứng dụng: phân tích sức khỏe kinh tế quốc gia, cảnh báo sớm rủi ro tài chính.
