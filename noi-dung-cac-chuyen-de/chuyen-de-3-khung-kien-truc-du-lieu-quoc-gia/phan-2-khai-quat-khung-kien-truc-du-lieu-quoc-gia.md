# Phần 2 - Khái quát khung kiến trúc dữ liệu quốc gia

#### **Sơ đồ tổng quát khung kiến trúc**

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

**(1)** **Người sử dụng (Người thụ hưởng dữ liệu)**

* Bao gồm: Người dân, cán bộ, công chức, viên chức, du khách; Các tổ chức, doanh nghiệp, cơ quan hành chính, tổ chức chính trị - xã hội.
* Đây là đối tượng cuối cùng thụ hưởng giá trị dữ liệu công thông qua dịch vụ số, ứng dụng, và các hệ thống phục vụ hành chính công.

**(2) Các kênh giao tiếp**

* Gồm hai nhóm chính:
  * Kênh truyền thống: trung tâm hành chính công, bộ phận một cửa.
  * Kênh số: kiosk, điện thoại, tin nhắn, email, ứng dụng di động, ứng dụng web, thiết bị desktop hoặc IoT.
* Các kênh này kết nối người dùng với hệ thống dữ liệu, giúp hình thành Chính phủ số lấy người dân làm trung tâm.

**(3) Các lớp dữ liệu**

* Phân lớp cơ sở dữ liệu & kho dữ liệu
  * Cơ sở dữ liệu tổng hợp quốc gia: trung tâm điều phối và tổng hợp toàn bộ dữ liệu công.
  * Cơ sở dữ liệu quốc gia: dữ liệu lõi như dân cư, đất đai, doanh nghiệp, tài chính, bảo hiểm.
  * Cơ sở dữ liệu dùng chung: phục vụ chia sẻ liên ngành, liên vùng.
  * Cơ sở dữ liệu chuyên ngành và hệ thống thông tin nghiệp vụ: các “hệ thống vệ tinh” cung cấp dữ liệu gốc cho trung tâm tổng hợp.
* Trao đổi dữ liệu hai chiều:
  * Dữ liệu từ các hệ thống chuyên ngành được đưa lên NDOP để tổng hợp, phân tích, chia sẻ.
  * Dữ liệu tổng hợp được phân phối trở lại cho các cơ quan phục vụ nghiệp vụ, chính sách.

**(4) Nền tảng Chia sẻ & Điều phối Dữ liệu (NDOP/LDOP)**

* NDOP/LDOP là xương sống kỹ thuật của kiến trúc dữ liệu quốc gia.
* Vai trò NDOP/LDOP:
  * Kết nối và điều phối dữ liệu giữa tất cả các cơ quan trong hệ thống chính trị.
  * Bảo đảm chuẩn giao tiếp, kiểm soát truy cập, và giám sát chất lượng dữ liệu.
* Là nền tảng duy nhất để trao đổi dữ liệu giữa CSDL tổng hợp quốc gia và các CSDL chuyên ngành.
  * Luồng chia sẻ dữ liệu: thực hiện theo yêu cầu hoặc chủ động từ CSDL chứa dữ liệu gốc
  * Luồng tích hợp và phân phối: thực hiện theo yêu cầu hoặc chủ động từ CSDL dùng chung (trung gian)

**(5) Hệ thống thông tin quốc gia phục vụ quản trị dữ liệu**

* Hệ thống Quản trị Dữ liệu Quốc gia;
* Hệ thống Giám sát an toàn, an ninh mạng (SOC) của Trung tâm Dữ liệu Quốc gia;
* Hệ thống Từ điển Dữ liệu Dùng chung Quốc gia;
* Hệ thống Cổng Dữ liệu Quốc gia (data.gov.vn);
* Sàn Dữ liệu thuộc TTDLQG;
* Kết nối với các hệ thống khác: Cổng Dịch vụ Công Quốc gia, Nền tảng VNeID, hệ thống định danh và xác thực điện tử.

→ Đây là hệ sinh thái dữ liệu công thống nhất để điều phối, giám sát và khai thác dữ liệu.

**(6) Các cơ quan trung ương, địa phương, quốc tế kết nối liên thông với NDOP**

* Truy cập, chia sẻ và khai thác dữ liệu thông qua NDOP để phục vụ công tác quản lý, hoạch định và ra quyết định chính sách.
* Tạo lập, cập nhật, khai thác và đồng bộ dữ liệu cấp cơ sở lên NDOP – đảm bảo dòng dữ liệu 2 chiều Trung ương ↔ Địa phương.
* Phục vụ thương mại, hợp tác quốc tế, và chia sẻ dữ liệu xuyên biên giới an toàn.

**(7) Hạ tầng truyền dẫn dữ liệu**

* Mạng Internet toàn cầu
* Mạng truyền số liệu chuyên dùng của Đảng và Nhà nước – đảm bảo bí mật, liên thông, ổn định.

**(8) Hạ tầng Trung tâm Dữ liệu**

* Trung tâm Dữ liệu Quốc gia (TTDLQG) – hạ tầng lõi trung tâm;
* Các trung tâm dữ liệu Bộ, ngành, khối cơ quan;
* Các trung tâm dữ liệu địa phương;
* Trung tâm dữ liệu doanh nghiệp (Private/Public Cloud).

***
