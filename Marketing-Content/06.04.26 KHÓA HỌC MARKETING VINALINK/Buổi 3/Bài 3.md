---
title: "Thiết lập tự động trả lời bình luận và gửi quà qua Facebook Chatbot"
course: "mang-ads-seo-marketing"
module: "06.04.26 KHÓA HỌC MARKETING VINALINK/Buổi 3"
instructor: "Không rõ"
difficulty: "Trung cấp"
tags:
  - Facebook Marketing
  - Chatbot Automation
  - Lead Generation
  - Gift Distribution
summary: "Bài học hướng dẫn cách cấu hình tự động trả lời bình luận, phân phối quà e-book và nhắn tin hàng loạt cho khách hàng tương tác qua Facebook Post, sử dụng biến personalization và quản lý ID bài viết."
---

# Thiết lập tự động trả lời và gửi quà qua Facebook Chatbot

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Học cách lấy Page ID và Post ID để liên kết bài viết với hệ thống tự động trả lời trên Facebook.
- Nắm quy trình thiết lập tự động phân phối quà (e-book, e-card) khi khách hàng bình luận hoặc nhắn tin.
- Sử dụng biến chatbot (gender, full name) để cá nhân hóa tin nhắn chào mừng và gửi quà cho từng khách.
- Tìm hiểu cách tạo kịch bản tin nhắn hàng loạt (broadcast) cho những người đã từng inbox hoặc bình luận trước đó.
- Hiểu luồng hoàn toàn: Lấy đường link bài viết → Trích xuất ID → Cài đặt tự động trả lời → Lưu và kiểm tra kết quả.

## 📖 Nội Dung Chi Tiết
### 1. Xác định Post ID và Page ID cho bài viết Facebook
- Để cài đặt tự động trả lời hoặc gửi quà, cần có hai thông số chính: **Page ID** (ID của Fanpage) và **Post ID** (ID của bài viết cụ thể).
- Cách lấy: Truy cập bài viết trên Fanpage, vào chế độ xem nguồn hoặc dùng công cụ developer, hoặc theo hướng dẫn trong giao diện chatbot để "bấm vào biểu tượng link/xanh" để hệ thống tự động nhận diện.
- Một đường link bài viết chứa cả hai phần tử này; sau khi copy link, hệ thống sẽ tách ra thành Page ID và Post ID riêng lẻ, là điều kiện tiên quyết để cấu hình tự động hóa.

### 2. Thiết lập tự động trả lời bình luận/kèm nút quà
- Sau khi có Post ID, vào phần cài đặt tự động trả lời trong chatbot.
- Chọn bài viết mục tiêu, bấm nút liên kết/cộng từ khóa hoặc chọn bài viết trực tiếp.
- Khi có người bình luận hoặc tương tác, hệ thống sẽ kích hoạt kịch bản được cấu hình sẵn.
- Cấu hình hiển thị nút "Nhận quà" hoặc đường dẫn dẫn đến file tải xuống (e-book, e-card), và thiết lập điều kiện kích hoạt (ví dụ: bình luận chứa từ khóa cụ thể).

### 3. Phân phối quà (e-book/e-card) và lấy thông tin khách hàng
- Khi khách hàng tương tác, kích hoạt kịch bản gửi tin chào mừng kèm yêu cầu留下 (留下) thông tin (email, số điện thoại) để nhận quà.
- Sử dụng biến personalization: **gender** (tự động thay thành "anh", "chị" hoặc "bạn"), **full name** để làm đẹp tin nhắn (ví dụ: "Chúc mừng anh/chị [tên] đã nhận quà").
- Quy trình: Khách bình luận/nhắn → Kích hoạt kịch bản chào mừng → Yêu cầu留下 thông tin → Hệ thống gửi file/link quà tự động.

### 4. Tạo kịch bản tin nhắn hàng loạt (Broadcast) cho khách cũ
- Sau khi có danh sách khách đã inbox hoặc bình luận trước đó, tạo nhóm khách hàng trong chatbot.
- Sử dụng tính năng nhắn tin hàng loạt (broadcast) để gửi lại nội dung giới thiệu chương trình, khuyến mãi hoặc nhắc nhận quà.
- Cấu hình bộ lọc theo thời gian, hành động (comment, inbox) để đảm bảo đúng đối tượng nhận tin, tuân thủ quy định về tin nhắn marketing của Facebook.

### 5. Biến personalization trong chatbot
- **gender**: Tự động thay thành "anh", "chị" hoặc "bạn" tùy giới tính nhận tin.
- **full name**: Thay bằng tên thực tế của khách hàng khi có dữ liệu.
- Cách cài: Trong nội dung tin nhắn, chèn đối tượng biến, hệ thống sẽ tự động điền khi gửi, giúp tin nhắn nghe tự nhiên và cá nhân hóa.

> **Ví dụ / Case Study:** Khách truy cập Fanpage, bình luận dưới bài quảng cáo hoặc nhắn tin vào Inbox. Hệ thống kích hoạt kịch bản chào mừng: "Chúc mừng bạn đã tham gia! Để nhận e-book miễn phí, vui lòng留下 địa chỉ email của bạn." Hệ thống tự động thay "bạn" bằng tên khách nếu có dữ liệu, hoặc "anh/chị" dựa trên giới tính, sau đó gửi link tải e-book tự động.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Làm sao để lấy Page ID và Post ID cho bài viết Facebook để cài tự động trả lời?
  - **Đáp:** Cần có đường link bài viết trên Fanpage, hệ thống sẽ tự tách ra Page ID và Post ID. Hoặc thủ công vào chế độ xem nguồn/cài đặt chatbot bấm vào biểu tượng link/xanh để hệ thống nhận diện bài viết.
- **Hỏi:** Quy trình tự động gửi quà e-book khi khách bình luận như thế nào?
  - **Đáp:** Khách bình luận → Kích hoạt kịch bản chào mừng → Yêu cầu留下 email/số điện thoại → Hệ thống gửi link/file quà tự động. Sử dụng biến personalization để gọi tên khách và cá nhân hóa tin nhắn.
- **Hỏi:** Có thể gửi tin nhắn hàng loạt cho những người đã từng inbox trước không? Làm sao?
  - **Đáp:** Có, tạo nhóm khách hàng trong chatbot và dùng tính năng broadcast. Bộ lọc theo hành động cũ (inbox, comment) và thời gian. Cần tuân thủ quy định về tin nhắn marketing của Facebook để tránh bị chặn.
- **Hỏi:** Cách sử dụng biến gender và full name để cá nhân hóa tin nhắn như thế nào?
  - **Đáp:** Trong nội dung kịch bản, chèn đối tượng {{gender}} hoặc {{full name}}. Hệ thống sẽ thay thế bằng giá trị thực tế của khách hàng khi gửi, giúp tin nhắn nghe tự nhiên (ví dụ: "Chúc mừng anh [Tên] đã nhận quà").