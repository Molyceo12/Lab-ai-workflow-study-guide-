# 06: Adaptability

The workflow is designed around **UX types, not specific products**. Every stage can be swapped for another tool of the same type without changing the prompts, the files or the flow.

## Proven During This Lab
The planned Stage 3 tool (Claude Code CLI) needed a paid plan. It was replaced with **Gemini CLI** using the **same prompt and the same input file**, and the workflow still produced the final PDF. That's a real tool swap mid-project, with no redesign.

## Tool Swap Table

| Stage | UX type | Used | Drop-in alternatives |
|---|---|---|---|
| 1. Outline | Chat | ChatGPT | Gemini, Claude.ai, Microsoft Copilot, Perplexity |
| 2. Expand | IDE | VS Code + GitHub Copilot | Cursor, Windsurf, JetBrains AI Assistant, VS Code + Gemini Code Assist |
| 3. Publish | CLI | Gemini CLI | Claude Code, GitHub Copilot CLI, Aider |
| PDF export | Any | Microsoft Edge (headless) | pandoc, Chrome headless, wkhtmltopdf, "Print to PDF" in any browser |

## What Makes It Portable

| Design choice | Why it keeps the workflow tool-agnostic |
|---|---|
| **Plain Markdown handoffs** (`outline.md`, `study-guide.md`) | Every AI tool can read and write Markdown; no proprietary formats |
| **Prompts saved as files** ([prompts/](prompts/)) | Copy and paste into any provider; nothing depends on one tool's features |
| **`{{TOPIC}}` placeholder** | The same prompts work for any subject, not just Agile and Scrum |
| **Fixed output format in every prompt** | Each stage knows exactly what it receives, whichever model produced it |
| **Output checks in every prompt file** | Results can be verified the same way whatever tool generated them |
| **Fallback built into the Stage 3 prompt** | "Use any tool available", with an HTML-to-PDF tip if pandoc is missing |

## Limitations
- The **chat → file** handoff is a manual copy and paste, because chat tools can't write into the project.
- Output **length and quality vary by model**: a weaker model may need the Stage 2 prompt run one section at a time.
- **Free tiers** (Gemini API) can be slow or hit quota limits on large files.
