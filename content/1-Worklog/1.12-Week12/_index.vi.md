---
title: "Tuần 12: Giao diện ReactJS Frontend, Kiểm thử & Đưa dự án Go-Live"
date: 2026-07-03
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu Tuần 12:
* Hoàn thiện ứng dụng Frontend (ReactJS + Tailwind CSS + Vite) và đồng bộ trơn tru với hệ thống API Gateway.
* Thiết lập xác thực danh tính an toàn qua Amazon Cognito (Ép buộc đổi mật khẩu & Xác thực bằng JWT Token).
* Xây dựng các component UI/UX cao cấp (Giao diện đối sánh Side-by-side, Thanh tiến trình cảnh báo ngân sách).
* Thực thi Kịch bản Kiểm thử, chốt Tài liệu Dọn dẹp Tài nguyên, và chính thức đưa ứng dụng lên mạng (Go-Live) bằng S3 Static Hosting và CloudFront.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - **Định danh & Xác thực Cognito:**<br>&emsp; + Cấu hình User Pool `idp-react-app`, vô hiệu hóa tự đăng ký (Self-registration) để chống spam tài khoản.<br>&emsp; + Code `Login.jsx` xử lý luồng OTP, luồng Challenge Password (ép đổi mật khẩu lần đầu) và lưu trữ JWT. | 06/07/2026 | 06/07/2026 | React/Vite / SDK |
| **Thứ Ba**<br>(Ngày 2) | - **Tích hợp API & Trực quan hóa dữ liệu:**<br>&emsp; + Tích hợp `CognitoUserPoolAuthorizer` vào API Gateway (Chừa lại method OPTIONS cho CORS).<br>&emsp; + Xây dựng `Dashboard.jsx` dùng thư viện `recharts` vẽ biểu đồ tài chính và làm thanh Progress Bar đổi màu (Xanh/Vàng/Đỏ) theo ngân sách. | 07/07/2026 | 07/07/2026 | React / Recharts |
| **Thứ Tư**<br>(Ngày 3) | - **UX Nâng cao (Đối sánh dữ liệu AI):**<br>&emsp; + Phát triển component `InvoiceEditModal.jsx`.<br>&emsp; + Thiết kế giao diện Side-by-side (Trái: Ảnh hóa đơn gốc, Phải: Form dữ liệu do AI bóc tách) để con người kiểm duyệt (Data Quality Control). | 08/07/2026 | 08/07/2026 | React / Tailwind |
| **Thứ Năm**<br>(Ngày 4) | - **Kiểm thử Tích hợp & Quy trình Thu hồi:**<br>&emsp; + Chạy 4 kịch bản lõi: Đăng nhập, Upload qua Presigned URL, Bộ lọc, Cảnh báo ngân sách trên UI.<br>&emsp; + Soạn thảo chi tiết Tài liệu Dọn dẹp Tài nguyên (Resource Cleanup Protocol) để tránh thất thoát chi phí sau dự án. | 09/07/2026 | 09/07/2026 | Tài liệu Test |
| **Thứ Sáu**<br>(Ngày 5) | - **Đưa dự án chạy thực tế (Go-Live):**<br>&emsp; + Chạy lệnh `npm run build` đóng gói và tối ưu hóa mã nguồn tĩnh.<br>&emsp; + Triển khai toàn bộ thư mục `dist/` lên S3 Bucket (`idp-frontend-bucket-1`).<br>&emsp; + Khởi tạo mạng phân phối nội dung Amazon CloudFront trỏ về S3 để tăng tốc độ tải trang toàn cầu qua HTTPS. | 10/07/2026 | 10/07/2026 | AWS Console |

### Kết quả đạt được:
* Bàn giao thành công một ứng dụng Single Page Application (SPA) có chất lượng thương mại, liên kết hoàn hảo với hệ sinh thái AWS Backend.
* Củng cố an ninh lớp ứng dụng bằng cách chặn đứng tấn công dò quét tài khoản (Account Enumeration) thông qua chính sách cấp phát tài khoản thủ công và ép đổi mật khẩu khắt khe từ Amazon Cognito.
* Nâng tầm trải nghiệm người dùng với giao diện Side-by-side, đảm bảo yếu tố "Con người kiểm soát AI" (Human-in-the-loop), triệt tiêu tỷ lệ sai sót dữ liệu.
* Phát hành dự án IDPCloud ra toàn cầu (Go-Live) thành công rực rỡ, tận dụng sức mạnh bảo mật và hiệu năng cực cao của hệ thống CDN Amazon CloudFront.

---


![Cognito Authentication UI](/workshop_intership_report/images/1-Worklog/1.12-Week12/week12-1.png)
<p align="center"><i>Hình 1: Luồng xác thực bảo mật xử lý yêu cầu đổi mật khẩu bắt buộc từ Amazon Cognito.</i></p>

![IDP Dashboard](/workshop_intership_report/images/1-Worklog/1.12-Week12/week12-2.png)
<p align="center"><i>Hình 2: Bảng điều khiển tài chính (Dashboard) với đồ thị trực quan và thanh cảnh báo ngân sách thời gian thực.</i></p>

![Side-by-side UX](/workshop_intership_report/images/1-Worklog/1.12-Week12/week12-3.png)
<p align="center"><i>Hình 3: Giao diện kiểm soát chất lượng dữ liệu Side-by-side, cho phép người dùng đối chiếu ảnh gốc với kết quả AI bóc tách.</i></p>