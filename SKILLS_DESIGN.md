# Skills Design

This document describes the custom skills built for this OpenClaw assistant, why they exist, and how they are organized.

## Repository layout

    .openclaw/
    ├── workspace/        (assistant identity and configuration files)
    └── skills/           (custom skills, one folder per skill)
        └── study-notes/
            └── SKILL.md  (documented workflow for the skill)

## Design principles

- **One skill, one job.** Each skill solves a single, clearly named problem.
- **Documented workflow.** Every skill has a `SKILL.md` with trigger, steps, inputs, outputs, and an example.
- **No secrets.** Skills never contain API keys, tokens, or credentials.
- **Predictable output.** Each skill defines its output format so results are consistent.

## Skills

### 1. study-notes

| Field | Description |
|-------|-------------|
| **Problem** | Turning long lessons, videos, or articles into short, reviewable study notes. |
| **Trigger** | The user asks to summarize, make notes from, or study a piece of learning material. |
| **Inputs** | Pasted text or a transcript, plus an optional topic name. |
| **Outputs** | Structured notes: key ideas, definitions, a short example, and review questions. |
| **Limits** | Works only on content provided in the chat; does not browse or fetch sources itself. |
| **Location** | `.openclaw/skills/study-notes/SKILL.md` |

## Adding a new skill

1. Create a folder: `.openclaw/skills/<skill-name>/`
2. Add a `SKILL.md` with a name, description, trigger, steps, and an example.
3. Add an entry to the **Skills** section above.
4. Test it in the local chat before committing.

## Future skills (ideas)

- Daily task planner
- Meeting notes summarizer
- Code-explainer for beginners
