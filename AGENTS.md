# State of CMS 2026 — Agent Instructions

This repository produces the **State of CMS 2026** report as modular Markdown. Agents must follow the conventions below unless the user explicitly asks otherwise.

## Approach

- **Markdown first.** The report is written in Markdown now; PDF and other exports come later.
- **Modular, not monolithic.** Do not put the full report in a single file. Split by chapter.
- **One canonical TOC.** `TOC.md` at the repo root is the single source of truth for report structure, chapter order, and links.
- **Dedicated chapter files.** Each chapter lives in its own file under `chapters/`.
- **Do not invent content.** Do not create or populate report chapters unless the user explicitly asks. Setting up structure, editing a named chapter, or drafting a specific section is fine when requested.

## Repository layout

All report files live at the **repo root** (not in a `content/` or `docs/` subfolder):

```
/
├── TOC.md                 # Canonical table of contents
├── chapters/              # One markdown file per chapter
│   ├── 01-<slug>.md
│   ├── 02-<slug>.md
│   └── ...
├── AGENTS.md              # This file (Cursor / agent instructions)
└── CLAUDE.md              # Same instructions for Claude Code
```

## File naming

- Prefix chapter files with a zero-padded number matching TOC order: `01-`, `02-`, …
- Use lowercase kebab-case slugs: `04-market-landscape.md`
- Appendix or back matter may use a non-numeric name (e.g. `appendix.md`) if listed in `TOC.md`

## Heading hierarchy

Each chapter file follows this hierarchy:

| Markdown | Role | Scope |
|----------|------|--------|
| `#` | Chapter title | **Once per file** — the chapter name |
| `##` | Major section | Sections within the chapter |
| `###` | Subsection | Nested content under a `##` |
| `####` | Sub-subsection | Use sparingly |

Rules:

- **`TOC.md`** holds the report title (e.g. `# State of CMS 2026`) and the chapter index. Chapter files do **not** repeat the report title.
- Do not use multiple `#` headings in one chapter file.
- When adding a new section, prefer `##` unless it clearly nests under an existing section (`###`).

## Working on the TOC

When chapters are added, removed, or reordered:

1. Update `TOC.md` first.
2. Create, rename, move, or delete the matching file under `chapters/`.
3. Keep numbering and TOC order in sync.

`TOC.md` should include:

- Report title and short description
- Ordered list or table of chapters with links to `chapters/*.md`
- Optional front-matter metadata (version, last updated) for future PDF export

## Working on a chapter

When asked to write or edit a chapter:

1. Read `TOC.md` for context and position in the report.
2. Edit only the relevant file in `chapters/`.
3. Start the file with a single `#` chapter title matching the TOC entry.
4. Use `##` / `###` for structure inside the chapter.
5. Do not duplicate content that belongs in another chapter; link to it if needed.

## What not to do

- Do not create a single `report.md` (or similar) containing the full report.
- Do not scaffold placeholder chapter files unless the user asks for structure setup.
- Do not add build scripts, PDF tooling, or extra docs unless requested.
- Do not change the root-folder layout without user approval.

## Future export (out of scope for now)

PDF and other formats will be generated from `TOC.md` + `chapters/` later. Preserve file order via `TOC.md` so a future build step can concatenate chapters in the correct sequence.
