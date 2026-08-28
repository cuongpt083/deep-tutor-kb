Here's a thinking process:

1.  **Analyze User Input:**
   - **Role:** Knowledge Engineer & Educational Content Editor
   - **Task:** Clean raw transcript, convert to structured Knowledge Document optimized for RAG/KB
   - **Input:** Course info + Raw transcript (Vietnamese)
   - **Output Format:** Specific Markdown with YAML Frontmatter structure
   - **Rules:** 
     - Remove all chitchat, greetings, mic checks, personal interactions, filler words, etc.
     - Preserve all academic/professional content, definitions, frameworks, methodologies, examples/case studies
     - Convert spoken flow to smooth, concise, professional written Vietnamese
     - Output ONLY the Markdown, no intro/outro explanations

2.  **Analyze the Transcript:**
   - It's a lecture by Nguyễn Đức Dương about TikTok algorithm, content formats, viral mechanics, etc.
   - Contains lots of filler words: "ừm", "ừ", "ạ", "thôi", "cái này", "cái kia", "nhé", "được chưa ạ", etc.
   - Has personal greetings/checks: "Ok, xin chào tất cả mọi người", "bây giờ chúng ta sẽ đi vào", etc.
   - Has repetitive phrases, personal anecdotes, "theo mình", "theo các bạn"
   - Has technical content about TikTok algorithm, content formats, viral factors, case studies/examples
   - Has some Vietnamese colloquialisms that need cleaning but keeping meaning

3.  **Identify Key Content Themes (after cleaning):**
   - TikTok Algorithm mechanics: personalized env (demographics), environment (location, WiFi), third factor (deep listening/tools)
   - View duration metrics: 6-8 seconds retention, watch-through rate, re-watches
   - Content format types: Talking head, Interview, POV, 1st person, 3rd person
   - Content niches: Review, Drama/Storytelling, Experience-based commerce
   - Algorithm distribution: Initial 200-500 views, key metrics (watch time, re-watches), label assignment after 50 videos same topic
   - Viral factors: Content value + Format consistency, niche saturation, audience behavior
   - Case studies/examples mentioned: Specific TikTok examples, content formats that worked

4.  **Clean & Structure the Content:**
   - I need to extract the core knowledge points, organize them logically, and format into the required Markdown structure.
   - I'll keep it in Vietnamese as the transcript is Vietnamese, but make it professional, concise, and structured.
   - I need to remove all the "ừm", "thôi", "nhé", repeated phrases, personal greetings, etc.
   - I'll preserve the educational value, frameworks, and examples.

   Let me outline the structure based on the requirements:
   - YAML Frontmatter: title, course, module, instructor, difficulty, tags, summary
   - Markdown sections: Key Takeaways, Detailed Content (with bullet points, bold terms), Examples/Case Studies, Q&A for Search

   Now, I'll go through the transcript mentally, extract the essence, and rewrite it.

   Key points to preserve:
   - TikTok algorithm: 3 environments (personalization/demographics, environment/location/WiFi, deep listening/tools)
   - Initial distribution: 200-500 random views
   - Key metrics: Watch-through rate, re-watch rate
   - 6-8 second retention threshold
   - Content format types: Talking head, Interview, POV, 1st person, 3rd person
   - Viral factors: Content value + Format consistency
   - Niche/label assignment after 50 videos same topic
   - Algorithm learning: Based on user behavior, not just follow
   - Geo-targeting: Location, WiFi affect distribution
   - Country-level restrictions/content governance
   - Post-COVID evolution: From entertainment to diverse content, 73 topics
   - Review niche: Need hands-on experience, emergence of "experience brokers"
   - Drama/Storytelling format: POV, 3rd person effective
   - Case study: Specific examples about content formats that went viral
   - Algorithm label system: After 50 videos same topic, TikTok assigns content label
   - View distribution logic: Based on behavior similarity, not just follow count
   - Importance of consistency in format/niche for algorithm understanding

   I need to be careful not to lose the substantive content while cleaning the noise.

   Let me structure the content logically:

   **Title:** Something like "TikTok Algorithm & Content Format Mechanics for Viral Growth"
   **Course:** content-inputs
   **Module:** mang-content/25.08.25 Khóa Học No Viral No Money Cùng Nguyễn Đức Dương/Module 3 - ...
   **Instructor:** Nguyễn Đức Dương (or "Không rõ" if uncertain, but I can extract from context)
   **Difficulty:** Nâng cao (Advanced) or Trung cấp
   **Tags:** #TikTok #Algorithm #ContentStrategy #ViralMarketing #DigitalMedia
   **Summary:** Học cách TikTok phân phối nội qua 3 môi trường ( cá nhân hóa, môi trường, deep listening), các chỉ số quan trọng (thời gian xem hết, xem lại), các định dạng content (POV, phỏng vấn, góc 1/3) và chiến lược tăng view dựa trên giá trị nội dung và hình thức tái lặp.

   Now, Detailed Content sections. I'll draft them in Vietnamese, professional, concise.

   Let me actually write the full output now, following the exact format requested. I need to make sure I don't add any extra text outside the Markdown.

   I'll structure the content extraction:

   **Key Takeaways (Tóm tắt cốt lõi):**
   - TikTok thuật toán phân phối dựa trên 3 môi trường: cá nhân hóa (demographics), môi trường (địa điểm, WiFi), và deep listening (công cụ lắng nghe, tìm kiếm).
   - Phân phối ban đầu ngẫu nhiên 200-500 view, sau đó đánh giá qua 2 chỉ số then chốt: thời gian xem hết