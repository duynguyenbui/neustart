# Obsidian Environment Rule

## Context

This project uses **Obsidian** as its primary knowledge base and note-taking environment.
The workspace may contain `.md` (Markdown) files that are part of an Obsidian vault.

## Rules

- **Obsidian Markdown**: Always write Markdown that is compatible with Obsidian's flavor.
  This includes support for `[[wikilinks]]`, `![[embedded files]]`, and `#tags`.

- **Frontmatter**: When creating or editing notes, use YAML frontmatter for metadata (e.g., `tags`, `aliases`, `date`).
  Frontmatter must be placed at the very top of the file, enclosed in `---` delimiters.

- **Wikilinks over standard links**: Prefer `[[Note Title]]` syntax for internal links between notes
  instead of standard Markdown links `[text](path)`, unless linking to external URLs.

- **Folder structure**: Respect the existing vault folder structure. Do not move, rename, or delete
  files/folders without explicit user confirmation, as this can break internal links.

- **Callouts**: Use Obsidian callout syntax for highlighted blocks:
  ```
  > [!NOTE]
  > Content here
  ```
  Supported types: `NOTE`, `TIP`, `IMPORTANT`, `WARNING`, `CAUTION`, `INFO`, `TODO`, `QUESTION`, `EXAMPLE`.

- **No unsupported syntax**: Avoid Markdown extensions that Obsidian does not support
  (e.g., some advanced HTML or non-standard plugins). Stick to core Obsidian syntax
  unless a specific community plugin is confirmed to be active in this vault.

- **Dataview awareness**: If `.md` files contain `dataview` code blocks, treat them as
  Obsidian Dataview queries — do not alter query syntax unless asked.

- **Attachments**: Images and other attachments referenced in notes (e.g., `![[image.png]]`)
  are stored inside the vault. Do not delete or relocate attachment files.
