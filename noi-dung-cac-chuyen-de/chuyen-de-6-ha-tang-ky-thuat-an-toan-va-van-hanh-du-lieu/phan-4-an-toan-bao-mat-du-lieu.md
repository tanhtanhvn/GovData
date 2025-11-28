# Phần 4 - An toàn, bảo mật dữ liệu

#### **1. Mục tiêu và ý nghĩa**

* Bảo đảm tính toàn vẹn, bí mật và sẵn sàng của dữ liệu trong toàn bộ hệ sinh thái số của Chính phủ.
* Phòng ngừa rủi ro mất mát, rò rỉ, truy cập trái phép hoặc tấn công mạng vào các cơ sở dữ liệu quốc gia và chuyên ngành.
* Xây dựng môi trường tin cậy dữ liệu, đáp ứng quy định pháp lý Luật An toàn thông tin, Luật An ninh mạng và Luật Bảo vệ dữ liệu cá nhân.
* Tăng cường niềm tin của công dân và doanh nghiệp khi sử dụng dịch vụ số.

#### **2.** **Nguyên tắc bảo mật dữ liệu**

**a) Nguyên tắc tổng quát “4 lớp bảo vệ”**

* Phòng ngừa chủ động (Proactive Protection)
  * Triển khai sớm biện pháp phòng ngừa, giám sát, vá lỗi và đánh giá rủi ro định kỳ.
  * Xây dựng kế hoạch phản ứng sự cố (Incident Response Plan).
* Kiểm soát phân vai (Role-based Control)
  * Xác định rõ vai trò: Chủ sở hữu dữ liệu (Data Owner), Quản trị kỹ thuật (Data Steward), Người dùng dữ liệu (Data User).
  * Gắn quyền truy cập theo vai trò (RBAC) hoặc thuộc tính (ABAC).
* Giám sát toàn trình (End-to-end Monitoring)
  * Theo dõi dữ liệu từ lúc tạo lập đến khi bị hủy, đảm bảo truy vết được (data lineage).
  * Ghi log toàn bộ truy cập, chỉnh sửa, chia sẻ dữ liệu.
* Tuân thủ pháp lý (Legal Compliance)
  * Thực thi nghiêm Luật An ninh mạng, Luật An toàn thông tin, Luật Bảo vệ dữ liệu cá nhân.
  * Kết nối hệ thống báo cáo định kỳ tới Bộ Công an.

**b) Nguyên tắc phân tầng theo nhạy cảm dữ liệu**

* Xác định cấp độ nhạy cảm (Data Sensitivity Level):
  * Cấp 1: Dữ liệu công khai.
  * Cấp 2: Dữ liệu nội bộ hành chính.
  * Cấp 3: Dữ liệu nhạy cảm (tài chính, y tế, dân cư).
  * Cấp 4: Dữ liệu quan trọng quốc gia (theo Luật Dữ liệu).
  * Cấp 5: Dữ liệu cốt lõi quốc gia (theo Luật Dữ liệu).
* Biện pháp bảo vệ áp dụng tăng dần theo cấp độ (mã hóa, truy vết, che giấu, cô lập mạng…).

#### **3. Khung bảo mật dữ liệu 8 lớp**

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

**Lớp 1 – Dữ liệu gốc**

* Mỗi tập dữ liệu được gắn định danh duy nhất (UUID) và metadata chuẩn hóa.
* Ghi nhận: nguồn gốc, cơ quan sở hữu, thời gian tạo lập, trạng thái, cấp độ nhạy cảm.
* Mục tiêu: đảm bảo dễ truy xuất, rõ ràng trách nhiệm và nguồn gốc dữ liệu.

**Lớp 2 – Phân loại và gán nhãn dữ liệu**

* Thực hiện phân loại tự động hoặc thủ công theo tiêu chí pháp lý và nghiệp vụ.
* Gán nhãn dữ liệu (label) theo metadata, ví dụ: “Công khai”, “Mật”, “Rất mật”, “Dữ liệu cá nhân nhạy cảm”.
* Hỗ trợ kiểm soát quyền truy cập tự động và đánh giá rủi ro chia sẻ.
* Cơ chế phân loại dựa trên chuẩn ISO/IEC 27001 và NIST 800-60.

**Lớp 3 – Kiểm soát truy cập, xác thực và mã hóa**

* Phân quyền truy cập theo vai trò (RBAC) và theo thuộc tính (ABAC).
* Xác thực đa yếu tố (MFA) áp dụng với mọi người dùng có quyền quản trị.
* Mã hóa dữ liệu:
  * Khi truyền (TLS, HTTPS, VPN).
  * Khi lưu trữ (AES-256, RSA-2048).
* Quản lý khóa mã hóa (KMS) theo từng cơ quan chủ quản, có sao lưu và luân chuyển định kỳ.
* Đảm bảo nguyên tắc “ít quyền nhất” (Least Privilege Principle).

**Lớp 4 – Che giấu và truy vết dữ liệu**

* Che giấu dữ liệu (Data Masking):
  * Ẩn thông tin nhạy cảm (CMND, số tài khoản, địa chỉ…).
  * Áp dụng tùy vai trò người truy cập.
* Tokenization & Hashing:
  * Mã hóa thông tin định danh cá nhân khi chia sẻ hoặc xử lý dữ liệu AI.
  * Giảm rủi ro rò rỉ và tăng bảo vệ dữ liệu cá nhân.
* Truy vết dữ liệu (Data Lineage):
  * Ghi lại lịch sử di chuyển, chỉnh sửa, chia sẻ của từng tập dữ liệu.
  * Giúp kiểm toán, phát hiện sai lệch hoặc hành vi bất thường.

**Lớp 5 – Giám sát và đánh giá “5 yếu tố an toàn”**

1. Người dùng an toàn (Safe People): Định danh, phân quyền rõ ràng, truy vết mọi hoạt động.
2. Dự án an toàn (Safe Projects): Chỉ xử lý dữ liệu khi được phê duyệt hoặc có căn cứ pháp lý.
3. Dữ liệu an toàn (Safe Data): Đúng phạm vi, đúng mục đích, kiểm soát quyền truy cập.
4. Môi trường an toàn (Safe Settings): Cách ly mạng, bảo vệ thiết bị đầu cuối, cô lập vùng thử nghiệm.
5. Kết quả an toàn (Safe Outputs): Kiểm duyệt đầu ra, ẩn danh dữ liệu cá nhân, che giấu dữ liệu nhạy cảm.

**Lớp 6 – Quản lý vòng đời dữ liệu**

* Áp dụng quy trình Data Lifecycle Management (DLM) thống nhất: Tạo lập → Lưu trữ → Chia sẻ → Sử dụng → Hủy bỏ.
* Quy định rõ trách nhiệm, quyền sở hữu và thời gian lưu trữ.
* Thực hiện xóa dữ liệu an toàn (secure deletion) khi hết mục đích sử dụng.
* Mọi hoạt động chia sẻ phải có văn bản thỏa thuận hoặc hợp đồng dữ liệu (Data Agreement).

**Lớp 7 – Công cụ kỹ thuật bắt buộc**

1. SIEM (Security Information & Event Management):
   1. Thu thập log bảo mật, phân tích sự kiện theo thời gian thực.
   2. Kết nối với Trung tâm điều hành an toàn thông tin (SOC).
2. DLP (Data Loss Prevention):
   1. Ngăn rò rỉ dữ liệu qua email, USB, sao chép trái phép.
3. DAM (Database Activity Monitoring):
   1. Theo dõi toàn bộ truy vấn, cập nhật, xóa dữ liệu trong CSDL.
4. Compliance Dashboard:
   1. Hiển thị trạng thái tuân thủ kỹ thuật – pháp lý, cảnh báo sớm vi phạm.
   2. Báo cáo theo từng bộ/ngành/địa phương, giúp kiểm toán và giám sát minh bạch.

**Lớp 8 – Báo cáo và đánh giá an toàn dữ liệu định kỳ**

* Tần suất: ít nhất 02 lần/năm (tháng 6 & tháng 12).
* Phạm vi: tất cả hệ thống dữ liệu sử dụng ngân sách nhà nước hoặc lưu trữ dữ liệu nhạy cảm.
* Nội dung báo cáo:
  * Sự cố bảo mật, trạng thái tuân thủ, chỉ số an toàn dữ liệu (Data Security Index).
  * Kết quả khắc phục, khuyến nghị cải thiện.
* Đơn vị thực hiện: Chủ quản dữ liệu bộ, ngành, địa phương
* Cơ quan giám sát: Bộ Công an.
* Kết quả đánh giá là căn cứ xếp hạng chuyển đổi số, phê duyệt đầu tư CNTT và phân bổ ngân sách dữ liệu.
