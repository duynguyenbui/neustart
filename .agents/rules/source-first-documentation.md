---
name: source-first-documentation
description: Require AI agents to search the local vault's authoritative documents before using external sources.
---

# Source-First Documentation

When answering questions about German grammar, vocabulary, pronunciation, sentence patterns, course notes, or existing vault knowledge, the AI agent MUST check the relevant local source documents first.

## Mandatory Order

1. **Search the vault first**: Use local search/read tools to find the most relevant document inside the Obsidian vault before answering.
   - Grammar questions: search `02_Grammatik/` first.
   - Vocabulary questions: search `01_Wörter/` first.
   - Sentence pattern questions: search `03_Sätze/` first.
   - Pronunciation questions: search `04_Aussprache/` first.
   - Course-related questions: search `05_NEC2610/` first.

2. **Use the exact matching document when available**: If a relevant note exists, base the answer on that note and cite the file path.

3. **Only search externally after local sources are insufficient**: Use external sources only when:
   - the vault has no relevant document,
   - the local document is incomplete or unclear,
   - the user explicitly asks for outside sources,
   - or current/up-to-date information is required.

4. **State the source status clearly**: Tell the user whether the answer is based on:
   - a local vault note,
   - an external source,
   - or a combination of both.

5. **Do not replace local study notes silently**: If an external source differs from a local note, mention the difference and ask before changing the vault's learning material.

This rule works together with @.agents/rules/anti-hallucination.md: no answer should be based only on memory when a local source document can be checked.
