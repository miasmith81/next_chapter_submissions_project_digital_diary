# AI Usage Log

This log records how AI tools supported the project, what each tool was asked to do, and where Mausi retained final decision-making authority. Model names are recorded only when they were confirmed.

## Tool and Agent Strategy

| AI tool or agent | Best use in this project | Why it fits | Current status |
|---|---|---|---|
| ChatGPT | Lead planning, requirements interpretation, interview rubber-ducking, prompt refinement, and explaining tradeoffs | Strong conversational partner for turning Mausi's ideas into a clear plan while preserving her voice | Keep |
| Codex | Repository inspection, implementation, testing, documentation maintenance, file organization, and evidence capture | Works directly with project files and can verify changes against the actual codebase | Keep |
| Claude | Independent architecture and code review | Provides a separate review perspective and can challenge assumptions after an implementation milestone | Keep when independent review adds value; do not use for routine duplicate work |
| Gemini Flash | Generating visual placeholder assets from a detailed creative brief | Appropriate for fast image iterations; outputs still require independent inspection and technical verification | Keep for image generation |

## Model and Token Strategy

- Use a fast, lower-cost model for contained drafting, formatting, classification, and repeated visual iterations.
- Use a stronger reasoning model for architecture decisions, privacy and safety analysis, conflicting requirements, and final reviews.
- Use Codex when the task requires direct knowledge of repository files, implementation, testing, or synchronized documentation.
- Do not ask multiple agents to perform the same task unless a deliberate independent review is needed.
- Record the exact model shown in the tool interface whenever possible. Do not guess model names after the fact.

## Interaction Log

### Claude — Original-project handoff

- Purpose: Summarize the earlier React, Express, and Neon diary build so the reusable visual concept, styling direction, animation ideas, and data approach could be evaluated.
- Output: A handoff report was supplied to ChatGPT/Codex.
- Human decision: Mausi chose to restart the admissions submission as a static project while retaining the original concept and selected design ideas.
- Model: Not confirmed in the available record.

### ChatGPT/Codex — Requirements and architecture review

- Purpose: Compare the original approach with the admissions requirements and identify an appropriate submission architecture.
- Recommendation: Build the admissions prototype with static HTML, CSS, and JavaScript so it can be deployed through GitHub Pages.
- Important correction: A username and password built only in client-side JavaScript would not make localStorage secure. The submission must describe localStorage as prototype persistence, not production protection for sensitive mental-health data.
- Human decision: Mausi accepted the static prototype approach and the transparent privacy limitation.
- Exact model: To be added from the interface if available.

### ChatGPT/Codex — Interview rubber-ducking

- Purpose: Help Mausi articulate the user, problem, value, design choice, minimum viable functionality, and responsible AI workflow in her own voice.
- Method: Mausi answered each question first; ChatGPT helped refine wording; Mausi made the final selection.
- Output: Refined answers are maintained in `INTERVIEW_PREP.md`.

### Gemini — First placeholder-image collection

- Purpose: Generate 12 calming placeholder images representing serenity, peace, love, compassion, and understanding.
- Result: Twelve landscape PNG images were produced with consistent abstract coloring and a visible lower-right AI-generation mark.
- Verification: The first collection was inspected independently. It did not meet the later portrait 4:5 requirement and was treated as an iteration rather than a final asset set.
- Model: Not confirmed in the available record.

### Gemini 1.5 Flash — Second placeholder-image collection

- Purpose: Regenerate the 12 images using a more direct brief for portrait-oriented, cohesive diary artwork.
- Result: Twelve portrait PNG files were produced. The original downloads had generic Gemini filenames.
- Independent verification: The files were 928 x 1152 pixels in RGBA PNG format. That ratio is close to, but not exactly, 4:5. The supplied Gemini report stated 1024 x 1280 and sequential filenames; those claims did not match the downloaded files.
- Naming decision: Deterministic project filenames `frame01.png` through `frame12.png` were selected. Renaming changes file organization only; it does not change image content.
- Disclosure decision: Mausi intentionally accepted the visible lower-right four-point Gemini mark because it clearly signals that the artwork was AI generated.
- Status: Exact 4:5 sizing remains pending.

### ChatGPT/Codex — Exact-size correction prompt

- Purpose: Remove ambiguity from the required image dimensions.
- Output: A detailed prompt requiring exactly 1024 x 1280 pixels for every image is stored in `docs/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.
- Human decision: Mausi will submit the prompt to Gemini and provide the resulting files for verification.

### Codex — Documentation reconstruction

- Purpose: Restore the missing project documentation folder from the latest available project record.
- Result: The root documentation, planning files, interview preparation, AI logs, prompt records, audits, evidence, and prompt templates were reconstructed and packaged together.
- Limitation: The earlier folder was no longer present, so this is a current reconstruction rather than a claim of byte-for-byte recovery of the missing bundle.

## Human Oversight

Mausi is the project orchestrator and final decision-maker. AI tools may suggest, draft, generate, review, or implement, but Mausi determines the project direction, accepts or rejects recommendations, and is responsible for explaining the result. AI-generated claims are independently checked whenever the actual files or code are available.
