# 08: Lessons Learned

## What Worked Well
- **Fixed output formats made the handoffs smooth.** Because Stage 1's prompt defined the exact heading structure, Stage 2 could keep all 44 headings unchanged, and Stage 3 could build its answer key from the "Quick Check" sections Stage 2 added.
- **Files as handoffs.** Once the outline was in the project, the IDE and CLI tools read it directly from disk, with no more copy and paste.
- **Built-in output checks.** Each prompt file lists what a correct result looks like, so every stage could be verified quickly (for example 35/35 subtopics, 8/8 Quick Checks).
- **Each UX type did what it's best at:** chat for fast structuring, the IDE for editing a large file in place, the CLI for multi-step file work and export.
- **Tool swap worked.** Replacing Claude Code with Gemini CLI needed no changes to the flow.

## What Went Wrong, and How It Was Handled

| Problem | Fix |
|---|---|
| ChatGPT's copied text had escaped bullets (`\-`) | Cleaned when saving `outline.md` |
| Copilot ran in Agent mode (can edit any file) instead of Edit mode | `git status` confirmed only one file changed |
| Claude Code CLI needs a paid plan | Switched Stage 3 to Gemini CLI (free) |
| Gemini Google sign-in failed | Used a free API key from Google AI Studio |
| No pandoc installed for PDF export | Printed HTML to PDF with headless Microsoft Edge |
| Gemini free quota ran out before the last command | Ran the prompt's Edge command manually |
| Gemini CLI was slow (~20 min) on large files | Accepted; a paid tier or a smaller file would be faster |

## Limitations
- **Accuracy isn't guaranteed.** AI-written study notes must be reviewed by a person, especially facts and definitions.
- **The chat stage needs a manual copy and paste** into the project.
- **Free tiers** limit speed and the amount of work per session.
- **Long outputs** may be cut off by some models, which then need a "continue" prompt.

## Improvements for Next Time
1. Use **Edit mode** in Copilot to restrict changes to the attached file.
2. Run Stage 3 in **two smaller prompts** (polish Markdown, then export) to stay within free-tier limits.
3. Include a **ready-made HTML template** so the CLI only fills in content, which is faster and more consistent.
4. Add a **fact-check step**: ask a second AI to review the notes for errors before export.
5. Automate the whole chain with a **script** that runs the CLI stages in sequence.

## Key Takeaway
The workflow's strength comes from the **contracts between stages** (fixed Markdown formats and saved prompts), not from any single AI tool. When one tool failed, another took its place without breaking the chain.
