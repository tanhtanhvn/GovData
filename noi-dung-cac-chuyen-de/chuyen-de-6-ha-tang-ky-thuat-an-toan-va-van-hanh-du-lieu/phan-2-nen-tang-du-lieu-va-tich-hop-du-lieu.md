# Phần 2 - Nền tảng dữ liệu và tích hợp dữ liệu

#### ​**1. Nền tảng dữ liệu**

**a) Vai trò và chức năng**

* Là xương sống kỹ thuật trong toàn bộ hệ sinh thái dữ liệu Chính phủ số.
* Đảm bảo kết nối, tích hợp, quản trị và khai thác dữ liệu đồng bộ giữa các bộ, ngành, địa phương và hệ thống chuyên ngành.
* Giúp thực thi nguyên tắc “Dữ liệu được quản trị tập trung nhưng triển khai phân tán”, hướng tới mô hình Data Fabric – Data Mesh trong quản trị quốc gia.
  * Data Fabric là mô hình kiến trúc cung cấp một lớp tích hợp dữ liệu thống nhất, dùng AI để tự động kết nối, khám phá, quản lý, bảo vệ và phân phối dữ liệu trên toàn tổ chức.
  * Data Mesh là mô hình quản lý dữ liệu phân tán, nơi mỗi miền dữ liệu (data domain) tự quản lý dữ liệu của mình như một “sản phẩm dữ liệu” (data product).

**b) Các thành phần chính của nền tảng dữ liệu**

* Nền tảng chia sẻ và điều phối dữ liệu
  * Trung tâm kết nối, trao đổi dữ liệu giữa các cơ quan hành chính.
  * Cung cấp dịch vụ điều phối (orchestration), đồng bộ, phân quyền truy cập, giám sát chia sẻ dữ liệu theo thời gian thực.
  * Bảo đảm giao tiếp chuẩn hóa thông qua API Gateway và các giao thức an toàn (HTTPS, MQTT, NGSI-LD…).
* Nền tảng phân tích, tổng hợp dữ liệu
  * Hỗ trợ thu thập, tổng hợp, xử lý và khai phá dữ liệu từ nhiều nguồn.
  * Tích hợp các công cụ BI (Business Intelligence), ML/AI và dashboard phục vụ phân tích dự báo, ra quyết định chính sách.
  * Cho phép thực hiện phân tích đa chiều (OLAP), mô hình dự báo và mô phỏng chiến lược.
* Nền tảng giám sát và quản trị dữ liệu (Data Governance Platform)
  * Quản lý toàn bộ vòng đời dữ liệu (data lifecycle), từ tạo lập, lưu trữ đến hủy bỏ.
  * Hỗ trợ kiểm soát chất lượng, metadata, lineage, quyền truy cập và tuân thủ pháp lý.
  * Tích hợp công cụ quản lý metadata (theo ISO/IEC 11179), hệ thống kiểm tra chất lượng (DQI), và dashboard giám sát (Data Quality Dashboard).

**2. Tích hợp dữ liệu**

**a) Mục tiêu tích hợp dữ liệu**

* Đảm bảo dòng chảy dữ liệu thống nhất giữa các hệ thống thông tin, cơ sở dữ liệu quốc gia, chuyên ngành, địa phương và nền tảng chia sẻ NDOP.
* Tạo điều kiện liên thông, tái sử dụng dữ liệu phục vụ nghiệp vụ quản lý, điều hành, hoạch định chính sách và cung cấp dịch vụ công.
* Hỗ trợ phân tích dữ liệu tổng hợp, khai phá dữ liệu và ra quyết định dựa trên dữ liệu (data-driven decision making).

**b) Hình thức tích hợp dữ liệu**

* Theo lô (batch):
  * Thu thập và xử lý dữ liệu định kỳ theo chu kỳ (giờ, ngày, tuần).
  * Dùng cho dữ liệu lớn, ổn định, phục vụ thống kê, báo cáo, đồng bộ định kỳ.
* Theo thời gian thực:
  * Dữ liệu được cập nhật ngay khi phát sinh (event-driven).
  * Ứng dụng trong giám sát điều hành, cảnh báo sớm, giao thông, y tế, tài chính...
* Qua API và cổng dữ liệu mở:
  * Dữ liệu được truy cập linh hoạt, theo yêu cầu của từng đối tượng.
  * Hỗ trợ chia sẻ qua API Gateway, NGSI-LD, Cổng dữ liệu (theo chuẩn DCAT-AP).

**c) Quy trình kiểm soát đầu vào (Data Ingestion)**

* Bước 1 – Xác thực nguồn dữ liệu: Kiểm tra định danh, chữ ký số, chứng thực truy cập.
* Bước 2 – Kiểm định định dạng: So khớp với schema chuẩn, loại dữ liệu, mã hóa.
* Bước 3 – Loại bỏ trùng lặp: So sánh định danh, khóa chính hoặc fingerprint dữ liệu.
* Bước 4 – Gắn metadata: Ghi nhận nguồn gốc, thời gian tạo lập, đơn vị sở hữu, cấp độ nhạy cảm.
* Bước 5 – Đưa vào pipeline xử lý: Phân tầng dữ liệu tương ứng để xử lý, phân tích hoặc lưu trữ.

**d) Cấu trúc phân tầng dữ liệu**

* Tầng Thô
  * Lưu trữ dữ liệu nguyên bản, chưa qua xử lý, như khi được thu thập.
  * Dữ liệu ở dạng file log, IoT stream, tập tin upload, v.v.
  * Mục đích: kiểm tra, đối chiếu, truy vết nguồn dữ liệu.
* Tầng Xử Lý
  * Làm sạch dữ liệu, chuẩn hóa định dạng, loại bỏ trùng lặp và sai lệch.
  * Dữ liệu sẵn sàng cho truy vấn nghiệp vụ, phân loại hoặc đối chiếu liên ngành.
  * Kết quả: dữ liệu đã có cấu trúc ổn định, phục vụ cho bước chuẩn hóa.
* Tầng Chuẩn Hóa
  * Lưu trữ dữ liệu đáng tin cậy, đã qua xác thực nghiệp vụ và kỹ thuật.
  * Dữ liệu có metadata, phiên bản (versioning), gắn quyền truy cập.
  * Là nguồn chính cho dashboard quản lý, phân tích thống kê, khai thác báo cáo.
* Tầng Phân Tích
  * Dữ liệu đã được tổng hợp, gom nhóm và xử lý phục vụ mô hình hóa, AI, học máy.
  * Lưu trong data warehouse, data lakehouse hoặc data mart.
  * Cho phép khai thác thông minh (predictive, prescriptive analytics).
