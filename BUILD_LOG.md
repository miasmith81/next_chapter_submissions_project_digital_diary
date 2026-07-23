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

## July 22, 2026 — Generate and audit Gemini placeholder images

### Goal

Create 12 cohesive, non-personal placeholder images that support the diary's themes of serenity, peace, love, compassion, and understanding.

### Decision and reasoning

I assigned this bounded visual-generation task to Gemini because it can generate and review visual assets. ChatGPT/Codex prepared the constraints and documentation so the task remains connected to the project's established palette, layout, privacy boundaries, and file structure.

The images must be separate portrait-oriented artworks rather than one collage. They must not contain text, logos, identifiable people, personal photographs, medical claims, crisis imagery, or a built-in polaroid border because the application's CSS will create the frame.

### Planned output

- 12 separate image files
- Consistent soft painterly or illustrated visual style
- Purple, blue, lilac, white, and subtle warm-gold palette
- Portrait 4:5 composition
- Final names `frame01.png` through `frame12.png`
- Final location `assets/frames/`

### AI collaboration

- **Gemini:** Generate the 12 visual assets from the approved prompt.
- **ChatGPT/Codex:** Define constraints, document the prompt, and later help review file consistency and integration readiness.
- **My responsibility:** Select the Gemini model, submit the prompt, review every image, reject or revise unsuitable results, rename approved files, and make the final decision about what enters the repository.

### Work completed

Gemini returned 12 separate abstract images and a three-page verification report. ChatGPT/Codex independently checked the report and files instead of accepting the self-audit as final verification.

### Verification performed

- Confirmed 12 distinct files using SHA-256 hashes.
- Confirmed every file is an 8-bit RGBA PNG.
- Confirmed consistent 1376 x 768 dimensions.
- Rendered all three PDF pages and checked that the report was readable and free of clipping or broken layout.
- Compared the files and Gemini's claims with the full approved brief.
- Visually checked for text, personal content, faces, medical claims, crisis content, built-in borders, and unintended marks.

### Unexpected result

Gemini's report concluded that all prompt criteria were satisfied, but its checklist omitted several requirements from the original prompt. All 12 files are landscape rather than portrait 4:5, use concept names rather than `frame01.png` through `frame12.png`, replace the approved scene list, and contain a repeated four-point star or watermark-like mark in the lower-right. The exact Gemini model was not included. The report's descriptions for `noor.png` and `consensus.png` also appear inconsistent with the supplied visuals.

### Decision

The first collection is not approved for repository integration. Its cohesive abstract direction and emotionally safe content are useful, but the current recommendation is to request a corrected second iteration. Mausi retains the final approval decision. No images were added to `assets/frames/`.

### What I learned

An AI-generated verification report is evidence of the tool's process, not independent proof that every original requirement was met. I need to compare the actual outputs with the complete prompt, document mismatches, and decide whether to accept, revise, or reject the result.

### Related prompt

See Prompts 4 and 5 in `prompt-history.md`, `docs/ASSET_GENERATION_BRIEF.md`, and `docs/PLACEHOLDER_IMAGE_AUDIT.md`.

### Related commit

Add the commit hash after the approved image assets are added and verified.

---

## July 22, 2026 - Audit the second Gemini collection and correct filenames

### Goal

Generate a second image collection that follows the approved portrait concepts and determine what remains before the assets can enter the repository.

### Work completed

- Gemini 1.5 Flash generated 12 new portrait PNG images matching the requested concepts and purple/lavender painterly direction.
- Gemini supplied a four-page verification report.
- ChatGPT/Codex rendered and inspected the report, reviewed the images, and checked the actual file metadata.
- Codex created renamed copies as `frame01.png` through `frame12.png` in the approved theme order.
- Codex verified that each renamed copy was byte-for-byte identical to its original and tested the renamed-image ZIP.
- ChatGPT/Codex prepared a focused prompt for exact-size correction.

### Unexpected result

Gemini's report stated that the images were already named `frame01.png` through `frame12.png` and measured 1024 x 1280 pixels. The delivered files actually used Gemini-generated filenames and measured 928 x 1152 pixels.

This reinforced the need to inspect the actual output files instead of relying only on an AI-generated verification report.

### Decision and reasoning

Mausi accepted the visual concepts, palette, style, and emotionally safe content. She also intentionally accepted the lower-right Gemini platform mark because it protects attribution and tells users that the artwork was AI-generated. This supersedes the earlier no-watermark requirement.

The naming problem did not require another generative-AI iteration. Codex handled it as a deterministic file-organization task. The only remaining image requirement is exact 1024 x 1280 sizing.

### AI collaboration

- **Gemini 1.5 Flash:** Generated the visual collection and supplied its verification report.
- **ChatGPT/Codex:** Independently audited the files and report, corrected the filenames, preserved the originals, verified copy integrity, documented the decision change, and prepared the exact-size prompt.
- **Mausi:** Reviewed the visible watermark, approved it as disclosure, and retained the final asset-approval decision.

### Verification performed

- Confirmed exactly 12 separate PNG files.
- Confirmed all files are 928 x 1152 portrait RGBA PNGs.
- Confirmed all 12 required visual concepts are represented in order.
- Confirmed a cohesive purple/lavender/blue/white/gold painterly system.
- Confirmed no readable text, personal information, medical claims, crisis scenes, or built-in polaroid frames.
- Confirmed renamed copies match the source files byte-for-byte.
- Confirmed the renamed ZIP contains all 12 files and has no archive errors.

### Remaining work

Submit the exact-size prompt, inspect the actual returned files, and require 1024 x 1280 metadata before repository integration.

### What I learned

AI orchestration includes assigning non-generative work to the right tool. Gemini produced the artwork; Codex handled deterministic naming and independent verification. I also learned that project requirements can change through a documented human decision, as with accepting the AI watermark for transparency.

### Related documentation

- `docs/SECOND_COLLECTION_AUDIT.md`
- `docs/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`
- `docs/prompts/GEMINI_EXACT_SIZE_PROMPT.md`
- Prompts 5 and 6 in `prompt-history.md`

### Related commit

Add after the final correctly sized images are integrated and committed.

---

## July 22, 2026 - Adopt live documentation as a standing project rule

### Goal

Ensure every material prompt, requirement change, AI output, verification result, and project decision is documented during development without requiring Mausi to repeat the instruction.

### Decision and reasoning

Documentation is now part of the definition of done for every material project task. The repository files, rather than conversational memory alone, will serve as the durable submission record.

### Work completed

- Added `AGENTS.md` with standing instructions for future project AI work.
- Added `docs/DOCUMENTATION_WORKFLOW.md` with triggers, affected documents, prompt-capture standards, and an end-of-work checklist.
- Updated the current documentation for the second Gemini iteration, Codex filename correction, watermark decision, and exact-size prompt.
- Preserved Gemini's second report under `docs/evidence/`.
- Preserved the complete Gemini prompts under `docs/prompts/`.

### Verification

Reviewed the documentation set for outdated status statements and rebuilt the downloadable archive after the updates.

### What I learned

Project memory is strongest when it is written into version-controlled files that travel with the repository. Platform memory and conversation history can support continuity, but submission evidence should remain in the project.

### Related prompt

See Prompt 7 in `prompt-history.md`.

### Related commit

Add after these documentation files are committed to the repository.

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
