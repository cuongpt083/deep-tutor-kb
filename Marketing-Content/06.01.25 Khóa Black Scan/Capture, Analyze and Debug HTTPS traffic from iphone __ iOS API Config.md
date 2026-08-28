---
title: "Capture, Analyze and Debug HTTPS traffic from iPhone - iOS API Config"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan"
instructor: "Unknown"
difficulty: "Intermediate"
tags:
  - "Burp Suite"
  - "iOS HTTPS Interception"
  - "Proxy Configuration"
  - "API Debugging"
  - "Burp Suite Community Edition"
  - "Device ID Generation"
summary: "Step-by-step technical guide to intercept and debug HTTPS traffic from an iOS device using Burp Suite Community Edition, including proxy setup, CA certificate installation, device ID generation, and API parameter capture for configuration."
---

# Capture, Analyze and Debug HTTPS traffic from iPhone - iOS API Config

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Configure iOS WiFi proxy to redirect traffic to Burp Suite using local IPv4 address and port 8081
- Install Burp CA certificate on iOS to enable HTTPS interception and trust valid certificates
- Use Burp Suite's Random String block to generate device ID patterns matching the target app's format (8 chars + hyphen + 12 chars)
- Capture and configure key API fields: device ID, authentication tokens, subscription status, expiry dates, and login credentials
- Set up success/failure key checks based on response keywords ("bad credentials", "valid true") to validate config integrity
- Test final configuration with proxy services (e.g., IPVanish) to verify bot status and captured data output

## 📖 Nội Dung Chi Tiết

### 1. Preparation & Proxy Configuration
- Retrieve the local IPv4 address via `ipconfig` on PC (e.g., 192.168.100.2)
- On the iOS device, navigate to Wi-Fi settings, select "Configure Proxy" → "Manual", and enter the PC's IPv4 address and port **8081**
- Download **Burp Suite Community Edition** (free) from the browser; sufficient for this configuration workflow
- Create a new **temporary project** in Burp and click **Start**; select "All Interfaces" and enable "HTP History"

### 2. Traffic Generation & Certificate Installation
- On the iPhone, visit any website to generate outbound HTTP/HTTPS traffic
- A Burp CA Certificate prompt will appear; click to download and install the profile via the downloaded configuration
- Go to iOS Settings → confirm the profile is installed; this trusts Burp's intercepted certificates

### 3. Burp Suite Configuration & Device ID Generation
- Log in to the target app (e.g., "Calm, Sleep and Medication") on iPhone to trigger API requests
- In Burp, use the **"Random String"** block to generate a device ID pattern: 
  - Generate 8 alphanumeric characters, add a hyphen, then 12 alphanumeric characters (e.g., `fg2468-[12-char string]`)
  - Adjust character counts based on the app's expected format observed in request headers
- Copy the generated device ID from the request headers in Burp's HTP History
- Create a **POST** method for the login/API endpoint
- Set **Content-Type** to `application/json`
- Configure **Custom Headers**:
  - `User-Agent`: iPhone iOS 14.8.8 (or current device version)
  - `PSS`: [relevant field value from app headers]
  - `Device ID`: [copied device ID value]

### 4. Data Capture & Logic Checks
- **Failure Key Check**: Set to detect `"bad credentials"` in response → triggers bot status **Fail**
- **Success Key Check**: Set to detect `"valid true"` / `"premium custom"` → triggers bot status **Success**
- **Field Captures** (via Parse/Extract blocks):
  - `device ID` / `token`: Use JSON Parse mode; set "Do not capture token length" to avoid excessive data
  - `name`: Enable capture; example value "Howard"
  - `email`: Enable capture; extract from login response
  - `subscription plan`: Set to "premium custom"; use "Left/Right String" mode to extract expiry year/month/date (select starting from "T" capital delimiter)
  - `auto renewal`: Capture boolean value; expected `false` for non-recurring accounts
- **Logic Conditions**: 
  - Use "Does not contain" condition set to word "subscription" to auto-set account tier to "custom" / "free"
  - Set `Valid true` / `Cancel true` flags to distinguish account status

### 5. Final Configuration & Testing
- Save configuration with **100 bots** limit (adjustable)
- Add additional information fields: proxy source (e.g., IPVanish), CPM settings if applicable
- Click **Save**; then **Start** to test the config
- Expected output: **Bot Status Success** with captured fields:
  - Name (e.g., "Howard")
  - Plan (premium custom)
  - Auto renewal (false)
  - Expiry date (year/month/date)
  - Config username (e.g., "yashviergaming")
- Tested and verified working with **IPVanish Free Proxies**; guarantees over 1000 CPM when configured correctly

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cách cấu hình proxy iOS để bắt traffic HTTPS qua Burp Suite như thế nào?
  - **Đáp:** Vào Settings > Wi-Fi, chọn Configure Proxy → Manual, nhập IPv4 của PC và cổng 8081. Tải Burp Suite Community Edition lên PC, tạo project tạm và Start. Trên iPhone truy cập website để tạo traffic, sau đó cài CA Certificate từ Burp.
- **Hỏi:** Pattern tạo device ID trên Burp Random String block là như thế nào?
  - **Đáp:** Tạo 8 ký tự alphanumeric, thêm dấu gạch ngang, sau đó 12 ký tự alphanumeric (ví dụ: fg2468-abcdef123456). Điều chỉnh dựa trên format headers của app mục tiêu.
- **Hỏi:** Làm sao để kiểm tra config thành công (Bot Status Success)?
  - **Đáp:** Cấu hình key checks để bắt từ "valid true" / "premium custom" trong response; bắt device ID, token, name, subscription plan và expiry date qua Parse blocks; lưu config và Start. Kết quả xuất name, plan premium, auto renewal false, expiry date và username config.
- **Hỏi:** Fields bắt buộc cần capture để config hoạt động đúng?
  - **Đáp:** Device ID, token, name, subscription plan, auto renewal status, expiry date. Bắt buộc phải có logic check "bad credentials" để phát hiện fail, và "valid true" để xác nhận success.
- **Hỏi:** Config có thể test với proxy miễn phí không? Proxy nào khuyên dùng?
  - **Đáp:** Có, config hoạt động với IPVanish Free Proxies. Nên thêm thông tin proxy nguồn trong additional options để theo dõi CPM và hiệu suất.