---
name: adhd-notes
description: >
  ADHD-optimized note-taking skill for creating concise, scannable conspects from courses, articles, books, and PDFs.
  USE THIS SKILL whenever the user shares learning material to take notes on — a course block, an article, a PDF, a URL, or a topic description.
  Triggers: "make notes", "summarize this block", "take notes on this", "conspect", "last block", "final block", any course/lesson content pasted in chat, any PDF or article shared for learning purposes.
  Produces: a tight, structured conspect in chat (per block) or as a .txt file (final block or article/book).
---

# ADHD Notes Skill

Produces concise, structured conspects optimized for ADHD review: minimal words, maximum signal. No filler. No repetition. No walls of text.

---

## Core principles (always apply)

- **Chunked structure**: Every section is visually separated. No merging of unrelated ideas.
- **One idea per line**: Never stack two concepts in one sentence.
- **Plain language**: If the source used jargon, explain it in one line beneath, in parentheses.
- **No filler**: Cut anything that doesn't add new information. Summaries of summaries are banned.
- **Anchor hooks**: Each section starts with a bolded key term or question — this is the memory hook.
- **Examples stay**: If the source gave a concrete example that clarifies the concept, keep it. Abstract theory without example is harder to recall for ADHD brains.
- **Personal connection flag**: If the user has shared relevant background context and the material connects to something they already know or have done, add a line: `→ connects to: [what it connects to]`. This is a memory anchor. Only use if the connection is real and specific.

---

## Language

- Match the language of the user's request. English request → English notes. If the user writes in another language, match that.
- If the user hasn't specified, default to the language of the source material.
- Personal connection anchors (`→ connects to:`) follow the same language rule.

---

## Input modes

### Mode 1 — Course block (mid-course)
User pastes or describes content from one lesson/block.

**Output**: Conspect in chat only. No file.

Format:
```
## [Course name] — [Block/Lesson name or number]

**[Key concept 1]**
- point
- point
(jargon explanation if needed)
→ connects to: [personal anchor, if applicable]

**[Key concept 2]**
- point
- point

---
⚡ Core takeaway: [one sentence, max 15 words]
❓ Open question / what to check next: [if something was unclear or worth digging into]
```

### Mode 2 — Final course block
User signals this is the last block of a course/topic.

**Output**: Conspect in chat (this block only) + full .txt file with all blocks combined.

For the .txt file:
- Filename: `[course-name]_notes.txt`
- Save to: `/mnt/user-data/outputs/`
- Structure: all blocks in order, same format as Mode 1, separated by `===`
- Add at the top: course name, date, total blocks covered

### Mode 3 — Article or PDF
User shares a URL, pastes article text, or uploads a PDF.

**Output**: .txt file only (no in-chat conspect unless user asks).

For the .txt file:
- Filename: `[topic-slug]_notes.txt`
- Save to: `/mnt/user-data/outputs/`
- Structure:

```
SOURCE: [title or URL]
DATE: [today]

## [Section or main theme 1]

**[Key concept]**
- point
- point
→ connects to: [if applicable]

## [Section 2]
...

---
⚡ Core takeaway: [one sentence]
❓ Worth checking: [gaps, follow-up questions]
```

---

## What to cut (always)

- Introductory fluff ("In this lesson we will explore...")
- Restatements of the same idea in different words
- Motivational filler ("This is important because...")
- Lists longer than 5 items — compress into categories
- Any sentence that could be deleted without losing information

## What to keep (always)

- Definitions of new terms
- Concrete examples
- Numbered processes / steps (preserve the order)
- Warnings or exceptions ("but only if...", "except when...")
- Anything the source emphasized as a common mistake
