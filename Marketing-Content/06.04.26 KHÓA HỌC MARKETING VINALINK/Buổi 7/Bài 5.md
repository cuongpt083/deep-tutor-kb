---
title: "Hướng dẫn cấu hình và triển khai mini-game trên Vinalink - Buổi 7 - Bài 5"
course: "mang-ads-seo-marketing"
module: "Buổi 7"
instructor: "Không rõ"
difficulty: "Trung cấp"
tags:
  - "Vinalink"
  - "Marketing"
  - "Mini-game"
  - "CMS"
  - "Chuyển đổi"
  - "Lead generation"
  - "Google Sheet"
summary: "Bài học hướng dẫn cách thiết lập và cấu hình mini-game trên nền tảng Vinalink, bao gồm việc thay đổi hình ảnh, background, các thông số game (tên, ID, tốc độ), thiết lập dữ liệu qua CMS, tích hợp Google Sheet để thu thập lead, và quy trình chuyển đổi về Messenger hoặc chốt đơn."
---

# Hướng dẫn cấu hình và triển khai mini-game trên Vinalink

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Hướng dẫn từng bước cấu hình mini-game: từ tạo tài khoản, sao chép mẫu, đến chỉnh sửa hình ảnh, background và các thông số game quan trọng (tên, ID, tốc độ) trên CMS.
- Thiết lập luồng dữ liệu và thu thập lead: sử dụng Google Sheet/Form để bắt thông tin khách hàng, đồng bộ trường dữ liệu với CMS để đảm bảo tự động lưu và quản lý.
- Quy trình chuyển đổi và tích hợp Messenger: sau khi khách hàng nhập thông tin, hệ thống tự động chuyển về Messenger để lấy số điện thoại và chốt đơn, có thể kết hợp chatbot để tự động hóa.

## 📖 Nội Dung Chi Tiết

### 1. Thiết lập và sao chép mẫu mini-game
- Tạo tài khoản trên nền tảng Vinalink và sao chép mẫu minigame sẵn có.
- Truy cập vào phần cấu hình game, nhập các thông số cơ bản như tên game, Game ID và tốc độ hoạt động.
- Lưu ý: Hệ thống sẽ tự động lưu các thông số khi nhấn nút "Xếp" và "Public".

### 2. Cấu hình hình ảnh, background và thiết kế giao diện
- Thay đổi background: chọn hình ảnh thay vì màu sólid. Sử dụng trình sửa ảnh (như Photoshop) hoặc trình编辑 trực tiếp trên nền tảng để upload hình ảnh vào cấu hình wheel.
- Đặt tỷ lệ và tên sản phẩm: nhập tên game, tỷ lệ tương ứng để hiển thị đúng trên giao diện vòng quay.
- Đường dẫn hình ảnh: copy đường dẫn từ CMS sau khi tạo game, dán vào cấu hình để hệ thống hiển thị hình ảnh đúng.
- Tùy chỉnh màu sắc và phông chữ cho các phần tử như nút quay, chữ và background (ví dụ: màu da cam cho phông chữ, trắng cho chữ quay).

### 3. Thiết lập dữ liệu và tích hợp Google Sheet
- Cấu hình dữ liệu trong CMS: các trường quan trọng bao gồm tên game, ID game, game token và đường dẫn background/vòng quay.
- Tạo Google Form/Google Sheet để thu thập thông tin khách hàng (họ và tên, số điện thoại, địa chỉ, thông tin thưởng).
- Đồng bộ trường dữ liệu: trong CMS, chọn các trường tương ứng để ánh xạ với các cột trong Google Sheet.
- Giải quyết vấn đề hiển thị dữ liệu: nếu Google Sheet hiện thiếu trường, kiểm tra cấu trúc file và đảm bảo các trường tên, địa chỉ được định nghĩa đúng trong phần cấu hình form.

### 4. Quy trình chuyển đổi (Redirect) và Messenger
- Sau khi khách hàng hoàn thành game, hệ thống tự động redirect về Google Sheet hoặc trực tiếp đến Messenger.
- Luồng chuyển đổi: Khách chơi game → Nhập thông tin → Hệ thống gửi dữ liệu về Messenger → Trích xuất số điện thoại → Chốt đơn.
- Tích hợp chatbot: có thể kết hợp với chatbot để hỗ trợ tự động chăm sóc khách hàng, gửi quà hoặc dẫn đường link Zalo/website.
- Ứng dụng offline-to-online: sử dụng đường link cá nhân hóa để chuyển đổi từ tương tác offline sang online, khách nhận quà qua link hoặc Zalo.

### 5. Nguyên lý thiết kế mini-game và lưu ý kỹ thuật
- Đa dạng hóa loại game: vòng quay, ladder, bingo, cá độ cá, etc. Mỗi loại có kỹ thuật và thiết kế riêng.
- Thiết kế cho nhiều thiết bị: đảm bảo giao diện hoạt động mượt trên cả web và điện thoại di động.
- Quan trọng về dữ liệu: cấu hình đúng các thông số CMS (tên, ID, token, đường dẫn) là then chốt cho việc game chạy ổn định và lưu dữ liệu.
- Triển khai chuyển đổi: khi khách hàng tương tác với hình ảnh hoặc link, hệ thống sẽ đẩy ra game trên điện thoại, sau đó có thể chuyển về Messenger để chốt đơn.

### 6. Cập nhật tương lai và hỗ trợ
- Nền tảng đang phát triển thêm các loại game cho livestream (vòng quay, ô chữ may mắn,...) sẽ cập nhật trong 3 tuần tới.
- Trong thời gian chờ, người học có thể tự chủ động làm theo hướng dẫn hoặc liên hệ hỗ trợ 1-1 (TeamViewer) để giải quyết kỹ thuật.
- Cảm ơn các học viên và khuyến khích chủ động thực hành hoặc thuê dịch vụ nếu cần.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Cách cấu hình mini-game và tích hợp Google Sheet để thu thập lead trên Vinalink như thế nào?
  - **Đáp:** Học viên cần tạo tài khoản, sao chép mẫu minigame, chỉnh sửa hình ảnh và background trên CMS, sau đó tạo Google Form/Sheet với các trường thông tin cần thu thập (họ tên, số điện thoại, địa chỉ). Trong phần cấu hình CMS, phải đồng bộ đúng các trường dữ liệu với các cột trong Google Sheet. Hệ thống sẽ tự động lưu và quản lý dữ liệu khách hàng sau khi chơi game.
- **Hỏi:** Quy trình chuyển đổi về Messenger và chốt đơn sau khi khách chơi mini-game là như thế nào?
  - **Đáp:** Sau khi khách hàng nhập thông tin trong game, hệ thống sẽ redirect dữ liệu về Messenger. Từ Messenger, có thể trích xuất số điện thoại và hướng dẫn khách chốt đơn. Quy trình có thể kết hợp với chatbot để tự động gửi quà, cung cấp link Zalo hoặc hỗ trợ giải đáp thắc mắc, từ đó tăng tỷ lệ chuyển đổi về đơn hàng.
- **Hỏi:** Các kỹ thuật thiết kế và lưu ý quan trọng khi tạo mini-game cho cả web và điện thoại là gì?
  - **Đáp:** Phải đảm bảo giao diện responsive hoạt động mượt trên cả hai thiết bị web và di động. Cần chú ý đến các thông số quan trọng trong CMS như tên game, ID game, game token và đường dẫn background/vòng quay. Ngoài ra, nên kiểm tra kỹ đường dẫn hình ảnh và cấu hình dữ liệu để tránh tình trạng không hiển thị hoặc mất dữ liệu. Nếu gặp khó khăn, có thể yêu cầu hỗ trợ 1-1 qua TeamViewer hoặc chờ cập nhật các loại game mới cho livestream trong thời gian tới.