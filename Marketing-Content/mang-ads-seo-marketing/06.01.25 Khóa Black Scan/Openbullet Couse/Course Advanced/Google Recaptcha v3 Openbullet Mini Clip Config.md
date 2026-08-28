---
title: "Google Recaptcha v3 Openbullet Mini Clip Config"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan/Openbullet Couse/Course Advanced"
instructor: "Unknown"
difficulty: "Advanced"
tags:
  - "reCAPTCHA"
  - "OpenBullet"
  - "Config"
  - "Miniclip"
  - "CAPTCHA v3"
  - "Web Automation"
summary: "Hướng dẫn cấu hình OpenBullet cho reCAPTCHA v3 trên miniclip.com. Bao gồm trích xuất tham số từ mã HTML, thiết lập yêu cầu GET/POST, quản lý CSRF token và khớp mã lỗi/thành công để tự động hóa đăng nhập."
---

# Google Recaptcha v3 Openbullet Mini Clip Config

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Trích xuất các tham số reCAPTCHA v3 (`v`, `co`, `key`) từ mã HTML bằng kỹ thuật Inspect Element và thao tác find-replace (Ctrl+H) để làm rõ payload request.
- Thiết lập cấu hình OpenBullet với hai yêu cầu POST riêng biệt: một cho xác thực API reCAPTCHA v3 và một cho xử lý login, kèm theo CSRF token, header tùy chỉnh và dữ liệu đăng nhập (email/pass).
- Khớp mã trạng thái HTTP 200 và từ khóa thành công (`Success`)/thất bại (`Error`) để xác định kết quả bot; cần sử dụng proxy và tài khoản hợp lệ cho hoạt động thực tế.

## 📖 Nội Dung Chi Tiết
### 1. Trích Xuất Tham Số reCAPTCHA v3
- Sử dụng Inspect Element trên widget reCAPTCHA và sao chép toàn bộ khối HTML.
- Áp dụng Ctrl+H (Find & Replace) để xóa các thuộc tính không cần thiết, giúp lộ ra các tham số fundamental như `v` (phiên bản), `co` (context/action) và `key` (prefix khóa site, ví dụ: QC5B...Y5B).
- Dán URL kết quả vào trình duyệt mới để xác nhận hiển thị lại nút reCAPTCHA và xác định chính xác cấu trúc payload trong Network tab.
> **Ví dụ / Case Study:** Trích xuất tham số từ miniclip.com: sử dụng Inspect Element trên widget reCAPTCHA, sao chép HTML, áp dụng Ctrl+H để làm rõ payload, và xác định các tham số `v`, `co`, `key` như QC5B...Y5B trong request GET.

### 2. Cấu Hình Yêu Cầu GET cho reCAPTCHA
- Trong công cụ Racks Config Tool, tạo yêu cầu GET với phương thức URL, điền tham số `v`, `co` và `key` đã trích xuất.
- Các biến `vcon` và `cocon` cần được sao chép chính xác từ payload request và gán vào các trường tương ứng trong config.
- Yêu cầu GET này dùng để lấy challenge và token cần thiết cho bước xác minh sau.

### 3. Cấu Hình Yêu Cầu POST cho Xác Thực và Login
- **POST User Verify:** Thiết lập phương thức POST với dữ liệu bao gồm `v`, `co`, `key` và các biến `vcon`/`cocon`. Đây là yêu cầu gửi đến Google reCAPTCHA API user verify endpoint.
- **POST Login:** Kết hợp CSRF token (trích xuất từ Network > Login request), trường `user` (email), `PASS` (mật khẩu), và phản hồi token reCAPTCHA (`tk`/`uv`). Đặt phương thức là POST và đảm bảo header tùy chỉnh bao gồm Referer và Host để mô phỏng traffic trình duyệt thật.
- Thêm custom headers: sao chép toàn bộ từ Referer đến Host trong request gốc và dán vào section Custom Headers của OpenBullet để tránh bị chặn bởi chính sách cùng nguồn (same-origin) hoặc kiểm tra referrer.

### 4. Khớp Lỗi và Thành Công (Error & Success Matching)
- **Success Key:** Đặt là `Success` với giá trị mong đợi `200` (status code) và nội dung phản hồi xác nhận login thành công.
- **Error Key:** Đặt là `Error` để bắt các thông báo như "credentials are incorrect" hoặc mã trạng thái khác 200, giúp bot dừng hoặc ghi nhận thất bại một cách có kiểm soát.

### 5. Thiết Lập Chạy và Lưu Config
- Lưu config trong Stacker/Obelisk, bật proxy và nhập thông tin tài khoản (mail/pass).
- Khởi chạy combo; theo dõi status bot. Config được thiết kế cho hành động login; đăng ký tài khoản mới hiện tại không khả dụng trên miniclip.com.
- Kiểm tra kết quả: khi có hits, tài khoản có thể truy cập miniclip.com; nếu lỗi, quay lại Inspect Element để điều chỉnh key check hoặc header.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cách trích xuất tham số `v`, `co` và `key` cho reCAPTCHA v3 trên OpenBullet như thế nào?
  - **Đáp:** Sử dụng Inspect Element để sao chép HTML của widget reCAPTCHA, sau đó dùng Ctrl+H để xóa các thuộc tính thừa, làm rõ payload. Dán URL vào tab mới để xem cấu trúc request và sao chép chính xác các tham số cần thiết.
- **Hỏi:** Các tham số bắt buộc trong yêu cầu GET và POST cho reCAPTCHA v3 là gì?
  - **Đáp:** Ba tham số then trọng tâm: `v` (phiên bản reCAPTCHA), `co` (context/action identifier) và `key` (prefix khóa site, ví dụ QC5B...Y5B). Chúng phải xuất hiện trong cả yêu cầu GET để lấy challenge và POST data cho xác thực user verify.
- **Hỏi:** Làm sao CSRF token và header tùy chỉnh được cấu hình trong OpenBullet cho config này?
  - **Đáp:** Trích xuất CSRF token từ request login trong Network tab, thêm vào config như một field token riêng. Đối với header, sao chép toàn bộ từ Referer đến Host trong request gốc và dán vào section Custom Headers để tránh bị chặn bởi chính sách cùng nguồn (same-origin) hoặc kiểm tra referrer.