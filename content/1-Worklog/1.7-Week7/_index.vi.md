---
title: "Tuần 7: Hệ sinh thái Lưu trữ Đa tầng & Quản trị Dữ liệu"
date: 2026-05-29
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:
* Nắm vững hệ sinh thái lưu trữ chia sẻ của AWS: Amazon S3 (Object), Amazon EFS (Linux) và Amazon FSx (Windows).
* Xây dựng cầu nối lưu trữ lai (Hybrid Cloud Storage) thông qua AWS Storage Gateway.
* Tự động hóa quy trình bảo vệ dữ liệu tập trung và tuân thủ tiêu chuẩn qua AWS Backup.
* Thiết lập bảo mật mức Đối tượng (Object-level) khắt khe nhằm ngăn chặn rò rỉ dữ liệu S3.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Khám phá các giải pháp lưu trữ nâng cao:<br>&emsp; + So sánh ứng dụng thực tế của EFS và FSx.<br>&emsp; + Tìm hiểu kiến trúc AWS Storage Gateway (File, Volume, Tape). | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành Lưu trữ Lai (Lab 24):**<br>&emsp; + Triển khai cổng AWS Storage Gateway (Dạng File Gateway).<br>&emsp; + Kết nối máy chủ mô phỏng On-premises đồng bộ dữ liệu trực tiếp lên Amazon S3 qua giao thức NFS/SMB. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Tìm hiểu Quản trị Phục hồi Dữ liệu Tập trung:<br>&emsp; + Các khái niệm lõi của AWS Backup (Vaults, Plans).<br>&emsp; + Quy tắc Vòng đời (Lifecycle) tự động đẩy bản sao lưu cũ sang kho lạnh để tối ưu chi phí. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành AWS Backup (Lab 13):**<br>&emsp; + Thiết lập Backup Plan duy nhất gom toàn bộ máy chủ EC2 và RDS vào vòng bảo vệ.<br>&emsp; + Xác định khung giờ sao lưu và thời hạn bảo lưu (Retention period) đáp ứng Compliance. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - **Quản trị Rủi ro & Bảo mật S3 (Lab 57):**<br>&emsp; + Ứng dụng nguyên tắc "Đặc quyền tối thiểu" thông qua Object Permissions.<br>&emsp; + Thực hành bật/tắt rào chắn "Block all public access" để nhận thức rõ ranh giới rò rỉ dữ liệu. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Xây dựng thành công kiến trúc lưu trữ lai bằng Storage Gateway, giúp giải quyết bài toán cạn kiệt dung lượng mạng nội bộ mà không cần thay đổi giao thức đọc/ghi truyền thống.
* Chuyển đổi tư duy từ việc tạo Snapshot thủ công rời rạc sang chiến lược Centralized Backup, tự động hóa toàn bộ quy trình sao lưu tài nguyên doanh nghiệp.
* Nâng cao năng lực Cybersecurity: Hiểu và thực thi việc chặn truy cập công khai trên S3, loại bỏ hoàn toàn nguyên nhân số 1 gây ra các thảm họa lộ lọt dữ liệu trên Cloud (Misconfiguration).
* Hoàn thành xuất sắc kỷ luật dọn dẹp tài nguyên (FinOps) thông qua việc gỡ bỏ Gateway và xóa Backup Vaults an toàn sau Lab.

---




![AWS Backup Plan](/images/1-Worklog/1.7-Week7/week7-2.png)
<p align="center"><i>Hình 1: Cấu hình hệ thống sao lưu tập trung AWS Backup Plan nhằm tự động hóa quy trình bảo vệ dữ liệu.</i></p>

![S3 Block Public Access](/images/1-Worklog/1.7-Week7/week7-3.png)
<p align="center"><i>Hình 2: Thực thi bảo mật dữ liệu đám mây mạnh mẽ bằng cách bật tính năng Block Public Access mặc định trên Amazon S3.</i></p>