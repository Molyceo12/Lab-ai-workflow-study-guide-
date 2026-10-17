# Stage 1 Prompt: Chat (Topic → Outline)

**UX type:** Chat · **Used with:** ChatGPT (works in Gemini, Claude.ai or any chat AI)
**Input:** a topic name · **Output:** `docs/outputs/outline.md`

## How to Use
1. Open a new chat.
2. Replace `{{TOPIC}}` below with your topic (demo: **Agile and Scrum**).
3. Paste the prompt and send it.
4. Copy the Markdown response into `docs/outputs/outline.md`.

## Prompt

```text
You are an expert instructor creating a study guide for beginners.

TASK
Create a structured OUTLINE for a study guide on: {{TOPIC}}

REQUIREMENTS
- 6 to 8 main sections, ordered from fundamentals to advanced
- Each main section has 3 to 5 subtopics
- Under each subtopic, add ONE short line (max 15 words) describing what it should cover
- Do NOT write the full content — this is only the outline

OUTPUT FORMAT (Markdown only, no extra commentary before or after)
# Study Guide: {{TOPIC}}
## 1. <Section title>
### 1.1 <Subtopic>
- <one-line description>
### 1.2 <Subtopic>
- <one-line description>
## 2. <Section title>
...
```

## Expected Output Check
- [ ] Starts with `# Study Guide: <topic>`
- [ ] 6–8 numbered `##` sections, each with numbered `###` subtopics
- [ ] One description line per subtopic
- [ ] No text outside the Markdown outline
