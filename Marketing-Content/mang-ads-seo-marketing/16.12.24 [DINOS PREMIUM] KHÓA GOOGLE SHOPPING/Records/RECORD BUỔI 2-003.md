---
title: "Hướng dẫn cấu hình và tối ưu Google Shopping/Merchant Center - Record Buổi 2-003"
course: "mang-ads-seo-marketing"
module: "16.12.24 [DINOS PREMIUM] KHÓA GOOGLE SHOPPING/Records"
instructor: "Anh Tùng"
difficulty: "Nâng cao"
tags:
  - Google Shopping
  - Google Merchant Center
  - Tối ưu hóa chiến dịch
  - Chính sách trả hàng
  - Cấu hình sản phẩm
  - Bidding strategy
summary: "Trình bày quy trình thiết lập Google Shopping từ khai báo doanh nghiệp, thống nhất địa chỉ/điện thoại/email, đến chiến lược bidding CPC, tracking chuyển đổi và tối ưu hóa theo từng sản phẩm/khối sản phẩm để đảm duyệt và hiệu quả tối đa."
---

# RECORD BUỔI 2-003: Hướng dẫn cấu hình và tối ưu Google Shopping/Merchant Center

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Google Shopping đòi hỏi khai báo đầy đủ và đồng nhất thông tin doanh nghiệp (công ty/hộ kinh doanh), địa chỉ, điện thoại, email và chính sách trả hàng để duyệt tài khoản.
- Cấu hình bidding CPC phải tùy ngành hàng (mỹ phẩm ~900đ, thực phẩm chức năng 700-1200đ) và tối ưu theo từng khối sản phẩm, không chạy Maximize Conversion trước khi đạt 100 đơn chuyển đổi.
- Tracking chuyển đổi và giá trị đơn hàng là then chốt; cần thống nhất dữ liệu kỹ thuật (Google Tag/Plugin mua nhanh) và nội dung trang web để Google tin tưởng và ưu tiên hiển thị.

## 📖 Nội Dung Chi Tiết
### 1. Khai báo doanh nghiệp & Điều kiện duyệt Google Shopping
- **Loại doanh nghiệp:** Phải khai báo rõ ràng là `Công ty trách nhiệm hữu hạn`, `Hộ kinh doanh` hoặc `Cá nhân`. Không được khai báo lẫn lộn giữa công ty và hộ kinh doanh trong cùng một tài khoản Shopping.
- **Thông tin đồng nhất:** Địa chỉ, số điện thoại, email trên mọi trang (web, GMC, GAD) phải khớp chính xác. Không được để dấu chấm, viết tắt hoặc số khác nhau (ví dụ: ghi số 7 ở một nơi, số 9 ở nơi khác) vì thằng Google sẽ không hiểu và đánh vào chính sách.
- **Chính sách trả hàng:** Bắt buộc khai báo tại GMC. Nếu thiếu hoặc không rõ quy trình trả/hủy, Google sẽ từ chối duyệt. Nội dung chính sách phải phù hợp với loại sản phẩm (mỹ phẩm, thực phẩm chức năng, gia dụng...).
- **Giới thiệu cửa hàng:** Phải có phần giới thiệu chuyên nghiệp, rõ mục đích bán hàng, có thông tin liên hệ, chứng minh niềm tin (không được sơ sài, thiếu nội dung dưới cùng).

> **Ví dụ / Case Study:** Instructor đã chạy Google Shopping suốt 5 năm không bị lỗ, doanh thu hàng tháng ổn định (từ vài chục triệu lên 96 triệu trong thời gian test). Vấn đề chính khi mở thị trường Thái Lan/Indo là khó thuê sim nước ngoài tại Việt Nam, cần nền tảng Việt Nam vững chắc trước. Các lỗi thường gặp dẫn đến từ chối: thông tin không đồng nhất, thiếu chính sách trả hàng, trang web trình bày sơ sài → giải pháp: thống nhất dữ liệu, viết lại trang chính sách, khai báo loại doanh nghiệp phù hợp.

### 2. Cấu hình chiến dịch & Chiến lược Bidding (CPC)
- **Hai loại chiến dịch chính:** 
  - *Chuẩn (Standard):* Khuyến nghị ban đầu, an toàn, phù hợp khi chưa đạt ngưỡng chuyển đổi.
  - *Tối đa hóa hiệu suất (Maximize Conversion):* Chỉ chạy sau khi tài khoản có khoảng 100 chuyển đổi thành công. Trước đó, giữ Standard để kiểm soát chi phí.
- **Mức CPC tối ưu theo ngành:**
  - Mỹ phẩm: ~900 VNĐ/cước (ưu tiên lợi nhuận cao).
  - Thực phẩm chức năng: 700-1200 VNĐ tùy mục tiêu (900đ cho cân bằng, 1200đ để tăng doanh số).
  - Gia dụng, thực phẩm khác: ~700 VNĐ.
- **Tối ưu theo khối sản phẩm:** Không dùng CPC chung cho toàn bộ sản phẩm. Phân loại sản phẩm, tăng CPC thủ công cho sản phẩm "bán chạy" (ví dụ: đồng hồ lút CPC 312đ nhưng muốn tăng lượng khách, nên tăng lên), giảm hoặc loại trừ sản phẩm có lợi nhuận thấp.
- **Loại trừ thiết bị:** Đối với Shopping, máy tính và máy tính bảng thường có tỷ lệ chuyển đổi "rác". Khuyến nghị loại trừ hoặc giảm hệ số bài toán (reduce bid modifier) cho các thiết bị này nếu chi phí cao nhưng đơn thấp.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Tôi cần khai báo loại doanh nghiệp nào cho Google Shopping?
  - **Đáp:** Phải khớp với giấy phép đăng ký. Thông thường nên khai báo `Công ty trách nhiệm hữu hạn` hoặc `Hộ kinh doanh` tùy loại đăng ký, nhưng tất cả thông tin (địa chỉ, điện thoại, email) phải đồng nhất với trang web và các tài khoản liên quan.
- **Hỏi:** CPC tối ưu cho sản phẩm của tôi là gì?
  - **Đáp:** Phải tùy ngành hàng. Ví dụ: Mỹ phẩm nên đặt CPC khoảng 900 VNĐ nếu mục tiêu lợi nhuận cao, 1.200 VNĐ nếu muốn tăng doanh số. Thực phẩm chức năng từ 700-1200 VNĐ. CPC cũng cần điều chỉnh theo từng khối sản phẩm có hiệu suất khác nhau.
- **Hỏi:** Tôi nên chạy chiến dịch Maximize Conversion ngay khi tạo tài khoản không?
  - **Đáp:** Không. Chỉ nên chuyển sang Maximize Conversion khi tài khoản đã có khoảng 100 chuyển đổi thành công. Trước đó, dùng chiến dịch Chuẩn để kiểm soát chi phí và thu thập dữ liệu chính xác.