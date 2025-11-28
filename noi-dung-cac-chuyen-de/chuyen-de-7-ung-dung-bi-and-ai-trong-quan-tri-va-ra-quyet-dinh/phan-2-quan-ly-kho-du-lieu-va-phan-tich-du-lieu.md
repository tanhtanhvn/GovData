# Phần 2 - Quản lý kho dữ liệu và phân tích dữ liệu

#### **1. Vì sao cần có kho dữ liệu?**

Mỗi hệ thống lại lưu dữ liệu ở định dạng, cấu trúc và tiêu chuẩn khác nhau, dẫn đến:

* Phân tán dữ liệu: thông tin bị chia cắt, khó tổng hợp.
* Không đồng nhất: cùng một chỉ tiêu có thể được tính theo nhiều cách khác nhau.
* Thiếu lịch sử và bối cảnh: dữ liệu giao dịch chỉ phản ánh hiện trạng, không thể phân tích xu hướng.
* Thiếu cơ chế tin cậy để ra quyết định: báo cáo từ các nguồn khác nhau có thể cho kết quả mâu thuẫn.

👉 Vì vậy, kho dữ liệu ra đời để hợp nhất, chuẩn hóa và lưu trữ dữ liệu tập trung, tạo nền tảng cho các hoạt động phân tích, báo cáo, dự báo và hoạch định chính sách.

#### **2. Khái niệm và đặc điểm của kho dữ liệu**

* Kho dữ liệu là nền tảng lưu trữ dữ liệu chuyên biệt, được thiết kế cho mục tiêu phân tích, khác với các hệ thống giao dịch (OLTP).
* Dữ liệu trong kho được tích hợp từ nhiều nguồn (hệ thống nghiệp vụ, cơ sở dữ liệu chuyên ngành, dữ liệu mở, v.v.), theo mô hình phân tích đa chiều (OLAP – Online Analytical Processing).
* Đặc trưng chính của kho dữ liệu:
  * Subject-oriented: Tổ chức dữ liệu theo chủ đề (ví dụ: dân cư, tài chính, y tế).
  * Integrated: Dữ liệu được chuẩn hóa, loại bỏ trùng lặp, thống nhất mã định danh và định dạng.
  * Time-variant: Dữ liệu lưu vết lịch sử để phục vụ phân tích theo thời gian.
  * Non-volatile: Dữ liệu sau khi vào kho không bị chỉnh sửa trực tiếp, chỉ được cập nhật qua quy trình ETL chuẩn hóa. Do vậy kho không chứa dữ liệu gốc.

#### **3. Chức năng cốt lõi của kho dữ liệu**

* Tích hợp và chuẩn hóa dữ liệu:
  * Thu thập từ các hệ thống nghiệp vụ (ERP, CRM, CSDL chuyên ngành).
  * Làm sạch, chuẩn hóa, loại bỏ dữ liệu trùng, sai định dạng.
  * Kỹ thuật tích hợp:
    * ETL/ELT: chuyển đổi – làm sạch – tải dữ liệu vào kho.
    * CDC (Change Data Capture): đồng bộ theo thời gian thực.
    * API Gateway: tích hợp qua nền tảng chia sẻ dữ liệu (NDOP).
* Lưu trữ và tổ chức dữ liệu phân tích:
  * Dữ liệu được tổ chức theo mô hình sao (Star Schema) hoặc tuyết (Snowflake Schema) để dễ dàng tổng hợp và truy vấn.
  * Chuẩn hóa các chỉ tiêu phân tích theo định nghĩa thống nhất.
* Cung cấp nền tảng cho hệ thống BI & phân tích nâng cao:
  * Các công cụ BI (Power BI, Tableau, Qlik, v.v.) kết nối trực tiếp đến kho dữ liệu để tạo dashboard, báo cáo động và mô hình dự báo.
  * Cung cấp nguồn dữ liệu đáng tin cậy cho mọi hoạt động ra quyết định.

#### **4. Vai trò của kho dữ liệu trong quản trị và ra quyết định**

Kho dữ liệu là hạ tầng phân tích trung tâm của tổ chức, giúp:

* Tổng hợp và đối chiếu thông tin từ các nguồn dữ liệu khác nhau.
* So sánh xu hướng theo thời gian, giữa các lĩnh vực hoặc đơn vị hành chính.
* Hỗ trợ hệ thống chỉ tiêu và ra quyết định (Decision Support System – DSS).
* Đảm bảo tính toàn vẹn dữ liệu: Mọi báo cáo và dashboard đều dựa trên cùng một nền dữ liệu gốc.

📌 _Ý nghĩa thực tiễn:_ Nhờ kho dữ liệu, các nhà quản lý có thể theo dõi tình hình kinh tế – xã hội, ngân sách, dân cư, y tế, giáo dục… trên cùng một nền dữ liệu thống nhất, giúp ra quyết định nhanh, chính xác và minh bạch.

#### **5. Cơ chế tổng hợp và tổ chức chỉ tiêu phân tích**

a) Cơ chế tổng hợp chỉ tiêu

* Là quy trình tính toán, đối soát và chuẩn hóa các chỉ tiêu phân tích từ dữ liệu gốc (chỉ lưu dữ liệu tổng hợp trong kho).
* Được thực hiện qua công cụ ETL/ELT (Extract – Transform – Load):
  * Extract: Trích xuất dữ liệu từ hệ thống nguồn.
  * Transform: Làm sạch, chuẩn hóa, chuyển đổi định dạng, tính toán chỉ tiêu.
  * Load: Tải vào kho dữ liệu để lưu trữ và phân tích.
* Mọi kết quả tổng hợp phải có dấu vết kiểm toán (audit trail) và lưu trữ theo thời gian, lĩnh vực, tổ chức nhằm phục vụ kiểm chứng, truy xuất nguồn gốc.

b) Tổ chức các chỉ tiêu phân tích

* Các chỉ tiêu phải có mã định danh, định nghĩa, đơn vị đo lường, chu kỳ cập nhật và nguồn dữ liệu.
* Chia nhóm theo mục tiêu phân tích:
  * Điều hành: phục vụ lãnh đạo giám sát tiến độ, hiệu quả.
  * Giám sát & cảnh báo: theo dõi các chỉ số rủi ro, cảnh báo sớm.
  * Dự báo & phân tích hiệu quả: phục vụ hoạch định chính sách.
* Mọi thay đổi trong cấu trúc chỉ tiêu phải qua quy trình quản lý thay đổi (Change Management) để đảm bảo thống nhất và truy vết.

#### **6. Tổ chức kho dữ liệu chuyên biệt**

a). Khái niệm Data Mart

* Là phân vùng dữ liệu được thiết kế riêng cho một lĩnh vực, phòng ban hoặc nghiệp vụ cụ thể.
* Giúp tăng tốc độ truy vấn, phân quyền truy cập chi tiết hơn, và tối ưu tài nguyên hệ thống.

b) Các mô hình tổ chức Data Mart

* Theo miền dữ liệu (Domain-based): ví dụ dân cư, kinh tế, xã hội.
* Theo cơ cấu tổ chức (Department-based): ví dụ Bộ Tài chính, Bộ Y tế.
* Theo nghiệp vụ (Subject-oriented): ví dụ ngân sách, giáo dục, lao động.

c) Nguyên tắc thiết kế

* Tương thích với mô hình dữ liệu tổng thể của kho trung tâm.
* Hỗ trợ tích hợp hai chiều:
  * Nhận dữ liệu đã chuẩn hóa từ kho trung tâm.
  * Phản hồi lại dữ liệu phân tích, kết quả chỉ tiêu lên hệ thống tổng hợp.
* Tuân thủ quản trị dữ liệu và bảo mật tập trung, tránh tạo “đảo dữ liệu” mới.

📌 _Ý nghĩa:_ Data Mart giúp phân quyền truy cập hợp lý, nâng cao tốc độ phân tích, và đưa dữ liệu tới đúng đối tượng sử dụng — đặc biệt quan trọng trong mô hình Chính phủ số đa tầng (Trung ương – Bộ ngành – Địa phương).
