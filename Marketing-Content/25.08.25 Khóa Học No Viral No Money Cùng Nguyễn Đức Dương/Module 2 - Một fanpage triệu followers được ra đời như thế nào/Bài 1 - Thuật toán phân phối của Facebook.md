---
title: "Thuật toán phân phối của Facebook - Bài 1"
course: "content-inputs"
module: "mang-content/25.08.25 Khóa Học No Viral No Money Cùng Nguyễn Đức Dương/Module 2 - Một fanpage triệu followers được ra đời như thế nào"
instructor: "Nguyễn Đức Dương"
difficulty: "Trung cấp"
tags:
  - "Facebook Algorithm"
  - "Thuật toán Phân Ph phối"
  - "Fanpage Growth"
  - "Content Strategy"
  - "Digital Marketing"
summary: "Bài giảng giải thích chi tiết quy trình phân phối nội dung của Facebook dựa trên 4 bước lặp đi lặp lại (Kho tin bài, Tín hiệu, Dự đoán, Đánh giá điểm). Bao gồm các yếu tố then chốt như trạng thái tài khoản, thời điểm đăng, định dạng nội dung và tương tác tự nhiên để tối ưu hóa reach."
---

# Thuật toán phân phối của Facebook

## 💡 Tóm Tắt Cốt Lõi
- Facebook phân phối nội dung qua 4 bước lặp lại: Kho tin bài → Tín hiệu → Dự đoán tương tác → Đánh giá điểm phân phối.
- Trạng thái tài khoản admin/editor phải sạch (không vi phạm chính sách) để tránh giảm tương tác.
- Thời điểm đăng bài ảnh hưởng lớn đến độ ưu tiên ban đầu do hành vi hoạt động của người dùng.
- Định dạng nội dung (ảnh + văn bản) hiện tại được Facebook ưu tiên hơn định dạng status đơn thuần tại thị trường Việt Nam.
- Tương tác tự nhiên (seeding) cần thiết để tạo điểm cao ban đầu; không có tương tác ban đầu sẽ khiến phân phối dừng lại hoặc giảm sút.
- Thuật toán không hoạt động như tích lũy view đơn thuần, mà là vòng lặp đánh giá và phân phối lại theo thời gian.

## 📖 Nội Dung Chi Tiết
### 1. Hiểu Nền Tảng Phân Phối Facebook

**1.1 Kho Tin Bài (Content Database)**
- Mọi nội dung đăng lên Facebook đều được lưu trữ trong cơ sở dữ liệu tập trung (kho tin bài) của nền tảng.
- Khi một bài đăng mới xuất hiện, Facebook sẽ quét bài so với DB để判断: bài mới hay đã từng xuất hiện (tái sử dụng/recycled)?; bài có tương tác (react) từ ban đầu hay không?
- Kết quả quét này là nền tảng cho các bước đánh giá sau.

**1.2 Tín Hiệu Tài Khoản (Account Signals)**
- Facebook đánh giá trạng thái của tài khoản quản trị viên (admin) và biên tập viên của Fanpage.
- Yêu cầu: Tài khoản phải hoàn toàn sạch, chưa từng vi phạm chính sách cộng đồng hoặc chính sách quảng cáo.
- Nếu tài khoản có lệnh hạn chế hoặc vi phạm, bài đăng sẽ bị "bóp rút" (reduced distribution) ngay từ bước đầu.

**1.3 Thời Điểm Đăng (Posting Timing)**
- Facebook ưu tiên phân phối cho bài đăng được đăng vào những khung giờ mà đại đa số người dùng đang hoạt động mạnh mẽ.
- Đối với Fanpage mới lập, việc chọn thời điểm đúng giúp tăng cơ hội tiếp cận ban đầu.
- Tốc độ kết nối Internet cũng ảnh hưởng đến chất lượng tải ban đầu (720p, 1080p, 4k); tốc độ chậm có thể làm giảm trải nghiệm ban đầu.

**1.4 Dự Đoán Tương Tác (Engagement Prediction)**
- Dựa trên dữ liệu lịch sử, Facebook dự đoán khả năng người dùng sẽ tương tác (click, comment, share, dwell time) với bài viết.
- Các định dạng nội dung có lịch sử tương tác cao sẽ được ưu tiên phân phối.
- Tại thị trường Việt Nam hiện nay, định dạng **ảnh + văn bản** được ưu tiên rõ rệt hơn định dạng **status** đơn thuần. Facebook đang đẩy mạnh các dạng có ảnh và có bài viết vì được coi là thu hút quan tâm hơn.

**1.5 Đánh Giá Điểm & Vòng Lặp Phân Ph phối (Scoring & Distribution Loop)**
- Facebook tổng hợp 4 yếu tố trên để gán cho bài viết một điểm số trên thang điểm nội bộ.
- Quy trình không phải tuyến tính tích lũy view, mà là vòng lặp lặp đi lặp lại: 
  * Bước 1: Quét kho tin bài → Bước 2: Kiểm tra tín hiệu → Bước 3: Dự đoán tương tác → Bước 4: Gán điểm → Phân phối → Quay lại bước 1 với dữ liệu tương tác mới.
- Nếu bài viết nhận được điểm cao, Facebook sẽ tiếp tục phân phối rộng hơn và đề xuất cho nhiều người dùng khác.

**1.6 Tương Tác Tự Nhiên & Seeding**
- Để bài viết có điểm ban đầu cao, cần có tương tác tự nhiên ban đầu.
- Cách thực hiện: Nhờ bạn bè, người thân tham gia seeding (like, comment, share chân thực) hoặc các phương pháp xây dựng tương tác hợp pháp ban đầu.
- Nếu thiếu tương tác tự nhiên, thuật toán sẽ đánh giá điểm thấp và phân phối hạn chế.

**1.7 Định Dạng Nội Dung Ưu Tiên**
- Facebook đang ưu tiên các dạng nội dung có yếu tố hình ảnh kèm theo văn bản có cấu trúc.
- Các dạng thuần text (status) có tương tác cao trong một thời段, nhưng đang bị ưu tiên thấp hơn so với định dạng kết hợp ảnh/văn bản tại giai đoạn hiện tại.

### 2. Các Bước Tiếp Theo Cấu Trúc 8 Bước Xây Fanpage (Tóm Lược)
- Bước 2: Xác định mục tiêu (xem bài 6 Module 1).
- Bước 3: Phân tích đối thủ và kênh liên quan.
- Bước 4: Phân tích nguồn lực nội lực cá nhân/team (điểm mạnh, điểm yếu, lợi thế độc điệu).
- Bước 5: Phân tích chân dung khách hàng mục tiêu (bài 2 Module 1).
- Bước 6: Xác định định vị thương hiệu (Unique Selling Point/Điểm bán hàng độc nhất) - chắc chắn là điểm khác biệt tuyệt đối mà đối thủ không có.
- Bước 7: Chọn chủ đề và định dạng nội dung phù hợp để theo dõi/follow.
- Bước 8: Đo lường hiệu quả và điều chỉnh chiến lược.

> **Ví dụ Minh Họa:** Giả sử một Fanpage mới về du lịch. Nếu admin tài khoản có lịch sử vi phạm chính sách, bài đăng đầu tiên sẽ bị giới hạn reach dù nội dung tốt. Ngược lại, nếu tài khoản sạch, đăng bài vào khung giờ cao điểm (ví dụ 19h-22h), kèm theo hình ảnh đẹp và kèm seeding như-minded người dùng, bài viết sẽ nhận điểm cao, Facebook sẽ phân phối rộng và liên tục tái đánh giá để mở rộng audience.

❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Facebook phân phối nội dung như thế nào qua các bước nào?
  - **Đáp:** Facebook thực hiện 4 bước lặp lại: (1) Kiểm tra kho tin bài (đăng mới hay tái sử dụng), (2) Đọc tín hiệu tài khoản (trạng thái vi phạm, sạch sẽ), (3) Dự đoán khả năng tương tác dựa trên định dạng nội dung, (4) Gán điểm số và quyết định phân phối. Quy trình này lặp đi lặp lại, không phải tích lũy view đơn thuần.
- **Hỏi:** Tại sao tài khoản quản trị Fanpage cần phải "sạch" (không vi phạm)?
  - **Đáp:** Nếu tài khoản admin/editor có vi phạm hoặc lệnh hạn chế từ Facebook, thuật toán sẽ tự động giảm tương tác (reduced distribution) cho mọi bài đăng của Fanpage đó, khiến reach ban đầu và dài hạn bị ảnh hưởng nghiêm trọng.
- **Hỏi:** Định dạng nội dung nào được Facebook ưu tiên hiện nay tại Việt Nam?
  - **Đáp:** Định dạng **ảnh + văn bản** được ưu tiên cao hơn định dạng **status** đơn thuần. Facebook đang thiên về các nội dung có yếu tố hình ảnh vì được coi có khả năng giữ chân và tương tác cao hơn trên thị trường Việt Nam.
- **Hỏi:** Làm sao để bài viết mới của Fanpage có reach ban đầu tốt?
  - **Đáp:** Cần đảm bảo tài khoản quản trị sạch, đăng bài vào khung giờ người dùng hoạt động nhiều, sử dụng định dạng ảnh + văn bản, và tạo tương tác tự nhiên ban đầu (seeding) qua like, comment, share chân thực để thuật toán gán điểm cao và bắt đầu phân phối rộng.