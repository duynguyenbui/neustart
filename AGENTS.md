# Overview

Dự án này là một kho lưu trữ kiến thức (Obsidian Vault) cá nhân được thiết kế để hỗ trợ việc học tiếng Đức từ trình độ cơ bản hướng tới mục tiêu đạt trình độ B2. Kho lưu trữ chứa các bài ghi chú ngữ pháp, từ vựng theo chủ đề, các bài tập thực hành viết, sửa lỗi và các tài liệu học tập có cấu trúc.

# Structure

Kho lưu trữ được cấu trúc theo các thư mục và tệp tin sau:
- **`01 Wörter`**: Kho từ vựng, cụm từ và từ điển cá nhân.
- **`02 Grammatik`**: Các bài viết chuyên sâu về ngữ pháp tiếng Đức.
- **`03 Sätze`**: Các mẫu câu giao tiếp và cấu trúc câu phổ biến.
- **`04 Aussprache`**: Tài liệu và hướng dẫn về phát âm.
- **`05 NEC2610`**: Ghi chú và bài tập từ khóa học tiếng Đức (Deutschkurs A1).
- **`99 Schreibübung.md`**: Tệp tin chuyên dụng để luyện viết tiếng Đức.
- **`.agents/`**: Cấu trúc cấu hình, kỹ năng (skills) và quy tắc (rules) dành cho trợ lý AI.

# Project Rules

Tệp tin này liệt kê các quy tắc và hướng dẫn áp dụng trên toàn bộ workspace cho các AI agent. Hãy luôn tham khảo các quy tắc này trước khi bắt đầu thực hiện bất kỳ nhiệm vụ nào.

## Rules List

- **Anti-Hallucination (CRITICAL):** @.agents/rules/anti-hallucination.md — Ngăn chặn việc AI tự tạo ra thông tin sai lệch bằng cách bắt buộc xác thực nguồn thông tin.
- **Obsidian Environment:** @.agents/rules/remember-obsidian.md — Nhắc nhở AI rằng đây là một Obsidian vault để tuân thủ đúng định dạng Markdown và liên kết nội bộ.
- **Always Explain Grammar:** @.agents/rules/always-explain-grammar.md — Luôn giải thích chi tiết ngữ pháp tiếng Đức khi người dùng làm bài tập hoặc luyện viết.