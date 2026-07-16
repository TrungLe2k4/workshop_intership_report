---
title: "Tuần 10: Thiết kế Kiến trúc & Tối ưu hóa Hệ thống Serverless IDP"
date: 2026-06-19
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:
* Thiết kế bản vẽ kiến trúc Runtime Architecture hoàn chỉnh cho hệ thống "Serverless Intelligent Document Processing (IDP)".
* Ứng dụng Kiến trúc Hướng sự kiện (Event-Driven) để giải quyết nút thắt cổ chai băng thông khi xử lý tệp tin lớn.
* Xây dựng vành đai bảo mật lớp biên (Edge Security) kết hợp Route 53, CloudFront, AWS WAF và Amazon Cognito.
* Tối ưu hóa chi phí vận hành (FinOps), đảm bảo ngân sách duy trì hệ thống luôn dưới mức $30/tháng.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - **Quy hoạch Bản vẽ Kiến trúc:**<br>&emsp; + Phân định ranh giới mạng: Global Services, Regional Services và Private VPC.<br>&emsp; + Tách biệt rõ ràng luồng Runtime (Người dùng) và Deployment (CI/CD). | 22/06/2026 | 22/06/2026 | Tài liệu Dự án |
| **Thứ Ba**<br>(Ngày 2) | - **Thiết kế Luồng Event-Driven & Bypass API:**<br>&emsp; + Thiết kế cơ chế Upload file trực tiếp lên S3 không qua máy chủ trung gian bằng Presigned URL.<br>&emsp; + Phân tách (Decouple) tiến trình xử lý AI bằng việc kết nối S3 Events với hàng đợi SQS. | 23/06/2026 | 23/06/2026 | Tài liệu Dự án |
| **Thứ Tư**<br>(Ngày 3) | - **Thiết lập An ninh Lớp biên & Định danh:**<br>&emsp; + Tái cấu trúc gắn trực tiếp AWS WAF để đánh chặn sớm mã độc.<br>&emsp; + Lên sơ đồ luồng CognitoUserPoolAuthorizer để bắt buộc xác thực JWT Token tại tầng API Gateway. | 24/06/2026 | 24/06/2026 | Tài liệu Dự án |
| **Thứ Năm**<br>(Ngày 4) | - **Kỷ luật FinOps & Tối ưu Chi phí:**<br>&emsp; + Loại bỏ hoàn toàn hệ thống NAT Gateway đắt đỏ khỏi sơ đồ.<br>&emsp; + Thay thế bằng giải pháp VPC Gateway Endpoints để định tuyến luồng dữ liệu nội bộ sang S3 và DynamoDB với chi phí $0. | 25/06/2026 | 25/06/2026 | Tài liệu Dự án |
| **Thứ Sáu**<br>(Ngày 5) | - **Chuẩn hóa AWS Well-Architected:**<br>&emsp; + Áp dụng quy tắc phân cụm màu (Color-coded) và bảng chú giải (Legend) cho bản vẽ.<br>&emsp; + Chốt bản thiết kế cuối cùng, sẵn sàng chia task cho nhóm 5 thành viên để triển khai thực tế. | 26/06/2026 | 26/06/2026 | Tài liệu Dự án |

### Kết quả đạt được:
* Hoàn thiện sơ đồ kiến trúc chuẩn Enterprise, minh bạch hóa hoàn toàn các phân vùng mạng và luồng lưu chuyển dữ liệu.
* Giải quyết triệt để bài toán "chảy máu tài chính" trên Cloud bằng cách loại bỏ máy chủ ảo chạy 24/7, ứng dụng 100% Serverless và Gateway Endpoints.
* Ứng dụng thành công tư duy Kiến trúc Hướng sự kiện (Event-Driven), đảm bảo hệ thống có khả năng tự động mở rộng (Auto-scaling) từ 0 lên hàng ngàn lượt xử lý tài liệu cùng lúc mà không bị quá tải.

---


![IDP Architecture Diagram](/workshop_intership_report/images/1-Worklog/1.10-Week10/week10-2.png)
<p align="center"><i>Hình 1: Bản vẽ kiến trúc Runtime hoàn chỉnh cho hệ thống xử lý tài liệu thông minh Serverless IDP.</i></p>

