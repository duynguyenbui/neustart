---
name: numbered-naming-convention
description: Naming convention for learning folders and files in this Obsidian vault.
---

## Numbered Naming Convention

Khi AI tạo mới hoặc đổi tên thư mục hay tệp nội dung học tập trong vault, bắt buộc tuân theo các quy tắc sau:

1. Tên phải bắt đầu bằng số thứ tự, sau đó là dấu gạch dưới (`_`).
   - Dùng ít nhất hai chữ số cho các số nhỏ hơn 100: `01_`, `02_`, `03_`.
   - Có thể dùng số lớn hơn khi cấu trúc vault yêu cầu, ví dụ `100_Docs`.
2. Không sử dụng dấu cách trong tên. Thay mọi dấu cách bằng dấu gạch dưới (`_`). Chỉ files source trong Vault (KHÔNG CHANGES `@./agents/rules` và `@./agents/skills`).
3. Nếu người dùng yêu cầu đánh dấu một thư mục hoặc tệp là quan trọng, thêm hai dấu gạch dưới (`__`) vào cuối tên (Ví dụ):
   - Thư mục: `03_PTE_Scoring__`
   - Tệp Markdown: `03_PTE_Scoring__.md`
   - Với tệp có phần mở rộng khác, đặt `__` ngay trước phần mở rộng: `03_Score_Guide__.pdf`
4. Không tự thêm `__` nếu người dùng chưa yêu cầu đánh dấu nội dung đó là quan trọng.
5. Số thứ tự phải tăng dần trong cùng một thư mục:
   - Trước khi tạo mục mới, kiểm tra tất cả tên hiện có cùng cấp.
   - Chọn số kế tiếp sau số lớn nhất hiện có. Ví dụ, nếu đã có `01_`, `02_` và `03_`, mục mới phải bắt đầu bằng `04_`.
   - Không dùng lại số cũ, không tạo số trùng và không tự chèn vào giữa dãy số, trừ khi người dùng yêu cầu rõ ràng.
   - Dấu `__` đánh dấu quan trọng không ảnh hưởng đến thứ tự tăng dần.
6. Không tự động đổi tên các tệp hoặc thư mục hiện có. Chỉ đổi tên khi người dùng yêu cầu rõ ràng vì việc đổi tên có thể ảnh hưởng đến liên kết Obsidian.
   Các tệp điều khiển và thư mục hệ thống không thuộc quy ước này, ví dụ: `AGENTS.md`, `README.md`, `.agents/`, `.obsidian/`, `.git/` và `.vscode/`.

### Ví dụ

- Hợp lệ: `01_Listening`
- Hợp lệ: `02_Read_Aloud.md`
- Hợp lệ và được đánh dấu quan trọng: `03_Repeat_Sentence__.md`
- Không hợp lệ: `Listening Notes.md`
- Không hợp lệ: `01 Listening.md`
- Không hợp lệ nếu chưa được người dùng đánh dấu quan trọng: `04_Write_Essay__.md`
