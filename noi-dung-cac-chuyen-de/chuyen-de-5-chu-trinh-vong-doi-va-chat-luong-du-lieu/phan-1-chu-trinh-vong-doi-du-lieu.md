# Phần 1 - Chu trình vòng đời dữ liệu

#### **1.** **Khái niệm và ý nghĩa**

* Vòng đời dữ liệu (Data Lifecycle) là chuỗi các giai đoạn mà dữ liệu trải qua — từ khi được thu thập, tạo lập đến khi bị hủy hoặc lưu trữ lâu dài.
* Mục tiêu của quản lý vòng đời là:
  * Bảo đảm chất lượng, an toàn và khả năng tái sử dụng dữ liệu.
  * Quản lý dữ liệu như một tài sản có giá trị, được bảo trì, khai thác và loại bỏ đúng quy trình.
  * Gắn kết với chu trình quản trị – tuân thủ – kiểm toán – cải tiến liên tục.

#### **2. Các giai đoạn trong vòng đời dữ liệu**

<figure><img src="../../.gitbook/assets/image (44).png" alt="" width="375"><figcaption></figcaption></figure>

**(1) Thu thập dữ liệu**

* Mục tiêu: Xác định nguồn và phương thức thu thập dữ liệu đầu vào.
* Nguồn thu thập:
  * Hệ thống hành chính, biểu mẫu điện tử, hồ sơ nghiệp vụ.
  * Thiết bị cảm biến, camera, IoT, dữ liệu giao dịch, dữ liệu từ bên thứ ba.
* Yêu cầu:
  * Có mục tiêu rõ ràng, định nghĩa dữ liệu đầu vào, quyền hợp pháp để thu thập.
  * Đảm bảo tính chính xác, hợp lệ và minh bạch nguồn gốc.

**(2) Tạo lập dữ liệu**

* Mục tiêu: Dữ liệu được sinh ra, nhập vào hệ thống và định danh.
* Hoạt động chính:
  * Chuẩn hóa định dạng (schema, code, định danh duy nhất).
  * Gắn metadata ban đầu (ngày tạo, người tạo, nguồn dữ liệu).
* Kết quả: Hình thành dữ liệu gốc (raw data) — nền tảng cho toàn bộ vòng đời tiếp theo.

**(3) Phân loại dữ liệu**

* Mục tiêu: Phân chia dữ liệu theo mức độ nhạy cảm, giá trị, và mục đích sử dụng.
* Phân loại cơ bản:
  * Theo mức độ bảo mật: công khai, nội bộ, mật, tuyệt mật.
  * Theo chức năng: dữ liệu hành chính, kỹ thuật, nghiệp vụ, tài chính.
  * Theo định dạng: cấu trúc, bán cấu trúc, phi cấu trúc.
  * Theo dữ liệu cá nhân: cá nhân cơ bản, cá nhân nhạy cảm, cá nhân khác
  * Theo mức độ quan trọng: dữ liệu cốt lõi, dữ liệu quan trọng,
* Ý nghĩa: Giúp xác định cách quản lý, quyền truy cập và mức bảo vệ phù hợp.

**(4) Dán nhãn dữ liệu**

* Khái niệm: Gắn nhãn hoặc thẻ định danh cho từng tập dữ liệu.
* Mục đích:
  * Giúp hệ thống tìm kiếm, lọc và truy xuất dễ dàng.
  * Là cơ sở cho AI, phân tích dữ liệu và chia sẻ dữ liệu mở.
* Ví dụ:
  * Dán nhãn “Dữ liệu cá nhân”, “Dữ liệu tài chính”, “Dữ liệu địa lý”.
  * Sử dụng chuẩn metadata ISO 11179 hoặc từ điển dữ liệu quốc gia.

**(5) Lưu trữ dữ liệu**

* Mục tiêu: Bảo đảm dữ liệu được lưu giữ an toàn, có thể truy cập và khôi phục khi cần.
* Các mô hình lưu trữ:
  * Cơ sở dữ liệu quan hệ (RDBMS), phi quan hệ (NoSQL.
  * Kho dữ liệu (Data Warehouse), Hồ dữ liệu (Data Lake).
  * Lưu trữ tại hạ tầng đám mây hoặc Trung tâm Dữ liệu Quốc gia (TTDLQG).
* Yêu cầu:
  * Quản lý phiên bản, sao lưu, và an ninh vật lý.
  * Đảm bảo khả năng mở rộng và tính sẵn sàng cao (24/7).

**(6) Bảo vệ dữ liệu**

* Mục tiêu: Giữ an toàn và bảo mật dữ liệu trong suốt vòng đời.
* Hoạt động chính:
  * Mã hóa dữ liệu (encryption).
  * Phân quyền truy cập theo vai trò (RBAC).
  * Ghi vết truy cập, phát hiện xâm nhập, phòng chống rò rỉ (DLP).
* Liên hệ pháp lý:
  * Tuân thủ luật an ninh mạng, an toàn thông tin về bảo vệ dữ liệu cá nhân.
  * Kết hợp cơ chế SOC – SIEM – IAM trong quản trị dữ liệu công.

**(7) Xử lý dữ liệu**

* Khái niệm: Dữ liệu được xử lý, làm sạch, tổng hợp và phân tích để tạo giá trị.
* Các bước:
  * Làm sạch (data cleansing), chuẩn hóa (standardization).
  * Tích hợp (integration), biến đổi (transformation), phân tích (analytics).
* Yêu cầu:
  * Bảo đảm quy trình xử lý tuân thủ chính sách, có khả năng tái lập (audit trail).
  * Ứng dụng công nghệ ETL/ELT, AI, Machine Learning, Data Pipeline.

**(8) Chia sẻ dữ liệu**

* Mục tiêu: Cho phép truy cập và sử dụng dữ liệu giữa các cơ quan, hệ thống.
* Cơ chế thực hiện:
  * Thông qua nền tảng chia sẻ NDOP/LGSP theo yêu cầu hoặc chủ động.
  * Áp dụng chuẩn mô tả dữ liệu DCAT-AP, định dạng JSON, XML, RDF.
* Nguyên tắc:
  * “Chia sẻ có kiểm soát” – chỉ cung cấp dữ liệu theo quyền hạn.
  * Mọi truy cập phải được ghi vết và có thể kiểm tra.

**(9) Khai thác dữ liệu**

* Mục tiêu: Tận dụng dữ liệu để ra quyết định, phục vụ người dân, doanh nghiệp, nghiên cứu, AI, đổi mới sáng tạo.
* Hình thức khai thác:
  * Dịch vụ trực tuyến, báo cáo phân tích, dashboard dữ liệu mở.
  * Khai thác dữ liệu qua API hoặc sàn dữ liệu (Data Marketplace).
* Yêu cầu:
  * Đảm bảo chất lượng, tính pháp lý, khả năng truy xuất và minh bạch.

**(10) Điều phối dữ liệu**

* Khái niệm: Là hoạt động điều hành, tích hợp và đồng bộ dữ liệu giữa các hệ thống.
* Công cụ: NDOP và LGSP/LDOP.
* Mục tiêu:
  * Kết nối dữ liệu từ các CSDL quốc gia, ngành, địa phương.
  * Bảo đảm dữ liệu được chia sẻ hai chiều và có kiểm soát.
* Ý nghĩa: Là “bộ não điều hành” giúp dữ liệu lưu thông an toàn, hợp chuẩn trong Chính phủ số.

**(11) Hủy dữ liệu**

* Mục tiêu: Xóa bỏ dữ liệu không còn giá trị sử dụng hoặc hết thời hạn lưu trữ.
* Hình thức:
  * Xóa logic (logical deletion) hoặc xóa vật lý (physical destruction).
  * Lưu trữ lâu dài dưới dạng bản sao phục vụ lịch sử (archive).
* Yêu cầu:
  * Tuân thủ quy trình phê duyệt, có biên bản hủy, ghi nhận đầy đủ.
  * Bảo đảm dữ liệu bị hủy không thể phục hồi và không vi phạm an ninh thông tin.

#### **3.** **Mối liên hệ giữa các giai đoạn**

* Các giai đoạn liên kết chặt chẽ, tuần hoàn và có phản hồi lẫn nhau.
  * Thu thập → Xử lý → Chia sẻ → Khai thác là chuỗi nghiệp vụ chính.
  * Bảo vệ → Kiểm toán → Cải tiến diễn ra xuyên suốt.
* Dữ liệu mới được tạo ra hoặc cập nhật sẽ quay lại vòng đời, hình thành chu trình cải tiến liên tục .

> Mọi dữ liệu đều có vòng đời – và chỉ khi được quản trị trọn vẹn qua từng giai đoạn, dữ liệu mới có giá trị, an toàn và bền vững
>
> Quản trị vòng đời dữ liệu = **Quản trị giá trị dữ liệu.**
