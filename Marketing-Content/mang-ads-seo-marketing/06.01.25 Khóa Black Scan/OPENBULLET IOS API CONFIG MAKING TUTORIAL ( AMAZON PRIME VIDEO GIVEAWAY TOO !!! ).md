---
title: "OPENBULLET IOS API CONFIG MAKING TUTORIAL"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan"
instructor: "Unknown"
difficulty: "Advanced"
tags:
  - "openbullet"
  - "ios-config"
summary: "Hướng dẫn chi tiết cấu hình OpenBullet 2 cho API iOS, bao gồm thiết lập proxy qua Burp Suite, tạo Device ID ngẫu nhiên, cấu hình headers xác thực, và bắt dữ liệu subscription, auto-renewal, expiry date với parsing LR string."
---

# OPENBULLET IOS API CONFIG MAKING TUTORIAL

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Thiết lập proxy mạng: Sử dụng IPconfig để lấy IPv4, cấu hình Burp Suite Community Edition bind cổng 8081 và địa chỉ IPv4, bật tất cả giao diện để iPhone truy cập qua mạng cục bộ.
- Cài đặt chứng chỉ CA: Tải và cài đặt CA Certificate từ Burp Suite lên iPhone thông qua trang web và profile download, cho phép truy cập HTTPS nội bộ.
- Tạo Device ID và headers API: Sử dụng block Random String trong OpenBullet để sinh Device ID (mẫu 2-4-6-8 ký tự), cấu hình Content-Type application/json và headers User-Agent, PSS, phiên bản iOS 14.8.8.
- Bắt dữ liệu token và subscription: Quá trình log in với tài khoản thật qua Burp Suite để 포획 token, name (Howard), subscription plan (Premium Custom), auto-renewal (False) và expiry date.
- Parse ngày hết hạn (Expiry): Sử dụng LR (Left-Right) string extraction trong OpenBullet: lấy đoạn từ đầu đến ký tự 'T' là ngày, từ 'T' đến cuối là tháng/ngày, gán vào key check custom.
- Kiểm tra và test config: Thiết lập 100 bots, 4 CPM, proxy IPVanish, xác thực account với mail/password, test kết quả mong đợi Bot Status Success kèm dữ liệu đã capture.

## 📖 Nội Dung Chi Tiết

### 1. Thiết lập Mạng Proxy và Burp Suite
- Mở CMD/PowerShell, chạy `ipconfig`, ghi nhận địa chỉ IPv4 (ví dụ: 192.168.100.2).
- Tải và cài đặt **Burp Suite Community Edition** (phiên bản miễn phí đủ cho mục đích này).
- Chạy Burp Suite, vô hiệu hóa **Intercept** và **Capture** trong tab Proxy.
- Vào **Options → Bind to port: 8081**, **Bind to address: [IPv4 address]**, chọn **All interfaces**.
- Trên iPhone: Cấu hình Proxy dùng địa chỉ IP PC và cổng 8081.
- Truy cập trang web mục tiêu trên iPhone, tải **CA Certificate**, cài đặt qua Settings → Profile Downloaded → Install.

### 2. Cấu hình OpenBullet 2 (Silver Bullet) cho API iOS
- Mở OpenBullet, tạo block mới **Random String** để sinh Device ID.
  - Độ dài: mẫu 2, 4, 6, 8 ký tự (tổng 37 ký tự theo ví dụ).
  - Tên variable: `ID` (hoặc tùy chọn).
- Thiết lập **POST method** với:
  - **Content-Type:** `application/json`
  - **Custom Headers:** Device ID, User-Agent (`iPhone iOS 14.8.8`), PSS, và các header khác đã extract từ phiên login.
- Tạo block **POST** để gửi yêu cầu login, bắt phản hồi chứa `bad credentials` hoặc thành công.

### 3. Bắt và Parse Dữ liệu Subscription/Tokens
- **Token:** Tìm block `post login` trong Burp Suite, sao chép token, thêm vào OpenBullet dưới dạng JSON, không tick **Is Capture** để tránh dữ liệu dư.
- **Name:** Tạo block capture tên (ví dụ: "Howard").
- **Subscription Plan:** Capture `premium custom`.
- **Auto-Renewal:** Giá trị `false`.
- **Expiry Date:** 
  - Sử dụng block **String (LR)**.
  - Left string: đoạn từ đầu cho đến ký tự `T` (in hoa).
  - Right string: thêm ký tự `T` để giới hạn đoạn sau.
  - Tick **Is Capture** để lấy expiry.
- **Validation Rule:** Thêm check "Does not contain subscription" → set config về **Custom Free** nếu từ "subscription" không xuất hiện trong phản hồi, tránh việc kiểm tra account có hạn chế subscription dẫn đến ban hoặc lỗi.

### 4. Cài đặt Bot và Test
- Thông số bổ sung: 100 bots, 4 CPM, proxy IPVanish.
- Cấu hình thêm: Mail và Password cho proxy IPVanish.
- Lưu config, đặt tên ví dụ: `Config by Yashvier Gaming`.
- Test: Bấm Start, mong đợi **Bot Status: Success**.
- Kết quả mong đợi: Capture Name, Plan (Premium Custom), Auto-Renewal (False), Expiry (ngày/tháng/year), và Config name.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cách lấy địa chỉ IPv4 để cấu hình proxy Burp Suite cho iPhone?
  - **Đáp:** Mở CMD/PowerShell, nhập `ipconfig`, tìm dòng IPv4 Address (ví dụ: 192.168.1.x). Ghi lại địa chỉ này để cấu hình bind trong Burp Suite.
- **Hỏi:** Device ID trong OpenBullet iOS API config tạo như thế nào?
  - **Đáp:** Sử dụng block Random String, thiết lập độ dài theo mẫu 2-4-6-8 ký tự, gán tên variable là `ID`, sau đó gán vào header Device ID trong cấu hình POST.
- **Hỏi:** Làm sao để bắt và lưu token, name, plan và expiry date trong OpenBullet?
  - **Đáp:** Log in tài khoản thật qua Burp Suite, sao chép token và thêm vào JSON POST block (không bật Is Capture). Dùng block LR string extraction để parse expiry: left string từ đầu đến 'T', right string từ 'T' đến cuối. Capture name và plan qua block capture có bật Is Capture.
- **Hỏi:** Quy tắc validation "Does not contain subscription" dùng để làm gì?
  - **Đáp:** Nếu phản hồi không chứa từ "subscription", config sẽ tự động chuyển về chế độ Custom Free, tránh việc kiểm tra account có hạn chế subscription dẫn đến ban hoặc lỗi.