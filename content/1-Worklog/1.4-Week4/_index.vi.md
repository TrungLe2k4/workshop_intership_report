---
title: "Tuần 4: Tự động hóa Hạ tầng & Cân bằng tải (ELB & ASG)"
date: 2026-05-08
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:
* Thiết kế và triển khai kiến trúc hệ thống có tính sẵn sàng cao (High Availability) và khả năng chịu lỗi trên AWS.
* Cấu hình Elastic Load Balancing (ELB) để phân phối lưu lượng truy cập đồng đều đến nhiều máy chủ.
* Tự động hóa quá trình mở rộng/thu hẹp hạ tầng bằng EC2 Auto Scaling Groups (ASG) dựa trên các chỉ số thời gian thực.
* Nâng cao bảo mật mạng bằng cách che giấu máy chủ backend và quản lý SSL/TLS tại tầng Load Balancer.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu Elastic Load Balancing (ELB):<br>&emsp; + So sánh Application Load Balancer (ALB) và Network Load Balancer (NLB).<br>&emsp; + Khái niệm Target Groups và Health Checks (Kiểm tra sức khỏe). | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành ALB:**<br>&emsp; + Khởi tạo Application Load Balancer.<br>&emsp; + Đăng ký nhiều máy chủ EC2 vào một Target Group.<br>&emsp; + Kiểm tra phân phối truy cập và giả lập lỗi (tắt 1 máy EC2 để xem ALB điều hướng). | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Tìm hiểu Auto Scaling Groups (ASG):<br>&emsp; + Cấu trúc bản mẫu khởi tạo (Launch Templates).<br>&emsp; + Các chiến lược mở rộng động (Target Tracking, Step Scaling). | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành ASG:**<br>&emsp; + Khởi tạo Launch Template chứa sẵn cấu hình Web Server (User Data).<br>&emsp; + Cấu hình ASG liên kết với ALB, sử dụng Target Tracking policy (VD: Tự thêm máy khi CPU > 50%). | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - Ứng dụng Thiết kế Bảo mật Web:<br>&emsp; + Tìm hiểu quy trình quản lý chứng chỉ SSL qua AWS Certificate Manager (ACM).<br>&emsp; + Cấu hình lại Security Groups: EC2 chỉ được phép nhận traffic từ ALB, chặn hoàn toàn kết nối trực tiếp từ Internet. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Xây dựng thành công kiến trúc mạng chịu lỗi trải dài trên nhiều Vùng sẵn sàng (Availability Zones).
* Nắm vững sự tích hợp giữa ALB và ASG, cho phép hệ thống tự động co giãn tài nguyên máy tính nhịp nhàng theo nhu cầu truy cập thực tế.
* Ứng dụng thành công mẫu thiết kế bảo mật mạng nâng cao (Defense-in-Depth): Che giấu hoàn toàn các máy chủ EC2 backend khỏi Internet công cộng bằng cách cấu hình Security Group của chúng chỉ chấp nhận lưu lượng HTTP xuất phát từ Application Load Balancer.

---


<!-- 
Lưu vào thư mục /images/1-Worklog/1.4-Week4/ và đặt tên tương ứng:
1. week4-1.png: Chụp màn hình Target Group hiển thị các máy chủ EC2 đang ở trạng thái "Healthy".
2. week4-2.png: Chụp chi tiết cấu hình của Auto Scaling Group hoặc Launch Template mà bạn đã tạo.

-->

![Target Group Health](/workshop_intership_report/images/1-Worklog/1.4-Week4/week4-1.png)
<p align="center"><i>Hình 1: Xác nhận các máy chủ EC2 vượt qua bài kiểm tra sức khỏe (Health Check) của Application Load Balancer.</i></p>

![Auto Scaling Group](/workshop_intership_report/images/1-Worklog/1.4-Week4/week4-2.png)
<p align="center"><i>Hình 2: Cấu hình Auto Scaling Group để tự động cấp phát máy chủ dựa trên tải lượng truy cập thực tế.</i></p>

