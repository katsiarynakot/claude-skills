# adhd-notes skill

Skill for Claude that produces concise, scannable conspects optimized for ADHD review.
No filler. No walls of text. Maximum signal per line.

---

## When it triggers

Say any of these and Claude will apply the skill automatically:

- `make notes` / `take notes on this`
- `summarize this block` / `conspect`
- `last block` / `final block`
- Any course/lesson content pasted in chat
- Any PDF or article shared for note-taking

---

## Language

Claude matches the language of your request. English request → English notes. Write in another language → notes in that language.

---

## Three modes

### Mode 1 — Course block (mid-course)
You paste or describe one lesson block.
**Output:** Conspect in chat only.

### Mode 2 — Final course block
You signal it's the last block of a course/topic.
**Output:** Conspect in chat + full `.txt` file with all blocks combined.

### Mode 3 — Article or PDF
You share a URL, paste text, or upload a PDF.
**Output:** `.txt` file only.

---

## Output format

Every conspect follows this structure:

```
## [Course] — [Block name]

**[Key concept]**
- point
- point
(jargon explained simply if needed)
→ connects to: [personal memory anchor, if relevant]

---
⚡ Core takeaway: one sentence, max 15 words
❓ Open question: anything unclear or worth digging into
```

---

## What gets cut

- Intro fluff and motivational filler
- Restatements of the same idea
- Lists longer than 5 items (compressed into categories)
- Anything deletable without information loss

## What stays

- Definitions of new terms
- Concrete examples
- Numbered steps (order preserved)
- Warnings and exceptions
- Common mistakes highlighted by the source
