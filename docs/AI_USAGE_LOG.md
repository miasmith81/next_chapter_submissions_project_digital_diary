# AI Usage Log

## Purpose

This log demonstrates intentional AI orchestration. It records why a particular tool and model were selected, what task it received, what judgment remained with me, and how its output was verified.

## Planned tool responsibilities

| AI tool | Primary responsibility | Use it for | Do not use it for |
|---|---|---|---|
| ChatGPT/Codex | Lead planning and implementation partner | Requirements, scoped repository work, documentation, testing, final rubric audit | Blindly making product or security decisions |
| Claude | Independent architecture and code reviewer | Second opinions, complex interaction review, handoff analysis | Duplicating every Codex task |
| GitHub Copilot | Bounded in-editor coding companion | Inline completions, repetitive markup, small focused suggestions | Whole-project architecture decisions without review |
| Gemini | Visual and responsive reviewer | Screenshot review, responsive layout, accessibility observations | Unverified security or privacy claims |
| Perplexity | Cited research assistant | Focused research requiring current external sources | Primary code generation |

## Model-selection strategy

- Use a fast or balanced model for routine planning, formatting, and small implementation tasks.
- Escalate to a stronger reasoning model for architecture, security, difficult debugging, or the final audit.
- Record the exact model name displayed in each product at the time of use.
- Do not claim a model was used unless it actually contributed to the project.
- Do not send the same task to every AI tool merely to increase the tool count.

---

## Entry 1 — Original diary handoff

**AI tool:** Claude  
**Model:** Add the exact model from Claude history  
**Task:** Create a complete handoff describing the original React/Express/Neon diary, visual design, animation, data architecture, known bugs, and unresolved decisions.  
**Why this tool:** Claude had context from the original diary work and was best positioned to summarize it for a new lead planning tool.  
**Result:** A detailed handoff preserved the reusable design and exposed the full-stack assumptions that needed to be compared with the admissions rubric.  
**My judgment:** I decided to preserve the idea, styles, and animation while removing my personal diary content and reassessing the architecture.

---

## Entry 2 — Admissions architecture review

**AI tool:** ChatGPT/Codex  
**Model:** Add the exact model displayed in Codex  
**Mode:** Teaching Mode  
**Task:** Compare the admissions requirements with the original handoff and identify conflicts, risks, and a compliant path.  
**Why this tool:** ChatGPT/Codex was selected as the lead planner for the rebuilt admissions project.  
**Result:** The review identified the GitHub Pages/static-site conflict and the privacy problem with an unauthenticated shared database.  
**What I challenged:** I questioned whether a username/password screen could make `localStorage` secure.  
**Verification:** The security boundary was checked against authoritative guidance.  
**Final decision:** Build a static functional prototype, avoid cosmetic authentication, use non-sensitive demonstration data, and document secure authenticated storage as a future feature.

---

## Entry template

**Date:**  
**Development milestone:**  
**AI tool:**  
**Model:**  
**Mode:** Teaching or Execution  
**Task assigned:**  
**Why this tool/model:**  
**Prompt-history reference:**  
**Output summary:**  
**What I accepted:**  
**What I modified or rejected:**  
**How I verified it:**  
**Files affected:**  
**Related commit:**

