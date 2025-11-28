# Phần 3 - Thiết kế kiến trúc miền dữ liệu và vai trò của Kiến trúc sư miền dữ liệu

#### **1.** **Nguyên tắc thiết kế kiến trúc miền dữ liệu**

a) Phù hợp với mô hình dữ liệu tổng thể quốc gia

* Mọi miền dữ liệu (domain) đều phải kế thừa và tuân thủ Khung Kiến trúc Dữ liệu Quốc gia.
* Các miền được thiết kế theo nguyên tắc phân tầng, gồm:
  * Tầng ngữ nghĩa (Semantic Layer): dùng ontology để định nghĩa ý nghĩa và mối quan hệ giữa các khái niệm.
  * Tầng metadata: mô tả cấu trúc, nguồn gốc, và chất lượng dữ liệu.
  * Tầng kỹ thuật (Data Dictionary Layer): định nghĩa định dạng, kiểu dữ liệu, mã hóa, đơn vị, và quy tắc chia sẻ.

b) Phát triển độc lập nhưng liên thông

* Mỗi miền dữ liệu (ví dụ: y tế, giáo dục, dân cư, tài chính) có thể được xây dựng và vận hành độc lập.
* Tuy nhiên, các miền phải tương thích ngữ nghĩa (semantic compatibility) để có thể liên kết, đồng bộ và phân tích liên miền khi cần (ví dụ: phân tích dữ liệu dân cư kết hợp giáo dục để dự báo nhu cầu trường học).

c) Hướng đến khả năng tích hợp – mở rộng – chia sẻ

* Thiết kế kiến trúc miền dữ liệu cần mở (open architecture), cho phép mở rộng dễ dàng với dữ liệu mới.
* Cần định nghĩa rõ các API chia sẻ, chuẩn trao đổi (DCAT-AP, JSON-LD, RDF) và chính sách bảo mật – truy cập dữ liệu.

d) Tích hợp đa tầng

* Tầng vật lý: nơi lưu trữ dữ liệu thô (data lake, lakehouse).
* Tầng logic: nơi cấu trúc dữ liệu theo chủ đề miền.
* Tầng ngữ nghĩa: nơi định nghĩa ontology giúp máy hiểu được ngữ cảnh.
* Tầng ứng dụng: nơi BI/AI và các công cụ khai thác hoạt động.

#### **2.** **Các bước thiết kế cơ bản kiến trúc miền dữ liệu**

a) Phân tích nghiệp vụ và đối tượng dữ liệu

* Xác định rõ miền nghiệp vụ: y tế, giáo dục, tài chính, dân cư, môi trường,...
* Thu thập yêu cầu nghiệp vụ, quy trình và các thực thể dữ liệu chính.
  * Ví dụ miền y tế: Bệnh nhân – Bác sĩ – Cơ sở y tế – Dịch vụ khám – Bệnh lý – Thuốc – Kết quả điều trị.

b) Xây dựng mô hình ngữ nghĩa (Ontology)

* Xác định các khái niệm (concepts), quan hệ (relations), và ràng buộc (constraints).
* Xây dựng ontology theo chuẩn quốc tế khi có thể (ví dụ: FHIR Ontology trong y tế, EDU Ontology trong giáo dục).
* Đảm bảo ontology phản ánh đúng logic nghiệp vụ – đây chính là “bộ não” của miền dữ liệu.

c) Chuẩn hóa phần tử dữ liệu và định danh trong từ điển dữ liệu

* Mỗi thực thể và thuộc tính trong ontology phải được gắn định danh kỹ thuật (metadata ID) trong từ điển dữ liệu.
* Đảm bảo tương thích với Hệ thống Từ điển Dữ liệu Dùng chung Quốc gia.
* Mục tiêu: ngữ nghĩa và cấu trúc thống nhất giữa các miền → tạo nền tảng liên thông quốc gia.

d) Thiết lập quy tắc chia sẻ, bảo mật và vòng đời dữ liệu

* Xác định phân quyền truy cập theo vai trò (RBAC).
* Định nghĩa vòng đời dữ liệu (Data Lifecycle): tạo lập → lưu trữ → khai thác → lưu trữ lâu dài → hủy/xóa.
* Cài đặt chính sách bảo mật và kiểm soát truy vết dữ liệu (data lineage).

đ) Kết nối với Cơ sở dữ liệu tổng thể quốc gia và các miền khác

* Thiết kế các API và pipeline để dữ liệu miền có thể:
  * Tích hợp đồng bộ với Cơ sở dữ liệu tổng hợp Quốc gia.
  * Chia sẻ theo yêu cầu hoặc chủ động thông qua NDOP.
* Đảm bảo khả năng phân tích liên miền (cross-domain analytics) – đây là giá trị cốt lõi của Chính phủ dữ liệu.

#### **3.** **Vai trò của Kiến trúc sư Miền Dữ liệu**

a) Định nghĩa vai trò

* Là người thiết kế mô hình dữ liệu, ontology và cấu trúc chia sẻ của một miền nghiệp vụ cụ thể.
* Đóng vai trò kết nối giữa chuyên môn nghiệp vụ, kỹ thuật dữ liệu và quản trị dữ liệu.
* Là người dịch ngôn ngữ nghiệp vụ thành ngôn ngữ dữ liệu có thể khai thác và liên thông.

b) Nhiệm vụ chính

* Xây dựng bản thiết kế miền dữ liệu.
* Đảm bảo miền dữ liệu phù hợp với kiến trúc tổng thể quốc gia, tương thích ngữ nghĩa và kỹ thuật.
* Phối hợp với các CDO (Chief Data Officer) và Data Engineer để triển khai, vận hành.
* Giám sát chất lượng dữ liệu, hỗ trợ các nhóm nghiệp vụ phân tích và khai thác dữ liệu.

c) Vai trò trong đổi mới dữ liệu công

* Kiến trúc sư miền dữ liệu là người đặt nền móng cho sáng tạo dữ liệu công:
  * Thiết kế sandbox thử nghiệm dữ liệu.
  * Xây dựng danh mục dữ liệu mở để thúc đẩy đổi mới sáng tạo.
  * Kết nối dữ liệu hành chính – dữ liệu nghiên cứu – dữ liệu mở để phát triển sản phẩm mới.
* Góp phần chuyển dịch từ “quản lý dữ liệu” → “khai thác dữ liệu tạo giá trị công”.

<figure><img src="../../.gitbook/assets/image (21).png" alt="" width="563"><figcaption></figcaption></figure>

#### **4.** **Kỹ năng cốt lõi của Kiến trúc sư Miền Dữ liệu**

a) Kỹ năng nghiệp vụ

* Hiểu sâu quy trình nghiệp vụ của miền được phụ trách (ví dụ: quy trình quản lý bệnh án, quy trình giáo dục, tài chính công,...).
* Biết phân tích yêu cầu và mô hình hóa quy trình thành dữ liệu.

b) Kỹ năng kỹ thuật

* Thành thạo mô hình hóa dữ liệu (ERD, UML, RDF Graph).
* Thiết kế ontology bằng OWL/RDF/Protégé.
* Quản lý metadata, từ điển dữ liệu và tiêu chuẩn DCAT-AP.
* Làm việc với các nền tảng dữ liệu như Data Lakehouse, BI Tools (Power BI, Tableau), AI pipelines.

c) Kỹ năng liên ngành và tư duy đổi mới

* Hiểu về quản trị dữ liệu, an toàn dữ liệu và quy định pháp lý.
* Có khả năng kết hợp dữ liệu liên miền để tạo giá trị mới.
* Thiết kế và giám sát các cơ chế sandbox để thử nghiệm các mô hình AI, dự báo, hoặc dịch vụ công dữ liệu mở.
