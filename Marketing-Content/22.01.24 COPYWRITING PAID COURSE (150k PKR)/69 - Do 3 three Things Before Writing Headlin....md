---
   title: "{Tên bài học rõ ràng}"
   course: "{Tên khóa học}"
   module: "{Chuyên đề/Học phần nếu có, hoặc để trống}"
   instructor: "{Tên giảng viên nếu xác định được, hoặc Không rõ}"
   difficulty: "{Cơ bản | Trung cấp | Nâng cao}"
   tags:
     - "{tag 1}"
     - "{tag 2}"
   summary: "{Tóm tắt ngắn gọn 2-3 câu về nội dung chính của bài học}"
   ---
   
   # {Tên bài học}
   
   ## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
   - {Ý then chốt 1}
   - {Ý then chốt 2}
   - {Ý then chốt 3}
   
   ## 📖 Nội Dung Chi Tiết
   ### 1. {Đề mục lớn 1}
   {Nội dung giải thích chi tiết, logic, rõ ràng. Dùng bullet points, in đậm thuật ngữ quan trọng.}
   
   > **Ví dụ / Case Study:** {Nếu có ví dụ minh họa của giảng viên}
   
   ### 2. {Đề mục lớn 2}
   ...
   
   ## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
   - **Hỏi:** {Câu hỏi 1 mà một người dùng có thể tìm kiếm về bài này?}
     - **Đáp:** {Câu trả lời trực tiếp, đầy đủ, súc tích.}
   - **Hỏi:** {Câu hỏi 2}
     - **Đáp:** {Câu trả lời}
   - **Hỏi:** {Câu hỏi 3}
     - **Đáp:** {Câu trả lời}
   ```

   I need to fill this based on the transcript. Let's deduce:
   - title: "Do 3 Things Before Writing Headlines" (from lesson title, but transcript ends at "headline". I'll use the lesson title as title, or derive from transcript. The lesson title is "69 - Do 3 three Things Before Writing Headlin...". I'll clean it to "Do 3 Things Before Writing Headlines".
   - course: "content-inputs"
   - module: "mang-content/22.01.24 COPYWRITING PAID COURSE (150k PKR)"
   - instructor: Not identified, maybe "Unknown" or leave blank? The format says "or Unknown". I'll put "Unknown" or omit if not sure. I'll put "Unknown".
   - difficulty: Not specified. I'll infer "Beginner" or "Intermediate" based on context, or leave as "Beginner". Actually, I should maybe put "Beginner" or keep it generic. The prompt says "{Cơ bản | Trung cấp | Nâng cao}". I'll choose "Beginner" as it's an intro to headlines.
   - tags: Related to copywriting, headline, content inputs. I'll pick 2: "copywriting", "headline".
   - summary: "The backbone of copywriting is the headline; lesson introduces key principles for crafting effective headlines."
   - Key Takeaways: 1. Headline is the backbone of copywriting. 2. (Maybe 3 things but not in transcript, I'll stick to what's extracted). I'll put 3 items but make sure they're valid or just put the core one and pad reasonably? The prompt says "- {Ý then chốt 1}" etc. I'll put 3 takeaways based on the concept: 1) Headline is the core of copywriting. 2) Understanding headline structure improves engagement. 3) Headlines require strategic thinking before writing. But I must be careful not to hallucinate beyond the transcript. The transcript only says "The backbone of copywriting is headline." I'll limit takeaways to what's certain, maybe 1-2, but the format expects 3. I'll structure them logically derived from the core, or I'll put the same core in different phrasings? Better to be strict: I'll put 3 takeaways but ensure they're directly from or directly inferable from the transcript without inventing. Since the transcript is minimal, I'll extract: "Headline is the backbone of copywriting", "The lesson focuses on the importance of headline in copywriting", "Preparation for headline writing is emphasized". That's safe.

   Actually, re-reading the user prompt: "Hãy làm sạch và cấu trúc lại toàn bộ kiến thức của bài học này theo định dạng yêu cầu." I need to output exactly the Markdown format. I'll clean the transcript, extract the essence, and fill the format.

   Let me process the cleaning:
   - Remove: "Assalamu alaikum, welcome to the week 5 lessons, okay?" -> remove
   - "Bہت-bہت آپ لوگوں کو مبارک ہو, کہ آپ نے week 4 weeks complete کر دی ہیں, بہت زبادہ results ابھی تک آ رہے ہیں." -> remove
   - "Okay, اس week میں بہت important چیز میں بتانے والا ہوں." -> remove
   - "Something جو کہ backbone of copywriting کہلاتی ہے." -> extract "The backbone of copywriting is..."
   - "دیکھیں وہ کیا ہے backbone of copywriting?" -> extract "What is the backbone of copywriting?"
   - "وہ ہے headline." -> extract "It is headline."
   - "Tuyên, ," -> remove

   Cleaned core: "The backbone of copywriting is headline."

   Now, structure. I'll assume the lesson title "Do 3 Things Before Writing Headlines" is the intended topic, and the transcript is a snippet introducing it. I'll create the document accordingly, but strictly based on the transcript content. I'll make the content about the headline being the backbone.

   Let's draft the Markdown:

   ```
   ---
   title: "Do 3 Things Before Writing Headlines"
   course: "content-inputs"
   module: "mang-content/22.01.24 COPYWRITING PAID COURSE (150k PKR)"
   instructor: "Unknown"
   difficulty: "Beginner"
   tags:
     - "copywriting"
     - "headline"
   summary: "The backbone of copywriting is the headline; this lesson introduces the foundational role of headlines in effective copy."
   ---
   
   # Do 3 Things Before Writing Headlines
   
   ## 💡 Tóm Tạo file markdown...