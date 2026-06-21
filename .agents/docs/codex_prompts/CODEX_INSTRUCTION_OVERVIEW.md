# Hướng dẫn dùng Codex chuyên nghiệp

Tài liệu này được tổng hợp ngày `2026-06-20` từ Codex manual chính thức và các trang docs của OpenAI, rồi viết lại theo hướng thực chiến để bạn có thể áp dụng ngay.

## 1. Tư duy đúng: dùng Codex như một teammate

Codex cho kết quả tốt nhất khi bạn không dùng nó như một chatbot hỏi đáp từng câu, mà như một cộng sự kỹ thuật:

- giao việc rõ ràng
- cung cấp context đúng
- định nghĩa tiêu chí hoàn thành
- bắt nó tự kiểm tra lại bằng test, lint, review
- biến các quy ước lặp lại thành cấu hình, `AGENTS.md`, skill, hoặc automation

Tóm gọn:

> Prompt giải quyết việc hôm nay.  
> `AGENTS.md` giải quyết việc lặp lại.  
> Skills/MCP giải quyết workflow và công cụ.  
> `codex exec` giải quyết automation.

## 2. Workflow chuyên nghiệp nhất

Đây là workflow mình khuyến nghị dùng mặc định.

### Bước 1: mở đúng surface

- `Codex CLI`: tốt nhất cho terminal-first, sửa code nhanh, review, automation
- `IDE extension`: tốt nhất khi bạn cần editor context như file đang mở, vùng đang chọn
- `Codex app`: tốt nhất cho research, planning, review, side chat, worktree, background work
- `Cloud task`: dùng khi muốn chạy song song hoặc giao việc từ xa

Quy tắc nhanh:

- sửa code trong repo local: bắt đầu bằng CLI hoặc IDE
- task nhiều nhánh song song: dùng app + worktree
- CI, script, batch: dùng `codex exec`

### Bước 2: luôn prompt theo 4 phần

OpenAI khuyến nghị prompt nên có 4 thành phần:

- `Goal`: cần thay đổi gì
- `Context`: file, thư mục, lỗi, docs nào liên quan
- `Constraints`: chuẩn code, kiến trúc, yêu cầu an toàn
- `Done when`: thế nào thì xem là xong

Mẫu prompt nên dùng:

```text
Goal:
Implement X / fix bug Y.

Context:
- Relevant files: ...
- Error/log: ...
- Existing pattern: ...

Constraints:
- Do not change public API unless necessary
- Keep implementation minimal
- Follow existing project conventions

Done when:
- Tests related to X pass
- Lint/typecheck pass
- Behavior is verified
- Summarize the diff and risks
```

Nếu task mơ hồ hoặc lớn:

- dùng `/plan` trước
- hoặc yêu cầu Codex "interview me first"
- hoặc dùng `/goal` khi cần theo đuổi mục tiêu dài hơi

### Bước 3: chuyển quy tắc lặp lại vào `AGENTS.md`

Đây là đòn bẩy lớn nhất để dùng Codex ổn định.

`AGENTS.md` nên chứa:

- cấu trúc repo
- lệnh run/build/test/lint
- conventions quan trọng
- rule không được vi phạm
- cách verify trước khi kết thúc
- review expectations

Khởi tạo nhanh:

```bash
/init
```

Nhưng không nên giữ file scaffold nguyên xi. Hãy sửa nó theo repo thật.

Mẫu `AGENTS.md` ngắn mà hiệu quả:

```md
# AGENTS.md

## Project map
- App code ở `src/`
- Integration tests ở `tests/integration/`

## Commands
- Install: `pnpm install`
- Dev: `pnpm dev`
- Lint: `pnpm lint`
- Test: `pnpm test`
- Typecheck: `pnpm typecheck`

## Rules
- Không thêm dependency production nếu chưa nêu lý do
- Ưu tiên sửa nhỏ, đúng chỗ
- Không refactor ngoài phạm vi task

## Done when
- Test liên quan pass
- Lint/typecheck pass
- Diff được self-review
- Tóm tắt rõ file nào đổi và rủi ro còn lại
```

Khi Codex lặp lại cùng một lỗi hai lần, hãy cập nhật `AGENTS.md`.

## 3. Cấu hình mặc định nên có

Tính đến `2026-06-20`, manual chính thức của Codex khuyến nghị:

- `gpt-5.5` cho hầu hết task phức tạp
- `gpt-5.4-mini` cho task nhẹ hơn, nhanh hơn, rẻ hơn

Starter config tối thiểu:

```toml
model = "gpt-5.5"
model_provider = "openai"
# model_reasoning_effort = "medium"
# model_verbosity = "medium"

[sandbox_workspace_write]
network_access = false
```

Khi nào dùng model nào:

- `gpt-5.5`: refactor khó, debug phức tạp, review, research, design decisions
- `gpt-5.4-mini`: chỉnh nhỏ, test nhỏ, docs, cleanup, subtask

Quy tắc reasoning:

- `low`: task rõ và hẹp
- `medium`: mặc định tốt
- `high` hoặc `xhigh`: migration, bug khó, nhiều bước, cần plan

Trong phiên làm việc:

- đổi model bằng `/model`
- kiểm tra context, quyền, writable roots bằng `/status`

## 4. Bảo mật và quyền: giữ chặt mặc định

Cách làm chuyên nghiệp không phải là cho full quyền ngay từ đầu.

Mặc định nên dùng:

- sandbox `workspace-write`
- approval `on-request`
- network `off`

Điều này cho phép Codex:

- đọc file
- sửa file trong workspace
- chạy command phù hợp
- nhưng vẫn phải xin phép khi vượt sandbox hoặc cần mạng

Lệnh hữu ích:

- `/permissions`: đổi mức tự do giữa lúc làm
- `/status`: kiểm tra workspace, model, context, quyền

Chỉ nới quyền khi có lý do rõ ràng:

- cần cài package
- cần gọi API hoặc truy cập docs live
- cần viết ngoài workspace

Không nên mặc định dùng:

- `danger-full-access`
- network mở toàn cục
- nhiều thread cùng sửa một file

## 5. Luôn buộc Codex tự kiểm tra

Đừng chỉ bảo nó "làm xong rồi báo em". Hãy yêu cầu:

- viết hoặc cập nhật test khi cần
- chạy test liên quan
- chạy lint, format, typecheck
- review lại diff
- nêu rủi ro còn lại

Mẫu prompt:

```text
Implement the fix, run the smallest relevant test set, then review your own diff for regressions before finishing.
```

Lệnh review nên dùng:

```bash
/review
```

Đây là một trong những thói quen làm tăng chất lượng nhanh nhất.

## 6. Chia việc đúng cách

Codex làm tốt hơn khi việc được chia nhỏ.

Mẫu chia 3 pha:

1. tìm hiểu và lập kế hoạch
2. implement tối thiểu
3. verify và review

Ví dụ prompt tốt:

```text
First inspect the relevant files and propose a minimal plan.
Then implement only the smallest safe fix.
Finally run the relevant checks and review the diff for regressions.
```

Nếu việc lớn:

- dùng `/plan`
- sau đó đặt `/goal`
- hoặc tách thành nhiều thread, nhưng tránh cho nhiều thread đụng cùng file

## 7. Dùng worktree để chạy song song mà không phá workspace chính

Nếu bạn dùng Codex app, worktree là cách chuyên nghiệp để:

- chạy nhiều task song song
- giữ local checkout sạch
- handoff một task từ background về local khi cần test kỹ

Khi nên dùng worktree:

- bạn đang làm một task foreground nhưng muốn giao thêm task khác
- cần nhiều branch song song
- muốn Codex tiếp tục làm mà không chạm workspace chính

Lưu ý quan trọng:

- Git không cho cùng một branch được checkout ở nhiều worktree cùng lúc
- nếu repo cần file ignore như `.env`, hãy dùng `.worktreeinclude`

## 8. Khi nào nên dùng skills, MCP, hooks

### Skills

Dùng khi bạn có workflow lặp lại:

- commit theo nhóm logic
- review theo checklist riêng
- cập nhật docs theo format cố định
- release checklist

Nguyên tắc:

- 1 skill = 1 job rõ ràng
- ưu tiên instruction trước script
- chỉ thêm script khi cần tính xác định cao

### MCP

Dùng khi Codex cần dữ liệu hoặc hành động ngoài repo:

- docs server
- GitHub, Linear, Figma
- browser automation
- internal knowledge base

Ví dụ thêm MCP bằng CLI:

```bash
codex mcp add context7 -- npx -y @upstash/context7-mcp
```

Check server đang có:

```bash
/mcp
```

### Hooks

Dùng khi bạn muốn enforce policy tự động:

- chặn prompt chứa secret
- bắt chạy validation ở cuối turn
- log hoạt động về hệ thống riêng
- kiểm tra command trước khi chạy

Hooks mạnh, nhưng nên dùng cho enforcement cơ học; đừng lạm dụng để thay thế `AGENTS.md`.

## 9. Dùng `codex exec` cho automation

`codex exec` là mode chuyên nghiệp cho CI, scripts, batch workflows.

Use case tốt:

- tổng hợp logs
- tạo release notes
- review diff trong CI
- đề xuất fix cho CI failures
- xuất dữ liệu có schema

Ví dụ:

```bash
codex exec "summarize the repository structure and list the top 5 risky areas"
```

JSON output:

```bash
codex exec --json "summarize the repo structure"
```

Structured output:

```bash
codex exec "Extract project metadata" \
  --output-schema ./schema.json \
  -o ./project-metadata.json
```

Khuyến nghị an toàn:

- trong automation, dùng quyền ít nhất có thể
- nếu chạy trên CI, ưu tiên GitHub Action chính thức của Codex
- không để API key lộ cho script hoặc code không đáng tin

## 10. Bộ lệnh nên nhớ

Interactive:

- `/plan`: lập kế hoạch trước khi code
- `/goal`: bám mục tiêu dài hơi
- `/model`: đổi model
- `/permissions`: đổi mức quyền
- `/status`: xem model, context, workspace, token
- `/review`: review working tree
- `/mcp`: xem MCP servers
- `/init`: scaffold `AGENTS.md`
- `/compact`: nén context khi thread quá dài

CLI:

- `codex`: mở interactive session
- `codex exec "..."`
- `codex exec --json "..."`
- `codex exec resume --last "..."`
- `codex mcp add ...`

## 11. Anti-patterns cần tránh

- prompt quá mơ hồ, không có `Done when`
- giao task lớn nhưng không `/plan`
- lặp lại cùng instruction ở mọi prompt thay vì đưa vào `AGENTS.md`
- mở quyền quá rộng ngay từ đầu
- để hai thread cùng sửa một vùng code
- bắt Codex refactor lớn khi mục tiêu chỉ là fix nhỏ
- không yêu cầu verify
- nhờ nó dùng tool ngoài repo nhưng chưa cấu hình MCP

## 12. Cách mình sẽ triển khai cho bất kỳ repo nào

Nếu bắt đầu một repo mới, mình sẽ làm theo thứ tự này:

1. chạy `/init`
2. sửa `AGENTS.md` thành bản ngắn, đúng repo
3. đặt model mặc định là `gpt-5.5`
4. giữ sandbox `workspace-write`, approval `on-request`
5. thêm các MCP thật sự cần
6. tạo 1-3 skills cho workflow lặp lại nhiều nhất
7. dùng `/plan` cho task mơ hồ
8. luôn kết thúc bằng test + `/review`
9. đưa các tác vụ định kỳ sang `codex exec` hoặc automation

## 13. Mẫu prompt chuyên nghiệp để dùng ngay

### Mẫu sửa bug

```text
Goal:
Fix the root cause of this bug.

Context:
- Repro steps: ...
- Error output: ...
- Likely files: ...

Constraints:
- Keep the fix minimal
- Do not refactor unrelated code

Done when:
- Bug is reproducible before and not reproducible after
- Relevant tests pass
- Explain root cause and changed files
```

### Mẫu review thay đổi

```text
Review the current diff for bugs, regressions, edge cases, and missing tests.
Prioritize findings by severity and cite the affected files.
```

### Mẫu research trước khi code

```text
First inspect the relevant parts of the codebase and propose a short plan.
Do not edit files yet.
Call out assumptions, risks, and the smallest safe implementation path.
```

## 14. Sources chính thức

Nguồn mình đã dùng để tổng hợp tài liệu này:

- Codex Manual: `https://developers.openai.com/codex/codex-manual`
- Best practices: `https://developers.openai.com/codex/learn/best-practices`
- Prompting: `https://developers.openai.com/codex/prompting`
- Agent approvals & security: `https://developers.openai.com/codex/agent-approvals-security`
- Models: `https://developers.openai.com/codex/models`
- Worktrees: `https://developers.openai.com/codex/app/worktrees`
- AGENTS.md guide: `https://developers.openai.com/codex/guides/agents-md`
- Skills: `https://developers.openai.com/codex/skills`
- MCP: `https://developers.openai.com/codex/mcp`
- Hooks: `https://developers.openai.com/codex/hooks`
- Non-interactive mode: `https://developers.openai.com/codex/noninteractive`

## 15. Kết luận ngắn

Muốn dùng Codex thật chuyên nghiệp, hãy chuẩn hóa theo công thức:

`Prompt rõ + AGENTS.md ngắn mà sắc + sandbox chặt + verify bắt buộc + skills/MCP cho workflow lặp lại + automation bằng codex exec`

Đó là cách biến Codex từ "trợ lý trả lời" thành "đồng đội kỹ thuật làm việc ổn định".
