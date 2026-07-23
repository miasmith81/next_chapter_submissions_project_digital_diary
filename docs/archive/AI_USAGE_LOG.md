# AI Usage Log

This log records how AI tools supported the project, what each tool was asked to do, and where Mia retained final decision-making authority. Model names are recorded only when they were confirmed.

## Tool and Agent Strategy

| AI tool or agent | Best use in this project | Why it fits | Current status |
|---|---|---|---|
| ChatGPT | Lead planning, requirements interpretation, interview rubber-ducking, prompt refinement, and explaining tradeoffs | Strong conversational partner for turning Mia's ideas into a clear plan while preserving her voice | Keep |
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
- Human decision: Mia chose to restart the admissions submission as a static project while retaining the original concept and selected design ideas.
- Model: Not confirmed in the available record.

### ChatGPT/Codex — Requirements and architecture review

- Purpose: Compare the original approach with the admissions requirements and identify an appropriate submission architecture.
- Recommendation: Build the admissions prototype with static HTML, CSS, and JavaScript so it can be deployed through GitHub Pages.
- Important correction: A username and password built only in client-side JavaScript would not make localStorage secure. The submission must describe localStorage as prototype persistence, not production protection for sensitive mental-health data.
- Human decision: Mia accepted the static prototype approach and the transparent privacy limitation.
- Exact model: To be added from the interface if available.

### ChatGPT/Codex — Interview rubber-ducking

- Purpose: Help Mia articulate the user, problem, value, design choice, minimum viable functionality, and responsible AI workflow in her own voice.
- Method: Mia answered each question first; ChatGPT helped refine wording; Mia made the final selection.
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
- Disclosure decision: Mia intentionally accepted the visible lower-right four-point Gemini mark because it clearly signals that the artwork was AI generated.
- Status: Exact 4:5 sizing remains pending.

### ChatGPT/Codex — Exact-size correction prompt

- Purpose: Remove ambiguity from the required image dimensions.
- Output: A detailed prompt requiring exactly 1024 x 1280 pixels for every image is stored in `docs/archive/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.
- Human decision: Mia will submit the prompt to Gemini and provide the resulting files for verification.

### Codex — Documentation reconstruction

- Purpose: Restore the missing project documentation folder from the latest available project record.
- Result: The root documentation, planning files, interview preparation, AI logs, prompt records, audits, evidence, and prompt templates were reconstructed and packaged together.
- Limitation: The earlier folder was no longer present, so this is a current reconstruction rather than a claim of byte-for-byte recovery of the missing bundle.

### Codex — AI Agent Prompt Library

- Date: July 22, 2026.
- Assigned responsibility: Create a curated document for recurring agent prompts, examples that produced precise execution, and prompts that produced useful partial or unsuccessful results.
- Why selected: Codex was assigned to preserve repository-level workflows and project-specific prompt lessons beside the chronological prompt record.
- Model: Not confirmed in the available creation record.
- Result: Created `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` and organized reusable prompts, project examples, improvements, verification expectations, and reuse guidance.
- Human direction: Mia requested the artifact and selected its three main categories. The library supplements rather than replaces `docs/prompt_history.md`.
- Verification: The library was reviewed against the existing prompt, audit, privacy, and image-generation records, then linked through the repository instructions and documentation indexes. Its creation and the initial checkpoint were committed as `69c55d2`.

### Codex (GPT-5) — Git diff and documentation synchronization audit

- Date: July 22, 2026.
- Assigned responsibility: Review the complete current Git change state and synchronize all affected project documentation before any additional application-code changes.
- Why selected: Codex can inspect the repository, Git state, and living project documents together.
- Independent verification: The initial `git status --porcelain=v1 --branch`, `git diff`, and `git diff --cached` confirmed that `main` matched `origin/main` at commit `c3cc102` with no changes. Later checks identified the concurrently added prompt library, preserved it, and confirmed that local and remote `main` advanced to commit `69c55d2`.
- Result: No application code required reconciliation. The prompt library was synchronized across every document affected by its introduction, the audit was added to the chronological records, and the completed synchronization was committed as `7cf426a`.
- Human direction: Mia required the documentation-first checkpoint. No AI recommendation changed product scope or requirements, and Mia did not accept or reject new generated application content during this audit.
- Files changed: Documentation only; no HTML, CSS, or JavaScript files were modified.
- Remaining limitation: The audit confirms repository state at the time it ran; future changes require a new synchronization pass.

### Codex (GPT-5) — Documentation naming and archive reorganization

- Date: July 22, 2026.
- Mode: Execution Mode.
- Assigned responsibility: Make the root `README.md` the repository's only file with that name, move the documentation collection under `docs/archive/`, rename both archive indexes, and synchronize all affected references without changing application files.
- Why selected: Codex can inspect and reorganize repository files, preserve Git history as renames, validate relative links, and audit the final change scope.
- Human direction: Mia specified the two index names, required preservation of every document, prohibited application changes, and prohibited committing or pushing.
- Result: Preserved all 18 documentation files formerly under `docs/`, renamed `docs/README.md` to `docs/archive/ARCHIVE_INDEX.md`, renamed the evidence index to `docs/archive/evidence/EVIDENCE_INDEX.md`, and updated affected instructions, paths, indexes, diagrams, prompts, and logs.
- Independent verification: Confirmed one repository-wide `README.md`, root README presence, unchanged documentation file count, valid relative Markdown links, an actual-tree-matching structure diagram, no whitespace errors, and a documentation-only Git change set.
- Files changed: Documentation and documentation paths only; no HTML, CSS, JavaScript, image, or application file was modified.
- Commit: None; Mia explicitly prohibited committing and pushing.

### ChatGPT/Codex — Part 9 verification and reviewer-facing documentation audit

- Date: July 23, 2026.
- Assigned responsibility: Verify the supplied Part 9 Prompt History requirements, inspect the committed repository structure, audit the current collaboration evidence, and implement Mia's approved reviewer-facing documentation strategy.
- Why selected: ChatGPT/Codex could compare the supplied Mission Brief with the repository's prompt records, instructions, links, Git state, and documentation structure.
- Human direction: Mia independently revisited the Technical Pre-Course, corrected the project direction after reviewing the official requirements, defined the prompt-rating and prompt-capture goals, proposed explanations beside README links, and approved the final documentation-only scope.
- Repository baseline: Clean and synchronized with `origin/main` at commit `bbd160e`, which preserved Mia's moves to `docs/BUILD_LOG.md` and `docs/prompt_history.md`.
- Result: Added a Part 9 evidence map, internal prompt-effectiveness ratings, the full Prompt 15 record, a guided README documentation table, and synchronized moved-file references.
- Evidence boundary: Only conversations available in the project record and repository were audited. Separate AI-platform histories were not represented as accessed or complete.
- Verification required: Repository-wide relative Markdown links, README structure accuracy, `git diff --check`, and documentation-only Git scope.
- Commit: None; the completed update is reserved for Mia's review.

### Codex — Applicant-name documentation standardization

- Date: July 23, 2026.
- Assigned responsibility: Apply Mia's project-specific naming and attribution rule consistently across the pending Next Chapter documentation update.
- Human direction: Use `Mia` throughout project documentation and `Mia Smith` only when a full name is needed. Keep naming rules for other organizations, websites, platforms, and conversations separate.
- Result: Standardized project narrative references, corrected the README author attribution, added durable repository instructions, and recorded the decision in the Prompt History and Build Log.
- Privacy choice: The chronological record summarizes the instruction without reproducing name forms that Mia explicitly excluded from this project's documentation.
- Verification required: No excluded nickname or alternate surname remains in project Markdown; all existing documentation, link, formatting, and scope checks must continue to pass.
- Commit: None; the update remains reserved for Mia's review.

## Human Oversight

Mia is the project orchestrator and final decision-maker. AI tools may suggest, draft, generate, review, or implement, but Mia determines the project direction, accepts or rejects recommendations, and is responsible for explaining the result. AI-generated claims are independently checked whenever the actual files or code are available.

A concrete example occurred during the prompt-rating audit. AI had added ratings for several strong prompts but omitted numeric ratings from the unsuccessful-prompt section. Mia reviewed the actual library, detected the inconsistency, required verification, evaluated the proposed correction, and approved the update. This demonstrates that AI completion claims remain subject to Mia's review.

Mia's multi-tool orchestration currently works through deliberate assignment and human-controlled context transfer:

- ChatGPT supports planning, requirements interpretation, teaching, and reflective follow-up.
- Codex inspects and changes the repository, runs checks, and maintains implementation evidence.
- Gemini produces visual iterations that must be independently inspected.
- Claude can provide a separate architecture or code-review perspective when an independent review is useful.
- Mia decides which tool receives each responsibility, transfers the necessary context between separate platforms, compares results, challenges errors, and makes the final project decision.

These tools are not assumed to communicate with one another automatically. Mia is the coordinating layer across them.
