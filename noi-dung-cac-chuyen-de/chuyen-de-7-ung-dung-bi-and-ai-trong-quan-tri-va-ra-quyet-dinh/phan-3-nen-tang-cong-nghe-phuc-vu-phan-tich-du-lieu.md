# Phần 3 - Nền tảng công nghệ phục vụ phân tích dữ liệu

#### **1. Mục tiêu và vai trò của nền tảng**

* Nền tảng phân tích dữ liệu là lớp trung gian chiến lược trong kiến trúc dữ liệu, kết nối giữa hạ tầng lưu trữ (data warehouse, data lake) và các ứng dụng phân tích, ra quyết định (BI, AI).
* Giúp tích hợp, chuẩn hóa, lưu trữ, xử lý và trực quan hóa dữ liệu trên quy mô lớn, phục vụ giám sát điều hành, hoạch định chính sách và đánh giá hiệu quả hoạt động.
* Là công cụ cốt lõi để hình thành nền quản trị dựa trên dữ liệu (data-driven governance) trong Chính phủ số.

#### **2. Các mô hình công nghệ lưu trữ và phân tích dữ liệu**

**a) Data Warehouse (Kho dữ liệu truyền thống)**

* Là hệ thống lưu trữ dữ liệu có cấu trúc, được trích xuất và chuẩn hóa từ các hệ thống nghiệp vụ khác nhau.
* Tổ chức dữ liệu theo mô hình phân tích đa chiều (OLAP), phục vụ báo cáo, dashboard và các công cụ BI.
* Đặc điểm chính:
  * Dữ liệu có cấu trúc, ổn định, có lịch sử.
  * Phục vụ các nhu cầu phân tích định kỳ, tổng hợp, thống kê.
  * Tích hợp chặt chẽ với các công cụ BI, DSS.
* Hạn chế: Khó xử lý dữ liệu phi cấu trúc hoặc dữ liệu khối lượng cực lớn.

**b) Data Lake (Hồ dữ liệu)**

* Là mô hình lưu trữ dữ liệu thô (raw data) ở mọi định dạng (cấu trúc, phi cấu trúc, bán cấu trúc).
* Dữ liệu được đổ vào hồ ngay khi thu thập, chưa cần làm sạch hay chuẩn hóa.
* Đặc điểm chính:
  * Linh hoạt, chứa dữ liệu từ nhiều nguồn: IoT, mạng xã hội, văn bản, hình ảnh, log hệ thống…
  * Phù hợp cho các ứng dụng AI/ML, khai phá dữ liệu (data mining) và nghiên cứu dữ liệu lớn.
* Hạn chế:
  * Dữ liệu thiếu kiểm soát, dễ trở thành “data swamp” nếu không có metadata quản trị.
  * Không tối ưu cho truy vấn báo cáo tức thì.

**c) Lakehouse (Mô hình hợp nhất)**

* Là xu hướng mới kết hợp ưu điểm của Data Warehouse và Data Lake.
* Cho phép lưu trữ dữ liệu đa dạng như hồ dữ liệu, nhưng có quản trị metadata, schema và chất lượng dữ liệu như kho dữ liệu.
* Đặc điểm chính:
  * Cung cấp nền tảng hợp nhất cho BI và AI.
  * Hỗ trợ truy vấn bằng SQL đồng thời xử lý mô hình học máy (machine learning).
  * Tích hợp kiểm soát chất lượng, lịch sử thay đổi (versioning), và lineage.
*   Ưu điểm:

    * Đảm bảo hiệu năng, khả năng mở rộng, tính toàn vẹn và phân tích thời gian thực.
    * Phù hợp cho các hệ thống dữ liệu quốc gia quy mô lớn như Trung tâm dữ liệu quốc gia.

    <figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

#### **3. Nền tảng phân tích và trực quan hóa BI**

* Là lớp trung gian phân tích giữa kho dữ liệu và lãnh đạo, cán bộ quản lý; giúp chuyển đổi dữ liệu thô → thông tin → hiểu biết → hành động.
* BI là công cụ giúp chuyển đổi dữ liệu thành thông tin phục vụ ra quyết định, qua ba tầng:
  * Tầng tích hợp: Kết nối và đồng bộ dữ liệu từ Warehouse, Lake hoặc API.
  * Tầng xử lý và phân tích: Xây dựng mô hình chỉ tiêu, tính toán, lập bảng điều khiển (dashboard).
  * Tầng trình bày: Trực quan hóa dữ liệu, kể chuyện bằng dữ liệu (data storytelling).
* Yêu cầu trình bày dữ liệu hiệu quả trong khu vực công:
  * Dễ hiểu – chính xác – ngắn gọn.
  * Có khả năng drilldown để truy xuất nguồn.
  * Kết hợp giải thích (insights), không chỉ biểu đồ.
* BI hiện đại không chỉ mô tả quá khứ mà còn dự báo tương lai và gợi ý hành động.
  * Mô tả: Phân tích số liệu lịch sử.
  * Chẩn đoán: Tại sao xảy ra?
  * Dự báo: Dùng AI dự đoán xu hướng, rủi ro, nhu cầu.
  * Đề xuất hành động: Gợi ý quyết định tối ưu.

Từ đây, BI hiện đại = BI + AI → trở thành “bộ não phân tích” của Chính phủ số.

#### **4. Yêu cầu kỹ thuật và vận hành của nền tảng công nghệ**

a) Hiệu suất và khả năng mở rộng

* Hệ thống phải đáp ứng phân tích Big Data với khả năng mở rộng linh hoạt (scalable).
* Hỗ trợ xử lý song song, lưu trữ phân tán, và phân tích đa chiều (OLAP).
* Cung cấp khả năng Drill-down / Roll-up để truy vấn chi tiết theo thời gian, khu vực, ngành, cấp hành chính.

👉 _Ý nghĩa:_ Bảo đảm nhà quản lý có thể khai thác dữ liệu thời gian thực, phục vụ chỉ đạo điều hành tức thì.b) Kiểm soát chất lượng dữ liệu

* Thiết lập quy trình kiểm soát 3 giai đoạn:
  * Đầu vào (Input): xác thực, loại bỏ trùng lặp, kiểm tra định dạng.
  * Trung gian (Process): làm sạch, chuẩn hóa, đối chiếu với nguồn tham chiếu.
  * Đầu ra (Output): kiểm định chỉ tiêu, cảnh báo sai lệch, lưu log kiểm toán.
* Tích hợp cơ chế tự động phát hiện và cách ly dữ liệu lỗi (quarantine), kết hợp hệ thống cảnh báo sớm.

👉 _Ý nghĩa:_ Đảm bảo dữ liệu phân tích có độ chính xác, tin cậy và truy xuất được nguồn gốc.c) Bảo mật và phân quyền truy cập

* Áp dụng mô hình RBAC (Role-Based Access Control) – cấp quyền theo vai trò (lãnh đạo, chuyên viên, kỹ thuật viên).
* Mọi thao tác truy cập, truy vấn đều phải có Access Log và Data Lineage Tracking để đảm bảo minh bạch.
* Kết hợp các kỹ thuật:
  * Mã hóa dữ liệu khi lưu trữ và truyền tải.
  * Che giấu dữ liệu nhạy cảm (data masking).
  * Giới hạn truy cập theo vùng dữ liệu hoặc cấp độ nhạy cảm.

👉 _Ý nghĩa:_ Tuân thủ Luật Bảo vệ dữ liệu cá nhân (2025) và quy định về an toàn thông tin quốc gia.d) Kết nối và tích hợp với hệ thống AI/ML

* Dữ liệu từ kho được trích xuất để huấn luyện mô hình AI/ML:
  * Dự báo xu hướng dân cư, kinh tế, xã hội.
  * Phát hiện rủi ro, gian lận hoặc bất thường.
* Các mô hình AI có thể được tích hợp trực tiếp vào pipeline BI (BI + AI Convergence).
  * Dashboard có thể hiển thị dự báo tự động, hoặc đề xuất hành động thông minh dựa trên mô hình học máy.

👉 _Ví dụ:_ Hệ thống BI cảnh báo ngân sách có thể dự báo nguy cơ vượt chi, hoặc đề xuất điều chỉnh kế hoạch đầu tư theo dữ liệu thực tế.

#### **5. Ý nghĩa và xu hướng phát triển**

* Nền tảng công nghệ phân tích dữ liệu (BI, AI, Lakehouse) là xương sống của hạ tầng quản trị dữ liệu quốc gia.
* Cho phép Chính phủ và các cơ quan quản lý:
  * Phân tích và dự báo chính sách dựa trên bằng chứng dữ liệu.
  * Tăng tốc ra quyết định, cải thiện hiệu quả điều hành.
  * Minh bạch hóa thông tin, thúc đẩy chuyển đổi số trong toàn bộ hệ thống hành chính.
* Xu hướng tương lai:
  * Tích hợp BI – AI – Data Lakehouse thành hệ sinh thái phân tích dữ liệu hợp nhất.
  * Ứng dụng điện toán đám mây, xử lý thời gian thực (real-time analytics) và điều hành thông minh (smart governance).
