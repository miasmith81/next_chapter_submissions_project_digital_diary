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

**Outcome:** The refined current answers are stored in `docs/archive/INTERVIEW_PREP.md`. Questions that require actual build experience remain open until implementation evidence exists.

## Prompt 4 — Generate the first 12 placeholder images

**Purpose:** Ask Gemini to create 12 placeholder images expressing serenity, peace, love, compassion, and understanding for the diary's visual experience.

**Outcome:** Gemini produced a cohesive abstract landscape collection. Independent review found that it did not satisfy the later portrait 4:5 specification.

**Related evidence:** `docs/archive/PLACEHOLDER_IMAGE_AUDIT.md` and, when available, `docs/archive/evidence/Placeholder_Image_Collection_Audit_Report_Gemini.pdf`.

## Prompt 5 — Regenerate the image collection with clearer requirements

**Purpose:** Give Gemini Flash a more detailed, direct brief for 12 cohesive portrait diary images.

**Exact prompt:** Preserved in `docs/archive/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`.

**Outcome:** Gemini created a much stronger portrait collection, but the downloaded filenames were generic and the files were 928 x 1152 instead of an exact 4:5 size.

**Related evidence:** `docs/archive/SECOND_COLLECTION_AUDIT.md` and `docs/archive/evidence/Image_Collection_Verification_Report_Gemini_Second_Iteration.pdf`.

## Prompt 6 — Require exact image dimensions

**Purpose:** Remove all ambiguity about the technical size requirement after the second collection missed exact 4:5 dimensions.

**Exact prompt:** Preserved in `docs/archive/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.

**Required result:** Exactly 12 PNG files, each exactly 1024 pixels wide by 1280 pixels high. No alternate dimensions, near matches, padding, borders, collages, or contact sheets.

**Status:** Awaiting regenerated files and independent verification.

## Prompt 7 — Establish live documentation as a standing rule

**Exact user prompt:**

> Chat every new prompt and update that we do must be captured and all applied docs be updated with every new change and update that I need you to make sure you are doing as we keep building. Question Chat am I going to have to prompt you to update all docs as we keep working or will you put in your memory while working on this project update all docs as new changes happen in live time?

**Outcome:** Live documentation became a standing project workflow. Relevant records must be updated during each material change rather than reconstructed only at the end.

**Implementation:** `AGENTS.md` and `docs/archive/DOCUMENTATION_WORKFLOW.md` encode the repository-level instruction.

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

## Prompt 12 — Create a curated AI Agent Prompt Library

**Date and stage:** July 22, 2026 — documentation-system improvement

**AI tool and model:** Codex; exact model not confirmed in the available record

**Exact user prompt:**

> Chat I want this prompt to Codex to be stored in an AI Agents prompt doc. I want to create a AI Agent doc that records recurring prompts, prompts that gave me precise execution, and maybe show a few prompts that did not work as well as I was expecting

**Purpose:** Create a reusable prompt library that complements the chronological history by organizing recurring prompts, precise-execution examples, and instructive partial or unsuccessful results.

**Response summary and outcome:** Created `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` with a recording standard, recurring agent prompts, strong project examples, weaker or partial examples, lessons, and reuse guidance. The library was then connected to the repository instructions, documentation workflow, README, documentation index, plan, AI usage log, and build log.

**Human decision:** Mausi requested this new documentation artifact and defined the categories it must preserve. No application requirement or visual decision changed.

**Verification:** Reviewed the library against the chronological prompt record and independently checked that every repository document claiming or governing the new library links to it consistently.

**Files affected:** `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`, `AGENTS.md`, `docs/archive/DOCUMENTATION_WORKFLOW.md`, `README.md`, `docs/archive/ARCHIVE_INDEX.md`, `docs/archive/PROJECT_PLAN.md`, `prompt-history.md`, `docs/archive/AI_USAGE_LOG.md`, and `BUILD_LOG.md`.

**Related commit:** `69c55d2` (library creation and initial documentation checkpoint).

## Prompt 13 — Audit the current Git diff and synchronize documentation

**Date and stage:** July 22, 2026 — repository and documentation foundation

**AI tool and model:** Codex, GPT-5

**Task type:** Execution Mode; repository audit and documentation synchronization

**Exact user prompt:**

> Review my current Git diff and synchronize every affected project document before making any additional code changes.

**Purpose:** Confirm the repository's current change state and ensure every document affected by that state is synchronized before application-code work resumes.

**Response summary:** Codex inspected the branch, staged changes, unstaged changes, untracked files, recent Git history, and the required living documentation. The repository was initially clean on `main`, tracking `origin/main`, at commit `c3cc102`. During the audit, the new untracked `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` appeared as a concurrent change and was committed with the initial checkpoint as `69c55d2`. Codex preserved it, reviewed its claims, and synchronized every document affected by its introduction.

**Human decision:** Mausi required documentation synchronization to happen before any additional code changes. No new product, design, privacy, asset, or scope decision was introduced.

**Verification and outcome:** Initial `git status --porcelain=v1 --branch`, `git diff`, and `git diff --cached` showed no pre-existing changes. Later checks identified the concurrent prompt-library addition and confirmed that local and remote `main` advanced to `69c55d2`. The final documentation diff was checked for whitespace errors and scope. No application code was changed. Requirements and asset audits were reviewed but did not require edits because their statuses did not change.

**Files affected:** `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`, `AGENTS.md`, `docs/archive/DOCUMENTATION_WORKFLOW.md`, `README.md`, `docs/archive/ARCHIVE_INDEX.md`, `docs/archive/PROJECT_PLAN.md`, `prompt-history.md`, `docs/archive/AI_USAGE_LOG.md`, and `BUILD_LOG.md`.

**Related commit:** `7cf426a` (completed documentation synchronization).

## Prompt 14 — Correct documentation naming and archive structure

**Date and stage:** July 22, 2026 — documentation structure correction

**AI tool and model:** Codex, GPT-5

**Task type:** Execution Mode; lossless documentation reorganization and verification

**Exact user prompt:**

> Work in Execution Mode.
>
> Inspect my current repository before changing anything. Correct the documentation naming and file structure so that only one file is named `README.md`, and that file remains at the direct root of the project.
>
> Make these changes:
>
> 1. Keep the root `README.md` exactly where it is.
> 2. Rename `docs/README.md` to `docs/archive/ARCHIVE_INDEX.md`
> 3. Rename `docs/archive/evidence/README.md` to `docs/archive/evidence/EVIDENCE_INDEX.md`
> 4. Do not delete any documentation.
> 5. Update every Markdown link, file reference, project-structure diagram, and Codex instruction affected by these renames.
> 6. Make sure the root README links directly to `docs/archive/ARCHIVE_INDEX.md`.
> 7. Make sure `ARCHIVE_INDEX.md` links to `EVIDENCE_INDEX.md` and every archived document.
> 8. Record this correction as the next numbered entry in `prompt-history.md`.
> 9. Update the AI Agent Prompt Library, AI Usage Log, Build Log, and any other affected documentation.
> 10. Do not modify `index.html`, application code, CSS, JavaScript, images, or unrelated files.
> 11. Do not commit or push anything.
>
> After making the changes, verify:
>
> - Exactly one file in the repository is named `README.md`.
> - The root `README.md` still exists.
> - No documentation files were deleted.
> - Every relative Markdown link points to an existing file.
> - The displayed project structure matches the actual repository.
> - The Git changes contain only the intended documentation reorganization.
>
> Show me the final file structure, the files renamed, the documents updated, the verification results, and the complete Git diff summary.

**Purpose and structure:** Establish unambiguous documentation index names, preserve the root README convention, archive the complete documentation set, and require evidence for preservation, link integrity, structural accuracy, and Git scope.

**Response summary and outcome:** Codex inspected the clean repository, later confirmed the baseline as `7cf426a`, recorded the original 18-file documentation inventory, moved the complete documentation set under `docs/archive/`, renamed both nested README files to dedicated archive-index names, and synchronized every affected instruction, link, file reference, structure diagram, prompt record, and living log.

**Human decision:** Mausi specified the final names and locations, required every document to be preserved, prohibited application changes, and retained final authority over the reorganization.

**Verification:** Exactly one `README.md` remains and it is at the project root; all 18 archived files remain present; every relative Markdown link resolves to an existing target; the root structure diagram matches the actual tree; `git diff --check` passes; and no HTML, CSS, JavaScript, image, or unrelated file appears in the change set.

**Files affected:** Documentation paths and documentation content only, including `AGENTS.md`, `README.md`, `BUILD_LOG.md`, `prompt-history.md`, and the archived documentation collection.

**Related commit:** None; committing and pushing were explicitly prohibited.

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
