# DeepTutor Knowledge Modules Repository (`deep-tutor-kms`)

Repository lưu trữ và quản lý tập trung các **Knowledge Modules (KMs)** chuẩn hóa (định dạng Markdown với YAML Frontmatter, Key Takeaways, Detailed Content & Q&A for Search) phục vụ cho hệ thống RAG **DeepTutor**.

---

## Cấu trúc Repository

```
deep-tutor-kms/
├── Marketing-Content/      # KM Chuyên đề Marketing & Content
│   ├── [Khóa học 1]/
│   │   ├── Buổi 1.md
│   │   └── ...
│   ├── [Khóa học 2]/
│   └── ...
├── .gitignore
└── README.md
```

---

## Danh mục Knowledge Modules

### 1. `Marketing-Content`
- **Mô tả:** Toàn bộ tri thức trích xuất và chuẩn hóa từ các khóa học Content Marketing, Copywriting, SEO, Ads & Chiến lược nội dung.
- **Quy cách tài liệu:** Markdown (`.md`) có cấu trúc:
  - **YAML Frontmatter:** `title`, `course`, `module`, `instructor`, `difficulty`, `tags`, `summary`.
  - **Key Takeaways (`## 💡 Tóm Tắt Cốt Lõi`):** Đúc kết ngắn gọn các ý chính.
  - **Detailed Content (`## 📖 Nội Dung Chi Tiết`):** Phân tích sâu theo đề mục & case study thực tế.
  - **Q&A for Search (`## ❓ Câu Hỏi & Trả Lời Trọng Tâm`):** Bộ hỏi - đáp phục vụ tìm kiếm ngữ nghĩa / RAG.

---

## Cấu hình DeepTutor tích hợp Git Repository

DeepTutor hỗ trợ 2 hình thức liên kết Knowledge Base với Git:

### Cách 1: Liên kết qua GitHub / Git Remote (Auto-sync)
1. Push repository này lên GitHub/Git server:
   ```bash
   git remote add origin <your-git-remote-url>
   git push -u origin main
   ```
2. Trên giao diện Web của **DeepTutor** (`http://192.168.100.16:3782`):
   - Vào **Knowledge Center** -> **New Knowledge Base** (hoặc chọn KB `Marketing-Content`).
   - Chọn nguồn **Git Repository / GitHub Source**.
   - Cấu hình:
     - **Repo URL:** `<your-git-repo-url>`
     - **Branch:** `main`
     - **Path / Glob:** `Marketing-Content/**/*.md`
   - DeepTutor sẽ tự động clone, theo dõi hash và tự động re-index khi có commit mới.

### Cách 2: Liên kết qua thư mục Local / Mount Path
Nếu DeepTutor chạy chung máy chủ hoặc được mount volume vào Docker:
```bash
deeptutor kb create Marketing-Content --docs-dir /path/to/deep-tutor-kms/Marketing-Content
```
Hoặc liên kết trực tiếp thư mục:
```bash
deeptutor kb link Marketing-Content /path/to/deep-tutor-kms/Marketing-Content
```
