# Phần 1 - Khái niệm và Vai trò của Kiến trúc Miền Dữ liệu

#### **1.** **Bối cảnh hình thành**

* Trong Kiến trúc dữ liệu tổng thể quốc gia, toàn bộ tài nguyên dữ liệu của Chính phủ được tổ chức theo mô hình phân tầng và phân miền, bảo đảm sự thống nhất ở cấp khung và linh hoạt ở cấp triển khai.
* Tầng trên cùng mô tả khung kiến trúc dữ liệu tổng thể của quốc gia, xác định các nguyên tắc, tiêu chuẩn, mô hình quản trị và cơ chế chia sẻ giữa các bộ, ngành, địa phương.
* Tầng dưới là các miền dữ liệu chuyên ngành (Data Domains) — ví dụ: dân cư, giáo dục, y tế, tài chính, giao thông, đất đai...
  * Mỗi miền này có đặc trưng nghiệp vụ, cấu trúc dữ liệu, quy tắc xử lý và hệ thống thông tin riêng biệt, phản ánh thực tế hoạt động của từng lĩnh vực quản lý nhà nước.
  * Tuy nhiên, các miền không tồn tại tách rời, mà liên thông với nhau thông qua khung kiến trúc tổng thể – nơi quy định chuẩn kết nối, định danh, và liên kết ngữ nghĩa.

> 🎯 **Tóm lại:** Kiến trúc dữ liệu tổng thể định hướng _“chúng ta quản lý dữ liệu ở cấp quốc gia như thế nào”_, còn kiến trúc miền dữ liệu cụ thể hóa _“chúng ta mô hình hóa dữ liệu trong từng lĩnh vực như thế nào”_.

#### **2.** **Định nghĩa Kiến trúc Miền Dữ liệu**

* Kiến trúc miền dữ liệu là cấu trúc mô tả toàn bộ các thực thể dữ liệu, mối quan hệ, quy tắc nghiệp vụ, quy trình vận hành và luồng chia sẻ dữ liệu trong một lĩnh vực nghiệp vụ cụ thể.
* Nó kết nối ba lớp logic trong quản trị dữ liệu:
  * Nghiệp vụ (Business Layer): các quy trình, chức năng, sự kiện và quy tắc của lĩnh vực (ví dụ: quản lý hồ sơ học sinh, bệnh nhân, doanh nghiệp…).
  * Dữ liệu (Data Layer): các bảng, trường, cấu trúc, chỉ số, quan hệ giữa các thực thể.
  * Công nghệ (Technology Layer): nền tảng kỹ thuật giúp lưu trữ, chia sẻ và phân tích dữ liệu.
* Kiến trúc miền dữ liệu vì thế đảm bảo sự hiểu thống nhất và khả năng tương tác ngữ nghĩa giữa dữ liệu, con người và công nghệ trong phạm vi của miền đó.

#### **3.** **Mối quan hệ giữa Kiến trúc Miền Dữ liệu và Kiến trúc Dữ liệu Tổng thể**

a) Vị trí trong hệ thống phân cấp kiến trúc dữ liệu quốc gia:

* Kiến trúc dữ liệu tổng thể là bản đồ tổng thể của hệ sinh thái dữ liệu quốc gia — định hướng các nguyên tắc, khung tiêu chuẩn, và cơ chế liên thông giữa các miền.
* Kiến trúc miền dữ liệu là bản đồ chi tiết của từng khu vực dữ liệu, cụ thể hóa cách triển khai các nguyên tắc đó trong từng lĩnh vực.

> 🧩 Tưởng tượng kiến trúc dữ liệu tổng thể là “bản quy hoạch đô thị quốc gia”, còn kiến trúc miền dữ liệu là “quy hoạch chi tiết từng quận, từng khu chức năng”.

b) Mối liên hệ hai chiều:

* Từ trên xuống (Top-down): Kiến trúc dữ liệu tổng thể đưa ra các chuẩn khung, phân loại, mã định danh, nguyên tắc quản trị, và mô hình tích hợp – được các miền kế thừa.
* Từ dưới lên (Bottom-up): Kiến trúc miền dữ liệu cung cấp các mô hình chi tiết, ontology, và thực tiễn nghiệp vụ – giúp hiệu chỉnh, cập nhật và mở rộng khung tổng thể.
* Hai lớp này liên tục tương tác để đảm bảo dữ liệu vừa chuẩn hóa vừa phản ánh thực tiễn.

c) Nguyên tắc tương tác giữa các miền:

* Các miền được thiết kế độc lập nhưng phải liên thông qua:
  * Chuẩn định danh chung (Số định danh cá nhân, số định danh tổ chức, mã lĩnh vực).
  * Chuẩn ngữ nghĩa chung (Ontology và từ điển dữ liệu dùng chung).
  * Chuẩn giao tiếp kỹ thuật (API, DCAT-AP, JSON-LD, NGSI-LD...).
* Nhờ vậy, dữ liệu từ miền _Y tế_ có thể kết nối với miền _Bảo hiểm_, _Dân cư_ hoặc _Giáo dục_, tạo thành bức tranh dữ liệu liên ngành thống nhất.

d) Mối quan hệ chức năng – quản trị:

* Kiến trúc dữ liệu tổng thể là khung định hướng chính sách dữ liệu,
* Còn kiến trúc miền dữ liệu là khung triển khai nghiệp vụ dữ liệu,
* Kết hợp lại tạo nên “vòng khép kín chiến lược – quản trị – vận hành” trong hệ thống quản trị dữ liệu công.

#### **4.** **Vai trò của Kiến trúc Miền Dữ liệu**

<figure><img src="../../.gitbook/assets/image (20).png" alt="" width="375"><figcaption></figcaption></figure>

a) Cầu nối giữa kiến trúc tổng thể và hệ thống dữ liệu chuyên ngành

* Chuyển hóa các nguyên tắc chiến lược trong kiến trúc dữ liệu tổng thể thành cấu trúc triển khai cụ thể.
* Là “mắt xích trung gian” giữa tầm nhìn dữ liệu quốc gia và ứng dụng dữ liệu thực tiễn.

b) Chuẩn hóa cách hiểu và sử dụng dữ liệu

* Đảm bảo các khái niệm dữ liệu được hiểu nhất quán giữa các cơ quan, đơn vị trong cùng lĩnh vực.
* Tạo nền tảng ngữ nghĩa thống nhất để các hệ thống AI, BI, và kho dữ liệu liên ngành có thể khai thác chính xác.

c) Tăng cường liên thông và tích hợp dữ liệu liên ngành

* Kiến trúc miền dữ liệu là nền tảng kỹ thuật và ngữ nghĩa để các miền khác có thể kết nối qua ontology và từ điển dữ liệu dùng chung.
* Ví dụ:
  * Miền _Dân cư_ cung cấp định danh công dân.
  * Miền _Y tế_ dùng định danh này để gắn hồ sơ bệnh án.
  * Miền _Giáo dục_ liên kết để theo dõi dữ liệu học sinh theo mã định danh.
* Nhờ đó, Chính phủ có thể phân tích đa chiều, dự báo chính sách và ra quyết định dựa trên dữ liệu tích hợp.

d) Tạo nền tảng cho đổi mới và dữ liệu mở

* Khi mỗi miền được thiết kế rõ ràng, dữ liệu có thể được mở, dùng lại, và kết hợp để hình thành dịch vụ dữ liệu công mới.
* Đây là nền tảng cho mô hình sandbox đổi mới và sàn dữ liệu quốc gia – nơi khu vực công và tư cùng hợp tác phát triển giá trị dữ liệu.
