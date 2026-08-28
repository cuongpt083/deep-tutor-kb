---
title: "How to use burp suite with Genymotion, OpenBullet _ Track API of any apk"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan/Openbullet Couse/Course Advanced"
instructor: "AshVey Gaming"
difficulty: "Nâng cao"
tags:
  - "burp-suite"
  - "genymotion"
  - "api-tracking"
  - "android-emulator"
  - "http-traffic"
summary: "Hướng dẫn cài đặt và cấu hình Genymotion cùng Burp Suite để bắt và theo dõi HTTP/HTTPS traffic từ thiết bị ảo Android, phù hợp cho việc phân tích API của các APK."
---

# How to use burp suite with Genymotion, OpenBullet _ Track API of any apk

## 💡 Tóm Tắt Cốt Lõi
- Cài đặt và cấu hình Genymotion để tạo thiết bị ảo Android (Google Nexus 6, Android 5.1, 2 processes).
- Cài đặt Burp Suite Community Edition và thiết lập proxy để bắt traffic từ emulator.
- Sử dụng kết hợp Genymotion + Burp Suite để bắt, bắt gỡ và theo dõi API calls của các ứng dụng Android.

## 📖 Nội Dung Chi Tiết
### 1. Cài đặt Genymotion
- Tải và cài đặt Genymotion từ trang chính thức.
- Khởi động ứng dụng và chọn "Create new virtual device".
- Chọn thiết bị mẫu: Google Nexus 6.
- Tùy chỉnh phiên bản Android: Khuyên dùng Android 5.1 để tương thích tốt với Burp Suite.
- Cấu hình số lượng process: Giữ ở mức 2 processes để đảm bảo hiệu suất ổn định.

### 2. Cài đặt Burp Suite và cấu hình proxy
- Tải phiên bản cộng đồng (Community Edition) từ official website.
- Cài đặt và khởi động Burp Suite.
- Cấu hình proxy trên Burp Suite (mặc định port 8080).
- Cài đặt chứng chỉ CA của Burp Suite vào Genymotion/emulator để bắt HTTPS traffic.

### 3. Bắt traffic HTTP/HTTPS từ Android ảo
- Chạy Genymotion và thiết bị ảo đã tạo.
- Trên emulator, cấu hình mạng để sử dụng proxy IP của máy host (thường là 10.0.2.2 hoặc cài đặt thủ công).
- Mở Burp Suite, vào tab Proxy -> Intercept để bật bắt gói tin.
- Các API calls của APK được cài trên emulator sẽ hiện ra trong Burp Suite Suite.

> **Ví dụ / Case Study:** Bài giảng演示 cách cài đặt APK test lên Genymotion, kích hoạt proxy trên Burp Suite và bắt được các request/login API của ứng dụng, từ đó phân tích cấu trúc dữ liệu hoặc tìm điểm yếu an ninh.

### 4. Tối ưu và mở rộng
- Sử dụng OpenBullet (như nội dung khóa học liên quan) để tự động hóa việc test API sau khi đã bắt traffic.
- Điều chỉnh thiết lập Android version và process tùy theo yêu cầu cụ thể của từng APK.
- Lưu ý: Luôn tuân thủ quy định pháp lý và đạo đức khi kiểm tra bảo mật hệ thống.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cách cài đặt Genymotion và Burp Suite để bắt traffic HTTP/HTTPS từ Android ảo là như thế nào?
  - **Đáp:** Tải Genymotion và tạo thiết bị ảo (ví dụ Google Nexus 6 với Android 5.1), sau đó tải Burp Suite Community Edition, cấu hình proxy trên emulator指向 máy host, cài đặt chứng chỉ CA của Burp và bật tính năng Intercept để bắt và xem các request API.
- **Hỏi:** Phiên bản Android và cấu hình phần nào khuyến nghị cho việc track API với Burp Suite?
  - **Đáp:** Phiên bản Android 5.1 là lựa chọn an toàn và tương thích tốt nhất, với cấu hình 2 processes để cân bằng hiệu suất và ổn định khi bắt traffic.
- **Hỏi:** Sau khi bắt traffic qua Burp Suite, làm gì tiếp theo (ví dụ kết hợp OpenBullet)?
  - **Đáp:** Dữ liệu traffic đã được bắt có thể xuất ra file (JSON, HAR) hoặc dùng trực tiếp trong Burp Suite Suite để phân tích, sau đó có thể nhập vào OpenBullet để tự động test các điểm yếu API, brute force credential hoặc fuzz request tùy mục đích nghiên cứu.