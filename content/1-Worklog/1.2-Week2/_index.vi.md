---
title: "Tuần 2: Quản trị Định danh & Truy cập mạng (AWS IAM) và Thiết lập CLI"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:
* Làm chủ cơ chế quản lý định danh và phân quyền bảo mật với AWS IAM tuân thủ nguyên tắc Đặc quyền tối thiểu (Least Privilege) và Zero Trust.
* Hiểu rõ cấu trúc và tự viết được các chính sách phân quyền IAM Policy bằng JSON.
* Cài đặt, cấu hình và tương tác thành thạo với AWS thông qua giao diện dòng lệnh (AWS CLI).
* Triển khai chiến lược gắn thẻ tài nguyên (Resource Tags) phục vụ quản trị hệ thống bài bản.

### Các công việc đã thực hiện trong tuần:

| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| :--- | :--- | :--- | :--- | :--- |
| **Thứ Hai**<br>(Ngày 1) | - Đi sâu vào các khái niệm cốt lõi của AWS IAM:<br>&emsp; + Phân biệt giữa Users, Groups, Roles, và Policies.<br>&emsp; + Thực hành an toàn bảo mật: Ngừng sử dụng tài khoản Root. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Ba**<br>(Ngày 2) | - **Thực hành Bảo mật Tài khoản:**<br>&emsp; + Bật xác thực đa yếu tố (MFA) cho tài khoản Root.<br>&emsp; + Tạo nhóm Admin (IAM Group) và tài khoản người dùng (IAM User) riêng cho công việc hàng ngày. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Tư**<br>(Ngày 3) | - Tìm hiểu cấu trúc của một JSON IAM Policy:<br>&emsp; + Nắm vững các thành phần cốt lõi: Effect, Action, Resource, Condition.<br>&emsp; + Viết các IAM Policy tùy chỉnh để cấp quyền cụ thể. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Năm**<br>(Ngày 4) | - **Thực hành AWS CLI:**<br>&emsp; + Khởi tạo Access Key & Secret Key cho tài khoản IAM User.<br>&emsp; + Cài đặt AWS CLI trên máy cá nhân và cấu hình xác thực (`aws configure`).<br>&emsp; + Kiểm tra kết nối bằng lệnh `aws sts get-caller-identity`. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **Thứ Sáu**<br>(Ngày 5) | - Tìm hiểu AWS Service Roles & Resource Tags:<br>&emsp; + Phân tích lý do vì sao phải dùng Service Roles cho tài nguyên AWS thay vì nhúng cứng Access Keys.<br>&emsp; + Định nghĩa chiến lược gắn thẻ (VD: Project: IDPCloud, Env: Dev) để theo dõi tài nguyên và quản lý chi phí (FinOps). | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được:
* Xây dựng nền tảng an toàn thông tin vững chắc bằng cách bảo vệ tài khoản Root với MFA và sử dụng tài khoản IAM User chuyên biệt.
* Làm chủ cấu trúc của JSON IAM Policy, cho phép cấp phát quyền truy cập chính xác và tuân thủ chặt chẽ nguyên tắc Đặc quyền tối thiểu.
* Cấu hình thành công môi trường làm việc tại máy cá nhân với AWS CLI và quản lý an toàn các khóa bảo mật (Access Keys).
* Định hình tư duy sử dụng IAM Roles cho giao tiếp giữa các dịch vụ đám mây, ngăn chặn triệt để các lỗ hổng bảo mật do lộ lọt thông tin xác thực nhúng cứng (Hardcoded credentials).

---

<!-- 
Trung hãy chụp 3 tấm ảnh sau, lưu vào thư mục /images/1-Worklog/1.2-Week2/ và đặt tên tương ứng nhé:
1. Ảnh 1 (week2-1.png): Chụp giao diện Security credentials (Thông tin bảo mật) hiển thị phần MFA (Multi-Factor Authentication) đã được chuyển sang trạng thái xanh (Đã bật).
2. Ảnh 2 (week2-2.png): Chụp giao diện khung soạn thảo JSON khi bạn đang tạo hoặc xem một IAM Policy bất kỳ trên AWS Console.
-->

![MFA Enabled](/images/1-Worklog/1.2-Week2/week2-1.png)
<p align="center"><i>Hình 1: Bảo mật thành công tài khoản AWS bằng cách kích hoạt tính năng Xác thực đa yếu tố (MFA).</i></p>

![JSON IAM Policy](/images/1-Worklog/1.2-Week2/week2-2.png)
<p align="center"><i>Hình 2: Xây dựng cấu trúc phân quyền IAM Policy tùy chỉnh bằng định dạng JSON để kiểm soát truy cập chặt chẽ.</i></p>

