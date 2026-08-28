---
title: Bài 6 Giao diện viết bài website Wordpress căn bản - Goo
course: content-inputs
module: mang-content/20.11.23 Đào tạo kỹ năng Content viết bài website từ A-Z
instructor: Không rõ
difficulty: Cơ bản
tags:
  - WordPress
  - Content Writing
  - SEO
  - User Roles
  - Writing Interface
summary: Bài giảng hướng dẫn giao diện viết bài WordPress cơ bản, bao gồm cấu trúc bài viết, phân quyền tài khoản người dùng (Admin, Editor, Author) và quy trình tối ưu SEO từ khóa cho nội dung web.
---

# Bài 6 Giao diện viết bài website Wordpress căn bản - Goo

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Giao diện soạn thảo bài viết WordPress hoạt động giống như trình soạn thảo văn bản (Word), nhưng bổ sung các công cụ cấu trúc và SEO bắt buộc.
- Phân quyền tài khoản (Admin, Editor, Author) xác định phạm vi thao tác: tạo/sửa/xóa nội dung, quản lý chuyên mục và cấu hình website.
- Chuyên mục (category) là bắt buộc cho mỗi bài viết và trực tiếp ảnh hưởng đến SEO; thẻ (tag) là tùy chọn hỗ trợ liên kết nội bộ.

### 1. Phân quyền tài khoản người dùng WordPress
- **Admin:** Quyền toàn quyền hệ thống. Có thể tạo/xóa tài khoản, cài đặt plugin/themes, sửa mã nguồn, quản lý mọi bài viết và người dùng.
- **Editor:** Quyền quản lý nội dung. Có thể tạo, sửa và xóa bài viết của mọi người dùng; kiểm soát chuyên mục (categories); nhưng không có quyền cài đặt hoặc tạo tài khoản mới.
- **Author:** Quyền tác giả. Chỉ có thể xem, tạo và sửa bài viết của chính mình. Không thể sửa bài viết của người khác, tạo chuyên mục mới hoặc thay đổi cấu hình website.
- **Subscriber:** Quyền đọc chỉ. Có thể quản lý hồ sơ cá nhân nhưng không thể tác động đến nội dung hoặc cấu hình.

> **Ví dụ / Case Study:** Phân quyền này giúp ngăn chặn việc can thao tác trái phép giữa các thành viên trong một nhóm nội dung đa tác giả, đảm bảo mỗi người chỉ sửa bài viết của mình.

### 2. Giao diện viết bài và cấu trúc nội dung
- **Tiêu đề bài viết:** Phần quan trọng nhất cho SEO; từ khóa chính nên xuất hiện ở đầu tiêu đề và slug (đường link cố định).
- **Slug (Đường link):** Tự động tạo từ tiêu đề; nên ngắn, chứa từ khóa và không có ký tự đặc biệt.
- **Khối nội dung (Content Area):** Giống soạn thảo Microsoft Word – hỗ trợ dày đậm, nghiêng, đánh dấu, danh sách có/không đầu, trích dẫn, căn lề và căn giữa/phải. Hỗ trợ chèn ảnh, video, liên kết nội bộ/ngoài.
- **Chuyên mục (Categories):** Bắt buộc cho mỗi bài viết. Xác định chủ đề phân loại; giúp crawler Google hiểu cấu trúc website. Bài viết thiếu chuyên mục sẽ bị đánh điểm xấu về SEO.
- **Thẻ (Tags):** Tùy chọn. Giúp liên kết nội bộ và phân loại chủ đề theo từ khóa cụ thể, nhưng quan trọng hơn là chuyên mục.
- **Ảnh đại diện (Featured Image):** Hình ảnh đại diện bài viết; hiển thị trên trang danh sách bài, kết quả tìm kiếm và khi chia sẻ lên mạng xã hội.
- **Tối ưu SEO từ khóa:** 
  * Từ khóa chính: Nhập vào ô mục tiêu của plugin SEO (Rank Math, Yoast).
  * Vị trí chiến lược: Tiêu đề, đoạn mở đầu bài viết, nội dung tự nhiên, văn bản thay thế ảnh (alt text), slug.
  * Từ khóa dài (long-tail): Các phiên bản mở rộng (ví dụ: "màu son in giá rẻ", "cách chăm sóc son cho da dày"). Thường nên giới hạn 3 từ khóa chính và nhiều biến thể dài.
  * Cấu hình kỹ thuật: Meta description, cấu trúc header (H1 cho tiêu đề, H2/H3 cho các đoạn con), tốc độ tải trang và tính di động.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cấp quyền nào trên WordPress cho phép viết và sửa bài nhưng không cho phép sửa bài của người khác?
  - **Đáp:** Quyền **Tác giả (Author)**. Người dùng này chỉ có thể sửa/xóa bài viết của chính mình.
- **Hỏi:** Tại sao chuyên mục (category) bắt buộc trong WordPress và tác động như thế nào đến SEO?
  - **Đáp:** Chuyên mục định cấu trúc phân loại nội dung, giúp crawler Google xác định chủ đề bài viết. Bài viết không có chuyên mục sẽ bị đánh điểm xấu và ảnh hưởng tiêu cực đến xếp hạng tìm kiếm.
- **Hỏi:** Từ khóa chính nên đặt ở vị trí nào trong bài viết WordPress để tối ưu hiệu quả SEO?
  - **Đáp:** Từ khóa chính nên xuất hiện ở đầu tiêu đề, đoạn mở đầu bài viết, và trong slug/URL. Nên sử dụng tự nhiên và kết hợp với các từ khóa dài (long-tail); tránh lặp từ khóa (keyword stuffing).