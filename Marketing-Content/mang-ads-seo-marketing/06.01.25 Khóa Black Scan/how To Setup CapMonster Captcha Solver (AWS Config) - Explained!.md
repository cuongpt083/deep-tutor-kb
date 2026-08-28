---
title: "How To Setup CapMonster Captcha Solver (AWS Config) - Explained!"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan"
instructor: "Yarchivier Gaming"
difficulty: "Nâng cao"
tags:
  - "CapMonster"
  - "AWS Automation"
  - "OpenBullet"
  - "SilverBullet"
  - "Captcha Solver"
  - "Proxy Management"
  - "Account Harvesting"
summary: "A technical walkthrough of setting up CapMonster to solve CAPTCHAs for automated AWS account creation and validation using OpenBullet or SilverBullet, covering RDP prerequisites, image capture, API configuration, proxy and combo integration, and result filtering into Hits and Customs categories."
---

# How To Setup CapMonster Captcha Solver (AWS Config) - Explained!

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- **Yêu cầu RDP:** Cần Remote Desktop Protocol với dung lượng RAM tối thiểu 8GB (khuyến nghị 16GB) để hoạt động ổn định cho tự động hóa.
- **Bắt ảnh chụp:** Phải thu thập và nhập ít nhất 15 ảnh thử thách CAPTCHA vào CapMonster để hệ thống tự động phân loại và nhận diện.
- **Cấu hình API:** Lấy API key từ CapMonster Cloud, cấu hình endpoint `api.capmonster.cloud:80` và dịch vụ tùy chỉnh trong cả CapMonster và OpenBullet/SilverBullet.
- **Phương pháp giải:** Sử dụng phương pháp Chrome cho ReCAPTCHA v2, tỷ lệ nhận diện vượt quá 80%.
- **Phân loại kết quả:** Hệ thống tách kết quả thành "Hits" (tài khoản hợp lệ có thể đăng nhập trực tiếp vào AWS Portal kèm balance và dịch vụ) và "Customs" (tài khoản có MFA, suspended, expired hoặc concerns về bảo mật).
- **Chi phí & hiệu suất:** $10 credit CapMonster có thể dùng khoảng 2 tuần ở tốc độ ~15 CPM (captchas per minute); hiệu suất phụ thuộc vào chất lượng proxy.

## 📖 Nội Dung Chi Tiết

### 1. Prerequisites & Environment Setup
- **RDP Requirement:** Một RDP là bắt buộc cho hoạt động ổn định (không nên dùng máy Windows cục bộ do tốc độ chậm). Yêu cầu RAM tối thiểu 8GB, 16GB khuyến nghị. Hình demo chạy Windows 10 trên phần cứng Intel Xeon (thông số có thể bị phóng đại).
- **Workflow Bắt ảnh:** 
  - Truy cập trang mục tiêu, chuột phải → lưu ảnh CAPTCHA.
  - Nhấn refresh để tạo thách mới, lặp lại cho đến khi có khoảng 15 ảnh.
  - Lưu tất cả ảnh vào thư mục chuyên dụng để nhập vào CapMonster.

### 2. CapMonster Configuration
- **Tạo Project:** Khởi động CapMonster (MCS - Monster Cloud Solver), tạo project mới, sử dụng "Load Captures".
- **Import & Sắp xếp:** Nhập tất cả ảnh đã lưu (Ctrl+A chọn tất cả → Open). Bật tự động sắp xếp. Kiểm tra nghiệm: hệ thống đã nhận diện tự động hơn 53 ảnh.
- **Lưu Project:** Lưu project cấu hình (ví dụ: AWS.cm2) để tái sử dụng, tránh tăng ký không cần thiết.
- **API Key & Endpoint:** 
  - Đăng ký và nạp tiền vào CapMonster Cloud để nhận API key riêng.
  - Trong Cài đặt CapMonster: bật "use keep alive" và "emulate capture service" (tất cả checkbox liên quan phải được tick).
  - Dán API key vào và bật chức năng "enable correction".
  - Đặt endpoint tùy chỉnh: `api.capmonster.cloud` cổng `80`.
- **Phương pháp giải ReCAPTCHA v2:** Chọn method Chrome. Tỷ lệ nhận diện báo cáo vượt quá 80%, được coi là tốt.

### 3. OpenBullet / SilverBullet Integration
- **Thay đổi dịch vụ CAPTCHA:** 
  - Vào Settings > Captchas trong OpenBullet hoặc SilverBullet.
  - Đổi service từ `toCaptcha` sang `custom toCaptcha`.
  - Dán API key CapMonster vào trường custom toCaptcha.
  - Xóa URL `example.com` và nhập `api.capmonster.cloud`. Cổng giữ mặc định là `80`.
- **Import Combos & Proxies:** 
  - Nhập danh sách combo (cấu hình AWS/credentials) và proxy list.
  - Ưu tiên proxy data center hoặc premium để tốc độ tốt hơn.
  - Đảm bảo proxies được bật trước khi khởi động bot.
- **Cấu hình Bot:** 
  - Thiết lập số luồng bot (ví dụ: bắt đầu 50, có thể tăng lên 72 hoặc 100 như demo).
  - Tải module AWS config đã lưu trong CapMonster nếu có.
  - Kiểm tra kết nối proxy và số dư credit trước khi bắt đầu.

### 4. Execution & Result Analysis
- **Khởi động:** Nhấn Start trong SilverBullet/OpenBullet. Bot sẽ bắt đầu giải CAPTCHA và thử xác thực tài khoản AWS.
- **Giám sát:** Các lần chạy đầu có thể xuất hiện vài retry; cần persistence. Theo dõi thanh tiến độ (ví dụ: 15 CPM) và dư credit thời gian thực.
- **Phân loại kết quả sau khi giải:**
  - **Hits:** Tài khoản cho phép đăng nhập trực tiếp vào AWS Portal. Hiển thị balance, danh sách dịch vụ được hỗ trợ (EC2, Amazon AWS, AWS LightSail, và plan khác tùy tài khoản).
  - **Customs:** Tài khoản có concerns bảo mật (2FA/MFA), suspended, expired hoặc các vấn đề khác. Các tài khoản này sẽ được chuyển vào thư mục Customs và không thể đăng nhập được.
- **Logic lọc tài khoản:** Hệ thống tự động tách: tài khoản có MFA/suspended/expired → Customs; chỉ tài khoản "sạch" có thể login trực tiếp → Hits. Hits còn ghi thêm thông tin balance và dịch vụ tài khoản có.

### 5. Case Study: AWS Account Filtering Logic
- Trong quá trình solve, CapMonster capture đầy đủ thông tin tài khoản AWS.
- Kết quả sau khi giải được phân loại rõ ràng:
  - Một tài khoản có security concerns (có 2FA/MFA) → vào Customs.
  - Một tài khoản suspended → vào Customs.
  - Tài khoản thứ ba cũng suspended.
  - Chỉ các tài khoảnHits (good accounts) mới xuất hiện với dữ liệu: balance, services (EC2, LightSail, v.v.), và plan tài khoản.
- Kết quả thực tế demo: đã có 1 custom (MFA), 3 customs (suspended), và 2 accounts có security concerns, trong khi hits chứa các account có thể login trực tiếp kèm dữ liệu dịch vụ.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Yêu cầu cấu hình phần cứng tối thiểu để chạy CapMonster với tự động hóa AWS là gì?
  - **Đáp:** Cần RDP có RAM tối thiểu 8GB (khuyến nghị 16GB), kết nối internet ổn định. Hình demo sử dụng RDP Windows 10 cấu hình cao (Intel Xeon, RAM lớn).
- **Hỏi:** Phải thu thập và nhập bao nhiêu ảnh CAPTCHA để hệ thống nhận diện hoạt động đáng tin cậy?
  - **Đáp:** Ít nhất 15 ảnh nên được chụp, lưu và nhập vào project CapMonster. Hình thức demo đã nhập và sắp xếp tự động hơn 53 ảnh với tỷ lệ nhận diện tốt.
- **Hỏi:** Cách cấu hình kết nối CapMonster với OpenBullet hoặc SilverBullet như thế nào?
  - **Đáp:** Đặt dịch vụ CAPTCHA thành `custom toCaptcha`, dán API key từ CapMonster Cloud, và thiết lập endpoint là `api.capmonster.cloud` trên cổng `80` (xóa/domain `example.com`). Tất cả các checkbox keep alive và emulate capture service cũng cần được kích hoạt.
- **Hỏi:** Hệ thống phân loại tài khoản AWS thành Hits hay Customs như thế nào?
  - **Đáp:** Sau khi giải CAPTCHA, tài khoản có MFA, suspended hoặc expired sẽ được chuyển vào Customs với nhãn "Security Concerns". Chỉ tài khoản cho phép login trực tiếp vào AWS Portal kèm balance và danh sách dịch vụ (EC2, LightSail, v.v.) sẽ xuất hiện trong Hits.