---
name: study-notes
description: Turn lesson text, transcripts, or articles into structured study notes with key ideas, definitions, an example, and review questions. Use when the user asks to summarize, make notes from, or study learning material.
---

# Study Notes Skill

## Purpose

Help the user learn faster by converting long or dense material into short, well-structured notes they can review later.

## When to use

Use this skill when the user:
- pastes a lesson, article, or video transcript and asks for a summary or notes
- says things like "explain this so I can study it" or "make notes from this"

Do not use it for casual questions that only need a short answer.

## Inputs

- **Required:** the source material (pasted text or transcript)
- **Optional:** topic name, how detailed the notes should be (brief or exhaustive)

## Workflow

1. **Read the material fully** before writing anything.
2. **Identify the topic** and give it a short title.
3. **Extract key ideas** (3 to 7 bullets, each one sentence).
4. **List important terms** with plain-language definitions.
5. **Give one concrete example** that shows the idea in practice.
6. **Write 3 to 5 review questions** the user can use to test themselves.
7. **Offer a next step**, such as a deeper version or a quiz.

## Output format

    # <Topic title>

    ## Key ideas
    - ...

    ## Terms
    - **Term:** definition

    ## Example
    ...

    ## Review questions
    1. ...

## Example

**Input:** a paragraph explaining what an API is.

**Output:**

    # What is an API?

    ## Key ideas
    - An API lets one program request data or actions from another.
    - It defines what you can ask for and what you get back.

    ## Terms
    - **API:** a set of rules for how programs talk to each other.
    - **Endpoint:** a specific address you send a request to.

    ## Example
    A weather app asks a weather service's API for today's forecast and shows the result.

    ## Review questions
    1. What problem does an API solve?
    2. What is an endpoint?

## Rules

- Use only the material provided; do not invent facts.
- Keep language simple and beginner-friendly.
- Never include secrets, keys, or personal data in the notes.
