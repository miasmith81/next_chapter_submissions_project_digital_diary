# Build Log

## Project

**Next Chapter Submissions Project — A Digital Diary**

## Purpose of this log

This is a living record of how the application is planned, built, tested, and improved. It should be updated during development rather than reconstructed at the end.

Each entry should explain:

- What I intended to accomplish
- What I changed
- Why I made the decision
- Which AI tool and model assisted me
- What I accepted, changed, or rejected from the AI response
- How I verified the result
- What I learned
- The related Git commit

---

## July 22, 2026 — Requirements review and project reset

### Goal

Review the Next Chapter admissions requirements against my original full-stack digital diary and decide whether the existing architecture matched the submission rubric.

### What I learned

My original application used React, Express, and Neon. The admissions project specifically requires a working HTML, CSS, and JavaScript application deployed through GitHub Pages. GitHub Pages hosts static files and does not run an Express server.

I also identified a privacy problem in the original public deployment plan: one Neon database without authentication would allow visitors to reach the same diary data.

### Decision

I will rebuild the admissions submission as a static functional prototype using HTML, CSS, JavaScript, and browser storage. It will preserve the diary concept, visual identity, responsive layout, and page-turn animation.

The prototype will not claim production-level privacy. It will use non-sensitive demonstration entries and clearly document that entries remain in the current browser and do not synchronize across devices.

### AI collaboration

- ChatGPT/Codex reviewed the rubric against the original architecture.
- I challenged whether a JavaScript username and password could secure `localStorage`.
- After requesting verification, I learned that a client-side login screen does not provide real authentication or authorization.
- I made the final decision to treat the submission as a functional prototype and document authenticated storage as a future production feature.

### Verification

- Compared the architecture with the supplied admissions requirements.
- Verified that the required deployment target is GitHub Pages.
- Reviewed authoritative browser-storage security guidance before deciding the prototype scope.

### Related commit

Add the first commit hash after these documents are added to the repository.

---

## Entry template

### Date and milestone

### Goal

### Work completed

### Decision and reasoning

### AI tool and model

### Prompt or prompt-history reference

### What I accepted, changed, or rejected

### Verification performed

### Bug or unexpected result

### What I learned

### Related commit

