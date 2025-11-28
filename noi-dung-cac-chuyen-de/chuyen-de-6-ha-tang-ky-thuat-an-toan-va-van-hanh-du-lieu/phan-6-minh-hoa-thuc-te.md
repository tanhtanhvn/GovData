# Phần 6 - Minh họa thực tế

#### **Chủ đề:** Trung tâm Dữ liệu Quốc gia

#### **1. Vị trí và vai trò của Trung tâm Dữ liệu Quốc gia**

**a) Vị trí hệ thống**

* Là trung tâm tích hợp và điều phối dữ liệu quốc gia do Chính phủ xây dựng, quản lý và khai thác.
* Tích hợp dữ liệu từ tất cả CSDL quốc gia và chuyên ngành (dân cư, y tế, giáo dục, bảo hiểm, lao động, tài chính…).
* Cung cấp hạ tầng CNTT dùng chung cho các cơ quan Đảng, Nhà nước, tổ chức chính trị – xã hội.

**b) Vai trò chức năng**

* Kho dữ liệu tổng hợp quốc gia: chứa thông tin về con người và các hoạt động kinh tế – xã hội.
* Nền tảng dữ liệu điều hành Chính phủ số: hỗ trợ phân tích, dự báo, hoạch định chính sách.
* Nền tảng chia sẻ và khai thác dữ liệu mở: phục vụ người dân, doanh nghiệp, các đối tác quốc tế.
* Trung tâm hạ tầng và an toàn dữ liệu quốc gia: cung cấp môi trường đặt máy chủ, đám mây, tính toán hiệu năng cao.

#### **2. Hạ tầng kỹ thuật và an toàn bảo mật dữ liệu**

**a) Kiến trúc hạ tầng**

* Hai vùng chính:
  * _Vùng chuyên dụng_: lưu trữ dữ liệu mật, vận hành hệ thống lõi.
  * _Vùng dùng chung_: hạ tầng đám mây, dịch vụ PaaS/SaaS, kho dữ liệu mở.
* Tiêu chuẩn trung tâm dữ liệu: TIA-942 Tier 3, TCVN 9250:2021, Uptime Tier III.
* Tích hợp điện toán đám mây, tính toán hiệu năng cao, bảo mật vật lý đa tầng.

**b) Mô hình vận hành**

* Trung tâm dữ liệu quốc gia chịu trách nhiệm vận hành vùng chuyên dụng, hạ tầng điện – mạng – bảo mật.
* Các bộ/ngành/địa phương: tự vận hành ứng dụng của mình trên hạ tầng đám mây TTDLQG (theo mô hình “shared cloud tenancy”).
* Hệ thống dự phòng (Disaster Recovery): bố trí tại Trung tâm dữ liệu Dân cư và các trung tâm dữ liệu bộ, ngành.

**c) Chuẩn vận hành**

* Mô hình 3-2-1 sao lưu;
* Cơ chế audit, logging toàn trình;
* Cấu hình đồng bộ và tự động mở rộng (auto-scaling).

**d) An toàn và bảo mật dữ liệu**

* **Nguyên tắc bảo mật**
  * Phòng ngừa chủ động – Kiểm soát phân vai – Giám sát toàn trình – Tuân thủ pháp lý.
  * Áp dụng theo cấp độ nhạy cảm dữ liệu (mật/tối mật/tuyệt mật/công khai).
* **Khung bảo mật 8 lớp tại TTDLQG**
  * **L1** – Định danh & Metadata.
  * **L2** – Phân loại & Gán nhãn dữ liệu.
  * **L3** – Phân quyền, MFA, mã hóa khi truyền & lưu.
  * **L4** – Che giấu (masking), tokenization, truy vết (lineage).
  * **L5** – Giám sát “5 yếu tố an toàn”: _Người – Dự án – Dữ liệu – Môi trường – Kết quả_.
  * **L6** – Quản lý vòng đời dữ liệu (thu thập – lưu – hủy – chia sẻ).
  * **L7** – Công cụ kỹ thuật: SIEM, DLP, DAM, Compliance Dashboard.
  * **L8** – Báo cáo, đánh giá an toàn dữ liệu định kỳ (2 lần/năm).
* **Quản trị quyền riêng tư**
  * Quyền được biết, truy cập, chỉnh sửa, yêu cầu xóa dữ liệu cá nhân.
  * Cơ chế công bố minh bạch chính sách bảo mật, hợp đồng chia sẻ dữ liệu.
  * Áp dụng mã hóa PII, ghi log truy cập, hệ thống xử lý yêu cầu của chủ thể dữ liệu (DSR System).

#### **3.** **Nhân lực, tổ chức và vận hành**

**a) Cơ cấu tổ chức**

* TTDLQG là đơn vị cấp Cục trực thuộc Bộ Công an (theo Nghị định sửa đổi 01/2018/NĐ-CP).
* Quản lý: Cục trưởng phụ trách hạ tầng, an ninh, dữ liệu; dưới có các phòng: kỹ thuật, an toàn thông tin, khai thác dữ liệu, pháp chế.

**b) Nguồn nhân lực**

* Huy động từ lực lượng Công an, học viện chuyên ngành;
* Tuyển dụng chuyên gia khoa học dữ liệu, kỹ sư AI, chuyên viên vận hành cloud;
* Có cơ chế đãi ngộ theo Nghị quyết 27-NQ/TW (2018), sử dụng quỹ lương để thuê chuyên gia công nghệ.

**c) Công tác đào tạo**

* Liên kết các đại học, viện nghiên cứu, doanh nghiệp công nghệ trong nước và quốc tế;
* Xây dựng hệ sinh thái nhân lực khoa học dữ liệu.
