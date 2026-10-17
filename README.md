# Multi-Stage AI Workflow: Study Guide Creator

Lab: Multi-Stage AI Workflow Across UX Types

## Problem
Creating a good study guide by hand is slow: researching a topic, structuring it, writing detailed notes, and formatting a clean document takes hours.

## Workflow (Chat → IDE → CLI)

| Stage | UX type | Tool | Input | Output |
|---|---|---|---|---|
| 1 | Chat | ChatGPT | Topic | `docs/outline.md` |
| 2 | IDE | VS Code + GitHub Copilot | `docs/outline.md` | `docs/study-guide.md` |
| 3 | CLI | Claude Code | `docs/study-guide.md` | `docs/Study-Guide.pdf` |

## Folder layout
```
AI-Workflow-Study-Guide/
├── README.md
└── docs/
    └── screenshots/   # evidence from each stage
```
