---
title: "AWS First Cloud AI Journey Community Day"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---



## Mục tiêu của sự kiện

AWS First Cloud AI Journey Community Day được tổ chức nhằm mang đến cho người tham dự cái nhìn tổng quan về các công nghệ AI và điện toán đám mây đang được ứng dụng trong thực tế. Nội dung chương trình tập trung vào ba mục tiêu chính:

- Cập nhật kiến thức về Generative AI, Large Language Models (LLMs) và kiến trúc Multi-Agent.
- Giới thiệu các giải pháp AWS giúp tối ưu chi phí, nâng cao hiệu năng và tăng cường bảo mật hệ thống.
- Chia sẻ kinh nghiệm phát triển sản phẩm từ các chuyên gia thông qua những dự án và cuộc thi Hackathon thực tế.

---

## Tóm tắt nội dung chương trình

### 1. Ứng dụng Multi-Agent trong đánh giá tín dụng Startup

**Diễn giả:** Vy Lam – Senior Business Systems Analyst, VPBank

Diễn giả đã phân tích những hạn chế của mô hình chấm điểm tín dụng truyền thống khi áp dụng cho các doanh nghiệp khởi nghiệp do thiếu dữ liệu tài chính và lịch sử hoạt động.

Giải pháp được giới thiệu là kiến trúc Multi-Agent, trong đó nhiều AI Agent đảm nhận các nhiệm vụ riêng như phân tích tài chính, đánh giá thị trường, phân tích rủi ro, đánh giá đội ngũ và kiểm tra tuân thủ. Cách tiếp cận này giúp nâng cao chất lượng đánh giá, đồng thời rút ngắn thời gian xử lý và giảm đáng kể chi phí vận hành.

---

### 2. Hiểu đúng về tính không xác định của LLM

**Diễn giả:** Duc Dao – Solution Architect, Cloud Kinetics

Buổi chia sẻ tập trung giải thích nguyên nhân khiến các mô hình ngôn ngữ lớn không phải lúc nào cũng tạo ra cùng một kết quả.

Mặc dù nhiều lập trình viên cho rằng đặt Temperature bằng 0 sẽ tạo ra kết quả cố định, nhưng trên thực tế các phép tính dấu phẩy động được thực hiện song song trên GPU vẫn có thể tạo ra sai khác nhỏ trong quá trình suy luận.

Diễn giả khuyến nghị nên sử dụng đầu ra dạng JSON kết hợp với Temperature thấp (khoảng 0.1) để đảm bảo tính ổn định khi triển khai trong các hệ thống thực tế.

---

### 3. Kinh nghiệm phát triển UTMorpho tại Lotus Hacks 2026

**Diễn giả:** Team VIB

Nhóm VIB chia sẻ hành trình xây dựng ứng dụng UTMorpho trong vòng 36 giờ tại cuộc thi Lotus Hacks 2026.

Trong quá trình phát triển, nhóm gặp nhiều khó khăn như giới hạn API Token, mở rộng phạm vi dự án quá mức và các lỗi phát sinh từ mã nguồn do AI sinh ra.

Qua trải nghiệm này, nhóm nhấn mạnh rằng sự phối hợp giữa các thành viên và việc ưu tiên hoàn thiện chức năng cốt lõi luôn quan trọng hơn việc bổ sung quá nhiều tính năng.

---

### 4. Tối ưu hạ tầng bằng Amazon CloudFront

**Diễn giả:** Nguyễn Tuấn Thịnh – DevOps Engineer

Nội dung trình bày giới thiệu Amazon CloudFront như một giải pháp giúp nâng cao hiệu năng và bảo mật cho hệ thống.

CloudFront phân phối nội dung thông qua mạng lưới Edge Location trên toàn cầu, góp phần giảm độ trễ và tăng khả năng chống tấn công DDoS nhờ tích hợp AWS Shield và AWS WAF.

Ngoài ra, diễn giả còn đề xuất sử dụng Origin Access Control (OAC), Mutual TLS và Lambda@Edge để tăng cường khả năng bảo vệ hạ tầng.

---

### 5. Vai trò của Context trong hệ thống AI

**Diễn giả:** Trịnh Trường – Platform Engineer, GoTymeX

Diễn giả cho rằng chất lượng phản hồi của AI phụ thuộc rất lớn vào chất lượng dữ liệu ngữ cảnh được cung cấp.

Việc đưa quá nhiều thông tin không liên quan sẽ làm tăng chi phí xử lý và giảm độ chính xác của mô hình. Một hệ thống AI hiệu quả cần có mục tiêu rõ ràng, ràng buộc cụ thể và lựa chọn ngữ cảnh phù hợp.

Bên cạnh đó, việc xây dựng bộ nhớ ngữ cảnh lâu dài cũng được xem là yếu tố quan trọng để tạo ra các hệ thống AI thông minh hơn.

---

### 6. Amazon Q hỗ trợ công việc doanh nghiệp

**Diễn giả:** Phạm Ngọc Hải Anh – G-AsiaPacific Vietnam, AWS Community Builder

Phiên trình bày cuối cùng giới thiệu Amazon Q như một trợ lý AI hỗ trợ tự động hóa nhiều công việc văn phòng như tạo biên bản cuộc họp, gửi email theo dõi và quản lý lịch làm việc.

Amazon Q còn có khả năng kết nối với nhiều nguồn dữ liệu doanh nghiệp, đồng thời tuân thủ các cơ chế phân quyền và bảo mật. Ngoài ra, việc ứng dụng AI để kiểm tra an toàn hạ tầng cũng mở ra nhiều tiềm năng trong quản trị hệ thống Cloud.

---

## Cảm nhận và ứng dụng thực tế

Sau khi tham gia sự kiện, tôi có cơ hội hiểu rõ hơn về cách AI và AWS được triển khai trong các hệ thống thực tế.
Tôi dự định áp dụng một số kiến thức đã học vào các dự án của mình.
1. **Thứ nhất**, tôi sẽ sử dụng đầu ra JSON kết hợp với cơ chế Retry thay vì chỉ phụ thuộc vào Temperature bằng 0 nhằm đảm bảo dữ liệu trả về luôn ổn định.
2. **Thứ hai**, tôi muốn áp dụng CloudFront cùng Origin Access Control để nâng cao khả năng bảo vệ các dịch vụ backend và dữ liệu quan trọng.
3. **Thứ ba**, tôi nhận thấy việc lựa chọn đúng Context trước khi gửi yêu cầu đến AI sẽ giúp giảm chi phí xử lý và cải thiện độ chính xác của mô hình.
4. **Cuối cùng**, bài học từ Team VIB giúp tôi hiểu rằng cần ưu tiên xây dựng một sản phẩm cốt lõi hoạt động ổn định trước khi mở rộng thêm các chức năng khác.

 **Kết luận:**  
 AWS First Cloud AI Journey Community Day không chỉ cung cấp kiến thức về AI và AWS mà còn mang đến nhiều kinh nghiệm thực tiễn trong thiết kế hệ thống và phát triển phần mềm. Đây là cơ hội giúp tôi thay đổi góc nhìn từ việc chỉ tập trung viết mã sang tư duy xây dựng các hệ thống Cloud và AI an toàn, ổn định và có khả năng mở rộng.

## Hình ảnh tại sự kiện

![](/images/4-EventParticipated/4.1-Event1/event-1.png)