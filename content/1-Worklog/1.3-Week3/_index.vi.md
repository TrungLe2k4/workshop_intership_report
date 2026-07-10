---
title: "Tuần 3: Hạ tầng Điện toán Đám mây & Amazon EC2"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3:
* Làm chủ vòng đời, cách cấu hình và quản trị máy chủ ảo Amazon EC2 (Elastic Compute Cloud).
* Hiểu rõ các Dòng máy chủ (Instance Types) và mô hình tối ưu chi phí (On-Demand, Reserved, Spot).
* Triển khai tự động hóa cài đặt ứng dụng ngay khi khởi động máy chủ thông qua EC2 User Data.
* Thiết lập an ninh mạng chặt chẽ ở cấp độ máy chủ bằng Security Groups.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu nền tảng Amazon EC2:<br>&emsp; + Các dòng máy chủ (Tối ưu tính toán, bộ nhớ, lưu trữ).<br>&emsp; + Khái niệm về Amazon Machine Images (AMI). | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - Khám phá Lưu trữ và Mạng cho EC2:<br>&emsp; + Phân biệt ổ cứng mạng EBS và ổ cứng vật lý Instance Store.<br>&emsp; + Tìm hiểu Elastic IPs và định tuyến IP Public/Private. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Đi sâu vào Security Groups (SG):<br>&emsp; + Hiểu bản chất SG là tường lửa có trạng thái (Stateful) hoạt động ở cấp độ card mạng ảo (ENI).<br>&emsp; + Viết quy tắc giới hạn truy cập SSH (Port 22) chỉ từ IP quản trị viên. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành EC2 (Phần 1):**<br>&emsp; + Khởi tạo 1 máy chủ Linux EC2 (Amazon Linux 2023).<br>&emsp; + Tạo và tải về an toàn cặp khóa SSH Key Pair (.pem).<br>&emsp; + Kết nối thành công vào máy chủ thông qua giao thức SSH. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - **Thực hành EC2 (Phần 2):**<br>&emsp; + Chèn script Bash vào EC2 User Data để tự động cài đặt Web Server (Apache/httpd).<br>&emsp; + Mở port 80 (HTTP) trên Security Group và kiểm tra truy cập trang web qua IP Public. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Triển khai và quản trị thành công máy chủ ảo trên đám mây sử dụng Amazon EC2.
* Tự động hóa quá trình cấu hình môi trường Web Server bằng EC2 User Data, giúp giảm thiểu đáng kể thời gian cài đặt thủ công.
* Thiết lập vành đai phòng thủ vững chắc bằng việc áp dụng các quy tắc Security Group khắt khe, tuyệt đối không mở các cổng quản trị (như SSH) cho toàn bộ Internet (`0.0.0.0/0`).
* Quản lý và sử dụng thành thạo cặp khóa mã hóa SSH Key Pair để truy cập hệ thống từ xa một cách an toàn.

---


<!-- 
Lưu vào thư mục /images/1-Worklog/1.3-Week3/ và đặt tên tương ứng:
1. week3-1.png: Chụp giao diện EC2 Dashboard có hiện máy chủ đang ở trạng thái "Running".
2. week3-2.png: Chụp phần cấu hình Inbound Rules của Security Group (Cho thấy mở port 80 và 22).

-->

![EC2 Instance Running](/images/1-Worklog/1.3-Week3/week3-1.png)
<p align="center"><i>Hình 1: Khởi tạo và vận hành thành công máy chủ ảo Linux trên Amazon EC2.</i></p>

![Security Group Configuration](/images/1-Worklog/1.3-Week3/week3-2.png)
<p align="center"><i>Hình 2: Cấu hình tường lửa có trạng thái thông qua Security Groups để cho phép truy cập HTTP và giới hạn SSH.</i></p>
