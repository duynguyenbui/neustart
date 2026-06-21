# Overview

Dự án này là một kho lưu trữ kiến thức (Obsidian Vault) cá nhân được thiết kế để hỗ trợ việc học tiếng Đức từ trình độ cơ bản hướng tới mục tiêu đạt trình độ B2. Kho lưu trữ chứa các bài ghi chú ngữ pháp, từ vựng theo chủ đề, các bài tập thực hành viết, sửa lỗi và các tài liệu học tập có cấu trúc.

# Structure

Kho lưu trữ được cấu trúc theo các thư mục và tệp tin sau:

- **`01_Wörter`**: Kho từ vựng, cụm từ và từ điển cá nhân.
- **`02_Grammatik`**: Các bài viết chuyên sâu về ngữ pháp tiếng Đức.
- **`03_Sätze`**: Các mẫu câu giao tiếp và cấu trúc câu phổ biến.
- **`04_Aussprache`**: Tài liệu và hướng dẫn về phát âm.
- **`05_NEC2610`**: Ghi chú và bài tập từ khóa học tiếng Đức (NEC2610 - Cô Hường Nguyễn).
- **`06_Tagesnotizen`**: Nhật ký học tập và ghi chú hàng ngày (daily notes).
- **`99_Docs/`**: Thư mục lưu trữ các tài liệu tham khảo, giáo trình học tập (ví dụ: Wortliste).
- **`9999_Schreibübung.md`**: Tệp tin chuyên dụng để luyện viết tiếng Đức.
- **`.agents/`**: Cấu trúc cấu hình, kỹ năng (skills) và quy tắc (rules) dành cho trợ lý AI.

# Project Rules

Tệp tin này liệt kê các quy tắc và hướng dẫn áp dụng trên toàn bộ workspace cho các AI agent. Hãy luôn tham khảo các quy tắc này trước khi bắt đầu thực hiện bất kỳ nhiệm vụ nào.

## Rules List

- **Anti-Hallucination (CRITICAL):** @.agents/rules/anti-hallucination.md — Ngăn chặn việc AI tự tạo ra thông tin sai lệch bằng cách bắt buộc xác thực nguồn thông tin.
- **Concise Yet Complete:** @.agents/rules/concise-yet-complete.md — Trả lời ngắn gọn, trực diện, không rườm rà nhưng bảo đảm đầy đủ ý chính, phân tích bản chất và chi tiết quan trọng.
- **Always Explain Grammar:** @.agents/rules/always-explain-grammar.md — Luôn giải thích chi tiết ngữ pháp tiếng Đức khi người dùng làm bài tập hoặc luyện viết.
- **Source-First Documentation:** @.agents/rules/source-first-documentation.md — Bắt buộc AI Agent tìm tài liệu chính xác trong vault trước, đặc biệt là tài liệu ngữ pháp, rồi mới tìm nguồn bên ngoài khi cần.
- **No Redundant H1:** @.agents/rules/no-redundant-h1.md — Không thêm thẻ Heading 1 (`#`) trùng lặp với tên file ở đầu các tài liệu do Obsidian đã tự động hiển thị tên file làm tiêu đề.
- **Remember Obsidian:** @.agents/rules/remember-obsidian.md — Luôn ghi nhớ đây là Obsidian Vault, tham khảo @AGENTS.md trước khi thay đổi file và bảo toàn cú pháp, liên kết cùng cấu trúc của vault.
- **Numbered Naming Convention:** @.agents/rules/numbered-naming-convention.md — Tên thư mục và tệp nội dung học tập phải bắt đầu bằng số thứ tự tăng dần, không dùng dấu cách, dùng `_` để phân tách từ và chỉ thêm `__` ở cuối khi người dùng yêu cầu đánh dấu quan trọng.
- **Noun Gender and Plural:** @.agents/rules/noun-gender-and-plural.md — Khi giới thiệu danh từ tiếng Đức, luôn ghi đầy đủ mạo từ xác định ở số ít và số nhiều (ví dụ: `das Buch, die Bücher`).
- **Reference NotebookLM:** @.agents/rules/reference-notebook-lm.md — Quy định khi tìm đọc và tra cứu tài liệu dung lượng lớn (PDF, audio, giáo trình) qua NotebookLM MCP, bắt buộc sử dụng notebook "Deutsch" (ID: 8b156a39-fae2-41af-bad5-120bdf834c6d).

## Skills List

- **Karpathy Guidelines:** @.agents/skills/karpathy-guidelines/SKILL.md — Hướng dẫn viết, review và refactor code đơn giản, có phạm vi rõ ràng và tiêu chí kiểm chứng.
