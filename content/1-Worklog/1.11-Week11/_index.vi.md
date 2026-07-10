---
title: "Tuần 11: Lập trình Backend Serverless & Tích hợp Trí tuệ Nhân tạo"
date: 2026-06-26
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu Tuần 11:
* Xây dựng trục xương sống lưu trữ Event-Driven với Amazon S3, SQS và cơ sở dữ liệu DynamoDB.
* Lập trình logic Serverless (AWS Lambda - Python 3.12) cấp phát Presigned URL để đẩy file an toàn, giảm tải cho API Gateway.
* Tích hợp AI (Amazon Textract) vào luồng xử lý bất đồng bộ để tự động bóc tách dữ liệu hóa đơn thô.
* Thiết lập an ninh Zero Trust với kỹ thuật Che giấu dữ liệu (Data Masking) và chống DDoS/Spam bằng AWS WAF.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - **Thiết lập Lưu trữ & Hàng đợi:**<br>&emsp; + Khởi tạo `idp-ingest-bucket-1` (Block all public access).<br>&emsp; + Tạo SQS standard queue (`idp-document-queue`), Visibility timeout 2 phút.<br>&emsp; + Tạo bảng DynamoDB `InvoicesData` chế độ On-demand. | 29/06/2026 | 29/06/2026 | AWS Console |
| **Thứ Ba**<br>(Ngày 2) | - **Tự động hóa Sự kiện & FinOps:**<br>&emsp; + Cấu hình S3 Event Notification (`SendToSQS`) đẩy thẳng sự kiện tạo file vào SQS.<br>&emsp; + Đặt quy tắc S3 Lifecycle (`Auto-Delete-Raw-Invoices`) tự xóa file gốc sau 1 ngày. | 30/06/2026 | 30/06/2026 | AWS Console |
| **Thứ Tư**<br>(Ngày 3) | - **Lập trình Compute (Lambda Python 3.12):**<br>&emsp; + Viết hàm `idp-api-presign` cấp URL an toàn (300 giây), ép cứng `ContentType` để chống giả mạo.<br>&emsp; + Phân quyền IAM Role `idp-lambda-ai-role` theo nguyên tắc Đặc quyền tối thiểu. | 01/07/2026 | 01/07/2026 | IDE / AWS Lambda |
| **Thứ Năm**<br>(Ngày 4) | - **Tích hợp Trí tuệ nhân tạo (Textract):**<br>&emsp; + Viết hàm `idp-ai-worker` đóng vai trò Consumer lấy message từ SQS (Batch size: 10).<br>&emsp; + Dùng tính năng `QUERIES` của Textract để bóc tách chính xác Số hóa đơn, Ngày, Tổng tiền, Tên NCC và ghi xuống DynamoDB. | 02/07/2026 | 02/07/2026 | AWS Textract SDK |
| **Thứ Sáu**<br>(Ngày 5) | - **Bảo mật API & Data Masking:**<br>&emsp; + Viết hàm `idp-api-get-invoices` áp dụng kỹ thuật Data Masking ẩn Mã số thuế (`******1234`).<br>&emsp; + Bật AWS WAF (`idp-api-waf-shield`), thêm Rule `BlockSpamIP` chặn các IP request quá 100 lần/5 phút. | 03/07/2026 | 03/07/2026 | AWS WAF & API Gateway |

### Kết quả đạt được:
* Xây dựng thành công kiến trúc xử lý tách biệt (Decoupled), giải quyết dứt điểm bài toán nghẽn cổ chai (Bottleneck) khi người dùng upload hàng loạt file lớn cùng lúc.
* Triển khai kỹ thuật Data Masking sâu dưới tầng Backend thay vì phó mặc cho Frontend, bảo vệ tuyệt đối thông tin định danh (PII) của doanh nghiệp theo chuẩn Zero Trust.
* Hoàn thiện lưới phòng thủ tài chính bằng hệ thống tường lửa AWS WAF (chống bạo lực mạng làm cạn tiền) và S3 Lifecycle (dọn dẹp dữ liệu rác lưu trữ nóng).

---

### [Ghi chú cho Trung: Các hình ảnh cần chụp để thay thế vào chỗ này]
![S3 Event & Lifecycle](/workshop_intership_report/images/1-Worklog/1.11-Week11/week11-1.png)
<p align="center"><i>Hình 1: Tự động hóa quy trình với S3 Event Notification và kỷ luật tài chính FinOps bằng S3 Lifecycle Rule.</i></p>

![Serverless AI Worker](/workshop_intership_report/images/1-Worklog/1.11-Week11/week11-2.png)
<p align="center"><i>Hình 2: Cấu trúc hàm Lambda AI Worker được kích hoạt thông qua hàng đợi SQS để bóc tách hóa đơn bằng Amazon Textract.</i></p>

![AWS WAF Rate Limiting](/workshop_intership_report/images/1-Worklog/1.11-Week11/week11-3.png)
<p align="center"><i>Hình 3: Thiết lập rào chắn AWS WAF chặn Spam API để chống cạn kiệt tài nguyên Serverless.</i></p>