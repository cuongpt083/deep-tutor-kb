---
title: "How to make OB Config ReCaptcha V3 Bypassed"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan/Captcha Bypass"
instructor: "Yashvier"
difficulty: "Nâng cao"
tags:
  - "openbullet"
  - "recaptcha-v3"
  - "captcha-bypass"
  - "config-tools"
  - "rockstar-games"
summary: "This lesson guides viewers through constructing an OpenBullet configuration to bypass ReCaptcha V3 Enterprise on Rockstar Games Social Club, covering network analysis, token capture, and request validation."
---

# How to make OB Config ReCaptcha V3 Bypassed

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Workflow for building an OB config from network inspection to token integration for ReCaptcha V3 bypass.
- Methods for capturing and parsing authentication tokens using left/right mode or JSON parsing in Mozilla Firefox.
- Configuration of POST requests, header management, and success/failure key validation for automated sign-in.

## 📖 Nội Dung Chi Tiết
### 1. Xây dựng cấu hình OpenBullet và bắt token ReCaptcha V3
- Mục tiêu: Tạo config OpenBullet để绕过 ReCaptcha V3 Enterprise trên Rockstar Games Social Club.
- Công cụ: Config Tools By Racks dành cho OpenBullet.
- Bước 1: Tạo tài khoản và lấy Google post URL nếu chưa có.
- Bước 2: Mở Inspect Element → Tab Network, thực hiện hành động đăng nhập để bắt request POST tới "Sign In Rockstar Social Club".
- Bước 3: Phân tích request: xác định phương thức POST, Content-Type application/json, và dữ liệu post chứa email/password.
- Bước 4: Tách token tier: scroll down, nhận diện token bắt đầu và kết thúc, thêm separator nếu cần để tránh cấu hình chập chờn.
- Bước 5: Bắt token: Sử dụng Mozilla Firefox (khuyến nghị) để xem response JSON; hoặc dùng chế độ left/right string hoặc JSON parsing. Trên trình duyệt khác có thể xuất hiện form data thay vì JSON.
- Bước 6: Capture trường dữ liệu bổ trợ: account name (xóa biến username), display name (nickname/alias), friend count (total friends), last games played (capture text inside brackets). Tick captured để kích hoạt.
- Bước 7: Thiết lập key success/failure: Key success thường là "success" hoặc "state: true"; uncheck ban if no key found. Key failure: tin nhắn "The email and password combination entered, do not match any account".

> **Ví dụ / Case Study:** Giảng viên演示 cách vào Inspect Element → Network, thực hiện đăng nhập Rockstar Social Club, bắt request POST, và phân tích response để lấy token và cấu hình success/failure keys. Quy trình bao gồm thay thế email/password bằng biến USER/PASS, thiết lập separator cho token, và dùng chế độ left/right string trong OpenBullet để capture dữ liệu profile như tên hiển thị và số bạn bè.

### 2. Cấu hình request POST, header và validate authentication
- Đặt tên request: Ví dụ "login", đảm bảo request nằm dưới phần labels đã định nghĩa.
- Cấu hình method: Đổi từ GET sang POST theo yêu cầu của website (Post Method).
- Header: Copy từ connection đến host, set Content-Type là application/json. Trong OpenBullet chọn content type qua dropdown hoặc paste toàn bộ.
- Post data: Paste toàn bộ dữ liệu post, thay email bằng `USER`, password bằng `PASS` (tất cả in hoa). Không cần sửa các setting khác.
- Thêm failure check: Dán đoạn tin nhắn "The email and password combination entered, do not match any account" vào phần kiểm tra thất bại.
- Thêm success check: Dựa trên response của tài khoản hợp lệ, xác định key success (ví dụ: `success` hoặc `state is true`). Nếu key không tìm thấy, config sẽ không đánh dấu thành công.
- Clone block: Nếu cần capture nhiều field, click một lần vào block bar rồi chọn clone để tạo bản sao, điều chỉnh left/right string hoặc JSON path cho từng field.
- Content type consistency: Đảm bảo method GET không có post data, method POST có post data; điều chỉnh Content-Type theo đúng loại request để tránh lỗi parsing.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** What are the essential steps to configure a POST request for ReCaptcha V3 bypass in OpenBullet?
  - **Đáp:** Identify the target POST endpoint, set Content-Type to application/json, replace credentials with USER/PASS variables, and implement success/failure checks based on response JSON keys such as "success" or "state".
- **Hỏi:** How should one capture and utilize the ReCaptcha V3 token within an OpenBullet config?
  - **Đáp:** Use Mozilla Firefox to inspect the response payload, extract the token via left/right string mode or JSON parsing, and set it as a custom header or post data variable, ensuring the success key matches the token's presence or state.
- **Hỏi:** What common issues arise from method/content-type mismatches in OpenBullet configs, and how can they be resolved?
  - **Đáp:** Mismatches between GET/POST methods and application/json/form-data content types cause request failures; resolve by verifying the endpoint's required method, adjusting Content-Type accordingly, and using Firefox for consistent JSON response parsing.