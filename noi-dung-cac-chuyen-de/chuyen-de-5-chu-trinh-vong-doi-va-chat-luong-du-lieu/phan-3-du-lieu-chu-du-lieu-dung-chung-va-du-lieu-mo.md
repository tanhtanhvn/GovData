# Phần 3 - Dữ liệu chủ, dữ liệu dùng chung và dữ liệu mở

#### **Mô hình phân lớp dữ liệu**

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

**(1) Siêu dữ liệu (Metadata)** — _Lớp nền định nghĩa dữ liệu khác_

* Vai trò: Cốt lõi trong việc mô tả, định nghĩa và quản lý các loại dữ liệu khác.
* Thành phần:
  * Siêu dữ liệu kỹ thuật: Mô tả cấu trúc vật lý của dữ liệu – bảng, cột, kiểu dữ liệu, chỉ mục, kho dữ liệu. → Quản lý trong _Từ điển dữ liệu kỹ thuật._
  * Siêu dữ liệu hoạt động: Mô tả luồng dữ liệu (data flow) – cách dữ liệu di chuyển, xử lý và điều phối. → Quản lý trong _hệ thống điều phối dữ liệu (data pipeline)._
  * Siêu dữ liệu nghiệp vụ: Mô tả ngữ nghĩa, thuật ngữ nghiệp vụ, phân cấp, danh mục – dùng cho người sử dụng dữ liệu. → Lưu trong _Từ điển dữ liệu nghiệp vụ (Business Glossary)._
  * Siêu dữ liệu xã hội: Dữ liệu chú thích, bình luận, phản hồi từ người dùng (ví dụ: “tập dữ liệu chưa được chứng nhận”). → Thường gắn liền với hoạt động _xác thực, chứng nhận, kiểm duyệt dữ liệu._

**(2) Dữ liệu danh mục dùng chung (Reference Data)** — _Lớp chuẩn hóa và đồng bộ_

* Đặc điểm:
  * Là tập hợp các bảng mã, danh mục, phân loại chuẩn hóa được ban hành bởi cơ quan có thẩm quyền.
  * Đảm bảo thống nhất, đồng bộ và tương thích giữa các hệ thống thông tin từ Trung ương đến địa phương.
* Vai trò:
  * Chuẩn hóa thông tin đầu vào, giảm sai lệch, nâng cao hiệu quả tích hợp.
  * Là nền tảng xây dựng các cơ sở dữ liệu quốc gia và phục vụ cải cách hành chính, hoạch định chính sách, chuyển đổi số.

**(3) Dữ liệu chủ (Master Data)** — _Lớp dữ liệu lõi, ổn định, có tính tham chiếu cao_

* Đặc điểm:
  * Mô tả các đối tượng cốt lõi: dân cư, doanh nghiệp, đất đai, đơn vị hành chính, mã ngành nghề...
  * Có tính ổn định, được sử dụng xuyên suốt trong nhiều hệ thống và nghiệp vụ.
* Vai trò:
  * Là nguồn dữ liệu thống nhất và đáng tin cậy cho toàn hệ thống.
  * Hỗ trợ chia sẻ dữ liệu mặc định, giảm trùng lặp, tăng tính đồng bộ và hiệu quả vận hành.

**(4) Dữ liệu giao dịch (Transaction Data)** — _Lớp dữ liệu phản ánh hoạt động thực tế_

* Đặc điểm: Là dữ liệu phát sinh trong quá trình xử lý nghiệp vụ, giao dịch hành chính, cung cấp dịch vụ công.
* Ví dụ: Hồ sơ thủ tục hành chính, phiếu tiếp nhận, chứng từ giao dịch, kết quả xử lý nghiệp vụ.
* Vai trò: Phản ánh các hoạt động giao dịch của chủ thể dữ liệu (người dân, doanh nghiệp).

**(5) Dữ liệu lớn (Big Data)** — _Lớp dữ liệu đa dạng, tốc độ cao, khối lượng lớn_

* Nguồn hình thành: Cảm biến IoT, mạng xã hội, Internet, thiết bị di động.
* Đặc trưng có 3V: Volume (khối lượng lớn), Variety (đa dạng định dạng), Velocity (tốc độ phát sinh cao).
* Ứng dụng: Phân tích xu hướng xã hội, dự báo hành vi, tối ưu hóa dịch vụ công, ra quyết định chiến lược.

**(6) Dữ liệu tổng hợp (Aggregate Data)** — _Lớp dữ liệu được xử lý, thống kê, nhóm theo chủ đề_

* Khái niệm: Kết quả của việc tổng hợp dữ liệu chi tiết theo vùng, thời gian, lĩnh vực.
* Ví dụ: Báo cáo thống kê dân cư, số lượng doanh nghiệp mới, tỷ lệ thất nghiệp theo tỉnh.
* Vai trò: Phục vụ phân tích vĩ mô, giám sát hiệu quả chính sách, lập quy hoạch và báo cáo điều hành.

**(7) Dữ liệu kết quả phân tích / suy diễn (Analytical Data)**

* Đặc điểm: Là dữ liệu được sinh ra sau quá trình phân tích, học máy, trí tuệ nhân tạo.
* Ví dụ: Dự đoán nhu cầu dịch vụ công, mô hình rủi ro tài chính, phân loại tự động hồ sơ.
* Vai trò: Giúp ra quyết định chủ động, dự báo và hoạch định chiến lược dựa trên dữ liệu (data-driven policy).

**(8) Dữ liệu mở (Open Data)** — _Lớp dữ liệu công bố, tái sử dụng tự do_

* Đặc điểm:
  * Là dữ liệu được công khai bởi cơ quan nhà nước có thẩm quyền, phục vụ khai thác lại bởi công dân, doanh nghiệp, tổ chức.
  * Phải được cơ quan chủ quản dữ liệu cấp giấy phép mở theo chuẩn mực quốc tế hoặc theo các điều khoản được lập riêng.
  * Được cung cấp qua các cổng dữ liệu (ví dụ: _data.gov.vn_), theo chuẩn định dạng mở (CSV, JSON, RDF).
* Nguyên tắc:
  * Không chứa dữ liệu cá nhân hoặc bí mật nhà nước.
  * Bảo đảm khả năng truy cập, tái sử dụng và tương thích.
