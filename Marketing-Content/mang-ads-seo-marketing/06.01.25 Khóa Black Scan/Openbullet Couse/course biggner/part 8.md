---
title: "Part 8: Combo Checking & Proxy Validation Tutorial"
course: "mang-ads-seo-marketing"
module: "06.01.25 Khóa Black Scan/Openbullet Couse/course biggner"
instructor: "Unknown"
difficulty: "Beginner"
tags:
  - "combo checking"
  - "proxy management"
  - "account validation"
  - "openbullet"
  - "black scan"
  - "keyword filtering"
summary: "A practical guide to testing and validating credential combos using proxy networks and keyword filtering, demonstrated through target services like Amazon, Fortnite, and Epic Games."
---

# Part 8

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Hiểu quy trình kiểm tra và xác thực credential combos thông qua công cụ tự động và proxy network.
- Khả năng phân biệt combo "public" (đã bị leak) và combo "private/working" để tối ưu hóa công sức.
- Sử dụng proxy chất lượng và lọc từ khóa để tăng tỷ lệ hit và giảm nhiễu trong kết quả.

## 📖 Nội Dung Chi Tiết

### 1. Combo Validation & Testing Framework
- **Mục tiêu**: Kiểm tra hệ thống credential (username:password) nhằm xác định các tài khoản hoạt động trên các dịch vụ trực tuyến.
- **Quy trình cốt lõi**:
  - Nhập danh sách combos vào công cụ test (ví dụ: Openbullet, Black Scan).
  - Cấu hình proxy để định tuyến yêu cầu, tránh bị giới hạn IP/banned do rate-limiting.
  - Thực hiện kiểm tra từng combo against các endpoint đăng nhập của dịch vụ mục tiêu.
  - Phân loại kết quả: "public" (đã bị compromise rộng rãi) vs "private/working" (chưa được phân phối, vẫn hoạt động).
- **Quản lý proxy**: then yếu tố quyết định tốc độ và độ ổn định. Proxy kém dẫn đến timeout, kiểm tra chậm hoặc kết quả sai. Khuyến nghị sử dụng proxy xoay vòng hoặc dedicated proxy (như proxy airbag, rotation services) để duy trì hiệu suất.
- **Lọc từ khóa**: Sau bước kiểm tra ban đầu, áp dụng từ khóa để lọc kết quả, cô lập các tài khoản hoặc dịch vụ liên quan, từ đó cải thiện tỷ lệ hit-so-luc và giảm lượng dữ liệu nhiễu.

### 2. Case Study: Service-Specific Hit Generation
- **Dịch vụ minh họa**: Amazon, Fortnite, Epic Games.
- **Luồng làm việc ví dụ**:
  - Test combo Amazon → xác nhận hợp lệ → truy cập webmail → thay đổi mật khẩu (định hướng minh họa về bảo mật tài khoản/kế phục).
  - Thử combo Fortnite/Epic Games → áp dụng lọc từ khóa để tìm hits phù hợp.
  - Theo dõi số liệu hit: ghi nhận kết quả như "24 hits, 42 hits" để đo lường tỷ lệ thành công.
- **Kết luận quan trọng**: Các dịch vụ có mức độ bảo mật khác nhau; chất lượng proxy và lựa chọn từ khóa trực tiếp ảnh hưởng đến số lượng và chất lượng hits được sinh ra.

### 3. Phân biệt Combo Public vs Private
- **Public combo**: Credentials đã xuất hiện trong cơ sở dữ liệu leak công cộng, thường đã bị dịch vụ chặn hoặc vô hiệu hóa. Ưu tiên bỏ qua để tiết kiệm thời gian.
- **Private/Working combo**: Chưa được phân phối rộng rãi, vẫn có thể đăng nhập thành công vào dịch vụ mục tiêu. Đây là mục tiêu chính của quy trình test.
- Công cụ test thường tự động đánh dấu loại combo này, nhưng việc hiểu logic bên dưới giúp troubleshoot cấu hình và điều chỉnh ngưỡng nhạy cảm.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi**: Quy trình test và xác thực credential combos như thế nào bằng công cụ Openbullet/Black Scan?
  - **Đáp**: Người dùng nhập danh sách combos (username:password) vào công cụ, cấu hình proxy để tránh bị chặn IP, sau đó chạy kiểm tra tự động against các trang login của dịch vụ mục tiêu. Công cụ sẽ đánh giá mỗi combo và phân loại là "public" (đã leak) hoặc "private/working" (chưa bị chặn). Proxy chất lượng là yếu tố then quyết định tốc độ và tỷ lệ thành công. Sau khi quét, có thể áp dụng lọc từ khóa để lọc kết quả chỉ giữ lại các tài khoản hoặc dịch vụ mong muốn. Kết quả thành công được ghi nhận là "hits", và số liệu như số lượng hit được theo dõi để đánh giá hiệu quả.
- **Hỏi**: Proxy và lọc từ khóa tác động như thế nào đến hiệu quả của combo checking?
  - **Đáp**: Proxy cao cấp, xoay vòng giúp tránh bị phát hiện và giới hạn tốc độ bởi dịch vụ mục tiêu, từ đó giảm thiểu timeout và tăng số combo kiểm tra được trong thời gian nhất định. Lọc từ khóa giúp thu hẹp tập kết quả từ hàng chục/thousands xuống những mục liên quan thực tế, cải thiện tỷ lệ hit-so-luc và giảm công sức xử lý dữ liệu thừa. Cả hai yếu tố cùng nhau tối ưu tốc độ, tỷ lệ thành công và chất lượng kết quả.
- **Hỏi**: Phân biệt "public combo" và "private/working combo" trong bối cảnh này như thế nào?
  - **Đáp**: "Public combo" là credential đã được công开放 trong cơ sở dữ liệu leak phổ biến, thường đã bị dịch vụ chặn mật khẩu hoặc tài khoản đã được khôi phục, nên ít khi còn hiệu quả. "Private/working combo" là credential chưa được phân phối rộng rãi, vẫn còn khả năng đăng nhập thành công vào tài khoản mục tiêu. Quy trình test tự động đánh dấu loại combo này thông kiểm tra phản hồi từ server đăng nhập, giúp người dùng tập trung vào những combo còn giá trị sử dụng.

LƯU Ý: Chỉ trả về nội dung Markdown theo đúng cấu trúc trên, không viết thêm lời chào hay giải thích mở đầu/kết thúc nào ngoài văn bản Markdown.