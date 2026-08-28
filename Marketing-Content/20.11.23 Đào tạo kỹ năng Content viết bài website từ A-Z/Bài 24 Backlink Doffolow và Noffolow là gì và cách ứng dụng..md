---
title: "Backlink DoFollow và NoFollow là gì và cách ứng dụng"
course: "20.11.23 Đào tạo kỹ năng Content viết bài website từ A-Z"
module: ""
instructor: "Không rõ"
difficulty: "Trung cấp"
tags:
  - "SEO"
  - "Backlink"
  - "DoFollow"
  - "NoFollow"
  - "Link Building"
summary: "Bài giảng giải thích khái niệm DoFollow và NoFollow, lý do cần xóa hoặc gắn NoFollow cho liên kết ngoài để bảo vệ sức mạnh website, và hướng dẫn cách thực hiện cùng chiến lược liên kết合理."
---

# Bài 24 Backlink DoFollow và NoFollow là gì và cách ứng dụng

## 💡 Tóm Tắt Cốt Lõi
- **DoFollow** là loại backlink mặc định truyền quyền uy tín và "sức mạnh" (PageRank) từ website đưa ra đến website nhận, tương tự như một lời khẳng định về tính chuyên môn của đối phương.
- **NoFollow** là thuộc tính cho phép ghi nhận hoặc trích dẫn nguồn mà không truyền quyền uy tín, giúp bảo vệ cấu trúc SEO và ngăn chặn "bơm" authority ra ngoài.
- Việc xóa link hoặc gắn NoFollow cho liên kết ngoài là cần thiết để duy trì sức mạnh của website, đặc biệt khi bài viết chứa nhiều nguồn tham khảo hoặc liên kết ngoài.

## 📖 Nội Dung Chi Tiết
### 1. Khái niệm DoFollow và NoFollow
- **DoFollow:** 
  - Mặc định mọi liên kết HTML đều là DoFollow nếu không có thuộc tính `rel="nofollow"`.
  - Khi gắn DoFollow, bạn đang truyền "tín hiệu uy tín" cho website liên kết, giúp cải thiện thứ hạng của đối phương.
  - Phù hợp khi bạn muốn khẳng định hoặc推荐 một nguồn tin cậy, chuyên gia hoặc đối tác.
- **NoFollow:** 
  - Thêm thuộc tính `rel="nofollow"` vào thẻ `<a>` (ví dụ: `<a href="url" rel="nofollow">Text</a>`).
  - Biểu thị ý nghĩa: "Tôi biết đến nguồn này nhưng không khẳng định uy tín hoặc không muốn truyền authority".
  - Dùng cho liên kết ngoài đến báo chí, diễn đàn, comment, nội dung user-generated, hoặc các nguồn chưa được kiểm chứng chất lượng.

### 2. Lý do xóa/gắn NoFollow cho liên kết ngoài
- **Bảo vệ PageRank:** Mỗi liên kết DoFollow ra ngoài đều một phần "bơm" sức mạnh website của bạn ra bên ngoài. Nếu quá nhiều, website sẽ dần yếu đi, có thể làm giảm thứ hạng trong thời gian 1-2 tháng liên tục.
- **Chuẩn mực SEO:** Google khuyến nghị sử dụng NoFollow cho các liên kết付费, quảng cáo, hoặc nguồn không kiểm soát được chất lượng nội dung.
- **Cách xóa link nhanh:** 
  - Bôi đen toàn bộ nội dung bài viết (Ctrl+A), sau đó bấm `Shift+S` (trên Windows) để xóa link giữ lại văn bản thuần túy.
  - Hoặc thủ công: chọn từng link và xóa, hoặc sửa thuộc tính HTML trực tiếp.

### 3. Cách thêm thuộc tính NoFollow
- **Trong trình soạn thảo trực quan (WordPress Block Editor):** 
  - Gắn link như thường lệ, sau đó chuyển sang chế độ "Text" hoặc dùng plugin/tiện ích để thêm `rel="nofollow"` vào mã liên kết.
  - Một số theme/plugin có nút "Add rel nofollow" tích hợp sẵn.
- **Trong mã HTML:** 
  - Thay đổi `<a href="url">Text</a>` thành `<a href="url" rel="nofollow">Text</a>`.
- **Dùng tiện ích kiểm tra:** Các extension trình duyệt (ví dụ: Check My Links, NoFollow SEO extension) giúp xem và sửa trạng thái DoFollow/NoFollow nhanh chóng trực tiếp trên trang web.

### 4. Chiến lược liên kết nội bộ và ngoài
- **Nội bộ:** 
  - Liên kết từ bài con trỏ về bài chính: **DoFollow** (truyền authority lên cao tầng, nâng cao uy tín cho bài chính).
  - Liên kết từ bài chính trỏ về bài con: **NoFollow** (để giữ authority tại bài chính, ngăn chặn phân tán sức mạnh ra các nội dung phụ).
- **Ngoài:** 
  - Nguồn báo lớn, tin tức uy tín: Có thể dùng DoFollow nhưng cần kiểm soát chặt lượng lượng.
  - Nguồn tham khảo, diễn đàn, comment, link付费/quảng cáo: **Bắt buộc NoFollow**.
  - Nguyên tắc chung: Ít DoFollow ngoài càng tốt, ưu tiên NoFollow để giữ sức mạnh cho website chính và tuân thủ hướng dẫn của Google.

> **Ví dụ / Case Study:** 
> Giả sử một bài viết "10 cách kiếm tiền online" (bài chính) liên kết đến 3 bài con chuyên về từng phương pháp. 
> - Các bài con liên kết về bài chính dùng **DoFollow** để nâng cao uy tín cho bài chính. 
> - Bài chính liên kết về các bài con dùng **NoFollow**, Google sẽ hiểu bài chính là nguồn gốc chính, còn bài con là nội dung phụ, giúp phân phối rõ ràng authority mà không làm loãng sức mạnh cho chủ domain.

### 5. Lưu ý thực tiễn
- Không nên gắn DoFollow cho tất cả liên kết ngoài, đặc biệt là các nguồn chưa được kiểm chứng hoặc là link từ comment, forum.
- Cân bằng: Sử dụng NoFollow cho đa số liên kết ngoài, giữ lại ít DoFollow cho các nguồn chất lượng cao thực sự đáng tin cậy.
- Kiểm tra định kỳ trạng thái backlink bằng các công cụ SEO (Ahrefs, SEMrush, hoặc các extension miễn phí) để đảm bảo cấu trúc liên kết tuân theo chiến lược mục tiêu.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Làm sao để biết một liên kết là DoFollow hay NoFollow?
  - **Đáp:** Mở phần mã HTML (F12 hoặc "Xem nguồn"), tìm thẻ `<a>` và kiểm tra thuộc tính `rel`. Nếu có `rel="nofollow"` thì là NoFollow, nếu không có hoặc là `rel="dofollow"` (thường là mặc định) thì là DoFollow. Các extension trình duyệt cũng có thể hiển thị ngay trạng thái.
- **Hỏi:** Tại sao nên dùng NoFollow cho liên kết ngoài trong bài viết SEO?
  - **Đáp:** Sử dụng NoFollow giúp bảo vệ sức mạnh (PageRank) của website, ngăn chặn việc "bơm" authority ra ngoài và tuân thủ các hướng dẫn của Google đối với các nguồn không kiểm soát được hoặc là nội dung付费/quảng cáo.
- **Hỏi:** Cách xóa tất cả liên kết trong một bài viết nhanh nhất là như thế nào?
  - **Đáp:** Bôi đen toàn bộ nội dung bài viết (Ctrl+A), sau đó bấm `Shift+S` (trên Windows) hoặc dùng chức năng "Chuyển sang văn bản thuần túy" của trình soạn thảo để xóa hết link giữ lại chữ. Nếu cần sửa từng link, có thể chọn từng link và xóa hoặc sửa thuộc tính `rel`.