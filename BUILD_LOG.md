# Build Log

This chronological log records significant project decisions, changes, verification results, and next steps. Dates should be expanded with exact dates from Git history when the repository is connected.

## 1. Original concept and reset decision

- Began with a personal digital diary implemented with React, Express, and Neon.
- Completed the admissions prework and reviewed the submission requirements.
- Decided to restart the admissions build as static HTML, CSS, and JavaScript for GitHub Pages compatibility.
- Preserved the core diary idea, visual direction, color palette, animation concept, and ability for users to personalize the diary.
- Removed Mausi's personal diary entries from the submission concept.

## 2. Minimum viable product defined

- Defined the first proof of value as the ability to write an entry, save it, and revisit it later.
- Prioritized working functionality before personalization, images, styling polish, and animation.
- Chose localStorage for prototype persistence.
- Documented that client-side localStorage is not secure storage for sensitive mental-health information and that a client-side username/password screen would not solve that limitation.

## 3. Interview preparation started

- Rubber-ducked the intended user, the problem, the value proposition, the digital-diary choice, and the minimum viable experience.
- Refined answers while preserving Mausi's meaning and voice.
- Deferred implementation-dependent interview questions until real build evidence exists.

## 4. First Gemini image collection

- Prompted Gemini to create 12 calming placeholder images.
- Received 12 landscape images using soft blue, green, peach, and neutral colors.
- Independently inspected the files and retained the audit evidence.
- Determined that the collection did not meet the later portrait 4:5 requirement.

## 5. Second Gemini image collection

- Revised the image prompt to make composition and collection consistency more explicit.
- Received 12 portrait images with generic Gemini filenames.
- Independently verified that the downloaded files were 928 x 1152 RGBA PNGs, not the 1024 x 1280 pixels stated in Gemini's report.
- Defined deterministic filenames `frame01.png` through `frame12.png`.
- Accepted the lower-right Gemini mark as intentional AI-generation disclosure.
- Created a final correction prompt requiring exactly 1024 x 1280 pixels.

## 6. Live documentation rule adopted

- Established a standing project rule: every material prompt, decision, implementation change, verification result, and limitation must be captured as the project progresses.
- Added `AGENTS.md` so Codex working inside the repository follows this documentation workflow.
- Confirmed that `prompt-history.md` belongs in the repository root so Codex can update it alongside the code.

## 7. Documentation folder restored

- The previously generated documentation output was no longer present in the working folder.
- Reconstructed the latest documentation set from the current project record and available source evidence.
- Included planning, requirements, privacy, interview preparation, AI usage, asset briefs, both image audits, exact prompts, source requirements, and workflow instructions.
- Packaged the reconstructed folder as a fresh ZIP and tested the archive before delivery.

## 8. AI Agent Prompt Library added — July 22, 2026

- Mausi requested a dedicated document for recurring prompts, prompts that produced precise execution, and examples that did not work as expected.
- Added `docs/AI_AGENT_PROMPT_LIBRARY.md` as a curated companion to the chronological `prompt-history.md`.
- Organized reusable prompts by agent and purpose, preserved strong and partial project examples, and documented lessons and verification expectations.
- Connected the library to the repository instructions, documentation workflow, README, documentation index, project plan, AI usage log, and prompt history.
- No application feature, requirement, privacy boundary, or visual-asset decision changed.
- The library creation and initial documentation checkpoint were committed as `69c55d2`.

## 9. Git diff and documentation synchronization checkpoint — July 22, 2026

- Mausi required a review of the current Git diff and synchronization of every affected project document before additional application-code changes.
- Verified that `main` initially tracked `origin/main` at commit `c3cc102` with no staged, unstaged, or untracked changes.
- A subsequent status check found the concurrently added `docs/AI_AGENT_PROMPT_LIBRARY.md`; preserved it as user-owned work and reviewed it rather than overwriting or removing it. A later check confirmed that it and the initial checkpoint were committed as `69c55d2` and that local and remote `main` had advanced to that commit.
- Synchronized the repository instructions, documentation workflow, prompt history, AI usage log, build log, README, documentation index, and project plan with the new library.
- Determined that requirements, privacy boundaries, feature implementation, and asset status did not change, so requirement and asset-audit documents did not require artificial edits.
- No application code was changed. The next build actions remain pending.

## Next Build Actions

1. Add the restored documentation to the repository.
2. Generate or resize the 12 images to exactly 1024 x 1280 pixels and verify every output.
3. Build the functional diary flow: create, save, list, open, and revisit an entry.
4. Test the core behavior before adding styling, personalization, imagery, or animation.
5. Record real implementation decisions and use them to complete interview questions 7 and 8.
