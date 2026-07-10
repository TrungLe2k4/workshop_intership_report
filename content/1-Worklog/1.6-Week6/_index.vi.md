---
title: "Tuần 6: Giám sát Hệ thống & Quản trị Tối ưu (CloudWatch & CloudTrail)"
date: 2026-05-22
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:
* Triển khai hệ thống giám sát toàn diện sử dụng Amazon CloudWatch (Metrics, Dashboards, và Alarms).
* Xây dựng luồng thông báo sự cố tự động thông qua Amazon Simple Notification Service (SNS).
* Thiết lập cơ chế kiểm toán an ninh mạng (Auditing) bằng cách theo dõi các lệnh gọi API qua AWS CloudTrail.
* Phân tích các lỗ hổng kiến trúc và tối ưu hóa chi phí dựa trên khuyến nghị từ AWS Trusted Advisor.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu Amazon CloudWatch:<br>&emsp; + Phân biệt giữa Chỉ số (Metrics), Nhật ký (Logs) và Sự kiện (Events).<br>&emsp; + Ứng dụng CloudWatch Dashboards để trực quan hóa hiệu năng. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành CloudWatch & SNS:**<br>&emsp; + Tạo SNS Topic và đăng ký (Subscribe) địa chỉ Email cá nhân.<br>&emsp; + Cấu hình CloudWatch Billing Alarm (Cảnh báo chi phí vượt quá $10) và kích hoạt gửi email qua SNS. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Tìm hiểu AWS CloudTrail:<br>&emsp; + Vai trò của CloudTrail trong quản trị, tuân thủ (Compliance) và kiểm toán (Auditing).<br>&emsp; + Phân biệt Management Events và Data Events. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành CloudTrail (Truy vết An ninh):**<br>&emsp; + Khám phá giao diện Event History.<br>&emsp; + Đóng vai trò kỹ sư bảo mật: Lọc log để tìm chính xác IAM User nào đã tắt (Terminate) một máy chủ EC2 hoặc chỉnh sửa Security Group. | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - Vận hành & Quản trị tài chính (FinOps):<br>&emsp; + Kiểm tra AWS Trusted Advisor để rà soát lỗ hổng bảo mật (VD: mở port 0.0.0.0/0) và cơ hội tiết kiệm chi phí.<br>&emsp; + Sử dụng AWS Cost Explorer để phân tích xu hướng chi tiêu. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Thiết lập thành công hệ thống giám sát vận hành tự động, đảm bảo ngay lập tức nhận được cảnh báo (qua Email) khi chi phí hoặc tải lượng CPU hệ thống vượt ngưỡng an toàn.
* Xây dựng năng lực kiểm toán an ninh mạng chuyên sâu (Security Monitoring): AWS CloudTrail cung cấp một bằng chứng số (Audit Trail) không thể chối cãi để điều tra sự cố hoặc phát hiện cấu hình sai lệch từ con người.
* Làm chủ công cụ AWS Trusted Advisor để liên tục quét và rà soát môi trường đám mây, kết hợp hài hòa giữa tư duy bảo mật hạ tầng (Security Posture) và quản trị tối ưu tài chính (FinOps).

---


<!-- 
Lưu vào thư mục /images/1-Worklog/1.6-Week6/ và đặt tên tương ứng:
1. week6-1.png: Chụp cấu hình CloudWatch Alarm (Billing hoặc CPU Alarm), hiện rõ biểu đồ và trạng thái (OK hoặc In alarm).
2. week6-2.png: Chụp màn hình hộp thư Email của bạn chứa tin nhắn thông báo (Notification) được gửi từ AWS SNS.
3. week6-3.png: Chụp giao diện AWS CloudTrail Event History hiển thị danh sách các API calls (VD: RunInstances, ConsoleLogin).
-->

![CloudWatch Alarm](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-1.png)
<p align="center"><i>Hình 1: Thiết lập cảnh báo Amazon CloudWatch Alarm để giám sát chỉ số và tự động hóa quy trình phản hồi sự cố.</i></p>

![SNS Email Notification](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-2.png)
<p align="center"><i>Hình 2: Nhận thành công email cảnh báo tự động được định tuyến qua dịch vụ Amazon SNS.</i></p>

![CloudTrail Event History](/workshop_intership_report/images/1-Worklog/1.6-Week6/week6-3.png)
<p align="center"><i>Hình 3: Ứng dụng AWS CloudTrail để duy trì nhật ký kiểm toán số độ chính xác cao phục vụ công tác điều tra an ninh mạng.</i></p>