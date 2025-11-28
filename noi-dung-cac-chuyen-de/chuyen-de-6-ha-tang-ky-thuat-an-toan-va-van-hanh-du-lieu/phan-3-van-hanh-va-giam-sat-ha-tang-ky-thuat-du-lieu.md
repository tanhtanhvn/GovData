# Phần 3 - Vận hành và giám sát hạ tầng kỹ thuật dữ liệu

#### **1. Mục đích vận hành**

* Đảm bảo tính sẵn sàng, ổn định và an toàn của toàn bộ hạ tầng kỹ thuật dữ liệu quốc gia.
* Duy trì hiệu năng và độ tin cậy cao cho các trung tâm dữ liệu và nền tảng điều phối dữ liệu.
* Bảo đảm việc giám sát, sao lưu, khôi phục và bảo trì hệ thống được thực hiện liên tục, chủ động và tuân thủ tiêu chuẩn.
* Từng bước hướng đến vận hành thông minh, tự động hóa (AIOps) và phòng ngừa sự cố chủ động.

#### **2. Nhiệm vụ vận hành**

a) Giám sát liên tục các trung tâm dữ liệu

* Thiết lập hệ thống giám sát 24/7 tại trung tâm dữ liệu.
* Giám sát các yếu tố:
  * Tài nguyên hạ tầng: CPU, RAM, lưu trữ, mạng, điện năng, làm mát.
  * Hệ thống mạng: lưu lượng, độ trễ, an toàn truy cập, tắc nghẽn.
  * Ứng dụng và dịch vụ dữ liệu: trạng thái hoạt động, lỗi, hiệu năng truy vấn.
* Sử dụng bảng điều khiển tập trung (Dashboard) hiển thị trạng thái theo thời gian thực (real-time).

b) Quản lý cấp phát và tối ưu tài nguyên

* Quản lý việc phân bổ tài nguyên tính toán, lưu trữ, mạng giữa các đơn vị sử dụng.
* Tự động cấp phát (auto-scaling) khi nhu cầu tăng đột biến.
* Thực hiện rà soát định kỳ nhằm tối ưu chi phí vận hành (Cost Optimization).
* Kiểm soát việc tái sử dụng tài nguyên ảo hóa để giảm lãng phí phần cứng.

c) Quản lý bảo hành, bảo trì, kiểm kê hạ tầng

* Theo dõi lịch bảo trì định kỳ, bảo hành thiết bị, cập nhật firmware, vá lỗi bảo mật.
* Kiểm kê, kiểm đếm định kỳ toàn bộ hệ thống hạ tầng vật lý (máy chủ, lưu trữ, thiết bị mạng) và hạ tầng ảo (máy ảo, container).
* Lập báo cáo tình trạng tài sản CNTT theo tháng/quý.

d) Theo dõi hiệu năng, cảnh báo và tối ưu vận hành

* Thiết lập các ngưỡng cảnh báo (thresholds) cho từng loại tài nguyên.
* Cảnh báo sớm các rủi ro: CPU quá tải, lưu trữ đầy, kết nối gián đoạn, lỗi truyền dữ liệu.
* Theo dõi chỉ số hiệu năng (KPI): uptime (tỷ lệ hoạt động), độ trễ truy vấn, tỷ lệ lỗi truy cập.

#### **3.** **Quản lý sao lưu và khôi phục dữ liệu**

a) Nguyên tắc 3-2-1 trong sao lưu

* 3 bản sao dữ liệu: 1 bản chính, 2 bản dự phòng.
* 2 loại thiết bị khác nhau: ổ đĩa nội bộ, lưu trữ đám mây hoặc NAS.
* 1 bản sao ngoài địa điểm chính (offsite) – thường tại trung tâm dự phòng (DR site).

b) Chỉ số phục hồi RPO/RTO

* RPO (Recovery Point Objective): Khoảng thời gian mất dữ liệu tối đa chấp nhận được (thường ≤ 4h).
* RTO (Recovery Time Objective): Thời gian tối đa để phục hồi hệ thống (thường ≤ 2h đối với hệ thống trọng yếu).
* Cần đặt ngưỡng rõ ràng theo cấp độ dữ liệu và dịch vụ.

c) Kiểm thử định kỳ khả năng khôi phục

* Mô phỏng các kịch bản mất dữ liệu, lỗi hệ thống, mất điện, tấn công mạng để kiểm tra tính sẵn sàng.
* Đảm bảo kế hoạch khôi phục thảm họa (Disaster Recovery Plan) có thể thực thi tự động và nhanh chóng.

d) Hệ thống lưu trữ phân cấp

* Phân chia dữ liệu lưu trữ theo vùng:
  * Vùng nóng: Dữ liệu giao dịch hiện tại.
  * Vùng ấm: Dữ liệu dùng cho phân tích định kỳ.
  * Vùng lạnh: Dữ liệu lưu trữ lâu dài và sao lưu.
* Tích hợp công cụ Data Archiving & Tiering để tự động di chuyển dữ liệu.

#### **4. Tăng cường tự động hóa vận hành**

a) Ứng dụng AI và Machine Learning trong vận hành

* Dự báo lỗi phần cứng, nghẽn mạng hoặc tấn công trước khi xảy ra.
* Phân tích hành vi hệ thống để nhận diện bất thường (anomaly detection).
* Tự động đề xuất phương án khắc phục, phân bổ lại tài nguyên.

b) Triển khai DevOps/AIOps

* DevOps: Kết nối chặt chẽ giữa phát triển và vận hành, đảm bảo triển khai nhanh và ổn định.
* AIOps (Artificial Intelligence for IT Operations):
  * Thu thập log, sự kiện, cảnh báo → tự động phân loại → đề xuất xử lý.
  * Học từ lịch sử sự cố để cải tiến quy trình tự động bảo trì.

c) Tự động hóa giám sát và phản ứng

* Script hóa các tác vụ lặp lại: sao lưu, kiểm tra hiệu năng, cập nhật phần mềm.
* Tự động scale-up/down tài nguyên khi tải tăng hoặc giảm.
* Cảnh báo thông minh (smart alerting): ưu tiên cảnh báo có ảnh hưởng nghiêm trọng.

d) Lợi ích đạt được

* Giảm chi phí vận hành 20–30%.
* Rút ngắn thời gian khắc phục sự cố từ hàng giờ xuống vài phút.
* Nâng cao độ tin cậy (reliability) và sẵn sàng (availability) của hệ thống dữ liệu quốc gia.
