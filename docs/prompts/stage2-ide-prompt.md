# Stage 2 Prompt: IDE (Outline → Study Notes)

**UX type:** IDE · **Used with:** VS Code + GitHub Copilot Chat (works in Cursor, Windsurf or any IDE AI)
**Input:** `docs/outputs/outline.md` · **Output:** `docs/outputs/study-guide.md`

## How to Use
1. Copy `docs/outputs/outline.md` to `docs/outputs/study-guide.md`.
2. Open `study-guide.md` in VS Code.
3. Open Copilot Chat in **Edit / Agent mode** and attach the file as context.
4. Paste the prompt below. For long outlines, run it one `##` section at a time.
5. Review and accept the edits, then save.

## Prompt

```text
You are editing the open file study-guide.md, which contains a study guide OUTLINE.

TASK
Expand the outline into full study notes, editing the file in place.

RULES
- Keep every existing heading (#, ##, ###) exactly as it is, in the same order
- Replace each one-line description under a ### subtopic with:
  1. **Explanation** — 2 to 4 clear paragraphs for a beginner
  2. **Key Terms** — a bullet list of important terms with short definitions
  3. **Example** — one practical, real-world example
- At the end of each ## section, add:
  #### Quick Check
  - 3 short review questions (no answers)
- Use plain Markdown only (no HTML), and keep a consistent style throughout
- Do not add a table of contents, title page or summary — a later stage does that
```

## Expected Output Check
- [ ] All original headings are unchanged
- [ ] Every subtopic has an Explanation, Key Terms and an Example
- [ ] Every section ends with a Quick Check
- [ ] Plain Markdown, with no table of contents or summary yet
