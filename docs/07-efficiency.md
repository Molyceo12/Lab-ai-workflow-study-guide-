# 07: Efficiency

## Time Comparison

| Stage | Task | Manual estimate | With the AI workflow | Measured from |
|---|---|---|---|---|
| 1. Chat | Research and structure an 8-section outline | ~30 min | **~1 min** (11:32 → 11:33) | Screenshot timestamps |
| 2. IDE | Write notes, key terms and examples for 35 subtopics, plus 24 review questions | ~3 hrs | **~8 min** (11:53 → 12:01; Copilot ran 2 min 5 s) | Screenshots + Copilot's summary |
| 3. CLI | Title page, table of contents, summary, answer key, formatting, PDF | ~45 min | **~20 min** (12:32 → ~12:52, free tier) | Screenshots + file timestamps |
| **Total** | | **~4 hrs 15 min** | **~30 min** | |

**Roughly 88% less time** (~4 hrs → ~30 min), including handoffs and human review.

> Manual estimates assume a learner writing ~45,000 characters of structured notes (~7,000 words) by hand, at a typical drafting speed plus formatting time.

## Manual Steps Removed
- Researching and deciding the topic structure
- Writing 35 explanations, ~105 key-term definitions and 35 examples
- Writing 24 review questions and their answers
- Building a table of contents and summary
- Formatting and exporting a print-ready PDF

## Manual Steps That Remain
| Step | Time | Why it stays manual |
|---|---|---|
| Copy the ChatGPT response into `outline.md` | < 1 min | Chat tools can't write into the project |
| Review each stage's output | ~2 min per stage | Human quality check (accuracy, completeness) |
| Approve IDE/CLI edits and commands | seconds | Safety: AI changes are confirmed before saving |

## Output Produced in ~30 Minutes
- **716-line** Markdown study guide (~52 KB)
- **33-page** PDF with a title page, table of contents, 8 sections, 35 subtopics, 24 review questions, a summary and an answer key

## Reusability
Because the prompts use a `{{TOPIC}}` placeholder, a new study guide on **any topic** only needs the topic changed in Stage 1, with no new prompt writing. The second run costs the same ~30 minutes.
