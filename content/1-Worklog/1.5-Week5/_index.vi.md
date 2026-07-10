---
title: "Tuần 5: Hệ thống Cơ sở dữ liệu Đa tầng (Amazon RDS & DynamoDB)"
date: 2026-05-15
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:
* Phân biệt rõ các kịch bản sử dụng và kiến trúc của cơ sở dữ liệu quan hệ SQL (Amazon RDS) và phi quan hệ NoSQL (Amazon DynamoDB).
* Triển khai kiến trúc cơ sở dữ liệu có tính sẵn sàng cao (HA) sử dụng cấu hình Multi-AZ và Read Replicas.
* Bảo mật tầng cơ sở dữ liệu bằng cách cô lập hoàn toàn trong Private Subnets và thiết lập Security Groups khắt khe.
* Ứng dụng mã hóa dữ liệu ở trạng thái nghỉ (Encryption at Rest) bằng AWS Key Management Service (KMS).

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu Relational Database Service (RDS):<br>&emsp; + Kiến trúc dự phòng Multi-AZ (Disaster Recovery).<br>&emsp; + Read Replicas giúp mở rộng hiệu năng đọc.<br>&emsp; + Cơ chế Sao lưu tự động (Automated Backups) và Snapshot thủ công. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành RDS:**<br>&emsp; + Khởi tạo cơ sở dữ liệu MySQL/PostgreSQL trên RDS.<br>&emsp; + Đặt Database tuyệt đối bên trong mạng nội bộ (Private Subnet).<br>&emsp; + Kết nối vào RDS thông qua máy chủ nhảy (EC2 Bastion Host). | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Tìm hiểu Amazon DynamoDB (NoSQL):<br>&emsp; + Mô hình dữ liệu Document & Key-Value.<br>&emsp; + Cấu trúc Khóa chính (Partition Key & Sort Key).<br>&emsp; + Phân biệt chế độ tính phí Provisioned và On-Demand. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành DynamoDB:**<br>&emsp; + Khởi tạo bảng DynamoDB (`InvoicesData`).<br>&emsp; + Thêm dữ liệu (Insert), truy vấn (Query) và quét (Scan) thông qua AWS Console và AWS CLI. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - **Thiết kế Bảo mật Cơ sở dữ liệu:**<br>&emsp; + Cấu hình mã hóa dữ liệu (Encryption at Rest) qua AWS KMS.<br>&emsp;. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Khởi tạo và quản trị thành công cả hai mô hình cơ sở dữ liệu SQL và NoSQL trên môi trường AWS.
* Làm chủ tư duy kiến trúc cô lập tầng dữ liệu (Data Tier): Đảm bảo các Database luôn nằm trong vùng mạng riêng (Private Subnet), triệt tiêu hoàn toàn khả năng bị tấn công trực diện từ Internet.
* Thực thi các chốt chặn an toàn thông tin mạnh mẽ bằng việc bật tính năng mã hóa KMS, bảo vệ dữ liệu nhạy cảm ngay cả khi ổ cứng lưu trữ vật lý bị xâm phạm.
* Kiểm thử thành công kết nối luồng mạng nội bộ thông qua việc truy cập RDS an toàn từ một máy chủ EC2 Bastion Host.

---

<!-- 
Lưu vào thư mục /images/1-Worklog/1.5-Week5/ và đặt tên tương ứng:
1. week5-1.png: Chụp màn hình RDS Dashboard hiển thị Database đang ở trạng thái "Available".
2. week5-2.png: Chụp màn hình DynamoDB (phần Explore items) hiển thị bảng dữ liệu có các item mẫu bên trong.
--!>

![Amazon RDS Deployment](/images/1-Worklog/1.5-Week5/week5-1.png)
<p align="center"><i>Hình 1: Khởi tạo thành công cơ sở dữ liệu Amazon RDS bên trong phân vùng mạng nội bộ (Private Subnet).</i></p>

![DynamoDB Table](/images/1-Worklog/1.5-Week5/week5-2.png)
<p align="center"><i>Hình 2: Tương tác với cơ sở dữ liệu phi quan hệ Amazon DynamoDB thông qua việc thêm và truy vấn các bản ghi.</i></p>

