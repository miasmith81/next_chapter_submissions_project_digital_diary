# Prompt History

This document captures the material human-AI interactions that shaped the project. It records the purpose, important wording, outcome, human decision, and related evidence. It is a curated admissions record, not a claim that every conversational filler message is reproduced verbatim.

## Prompt 1 — Review requirements and reconsider the original architecture

**Purpose:** Review the Next Chapter admissions requirements, Mausi's written responses, and the original diary handoff; identify a compliant direction while preserving the strongest parts of the original idea.

**Important instructions:** Keep the personal digital-diary concept, remove Mausi's personal entries, let each user personalize the diary, preserve the style and color palette, retain appropriate animation ideas, and document the full process and AI-agent choices.

**Outcome:** The project direction changed from React, Express, and Neon to a static HTML, CSS, and JavaScript prototype suitable for GitHub Pages. The core diary idea and selected design concepts were retained.

**Human decision:** Mausi accepted the reset because it aligned the build with the submission requirements.

## Prompt 2 — Test the localStorage security assumption

**Purpose:** Determine whether a username and password created entirely in the static application would secure diary entries stored in localStorage.

**Outcome:** ChatGPT/Codex explained that JavaScript running on the site can read localStorage and that a client-only login screen does not create production-grade protection. localStorage can support admissions-prototype functionality, but the limitation must be disclosed.

**Human decision:** Mausi agreed to describe the project as a functional prototype rather than a secure mental-health platform.

## Prompt 3 — Rubber-duck interview answers

**Purpose:** Help Mausi explain the intended user, problem, value, diary format, minimum viable functionality, build order, and responsible AI use in clear professional language.

**Process:** Mausi answered first in her own words. ChatGPT suggested refinements. Mausi selected the final wording and meaning.

**Outcome:** The refined current answers are stored in `docs/INTERVIEW_PREP.md`. Questions that require actual build experience remain open until implementation evidence exists.

## Prompt 4 — Generate the first 12 placeholder images

**Purpose:** Ask Gemini to create 12 placeholder images expressing serenity, peace, love, compassion, and understanding for the diary's visual experience.

**Outcome:** Gemini produced a cohesive abstract landscape collection. Independent review found that it did not satisfy the later portrait 4:5 specification.

**Related evidence:** `docs/PLACEHOLDER_IMAGE_AUDIT.md` and, when available, `docs/evidence/Placeholder_Image_Collection_Audit_Report_Gemini.pdf`.

## Prompt 5 — Regenerate the image collection with clearer requirements

**Purpose:** Give Gemini Flash a more detailed, direct brief for 12 cohesive portrait diary images.

**Exact prompt:** Preserved in `docs/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`.

**Outcome:** Gemini created a much stronger portrait collection, but the downloaded filenames were generic and the files were 928 x 1152 instead of an exact 4:5 size.

**Related evidence:** `docs/SECOND_COLLECTION_AUDIT.md` and `docs/evidence/Image_Collection_Verification_Report_Gemini_Second_Iteration.pdf`.

## Prompt 6 — Require exact image dimensions

**Purpose:** Remove all ambiguity about the technical size requirement after the second collection missed exact 4:5 dimensions.

**Exact prompt:** Preserved in `docs/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.

**Required result:** Exactly 12 PNG files, each exactly 1024 pixels wide by 1280 pixels high. No alternate dimensions, near matches, padding, borders, collages, or contact sheets.

**Status:** Awaiting regenerated files and independent verification.

## Prompt 7 — Establish live documentation as a standing rule

**Exact user prompt:**

> Chat every new prompt and update that we do must be captured and all applied docs be updated with every new change and update that I need you to make sure you are doing as we keep building. Question Chat am I going to have to prompt you to update all docs as we keep working or will you put in your memory while working on this project update all docs as new changes happen in live time?

**Outcome:** Live documentation became a standing project workflow. Relevant records must be updated during each material change rather than reconstructed only at the end.

**Implementation:** `AGENTS.md` and `docs/DOCUMENTATION_WORKFLOW.md` encode the repository-level instruction.

## Prompt 8 — Connect Codex directly to the repository workflow

**Exact user prompt:**

> Chat how do we get Codex the ability to update all my docs workflow working with me directly alongside my code?

**Outcome:** The recommended workflow is to open the actual repository as the Codex workspace and keep the documentation files inside that repository. Codex can then inspect code, implement approved work, verify it, and update the related documentation in the same task.

## Prompt 9 — Decide whether Codex needs `prompt-history.md`

**Exact user prompt:**

> chat do I need to give this prompt-history.md to codex

**Outcome:** Yes. `prompt-history.md` should be placed in the repository root. Codex does not need a separate upload when it is already working in that repository because it can read and update the file directly.

## Prompt 10 — Restore the complete documentation folder

**Exact user prompt:**

> chat please give me all the docs and make sure you are give me the most up to date because for some reason i no longer have a docs folder with all the docs

**Outcome:** Reconstructed the latest complete project documentation bundle, added the available source evidence, packaged it as a new ZIP, and performed an archive integrity test.

**Recovery note:** The earlier generated folder was no longer present. This bundle is a current reconstruction from the latest project record and available source files; it is not represented as a byte-for-byte recovery of the missing folder.

## Prompt 11 — Confirm the complete VSCode file structure

**Exact user prompt:**

> Chat can you please show me the whole file structure and what it should look like in my VSCode before I update the files

**Purpose:** Give Mausi a safe visual reference showing where every restored root document, `docs` subfolder, evidence file, prompt file, code folder, and asset folder belongs before she replaces or adds files in VSCode.

**Outcome:** Supplied the complete target repository tree and clarified that the contents of `next_chapter_documentation` should be copied into the existing repository root, not kept as an extra nested folder. Existing `assets`, `css`, `js`, `index.html`, and `LICENSE` files should remain in place.

## Prompt 12 — Audit the current Git diff and synchronize documentation

**Date and stage:** July 22, 2026 — repository and documentation foundation

**AI tool and model:** Codex, GPT-5

**Task type:** Execution Mode; repository audit and documentation synchronization

**Exact user prompt:**

> Review my current Git diff and synchronize every affected project document before making any additional code changes.

**Purpose:** Confirm the repository's current change state and ensure every document affected by that state is synchronized before application-code work resumes.

**Response summary:** Codex inspected the branch, staged changes, unstaged changes, untracked files, recent Git history, and the required living documentation. The repository was clean on `main`, tracking `origin/main`, at commit `c3cc102`; no application-code or pre-existing documentation diff existed to reconcile.

**Human decision:** Mausi required documentation synchronization to happen before any additional code changes. No new product, design, privacy, asset, or scope decision was introduced.

**Verification and outcome:** `git status --porcelain=v1 --branch`, `git diff`, and `git diff --cached` showed no pre-existing changes. This audit was recorded in the prompt history, AI usage log, and build log. No application code was changed. README, project plan, requirements, and asset audits were reviewed but did not require edits because their statuses did not change.

**Files affected:** `prompt-history.md`, `docs/AI_USAGE_LOG.md`, and `BUILD_LOG.md`.

**Related commit:** Pending.

## Ongoing Recording Standard

For every material interaction, add:

1. Sequential prompt number and descriptive title.
2. Date and AI tool/model when confirmed.
3. User purpose and exact prompt when it is important evidence.
4. AI output summary, including mistakes or limitations.
5. Mausi's decision and reasoning.
6. Files changed and verification performed.
7. Open questions or next action.

Sensitive diary content, passwords, secrets, access tokens, and unrelated personal information must never be copied into this record.
