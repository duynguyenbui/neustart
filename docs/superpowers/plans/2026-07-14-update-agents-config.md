# Update AGENTS.md and Clean Up redundant .AGENTS.md Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update AGENTS.md to match the correct rules and directories, and delete .AGENTS.md.

**Architecture:** Update AGENTS.md using the correct rules list and directories, then delete the obsolete `.AGENTS.md` file using terminal commands.

**Tech Stack:** Markdown, Git, Shell Commands

## Global Constraints

- Keep only `AGENTS.md` and delete `.AGENTS.md`.
- Ensure all rule paths exist.

---

### Task 1: Update AGENTS.md

**Files:**
- Modify: `AGENTS.md`

**Interfaces:**
- Consumes: None
- Produces: Updated `AGENTS.md`

- [ ] **Step 1: Replace file contents of AGENTS.md**

Update `/Users/nguyenbui/Projects/neustart/AGENTS.md` with the verified contents.

Code to write:
```markdown
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
- **`99_Schreibübung.md`**: Tệp tin chuyên dụng để luyện viết tiếng Đức.
- **`.agents/`**: Cấu trúc cấu hình, kỹ năng (skills) và quy tắc (rules) dành cho trợ lý AI.
- **`docs/`**: Thư mục lưu trữ các tài liệu tham khảo, giáo trình học tập (ví dụ: Wortliste).

# Project Rules

Tệp tin này liệt kê các quy tắc và hướng dẫn áp dụng trên toàn bộ workspace cho các AI agent. Hãy luôn tham khảo các quy tắc này trước khi bắt đầu thực hiện bất kỳ nhiệm vụ nào.

## Rules List

- **Anti-Hallucination (CRITICAL):** @.agents/rules/anti-hallucination.md — Ngăn chặn việc AI tự tạo ra thông tin sai lệch bằng cách bắt buộc xác thực nguồn thông tin.
- **Always Explain Grammar:** @.agents/rules/always-explain-grammar.md — Luôn giải thích chi tiết ngữ pháp tiếng Đức khi người dùng làm bài tập hoặc luyện viết.
- **Source-First Documentation:** @.agents/rules/source-first-documentation.md — Bắt buộc AI Agent tìm tài liệu chính xác trong vault trước, đặc biệt là tài liệu ngữ pháp, rồi mới tìm nguồn bên ngoài khi cần.
- **No Redundant H1:** @.agents/rules/no-redundant-h1.md — Không thêm thẻ Heading 1 (`#`) trùng lặp với tên file ở đầu các tài liệu do Obsidian đã tự động hiển thị tên file làm tiêu đề.
```

- [ ] **Step 2: Commit changes to AGENTS.md**

Run command to commit:
```bash
git add AGENTS.md
git commit -m "docs: update AGENTS.md to match current project rules and structure"
```

---

### Task 2: Delete redundant .AGENTS.md

**Files:**
- Delete: `.AGENTS.md`

**Interfaces:**
- Consumes: Updated `AGENTS.md`
- Produces: Cleaned up project state

- [ ] **Step 1: Delete .AGENTS.md**

Run command to delete `.AGENTS.md`:
```bash
rm .AGENTS.md
```

- [ ] **Step 2: Commit the deletion**

Run command to commit:
```bash
git add .AGENTS.md
git commit -m "docs: remove redundant .AGENTS.md file"
```
