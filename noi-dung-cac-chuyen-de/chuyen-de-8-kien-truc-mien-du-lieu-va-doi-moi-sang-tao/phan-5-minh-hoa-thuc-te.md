# Phần 5 - Minh họa thực tế

#### **Chủ đề:** “_Kiến trúc miền dữ liệu giao thông vận tải - Kinh nghiệm quốc tế và tại Việt Nam_"

#### **1. Bối cảnh hình thành**

* Giao thông vận tải là một miền dữ liệu đặc thù, có mức độ kết nối cao giữa nhiều lĩnh vực: dân cư, kinh tế, môi trường, đô thị và an toàn xã hội.
* Dữ liệu giao thông không chỉ phản ánh hoạt động vận tải mà còn là dữ liệu chiến lược để phân tích quy hoạch hạ tầng, dự báo luồng giao thông, giảm phát thải, và phát triển kinh tế số.
* Kiến trúc miền dữ liệu giao thông vận tải giúp:
  * Chuẩn hóa cách thu thập, chia sẻ và phân tích dữ liệu về phương tiện, người điều khiển, kết cấu hạ tầng và luồng giao thông.
  * Tạo nền tảng cho phát triển hệ thống giao thông thông minh (ITS) và đô thị thông minh.

#### **2. Kinh nghiệm quốc tế**

**a) Hoa Kỳ – Kiến trúc tham chiếu ARC-IT (Architecture Reference for Cooperative & Intelligent Transportation)**

* Khởi nguồn từ National ITS Architecture (1993), hiện nay được phát triển thành ARC-IT phiên bản 9.0 (2020).
* Cấu trúc gồm 4 lớp chính:
  * Physical View – mô hình hóa các thực thể (trung tâm điều khiển, phương tiện, người tham gia giao thông…).
  * Functional View – mô tả các chức năng và luồng thông tin.
  * Communications View – chuẩn hóa giao diện, giao thức dữ liệu (ví dụ: SAE J2735, ISO 14827).
  * Organizational View – mô tả khung chính sách, trách nhiệm và các bên tham gia.
* Mục tiêu: tạo một ngôn ngữ dữ liệu chung cho tất cả các dự án ITS tại Hoa Kỳ.
* Lợi ích:
  * Giúp tái sử dụng thiết kế dữ liệu, giảm rủi ro khi triển khai hệ thống mới.
  * Đảm bảo tính liên thông dữ liệu liên bang – bang – địa phương.
  * Hỗ trợ xây dựng sandbox thử nghiệm các dịch vụ giao thông thông minh, như mô hình xe tự hành, điều khiển tín hiệu giao thông thông minh, và phân tích dữ liệu thời gian thực.

**b) Châu Âu – Mô hình dữ liệu DATEX II và tiêu chuẩn ISO 14827**

* DATEX II (EU ITS Directive) là mô hình ngữ nghĩa và kỹ thuật chuẩn để trao đổi dữ liệu giao thông giữa các quốc gia EU.
  * Mô tả thông tin sự cố, lưu lượng, thời tiết, công trình và trạng thái mạng đường.
  * Sử dụng ontology giao thông và metadata mở, giúp chia sẻ dữ liệu theo thời gian thực.
* ISO 14827 / TCVN 13600-1:2022: quy định về giao diện dữ liệu giữa các trung tâm thông tin giao thông, giúp đồng bộ dữ liệu giữa các đơn vị điều hành.
* Lợi ích:
  * Tạo khả năng liên thông ngữ nghĩa xuyên biên giới.
  * Hỗ trợ phát triển hệ sinh thái dịch vụ dữ liệu mở, thúc đẩy kinh tế số trong lĩnh vực vận tải.

#### **3. Kinh nghiệm tại Việt Nam**

**a) Khung tiêu chuẩn dữ liệu giao thông Việt Nam**

* Bộ KH\&CN đã thẩm định và ban hành các tiêu chuẩn dữ liệu dùng chung trong ngành Bộ GTVT:
  * TCVN 13420:2021 – Dữ liệu quản lý phương tiện, người điều khiển và hoạt động vận tải.
  * TCVN 13421:2021 – Dữ liệu quản lý kết cấu hạ tầng giao thông.
* Các tiêu chuẩn này quy định:
  * Cấu trúc dữ liệu, mã hóa, định danh và quy tắc chia sẻ.
  * Chuẩn hóa dữ liệu giữa các lĩnh vực giao thông đường bộ, đường sắt, hàng hải, hàng không và đường thủy nội địa.

**b) Kiến trúc Chính phủ điện tử Bộ GTVT phiên bản 2.0 (QĐ 2097/QĐ-BGTVT, 2020)**

* Được coi là bước đầu của kiến trúc dữ liệu ngành GTVT.
* Bao gồm hai định hướng chính:
  * Chính phủ số ngành GTVT – tập trung số hóa quản lý nhà nước, dịch vụ công.
  * Kinh tế số GTVT – phát triển hạ tầng dữ liệu và sàn dữ liệu vận tải thông minh (ITS).
* Kiến trúc này cần được nghiên cứu kế thừa và mở rộng theo hướng:
  * Xây dựng miền dữ liệu giao thông tích hợp các tiêu chuẩn TCVN đã ban hành.
  * Kết nối dữ liệu GTVT với các lĩnh vực liên quan (dân cư, an ninh, tài chính, bảo hiểm...) qua Nền tảng chia sẻ dữ liệu quốc gia (NDOP).
  * Ứng dụng sandbox thử nghiệm AI dự báo dựa trên các nguồn dữ liệu giao thông vận tả

#### **4. Bài học tổng kết**

* Từ quốc tế:
  * Cần có kiến trúc tham chiếu ITS thống nhất, đóng vai trò “ngôn ngữ chung” giữa các hệ thống.
  * Ontology giao thông là lớp ngữ nghĩa giúp máy hiểu và xử lý dữ liệu vận tải.
  * Xây dựng sandbox dữ liệu giao thông để thử nghiệm đổi mới sáng tạo an toàn.
* Từ Việt Nam:
  * Chuẩn hóa dữ liệu giao thông bằng các TCVN, đảm bảo tương thích quốc tế.
  * Cần phát triển Kiến trúc miền dữ liệu giao thông như một phần nằm trong Khung Kiến trúc Dữ liệu Quốc gia.
  * Khuyến khích phát triển sàn dữ liệu và nền tảng phân tích mở, phục vụ cả quản lý nhà nước và doanh nghiệp logistics, vận tải.
* Kiến trúc miền dữ liệu giao thông vận tải là minh chứng điển hình cho việc kết nối giữa kiến trúc dữ liệu tổng thể – tiêu chuẩn dữ liệu – đổi mới sáng tạo dữ liệu công.
* Việc học hỏi kinh nghiệm quốc tế (như ARC-IT, DATEX II) kết hợp với tiêu chuẩn Việt Nam (TCVN 13420, TCVN 13421) sẽ:
  * Giúp Việt Nam xây dựng mô hình giao thông thông minh đồng bộ, liên thông;
  * Mở ra cơ hội cho đổi mới sáng tạo, sandbox thử nghiệm dữ liệu, và phát triển kinh tế dữ liệu giao thông trong giai đoạn 2025-2035.
