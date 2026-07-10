---
title: "Tuần 9: Đám mây Riêng ảo & Bảo mật Mạng Diện rộng (Amazon VPC)"
date: 2026-06-12
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:
* Thiết kế và xây dựng từ con số không (from scratch) kiến trúc mạng đám mây riêng ảo Amazon VPC (Virtual Private Cloud).
* Làm chủ quy hoạch dải địa chỉ mạng (CIDR Blocks) và phân đoạn ranh giới (Public/Private Subnets).
* Triển khai hệ thống phòng thủ mạng chiều sâu (Defense-in-Depth) kết hợp NACL (phi trạng thái) và Security Groups (có trạng thái).
* Thiết lập định tuyến Internet một chiều an toàn qua NAT Gateway và kết nối mạng nội bộ chéo qua VPC Peering.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu kiến trúc mạng Amazon VPC:<br>&emsp; + Quy hoạch dải IP (CIDR Blocks).<br>&emsp; + Khái niệm VPC, Subnets, và Internet Gateways (IGW). | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành Xây dựng VPC Nền tảng:**<br>&emsp; + Khởi tạo VPC tùy chỉnh.<br>&emsp; + Phân chia VPC thành 1 Public Subnet và 1 Private Subnet.<br>&emsp; + Gắn IGW và cấu hình Bảng định tuyến công khai (Public Route Table trỏ `0.0.0.0/0` ra IGW). | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Triển khai NAT và Cập nhật Định tuyến:<br>&emsp; + Cài đặt NAT Gateway nằm trong Public Subnet.<br>&emsp; + Cập nhật Private Route Table điều hướng luồng dữ liệu ra Internet thông qua NAT Gateway để các máy chủ nội bộ tải bản vá bảo mật an toàn. | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thiết lập An ninh mạng Đa tầng (Defense-in-Depth):**<br>&emsp; + Cấu hình Network Access Control Lists (NACL) ở tầng mạng con (Lọc phi trạng thái).<br>&emsp; + Kết hợp NACL với Security Groups ở tầng máy chủ (Có trạng thái) để chặn đứng các dải IP độc hại ngay tại cửa ngõ. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - **VPC Peering & Kỷ luật Dọn dẹp:**<br>&emsp; + Thiết lập kết nối VPC Peering để trao đổi dữ liệu an toàn giữa hai VPC độc lập thông qua hạ tầng cáp quang nội bộ của AWS.<br>&emsp; + Tuân thủ nghiêm ngặt trình tự gỡ bỏ tài nguyên mạng (EC2 -> NAT -> IGW -> VPC) để tránh phát sinh chi phí ẩn. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Tự tay quy hoạch và kiến thiết thành công một môi trường mạng chuẩn doanh nghiệp, hoàn toàn cô lập khỏi các thiết lập mặc định có sẵn.
* Định hình sâu sắc tư duy an toàn thông tin về sự Cô lập mạng (Network Isolation): Đảm bảo các tài nguyên lõi (như Database) tuyệt đối phải nằm ở vùng Private Subnets và chỉ được phép truy cập Internet một chiều qua NAT Gateway.
* Dựng lên tấm khiên bảo vệ đa tầng vững chắc bằng cách bọc lót NACL (chặn IP xấu ở vòng ngoài) và Security Groups (lọc cổng dịch vụ ở vòng trong).
* Mở rộng an toàn các kết nối liên mạng thông qua VPC Peering, triệt tiêu nguy cơ dữ liệu doanh nghiệp bị phơi nhiễm ra môi trường Internet công cộng.

---


<!-- 
Lưu vào thư mục /images/1-Worklog/1.9-Week9/ và đặt tên tương ứng:
1. week9-1.png: Chụp màn hình "Resource Map" của VPC (trong giao diện chi tiết VPC), nơi hiển thị trực quan sơ đồ nối từ VPC -> Subnets -> Route Tables -> Internet Gateway.
2. week9-2.png: Chụp giao diện cấu hình Network Access Control List (NACL), hiển thị bảng Inbound/Outbound rules có số thứ tự (Rule number) cụ thể.
3. week9-3.png: Chụp giao diện "Peering connections" hiển thị một kết nối đang có trạng thái (Status) là "Active".
-->

![VPC Resource Map](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-1.png)
<p align="center"><i>Hình 1: Trực quan hóa kiến trúc liên kết mạng của Amazon VPC tùy chỉnh, thể hiện sự phân ranh giới rõ ràng giữa Public và Private Subnets.</i></p>

![Defense-in-Depth NACL](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-2.png)
<p align="center"><i>Hình 2: Cấu hình quy tắc tường lửa phi trạng thái (NACL) nhằm đánh chặn sớm các luồng truy cập độc hại tại cửa ngõ phân khu mạng.</i></p>

![VPC Peering Connection](/workshop_intership_report/images/1-Worklog/1.9-Week9/week9-3.png)
<p align="center"><i>Hình 3: Thiết lập cầu nối mạng nội bộ bảo mật cao cấp giữa các VPC độc lập thông qua VPC Peering.</i></p>