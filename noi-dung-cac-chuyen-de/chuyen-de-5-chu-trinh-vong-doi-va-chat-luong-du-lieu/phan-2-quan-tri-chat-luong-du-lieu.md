# Phần 2 - Quản trị chất lượng dữ liệu

#### **1.** **Khái niệm và tiêu chí chất lượng**

* Quản trị chất lượng dữ liệu (Data Quality Management – DQM) là tập hợp quy trình, tiêu chuẩn và công cụ nhằm đảm bảo dữ liệu có độ chính xác, đầy đủ, thống nhất, tin cậy và cập nhật.
* Nhóm tiêu chí chất lượng dữ liệu (theo ISO 8000)
  * Tính đầy đủ (Completeness): Có đủ các trường dữ liệu cần thiết.
  * Tính nhất quán (Consistency): Không mâu thuẫn giữa các nguồn.
  * Tính chính xác (Accuracy): Phản ánh đúng thực tế khách quan.
  * Tính kịp thời (Timeliness): Được cập nhật đúng thời điểm nghiệp vụ yêu cầu.
  * Tính duy nhất (Uniqueness): Không trùng lặp dữ liệu định danh hoặc dữ liệu chủ.
  * Tính toàn vẹn (Integrity): Liên kết dữ liệu chính xác giữa các thực thể.

#### **2. Chu trình đảm bảo chất lượng dữ liệu**

**a) Giám sát và xác định vấn đề chất lượng dữ liệu**

* Mục tiêu: Phát hiện sớm – cảnh báo kịp thời – xử lý chủ động.
* Các hoạt động gồm: theo dõi chỉ số, kiểm tra chéo dữ liệu, giám sát hệ thống tự động, ghi nhận nhật ký sự cố.

**b) Khắc phục vấn đề chất lượng dữ liệu**

* Phân tích nguyên nhân gốc rễ (Root-cause analysis): xác định sai từ khâu tạo lập, nhập liệu hay đồng bộ.
* Xây dựng phương án khắc phục và phòng ngừa tái diễn: điều chỉnh quy trình, cập nhật quy tắc kiểm tra.
* Thiết lập kế hoạch triển khai chi tiết: gồm thời gian, đơn vị phụ trách, xác nhận kết quả.

**c) Xây dựng và phê duyệt cam kết mức dịch vụ (SLA – Service Level Agreement)**

* Mỗi đơn vị phải ban hành SLA về chất lượng dữ liệu với các nội dung:
  * Thời gian xử lý và khắc phục sự cố dữ liệu.
  * Các tiêu chí đo lường hiệu quả cải thiện chất lượng.
  * Trách nhiệm, chế tài khi vi phạm SLA.
* Mục tiêu: Đảm bảo tính minh bạch, trách nhiệm và liên kết giữa các bên.

#### **3. Vận hành hệ thống đảm bảo chất lượng dữ liệu**

**a) Tài liệu hóa quy tắc chất lượng dữ liệu**

* Các bộ, ngành, địa phương phải xây dựng tài liệu quy tắc kiểm tra dữ liệu nghiệp vụ quan trọng.
* Quy tắc phải nêu rõ: loại dữ liệu, điều kiện hợp lệ, định dạng, giá trị cho phép, mối quan hệ logic.
* Là cơ sở cho kiểm tra tự động (data validation) và làm sạch dữ liệu (data cleansing).

**b) Lập hồ sơ dữ liệu (Data Profiling)**

* Thực hiện định kỳ (quý/năm) để đánh giá thực trạng dữ liệu trong hệ thống.
* Mục tiêu: phát hiện lỗi sai, thiếu dữ liệu, trùng lặp hoặc mâu thuẫn giữa các hệ thống.
* Kết quả profiling dùng để cập nhật DQI và đề xuất cải thiện.

**c) Đánh giá và điều chỉnh ngưỡng chất lượng**

* Căn cứ kết quả profiling, điều chỉnh ngưỡng chấp nhận hoặc quy tắc chất lượng.
* Đảm bảo các chỉ số phù hợp thực tế, nhưng vẫn hướng đến nâng chuẩn.

**d) Phân tích nguyên nhân và báo cáo khắc phục**

* Báo cáo phải bao gồm:
  * Mô tả vấn đề chất lượng cụ thể.
  * Ảnh hưởng tới quy trình nghiệp vụ.
  * Kết quả truy vết nguồn gốc (lineage).
  * Giải pháp cải thiện và phòng ngừa tái diễn.
* Mục tiêu: hình thành chu trình phản hồi minh bạch và cải tiến liên tục.

**đ) Xây dựng & phê duyệt kế hoạch khắc phục chất lượng dữ liệu**

* Nội dung kế hoạch:
  * Mốc thời gian triển khai.
  * Đơn vị phụ trách, nguồn lực.
  * Chỉ tiêu cải thiện cụ thể (KPI/KQI).
* Kế hoạch phải được phê duyệt chính thức và giám sát tiến độ qua hệ thống.

**e) Theo dõi SLA và đánh giá thực thi**

* Xây dựng hệ thống dashboard giám sát SLA giữa các cơ quan.
* Đo lường tỷ lệ hoàn thành SLA, thời gian xử lý trung bình, số lượng sự cố tồn đọng.
* Dữ liệu SLA là cơ sở đánh giá năng lực quản trị dữ liệu của từng đơn vị.

**g) Duy trì nhật ký vấn đề chất lượng dữ liệu**

* Nội dung cần lưu trữ:
  * Mô tả vấn đề, ngày phát hiện, nguyên nhân.
  * Biện pháp xử lý và mức cải thiện đạt được.
  * Tỷ lệ xử lý/vi phạm SLA.
* Mục tiêu: lưu vết và học hỏi từ sai lệch – nền tảng cho quản trị dữ liệu trưởng thành.

#### **4. Công cụ tự động hóa quản lý chất lượng dữ liệu**

* Phát hiện tự động (Automatic Data Quality Detection):
  * Phân tích theo quy tắc đã cấu hình để phát hiện lỗi, trùng lặp, dữ liệu thiếu.
* Phân luồng và giao việc xử lý (Workflow Automation):
  * Tự động chuyển yêu cầu khắc phục đến đúng đơn vị phụ trách.
* Cảnh báo sớm và giám sát thời gian thực (Real-time Alerts & Dashboard):
  * Hiển thị bảng điều khiển chất lượng dữ liệu, cảnh báo theo SLA.
* Phân tích xu hướng và báo cáo định kỳ:
  * Theo dõi DQI theo thời gian, phát hiện xu hướng suy giảm chất lượng.
  * Hỗ trợ ra quyết định chiến lược dựa trên dữ liệu đo lường.

#### **5.** **Kết quả mong đợi**

* Hình thành chu trình đảm bảo chất lượng dữ liệu khép kín: _Đo lường → Phát hiện → Khắc phục → Giám sát → Cải tiến._
* Tạo nền tảng dữ liệu tin cậy – đồng bộ – sẵn sàng chia sẻ cho Chính phủ số và kinh tế
