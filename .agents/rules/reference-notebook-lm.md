---
name: reference-notebook-lm
description: Guide AI agents to retrieve and reference large learning assets (PDFs, audio recordings, textbooks) via NotebookLM MCP using the project's configured target notebook.
---

# Reference NotebookLM

NotebookLM serves as the external repository and retrieval engine for heavy study assets—such as full-length PDF textbooks, lecture audio recordings, listening exercises, and extensive course slide decks—that are unsuited for direct storage in the Markdown vault.

---

## 1. Configured Target Notebook

Update the metadata below whenever rebinding this project to a different notebook:

---

## 2. Knowledge Retrieval Workflow

1. **Vault Notes First:** Check local vault summaries and grammar notes first as defined in @.agents/rules/source-first-documentation.md.
2. **Deep Reference in NotebookLM:** When the user query requires in-depth textbook explanations, exact citations from course PDFs, or audio transcript analysis, query the configured NotebookLM notebook using `gemini-notebook-mcp` tools (`notebook_query` or `source_get_content`).
3. **Synthesis:** Combine concise vault rules with the rich context retrieved from NotebookLM to provide complete, grounded explanations.

---

## 3. Strict Notebook Scoping

- **Target Binding:** Always pass the active `Notebook ID` (`8b156a39-fae2-41af-bad5-120bdf834c6d`) to all MCP tool calls requiring `notebook_id` (`notebook_query`, `source_add`, `studio_create`, `note`, `source_list_drive`, etc.).
- **Isolation:** Do not query, modify, add sources to, or delete other notebooks in the Google account (e.g., personal or non-German notebooks) unless explicitly requested by the user with a specific notebook name.
