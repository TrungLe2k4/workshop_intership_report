---
title: "Tuần 8: Quy trình Di trú Hệ thống & Phục hồi Thảm họa"
date: 2026-06-05
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:
* Làm chủ chiến lược di trú "Lift-and-Shift" để dịch chuyển máy chủ vật lý/ảo hóa nội bộ lên đám mây AWS.
* Thực thi luồng công việc VM Import/Export thông qua AWS CLI và môi trường trung chuyển Amazon S3.
* Xác thực khả năng Phục hồi sau thảm họa (Disaster Recovery - DR) thông qua quy trình Khôi phục thử nghiệm (Test Restore).
* Bảo mật tuyệt đối các tệp đĩa ảo hệ thống (VM Images) tránh truy cập trái phép trong quá trình dịch chuyển.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Tìm hiểu Chiến lược Di trú Đám mây:<br>&emsp; + 6 chiến lược cốt lõi (6 R's: Rehost, Replatform...).<br>&emsp; + Tổng quan công nghệ nhân bản dữ liệu thời gian thực AWS MGN. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Lý thuyết VM Import/Export:**<br>&emsp; + Quy trình đóng gói máy chủ On-premises (định dạng OVA/VMDK).<br>&emsp; + Yêu cầu cấp quyền IAM Role (`vmimport`) và chuẩn bị S3 Bucket. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - **Thực hành Di trú (Lab 14 - Phần 1):**<br>&emsp; + Tải an toàn tệp đĩa ảo (VM disk image) lên Amazon S3.<br>&emsp; + Cấu hình kiểm soát truy cập (S3 ACLs) khắt khe ở mức độ chi tiết cho tệp tin này. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành Di trú (Lab 14 - Phần 2):**<br>&emsp; + Sử dụng AWS CLI để khởi chạy lệnh `import-image`.<br>&emsp; + Giám sát tiến trình chuyển đổi và khởi tạo thành công máy chủ EC2 từ AMI vừa được tạo. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - **Kiểm thử Phục hồi Thảm họa (Mở rộng Lab 13):**<br>&emsp; + Thực hiện quy trình Test Restore (Khôi phục thử nghiệm) từ Backup Vault.<br>&emsp; + Kiểm tra tính toàn vẹn của dữ liệu sau khôi phục nhằm cam kết chỉ số RTO/RPO. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Hiện thực hóa chiến lược di trú "Lift-and-Shift" bằng việc chuyển đổi thành công tệp ảnh đĩa hệ thống nội bộ thành một Amazon Machine Image (AMI) hoạt động trơn tru trên AWS.
* Khẳng định tư duy an ninh mạng (Cybersecurity-first) trong quá trình di trú: Ứng dụng nghiêm ngặt nguyên tắc đặc quyền tối thiểu thông qua S3 ACLs, đảm bảo các file hệ điều hành chứa thông tin mật không bị phơi nhiễm ra Internet.
* Xác thực tính hiệu quả của kế hoạch Disaster Recovery thông qua việc thực hiện thành công Test Restore, chứng minh hệ thống sao lưu không chỉ lưu trữ tốt mà còn luôn sẵn sàng khôi phục khi có thảm họa.

---


