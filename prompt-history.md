# Prompt History

## Project

**Next Chapter Submissions Project — A Digital Diary**

## Purpose

This file highlights the prompts that best demonstrate how I plan, question, iterate, debug, and verify work with AI. It is a curated project record, not an unfiltered transcript.

Sensitive personal information, credentials, private diary entries, and authentication codes must never be included.

---

## Prompt 1 — Requirements and architecture review

**Stage:** Planning  
**AI tool:** ChatGPT/Codex  
**Model:** Record the exact model shown in the product interface  
**Mode:** Teaching Mode

### Prompt

Review the Next Chapter admissions requirements and my original digital diary handoff. Help me determine what can be preserved, what conflicts with the rubric, how I should document the build and prompt history, and which AI tools should be assigned to each type of task. Do not generate code yet.

### Why this was a strong prompt

- Supplied both the requirements and the previous-project context.
- Defined the desired outcome.
- Established a no-code boundary.
- Asked for architecture, documentation, and AI-tool decisions rather than code generation alone.

### Result and decision

The review identified a conflict between the original React/Express/Neon architecture and the static GitHub Pages requirement. I decided to rebuild the admissions version as a static functional prototype while preserving the diary design and animation.

### Verification

I compared the recommendation against the actual submission checklist and deployment requirement.

---

## Prompt 2 — Challenge the storage recommendation

**Stage:** Security and scope decision  
**AI tool:** ChatGPT/Codex  
**Mode:** Teaching Mode

### Prompt

If I use `localStorage` instead of a cloud database, can I create a username and password model that is enough to keep each user's saved mental-health diary data secure?

### Why this was an important follow-up

The prompt did not automatically accept the first architecture recommendation. It questioned a security assumption before implementation.

### Result and decision

I learned that a JavaScript-only login screen would not provide real authentication because JavaScript on the same website can access the browser storage. I decided not to build cosmetic security or claim that the prototype is production-secure.

### Verification

The answer was checked against authoritative browser-storage security guidance.

---

## Prompt 3 — Interview rubber-ducking

**Stage:** Interview preparation  
**AI tool:** ChatGPT/Codex  
**Mode:** Teaching Mode

### Prompt

Rubber-duck the possible admissions interview questions with me one question at a time. Help me separate the problem, value, and solution, preserve my voice, identify anything missing, and wait for me to explain each idea in my own words before refining the answer.

### Why this was a strong prompt

- Defined a step-by-step learning process.
- Protected my ownership of the answers.
- Asked AI to identify gaps rather than replace my thinking.
- Produced explanations I can genuinely defend in an interview.

### Result

Questions about the problem, user value, solution choice, build order, AI collaboration, and challenging an AI recommendation were developed and refined. Bug and verification answers were intentionally postponed until evidence exists from the build.

---

## Prompt-entry template

**Prompt number and title:**  
**Date:**  
**Development stage:**  
**AI tool:**  
**Model:**  
**Mode:** Teaching or Execution  

### Goal

### Complete prompt

### Why I wrote the prompt this way

### AI response summary

### Follow-up prompt

### What I accepted

### What I changed or rejected

### Files affected

### How I verified the result

### Related commit

