---
title: "Buổi 2 - Ứng dụng AI để nghiên cứu thị trường và phân tích khách hàng"
course: "mang-ads-seo-marketing"
module: "09.03.26 Khóa Học AI For Marketing - MindX/Bài giảng"
instructor: "Văn"
difficulty: "Trung cấp"
tags:
  - "AI Marketing"
  - "Market Research"
  - "Customer Persona"
  - "NotebookLM"
  - "Prompt Engineering"
summary: "Bài giảng hướng dẫn cách áp dụng AI để nghiên cứu thị trường và xây dựng chân deduction khách hàng. Nội dung bao gồm khái niệm Target Audience vs Persona, 3 yếu tố định nghĩa khách hàng mục tiêu, quy trình thu thập và phân tích dữ liệu, và ứng dụng các công cụ AI (NotebookLM, ChatGPT) để tạo ra các persona chi tiết cho chiến lược marketing."
---

# Buổi 2 - Ứng dụng AI để nghiên cứu thị trường và phân tích khách hàng

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- **Khái niệm Target Audience vs Customer Persona:** Target Audience là nhóm người rộng lớn mà bạn muốn tiếp cận dựa trên demographics, behavior, needs. Chân deduction khách hàng (Customer Persona) là một cá nhân giả định cụ thể bên trong nhóm mục tiêu, có tên và đặc điểm chi tiết để giúp team hình dung và giao tiếp dễ dàng hơn.
- **3 yếu tố then chốt để định nghĩa khách hàng mục tiêu:** Nhân khẩu học (tuổi, giới tính, thu nhập), Thành vi dùng (thói quen mua hàng, kênh tiếp cận), Nhu cầu (nỗi đau, yêu cầu cụ thể, động lực mua hàng).
- **Quy trình xây dựng Chân deduction khách hàng:** Xác định Target Origin → Thu thập dữ liệu (khoa sát, phỏng vấn, phân tích nội dung đối thủ) → Phân tích dữ liệu bằng AI → Xây dựng chân deduction với ít nhất 3 thông tin: Thông tin cá nhân, Hành vi & Lối sống, Nhu cầu & Vấn đề.
- **Ứng dụng AI trong nghiên cứu thị trường:** Sử dụng NotebookLM để quét và tóm tắt nội dung từ các nguồn (website, bài viết, catalog); Sử dụng ChatGPT với prompt kỹ lưỡng để phân tích, tạo persona và biểu đồ số liệu; Octoparse để trích xuất dữ liệu từ trang web.
- **Ví dụ thực tế:** Xây dựng chân deduction "Khách Vĩ" cho cửa hàng cây cảnh (nữ 25 tuổi, TP.HCM, Content Maker, nỗi đau: stress công việc, động lực: thư giãn) và phân tích 377 comment bất động sản để tạo ra 3 persona doanh nghiệp (Chủ cửa hàng lẻ, Doanh nghiệp ăn uống, Nhà đầu tư BĐS).

## 📖 Nội Dung Chi Tiết

### 1. Khái niệm và Phân biệt Target Audience với Chân deduction Khách hàng
- **Target Audience (Khách hàng mục tiêu):** Là nhóm người cụ thể mà bạn muốn hướng tới với sản phẩm/dịch vụ. Xác định dựa trên ba yếu tố chính:
  - **Nhân khẩu học:** Tuổi, giới tính, thu nhập, nghề nghiệp, địa lý.
  - **Thành vi dùng:** Thói quen mua hàng, kênh tiếp cận ưa thích (Facebook, TikTok, Google), tần suất sử dụng.
  - **Nhu cầu sản phẩm:** Nỗi đau (pain points) của khách hàng, yêu cầu cụ thể họ cần giải quyết, và xem sản phẩm/dịch vụ của bạn có giải quyết được không.
- **Chân deduction Khách hàng (Customer Persona):** Là một khách hàng giả định, có tên, tuổi, nghề nghiệp và đặc điểm chi tiết, đại diện cho một đoạn nhỏ trong Target Audience. Mục đích là chuyển đổi dữ liệu khô khan thành một "cá nhân" dễ hình dung, giúp team marketing đưa ra quyết định chính xác hơn.
- **Sự khác biệt then chốt:** Target Audience là "nhóm người chung chung"; Chân deduction là "một người cụ thể trong nhóm". Ví dụ: Target có thể là "nữ 18-25 tuổi thích thời trang", còn Chân deduction có thể là "Lê Đức Hoàng, 30 tuổi, nhân viên văn phòng, yêu thích thời trang thanh lịch".

### 2. Quy trình xây dựng một Chân deduction khách hàng hoàn chỉnh
Quy trình đi từ Target Audience đến Chân deduction cụ thể bao gồm 4 bước then chốt:

1.  **Xác định Target Origin:** Liệt kê nhóm khách hàng tiềm năng quan tâm sản phẩm dựa trên 3 yếu tố demographics, behavior, needs.
2.  **Thu thập dữ liệu thực tế:**
    - Sử dụng công cụ khảo sát và phỏng vấn để thu thập phản hồi trực tiếp.
    - Sử dụng Octoparse hoặc Facebook Ad Library/Website Analytics để thu thập dữ liệu từ nội dung đối thủ (bài viết, comment, quảng cáo).
3.  **Phân tích dữ liệu bằng AI:**
    - **NotebookLM:** Nhập các nguồn liên kết (website, bài viết) vào NotebookLM, công cụ sẽ quét và tóm tắt nội dung, giúp nhận diện các chủ đề chính và xu hướng.
    - **ChatGPT:** Sử dụng prompt để yêu cầu AI đóng vai "Marketer" hoặc "Phân tích dữ liệu", yêu cầu xuất ra các ý chính, điểm pain, hoặc xây dựng persona.
    - **Ví dụ prompt:** "Phân tích 377 comment bài viết về thuê nhà mặt phố. Xây dựng 3 chân deduction khách hàng dựa trên đặc điểm demographics, behavior và needs. Đưa ra kết quả dưới dạng bảng."
4.  **Xây dựng Chân deduction chi tiết:** Tổng hợp ít nhất 3 thông tin then chốt cho mỗi persona:
    - **Thông tin cá nhân:** Tên, tuổi, giới tính, nghề nghiệp, địa chỉ.
    - **Hành vi & Lối sống:** Thói quen mua hàng, kênh ưa thích, phong cách sống.
    - **Nhu cầu & Vấn đề:** Nỗi đau chính, mục tiêu mong muốn, rào cản quyết định mua hàng.
    - **Động lực mua hàng:** Những gì khiến họ quyết định "có tiền bỏ" cho sản phẩm này.

### 3. Ví dụ Minh họa thực tế

**Ví dụ 1: Cửa hàng bán cây cảnh**
- **Tên chân deduction:** Khách Vĩ.
- **Thông tin cơ bản:** Nữ, khoảng 25 tuổi, ở Thành phố Hồ Chí Minh, trình độ cử nhân, nghề làm Content Marketing.
- **Thu nhập trung bình:** 10 triệu đồng/tháng, nữ độc thân.
- **Hành vi trực tuyến:** Hay lướt Facebook, Instagram, TikTok; thích theo dõi các thương hiệu cây tươi, lá con, Amber Garden.
- **Nhu cầu:** Mua cây cảnh để bàn làm việc, giảm stress sau giờ làm việc.
- **Nỗi đau:** Việc bận rộn, stress về công việc, cần sự thư giãn.
- **Ứng dụng:** Các anh chị có thể xây dựng nội dung về "chữa lành bằng cây cảnh", "chọn cây theo mốt", hoặc video quay phút giây về tác dụng của cây cảnh đối với sức khỏe tinh thần cho Gen Z.

**Ví dụ 2: Phân tích 377 comment bất động sản (Bài viết về chung cư giá 2,5 - 3 tỷ)**
- Quy trình: Sử dụng Octoparse để trích xuất toàn bộ comment → Dùng ChatGPT để phân tích.
- **3 Chân deduction được tạo ra:**
  1. **Chủ cửa hàng bán lẻ truyền thống:** Quan tâm đến mặt bằng, tiện ích xung quanh, thuê để kinh doanh.
  2. **Doanh nghiệp kinh doanh ăn uống:** Quan tâm đến lưu lượng khách, không gian, mô hình kết hợp bán hàng trực tiếp/online.
  3. **Nhà đầu tư Bất động sản:** Quan tâm đến lợi nhuận thuê, tăng giá trị tài sản, khu vực phát triển tương lai.
- **Xu hướng thị trường:** 32% bình luận về khó khăn thuê nhà, 23,5% về xu hướng thị trường, 21,1% về giải pháp từ cộng đồng.

### 4. Ứng dụng AI để Nghiên cứu đối thủ và Phân tích Content
- **Nghiên cứu qua Facebook Ad Library:** Nhập ngành nghề và sản phẩm, chọn các mẫu quảng cáo có nhiều like/share để làm đối tượng nghiên cứu.
- **Nghiên cứu qua Website:** Tìm kiếm keyword trên Google, chọn top 3 website đối thủ, sử dụng NotebookLM để quét nội dung.
- **Phân tích Content Plan:** Thu thập ít nhất 1 tháng nội dung của đối thủ, upload lên NotebookLM, yêu cầu AI phân tích: "Phân tích điểm mạnh/weak của 3 trung tâm IELTS dựa trên nội dung website và catalog".
- **Kết quả:** AI sẽ đưa ra bảng so sánh các điểm mạnh (ví dụ: đa dạng khóa học, đội ngũ giảng viên, chính sách hỗ trợ) và điểm yếu (ví dụ: khó lựa chọn, không phù hợp với học viên thích học trực tiếp), cùng với các xu hướng cần điều chỉnh chiến lược.

### 5. Tiêu chí xây dựng Chân deduction cho chiến lược marketing
Để một chân deduction có giá trị thực tế cho marketing, nó cần đáp ứng 4 tiêu chí sau:
1.  **Thông tin cá nhân đủ điều kiện:** Tên, tuổi, nghề nghiệp, địa lý đủ để định hình mục tiêu tiếp thị.
2.  **Hành vi mua hàng cụ thể:** Kênh ưa thích, thói quen chi tiêu, tần suất tiếp cận sản phẩm.
3.  **Nhu cầu và vấn đề rõ ràng:** Nỗi đau thực tế, mục tiêu mong muốn, và sản phẩm/dịch vụ có giải quyết được không.
4.  **Động lực quyết định mua:** Các yếu tố kích thích khách hàng thực hiện hành động mua hàng (tiện lợi, giá cả, chất lượng, chương trình ưu đãi).

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** Khách hàng mục tiêu và chân deduction khách hàng khác nhau như thế nào?
  - **Đáp:** Khách hàng mục tiêu là nhóm người rộng lớn mà bạn muốn tiếp cận dựa trên demographics, behavior, needs. Chân deduction khách hàng là một cá nhân giả định cụ thể bên trong nhóm mục tiêu, có tên, nghề nghiệp và đặc điểm chi tiết để giúp team hình dung và giao tiếp dễ dàng hơn.
- **Hỏi:** Cách dùng NotebookLM để nghiên cứu thị trường và xây dựng persona như thế nào?
  - **Đáp:** Người dùng nhập các nguồn liên kết (website, bài viết, catalog) vào NotebookLM, công cụ sẽ quét và tóm tắt nội dung. Sau đó, người dùng có thể yêu cầu NotebookLM hoặc ChatGPT phân tích dựa trên các tiêu chí cụ thể (ví dụ: điểm mạnh/weak, persona, xu hướng) để xuất ra báo cáo hoặc chân deduction chi tiết.
- **Hỏi:** Các bước cơ bản để xây dựng chân deduction khách hàng cho một sản phẩm mới như thế nào?
  - **Đáp:** Bước 1: Xác định Target Audience qua 3 yếu tố (Nhân khẩu học, Thành vi, Nhu cầu). Bước 2: Thu thập dữ liệu thực tế qua khảo sát, phỏng vấn hoặc phân tích nội dung đối thủ. Bước 3: Sử dụng AI (ChatGPT/NotebookLM) để phân tích dữ liệu và tổng hợp ít nhất 3 điểm: thông tin cá nhân, hành vi, nhu cầu/vấn đề. Bước 4: Đặt tên và tạo profile chi tiết cho chân deduction để áp dụng vào chiến lược content và quảng cáo.