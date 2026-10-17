# 01: Problem Statement

## The Problem
Making a good study guide by hand is slow and repetitive. A learner has to:

1. Research the topic and decide what matters
2. Organize it into a logical structure
3. Write clear explanations, examples and review questions for every section
4. Format everything into a clean, readable document

For a topic like **Agile and Scrum**, this easily takes **2–3 hours**. Most of that time goes to structuring and formatting, not learning.

## Why It Splits Into Stages
Each step needs a different kind of work, and each kind fits a different AI UX type:

| Stage | Work needed | Best-fit UX type | Why |
|---|---|---|---|
| 1. Outline | Brainstorm and structure the topic | **Chat** | A conversation is ideal for exploring a topic and producing a structured plan quickly |
| 2. Expand | Write detailed notes section by section, inside a file | **IDE** | The AI edits the file in place and sees the whole outline as context |
| 3. Publish | Polish, add a table of contents and summary, export to PDF | **CLI** | The AI can read and write files and run conversion commands on its own |

## The Solution
A three-stage workflow where **each stage's output file becomes the next stage's input**:

```
Topic → [Chat] → outline.md → [IDE] → study-guide.md → [CLI] → Study-Guide.pdf
```

- **Handoffs are plain Markdown files**, so any chat, IDE or CLI AI tool can be swapped in.
- **Prompts are saved and reusable** (see [prompts/](prompts/)), so the workflow works for any topic.
- **A human reviews each output** before it moves to the next stage.

## Scope
- **Topic used for the demo:** Agile and Scrum
- **Input:** a topic name
- **Final output:** a formatted study guide PDF with a title page, table of contents, detailed sections, review questions and a summary

## Success Criteria
- The workflow runs end-to-end from a topic name to a finished PDF
- Each stage's output is used directly as the next stage's input, without rewriting it by hand
- It takes much less time than the manual approach (measured in [07-efficiency.md](07-efficiency.md))
