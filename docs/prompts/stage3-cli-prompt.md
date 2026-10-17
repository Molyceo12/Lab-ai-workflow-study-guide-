# Stage 3 Prompt: CLI (Study Notes → PDF)

**UX type:** CLI · **Used with:** Gemini CLI (works in Claude Code, GitHub Copilot CLI or any CLI AI)
**Input:** `docs/outputs/study-guide.md` · **Output:** `docs/outputs/Study-Guide.pdf`

## How to Use
1. Open a terminal in the project folder.
2. Start the CLI AI (for example `gemini`).
3. Paste the prompt below.
4. Approve the file edits and commands it asks to run.
5. Open the PDF and check it.

## Prompt

```text
Read docs/outputs/study-guide.md. It contains detailed study notes in Markdown.

TASK
Turn it into a polished, print-ready study guide and export it as a PDF.

STEPS
1. Add at the top:
   - A title page: the guide title, a one-line subtitle, and today's date
   - A table of contents listing every ## section
2. Add at the end:
   - ## Summary — 5 to 8 bullet points covering the most important ideas
   - ## Answer Key — short answers to every "Quick Check" question in the guide
3. Clean up formatting: consistent heading levels, spacing, bullet style; fix typos
4. Save the polished Markdown back to docs/outputs/study-guide.md
5. Convert it to docs/outputs/Study-Guide.pdf using any tool available on this
   machine (e.g. pandoc, or render to HTML and print to PDF). Use readable
   fonts, page margins, and a page break before each ## section.
   Tip: if pandoc is not installed, write a styled docs/outputs/study-guide.html
   and print it with a headless browser, e.g. on Windows:
   & "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="<full path>\docs\outputs\Study-Guide.pdf" "<full path>\docs\outputs\study-guide.html"
6. Confirm the PDF exists and report its page count.

RULES
- Do not change the meaning of the content
- Do not delete any section
```

## Expected Output Check
- [ ] Title page and table of contents at the start
- [ ] Summary and Answer Key at the end
- [ ] `Study-Guide.pdf` opens with readable layout and page breaks
- [ ] No sections lost compared with `study-guide.md`
