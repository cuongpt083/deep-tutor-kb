---
title: "Bài 24 Backlink DoFollow và NoFollow là gì và cách ứng dụng"
course: "content-inputs"
module: "mang-content/20.11.23 Đào tạo kỹ năng Content viết bài website từ A-Z"
instructor: "Không rõ"
difficulty: "Trung cấp"
tags:
  - "backlink"
  - "dofollow"
  - "nofollow"
  - "seo"
  - "content-writing"
summary: "Giải thích khái niệm DoFollow và NoFollow, tác động đến SEO, và cách ứng dụng chiến lược liên kết trong nội dung website theo cấu trúc pillar content."
---

# Bài 24 Backlink DoFollow và NoFollow là gì và cách ứng dụng

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- **DoFollow** là loại link truyền "sức mạnh" (link juice) và uy tín từ website đang chiếu ra đến website đích; essentially một lời khẳng định hoặc quảng bá.
- **NoFollow** là loại link báo cho Google rằng: "Tôi biết đối tượng này nhưng không lấy y tín của mình để đảm bảo cho họ"; dùng cho việc trích dẫn, tham khảo mà không muốn ảnh hưởng đến autoritay của trang chủ.
- **Tác động SEO:** Việc quá nhiều link DoFollow ra ngoài mà không kiểm soát có thể khiến website mất sức mạnh dần theo thời gian (thường 1-2 tháng với lượng link nhiều). NoFollow giúp giữ lại sức mạnh cho domain của bạn.
- **Cấu trúc Pillar Content:** Trong hệ thống bài viết pillar - sub, bài chính nên gắn NoFollow khi trỏ về bài con, còn bài con nên gắn DoFollow khi trỏ về bài chính. Điều này tạo luồng liên kết合理化 và bảo vệ autoritay của trang chính.
- **Cách thực hành:** Thêm thuộc tính `rel="nofollow"` vào thẻ `<a>` hoặc sử dụng công cụ/plugin SEO để đánh dấu nhanh. Ví dụ: `<a href="url" rel="nofollow">Anchor Text</a>`.

## 📖 Nội Dung Chi Tiết
### 1. Khái niệm DoFollow và NoFollow
- **DoFollow:** Khi bạn gắn link cho người khác trong bài viết của mình, bạn đang "quảng cáo" họ và đang lấy danh dự/y tín của mình để đảm bảo cho họ. Điều này truyền sức mạnh (SEO juice) đến đối phương.
- **NoFollow:** Chỉ là việc đưa ra người tham khảo. Bạn đã từng biết người đó, có thể nhận diện giá trị, nhưng bạn không cam kết hay lấy y tín của mình để bảo证他们. Google sẽ không tính link này vào đánh giá autoritay của trang bạn.

### 2. Khi nào nên dùng NoFollow?
- Khi trích dẫn các nguồn uy tín như báo chí lớn (VnExpress, Kênh 14, ...): Dùng NoFollow để không "bơm" sức mạnh của website ra ngoài.
- Khi đưa link đến trang user-generated, comment, hoặc các liên kết không kiểm soát hoàn toàn.
- Trong cấu trúc nội nội bộ theo mô hình pillar-content: Trang chính → Trang con nên là NoFollow.

### 3. Cấu trúc liên kết合理 hóa cho Website
- **Bài con → Bài chính:** Sử dụng DoFollow. Điều này giúp truyền lên uy tín và cấu trúc cho bài main biết có các nội dung liên quan tốt.
- **Bài chính → Bài con:** Sử dụng NoFollow. Giúp Google hiểu rằng bài main là "bài chủ chốt" (main content), còn các bài con là nội dung phụ, hỗ trợ.
- **Trong cùng một nhóm bài con:** Có thể dùng DoFollow để lồng ghép nội liên giữa các bài con, tạo mạng lưới liên kết nội bộ mạnh mẽ.

### 4. Cách thêm thuộc tính NoFollow
Cách thủ công trong HTML:
```html
<a href="https://example.com" rel="nofollow">Anchor Text</a>
```
Trong các trình soạn thảo nội dung (CMS như WordPress, Notion, v.v.) hoặc plugin SEO, thường có dropdown hoặc ô nhập thuộc tính `rel` – chọn `nofollow`. Một số extension như Cellquake có thể giúp bạn highlight và kiểm tra xem link đang là nofollow hay dofollow.

### 5. Lời khuyên và Lỗi cần tránh
- Không nên xóa hoàn toàn mọi link DoFollow – chúng cần thiết cho nội liên và uy tín ban đầu.
- Nếu bài viết độc lập và chỉ chứa các backlink dẫn chứng từ báo chí, 100% nên đặt là NoFollow để bảo vệ autoritay của trang.
- Cân bằng: Sử dụng NoFollow cho outbound link đến nguồn bên ngoài, giữ DoFollow cho liên kết nội bộ có ý nghĩa và cấu trúc合理.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** DoFollow và NoFollow khác nhau như thế nào về tác động đến SEO?
  - **Đáp:** DoFollow truyền "sức mạnh" (link juice) và uy tín từ website chiếu ra đến đích, giúp cải thiện ranking cho trang đích. NoFollow báo cho Google không theo dõi/link juice chuyển đi, dùng cho trích dẫn hoặc liên kết không muốn ảnh hưởng đến autoritay của trang chủ.
- **Hỏi:** Khi nào nên sử dụng NoFollow cho các link ngoài trang web của mình?
  - **Đáp:** Nên dùng NoFollow khi trích dẫn báo chí, nguồn tin, hoặc bất kỳ nội dung nào bạn muốn tham khảo nhưng không cam kết y tín cho nó. Trong cấu trúc pillar content, liên kết từ bài chính về bài con cũng nên là NoFollow.
- **Hỏi:** Cách cấu trúc liên kết giữa bài chính (pillar) và bài con (sub) như thế nào để tối ưu SEO?
  - **Đáp:** Bài con nên gắn DoFollow khi trỏ về bài chính để truyền lên uy tín. Bài chính nên gắn NoFollow khi trỏ về bài con, giúp Google phân biệt bài main là nội dung gốc và bài con là nội dung hỗ trợ/phụ.
- **Hỏi:** Cách kỹ thuật để thêm thuộc tính NoFollow vào link là gì?
  - **Đáp:** Trong mã HTML, thêm `rel="nofollow"` vào thẻ `<a>`. Hoặc sử dụng các tính năng trong plugin SEO / trình soạn thảo nội dung để đánh dấu thuộc tính này mà không cần sửa code trực tiếp.