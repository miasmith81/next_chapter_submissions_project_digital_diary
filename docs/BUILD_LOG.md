# Build Log

This chronological log records significant project decisions, changes, verification results, and next steps. Dates should be expanded with exact dates from Git history when the repository is connected.

## 1. Original concept and reset decision

- Began with a personal digital diary implemented with React, Express, and Neon.
- Completed the admissions prework and reviewed the submission requirements.
- Decided to restart the admissions build as static HTML, CSS, and JavaScript for GitHub Pages compatibility.
- Preserved the core diary idea, visual direction, color palette, animation concept, and ability for users to personalize the diary.
- Removed Mia's personal diary entries from the submission concept.

## 2. Minimum viable product defined

- Defined the first proof of value as the ability to write an entry, save it, and revisit it later.
- Prioritized working functionality before personalization, images, styling polish, and animation.
- Chose localStorage for prototype persistence.
- Documented that client-side localStorage is not secure storage for sensitive mental-health information and that a client-side username/password screen would not solve that limitation.

## 3. Interview preparation started

- Rubber-ducked the intended user, the problem, the value proposition, the digital-diary choice, and the minimum viable experience.
- Refined answers while preserving Mia's meaning and voice.
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
- Initially placed `prompt-history.md` in the repository root so Codex could update it alongside the code. Mia later moved it to `docs/prompt_history.md` and kept it directly linked from the root README.

## 7. Documentation folder restored

- The previously generated documentation output was no longer present in the working folder.
- Reconstructed the latest documentation set from the current project record and available source evidence.
- Included planning, requirements, privacy, interview preparation, AI usage, asset briefs, both image audits, exact prompts, source requirements, and workflow instructions.
- Packaged the reconstructed folder as a fresh ZIP and tested the archive before delivery.

## 8. AI Agent Prompt Library added — July 22, 2026

- Mia requested a dedicated document for recurring prompts, prompts that produced precise execution, and examples that did not work as expected.
- Added `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` as a curated companion to the chronological prompt history, now stored at `docs/prompt_history.md`.
- Organized reusable prompts by agent and purpose, preserved strong and partial project examples, and documented lessons and verification expectations.
- Connected the library to the repository instructions, documentation workflow, README, documentation index, project plan, AI usage log, and prompt history.
- No application feature, requirement, privacy boundary, or visual-asset decision changed.
- The library creation and initial documentation checkpoint were committed as `69c55d2`.

## 9. Git diff and documentation synchronization checkpoint — July 22, 2026

- Mia required a review of the current Git diff and synchronization of every affected project document before additional application-code changes.
- Verified that `main` initially tracked `origin/main` at commit `c3cc102` with no staged, unstaged, or untracked changes.
- A subsequent status check found the concurrently added `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`; preserved it as user-owned work and reviewed it rather than overwriting or removing it. A later check confirmed that it and the initial checkpoint were committed as `69c55d2` and that local and remote `main` had advanced to that commit.
- Synchronized the repository instructions, documentation workflow, prompt history, AI usage log, build log, README, documentation index, and project plan with the new library.
- Determined that requirements, privacy boundaries, feature implementation, and asset status did not change, so requirement and asset-audit documents did not require artificial edits.
- No application code was changed. The next build actions remain pending.
- The completed documentation synchronization was committed as `7cf426a`.

## 10. Documentation naming and archive reorganization — July 22, 2026

- Mia required the direct project root `README.md` to be the repository's only file named `README.md`.
- Inspected a clean repository, later confirmed at `7cf426a`, and found three `README.md` files and 18 files under `docs/` before the change.
- Moved the complete documentation collection under `docs/archive/` without deleting any document.
- Renamed `docs/README.md` to `docs/archive/ARCHIVE_INDEX.md` and the archived evidence `README.md` to `docs/archive/evidence/EVIDENCE_INDEX.md`.
- Updated repository instructions, indexes, Markdown links, repository-relative file references, the root project-structure diagram, prompt history, prompt library, AI usage log, and project plan.
- Verified that exactly one `README.md` remains, all 18 archived documentation files remain present, relative Markdown links resolve, and the Git change set contains no application files.
- No commit or push was performed.

## 11. Documentation location commit and Part 9 collaboration audit — July 23, 2026

- Mia moved the Build Log to `docs/BUILD_LOG.md` and the Prompt History to `docs/prompt_history.md`.
- Mia committed and synchronized those moves with GitHub in commit `bbd160e`.
- Rechecked the supplied Technical Pre-Course Mission Brief and verified that Part 9 requests selected prompts that demonstrate collaboration through planning, curiosity, iteration, debugging, verification, questions, follow-ups, and requests for explanation.
- Audited the current Prompt History and Prompt Library instead of claiming that every prior AI conversation had already been preserved.
- Added a Part 9 collaboration-evidence map while leaving implementation-dependent code-debugging and code-explanation evidence marked pending.
- Added internal `4/5` and `5/5` prompt-effectiveness criteria to the Prompt Library. These are project learning ratings, not official Next Chapter grades.
- Preserved the complete Prompt 15 wording as evidence of Mia verifying the rubric, correcting direction, and defining a reviewer-centered documentation strategy.
- Reworked the root README documentation section into a guided map explaining why each record exists and how it connects to the build.
- Synchronized instructions, indexes, workflows, and references with the committed `docs/` locations.
- Limited the update to documentation and left the changes uncommitted for Mia's review.

## 12. Applicant-name standardization — July 23, 2026

- Mia established a project-specific naming rule for the Next Chapter submission.
- Standardized narrative references throughout the project documentation from the personal nickname to `Mia`.
- Changed the full author attribution from the previously used hyphenated name to `Mia Smith`.
- Added standing instructions requiring `Mia` in project documentation and `Mia Smith` only when a full name is needed.
- Kept this rule limited to the Next Chapter project rather than applying it to unrelated organizations, websites, platforms, or conversations.
- Recorded the decision without reproducing excluded name forms in the chronological prompt record.
- Left the complete documentation update uncommitted for Mia's review.

## 13. Prompt-rating gap detected and corrected — July 23, 2026

- Mia reviewed the completed Prompt Library and noticed that unsuccessful prompts had explanations but no explicit numeric ratings.
- Codex verified that the omission was real rather than assuring Mia that the earlier update was complete.
- Mia reviewed and approved the proposed correction before any files were changed.
- Expanded the internal scale to define `1/5` through `5/5`.
- Clarified that a rating evaluates prompt quality, while AI-output accuracy remains a separate verification question.
- Added explicit ratings and reasons to the precise Gemini examples and all examples in the unsuccessful-prompt section.
- Recorded how Mia caught the gap, challenged the documentation, approved the correction, and orchestrates ChatGPT, Codex, Gemini, and Claude while retaining decision authority.
- Kept the tools' roles accurate: Mia carries context and decisions across separate platforms; the AI tools are not described as automatically communicating with one another.
- Left the correction uncommitted for Mia's review.

## 14. Generator-independent AI-image disclosure rule — July 23, 2026

- Mia questioned whether OpenAI image generation provides visible proof comparable to Gemini's lower-right platform mark.
- Verified the difference between visible disclosure and technical provenance signals such as C2PA Content Credentials and SynthID.
- Identified the post-processing risk: exact-size cropping, resizing, or conversion may remove metadata or reduce detectable provenance.
- Mia decided that the project will not depend on Gemini's mark, an OpenAI provenance signal, or any generator-specific identifier as its only disclosure.
- Added the required visible text `AI-generated artwork — Directed by Mia` to every final AI-created asset.
- Preserved C2PA and SynthID as additional signals to verify on the final file, not assumptions to claim from the original generation.
- Added preservation of original generated exports, final-file provenance checks, honest reporting, and visual approval to the asset workflow.
- Updated the earlier “no readable text” rule with one narrow exception for the required disclosure.
- Changed the asset status so exact dimensions, disclosure placement, provenance reporting, display testing, and final integration all remain pending.

## Next Build Actions

1. Review and commit the synchronized Part 9 documentation update.
2. Generate or resize the 12 images to exactly 1024 x 1280 pixels, apply the visible AI disclosure, preserve the originals, and verify every final output.
3. Build the functional diary flow: create, save, list, open, and revisit an entry.
4. Test the core behavior before adding styling, personalization, imagery, or animation.
5. Record real implementation prompts, debugging, code explanations, decisions, and verification as they occur.
6. Use that evidence to complete interview questions 7 and 8.
