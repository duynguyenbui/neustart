---
name: german-tutor
description: "The main orchestrator for German learning. Triggers when the user asks for help with German learning, writing correction (Schreibübung), grammar explanations, or vocabulary management. Use this skill whenever German learning assistance is needed, or there are follow-up tasks like 'correct my writing', 'explain this grammar', 'add this word'."
---

# German Tutor Orchestrator

This skill orchestrates the German learning assistant team. It routes the user's request to the appropriate subagent.

## Workflow

### Phase 1: Context Check & Intent Classification
Analyze the user's request to determine the primary intent:
- **Grammar Explanation**: User asks about a grammar rule or why a sentence is constructed a certain way. -> Route to `grammar-expert`.
- **Writing Correction**: User asks to review a text or specifically mentions `99 Schreibübung.md`. -> Route to `writing-evaluator`.
- **Vocabulary**: User asks for the meaning of a word, or wants to add a word to the vocabulary list. -> Route to `vocab-manager`.

### Phase 2: Execution via Subagents
Invoke the relevant subagent using the `invoke_subagent` tool.

- For **Grammar**:
  - `TypeName`: `grammar-expert`
  - `Prompt`: "Explain [grammar concept] or analyze [text]. Use vault notes in `02 Grammatik` if possible."
- For **Writing**:
  - `TypeName`: `writing-evaluator`
  - `Prompt`: "Review the text in [file path, e.g. `99 Schreibübung.md`] or [text]. Correct mistakes and explain them."
- For **Vocabulary**:
  - `TypeName`: `vocab-manager`
  - `Prompt`: "Define [word] or add [word] to `01 Wörter`. Include gender, plural, and examples."

### Phase 3: Integration and Output
1. Wait for the subagent to complete its task.
2. Present the result to the user clearly.
3. If writing files, confirm the changes.

## Error Handling
- If a subagent fails to find relevant information in the vault, instruct it to use its general knowledge but explicitly state that it's not from the vault (per Anti-Hallucination rule).
- If multiple intents are detected, handle them sequentially or invoke parallel subagents if they are independent.

## Test Scenarios
- **Happy Path (Writing)**: User says "Check my new entry in 99 Schreibübung.md". Orchestrator invokes `writing-evaluator`, which reads the file, identifies mistakes, and returns a correction report.
- **Happy Path (Grammar)**: User asks "Why is it 'dem Mann' and not 'den Mann'?". Orchestrator invokes `grammar-expert`, which explains the dative case.
- **Happy Path (Vocabulary)**: User asks "What is the meaning of 'Entwicklung'?". Orchestrator invokes `vocab-manager`, which defines the word and suggests adding it to `01 Wörter`.
