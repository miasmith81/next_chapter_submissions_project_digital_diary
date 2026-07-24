# Prompt History

This document captures the material human-AI interactions that shaped the project. It records the purpose, important wording, outcome, human decision, and related evidence. It is a curated admissions record, not a claim that every conversational filler message is reproduced verbatim.

## Part 9 Collaboration Evidence Map

The admissions requirements ask for selected prompts that best demonstrate how Mia collaborates with AI. The examples below map the current record to the habits reviewers identified.

| Reviewer signal | Current evidence | What it demonstrates |
| --- | --- | --- |
| Planning | Prompts 1, 3, 11, 13, 14, 15, and 19 | Defining the MVP, build order, documentation system, repository structure, reviewer experience, and responsible AI-asset disclosure before implementation |
| Feature requests | Prompts 1, 3, 4, 5, and 6 | Defining the diary experience, interview-support needs, and visual-asset requirements while separating requested features from verified completion |
| Curiosity and questions | Prompts 2, 8, 9, 15, and 19 | Testing assumptions, asking how Codex should work beside the code, checking official requirements, and questioning how viewers can verify that artwork was AI-generated |
| Iteration | Prompts 4, 5, 6, 12, 14, 15, and 17 | Improving image prompts, strengthening documentation, correcting structure, refining the prompt-history strategy, and learning from prompts that did not work |
| Debugging | Prompts 4 through 6 | Investigating why generated assets missed orientation, naming, and exact-size requirements; application-code debugging will be added from real build work |
| Verification | Prompts 2, 5, 6, 13, 14, 15, 18, and 19 | Challenging security assumptions, inspecting actual files instead of trusting AI reports, checking Git state, validating links, comparing the project with the rubric, auditing approved documentation, and separating visible disclosure from technical provenance |
| Follow-up questions | Prompts 6, 8, 9, 15, and 18 | Building on prior answers, checking the completed documentation, and requiring correction instead of treating each AI response as final |
| Unsuccessful prompts and lessons | Prompts 4 through 6, 17, and 18 | Preserving what did not work, identifying missing instructions or documentation, rating prompt quality honestly, and showing how the next prompt or update improved |
| Human judgment and orchestration | Prompts 2, 13, 15, 18, and 19 | Assigning responsibilities across AI tools, challenging recommendations, catching omissions, setting responsible disclosure requirements, approving corrections, and retaining final decision authority |
| Requests to explain code | Pending implementation | These will be recorded when Mia begins building, reviewing, and debugging the HTML, CSS, and JavaScript |

This map will grow from real project work. Categories marked pending are not represented as complete before supporting conversations and code evidence exist.

## Prompt 1 — Review requirements and reconsider the original architecture

**Purpose:** Review the Next Chapter admissions requirements, Mia's written responses, and the original diary handoff; identify a compliant direction while preserving the strongest parts of the original idea.

**Important instructions:** Keep the personal digital-diary concept, remove Mia's personal entries, let each user personalize the diary, preserve the style and color palette, retain appropriate animation ideas, and document the full process and AI-agent choices.

**Outcome:** The project direction changed from React, Express, and Neon to a static HTML, CSS, and JavaScript prototype suitable for GitHub Pages. The core diary idea and selected design concepts were retained.

**Human decision:** Mia accepted the reset because it aligned the build with the submission requirements.

## Prompt 2 — Test the localStorage security assumption

**Purpose:** Determine whether a username and password created entirely in the static application would secure diary entries stored in localStorage.

**Outcome:** ChatGPT/Codex explained that JavaScript running on the site can read localStorage and that a client-only login screen does not create production-grade protection. localStorage can support admissions-prototype functionality, but the limitation must be disclosed.

**Human decision:** Mia agreed to describe the project as a functional prototype rather than a secure mental-health platform.

## Prompt 3 — Rubber-duck interview answers

**Purpose:** Help Mia explain the intended user, problem, value, diary format, minimum viable functionality, build order, and responsible AI use in clear professional language.

**Process:** Mia answered first in her own words. ChatGPT suggested refinements. Mia selected the final wording and meaning.

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

**Superseded location decision:** On July 23, 2026, Mia intentionally moved the file to `docs/prompt_history.md` and kept it directly linked from the root README. The historical outcome above remains unchanged as a record of the earlier recommendation.

## Prompt 10 — Restore the complete documentation folder

**Exact user prompt:**

> chat please give me all the docs and make sure you are give me the most up to date because for some reason i no longer have a docs folder with all the docs

**Outcome:** Reconstructed the latest complete project documentation bundle, added the available source evidence, packaged it as a new ZIP, and performed an archive integrity test.

**Recovery note:** The earlier generated folder was no longer present. This bundle is a current reconstruction from the latest project record and available source files; it is not represented as a byte-for-byte recovery of the missing folder.

## Prompt 11 — Confirm the complete VSCode file structure

**Exact user prompt:**

> Chat can you please show me the whole file structure and what it should look like in my VSCode before I update the files

**Purpose:** Give Mia a safe visual reference showing where every restored root document, `docs` subfolder, evidence file, prompt file, code folder, and asset folder belongs before she replaces or adds files in VSCode.

**Outcome:** Supplied the complete target repository tree and clarified that the contents of `next_chapter_documentation` should be copied into the existing repository root, not kept as an extra nested folder. Existing `assets`, `css`, `js`, `index.html`, and `LICENSE` files should remain in place.

## Prompt 12 — Create a curated AI Agent Prompt Library

**Date and stage:** July 22, 2026 — documentation-system improvement

**AI tool and model:** Codex; exact model not confirmed in the available record

**Exact user prompt:**

> Chat I want this prompt to Codex to be stored in an AI Agents prompt doc. I want to create a AI Agent doc that records recurring prompts, prompts that gave me precise execution, and maybe show a few prompts that did not work as well as I was expecting

**Purpose:** Create a reusable prompt library that complements the chronological history by organizing recurring prompts, precise-execution examples, and instructive partial or unsuccessful results.

**Response summary and outcome:** Created `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` with a recording standard, recurring agent prompts, strong project examples, weaker or partial examples, lessons, and reuse guidance. The library was then connected to the repository instructions, documentation workflow, README, documentation index, plan, AI usage log, and build log.

**Human decision:** Mia requested this new documentation artifact and defined the categories it must preserve. No application requirement or visual decision changed.

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

**Human decision:** Mia required documentation synchronization to happen before any additional code changes. No new product, design, privacy, asset, or scope decision was introduced.

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

**Human decision:** Mia specified the final names and locations, required every document to be preserved, prohibited application changes, and retained final authority over the reorganization.

**Verification:** Exactly one `README.md` remains and it is at the project root; all 18 archived files remain present; every relative Markdown link resolves to an existing target; the root structure diagram matches the actual tree; `git diff --check` passes; and no HTML, CSS, JavaScript, image, or unrelated file appears in the change set.

**Files affected:** Documentation paths and documentation content only, including `AGENTS.md`, `README.md`, `BUILD_LOG.md`, `prompt-history.md`, and the archived documentation collection.

**Related commit:** None; committing and pushing were explicitly prohibited.

## Prompt 15 — Verify Part 9 and strengthen the reviewer-facing AI collaboration record

**Date and stage:** July 23, 2026 — admissions-requirement verification and documentation strategy

**AI tool and model:** ChatGPT/Codex; exact interface model not independently confirmed in the project record

**Task type:** Planning, curiosity, iteration, verification, and documentation review

**Exact user prompt:**

> Chat I need to apologize. I am sorry I kinda over reacted because I went back and went to the Technical Pre-Course online and went through of the requirements of the project and it seems like we are staying in scope with just additional documentation which I love and want to keep tracking and updating along with the required docs. Really the only thing that I updated was the archive folder was in the docs folder like this docs/archive and the archive folder was not underneath the docs folder so I fixed that. So what I would like us to make sure we are and keep doing is keep track of my prompt history and recurring or prompts that gave a 5 out of 5 star or even 4 out of 5 lets show what the actual prompt was in our prompt file AI_AGENT_PROMPT_LIBRARY but the really important prompts to follow that they are looking for is verify this but in Part 9 Prompt History requirements the reviewer is looking at prompts that best demonstrate your thinking throughout the project: examples might include: Planning prompts, Feature requests, Debugging conversations, Questions you asked AI, Follow-up questions, Times you asked AI to explain code. Why they are asking for this...they are looking for evidence of how I collaborate with AI. They are saying that strong prompt histories often demonstrate: planning, curiosity, iteration, debugging, verification. So lets keep tracking my prompt history and saving really good prompts in the prompt library but the requirements I just spoke to you about lets make sure we really make sure we can show that prompt history. When I start building the actual code with Codex we will have a lot of the prompting history they are looking for too. I need you to look at I updated our file structure and update the README. So I would like to know your option about this I idea I have: (I also want and hope you have been documenting our interaction and how we have been interacting. If you feel you have fell short on documenting our interaction and my interactions with my other AI Tools please go back in our conversations and update our doc.) I have additional documentation which I think is going to make me stand out and I love that so thank you for following my vision and direction and what I wanted the reviewer to see how I can document all of my interactions with my AI tools and really be detailed about it. But what I was thinking is that maybe I could have an explanation next to the linked page describing the document and why I have it and what its documenting and maybe how it relates to the build of the project and how it could help another developer see my whole vision of the project and the relationship I have with my AI Tools. Now if you can review and respond to everything step by step.

**Follow-up approval:**

> Chat that was beautifully put of my direct prompt and direction and correction of the direction and framework of the project. Yes I approve the update and also I committed my move of docs and synced to GitHub. Please update all that we discussed and then show me the update so I can review. Thank you.

**Purpose and thinking demonstrated:** Mia independently returned to the Technical Pre-Course, verified the official Part 9 language, corrected her earlier concern, and redirected the documentation toward the evidence reviewers actually requested. She distinguished the chronological prompt history from the reusable prompt library and proposed adding explanations that connect each document to the build and to future developers.

**Response summary:** Codex verified the supplied Mission Brief, inspected the committed repository, audited the prompt history and prompt library, identified stale references created by the document moves, and proposed a reviewer-oriented README documentation table, a Part 9 evidence map, and an internal `4/5` and `5/5` prompt-effectiveness framework.

**Human decision:** Mia approved the documentation-only update, confirmed that she had committed and synchronized the document moves in commit `bbd160e`, and requested the final changes for review.

**Verification:** The update must preserve Mia's chosen `docs/` locations, repair every affected link and instruction, update only documentation, pass a repository-wide relative Markdown-link audit and `git diff --check`, and remain uncommitted for Mia's review.

**Files affected:** `README.md`, `AGENTS.md`, `docs/prompt_history.md`, `docs/BUILD_LOG.md`, `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`, `docs/archive/AI_USAGE_LOG.md`, `docs/archive/ARCHIVE_INDEX.md`, `docs/archive/DOCUMENTATION_WORKFLOW.md`, and `docs/archive/PROJECT_PLAN.md`.

**Open evidence boundary:** Codex can preserve conversations available in the current project record and repository. Separate ChatGPT, Claude, Gemini, or other AI conversations cannot be claimed as reviewed unless Mia supplies or connects those records.

## Prompt 16 — Standardize the applicant name for the Next Chapter project

**Date and stage:** July 23, 2026 — project identity and documentation governance

**AI tool:** Codex

**Task type:** Documentation correction and project-specific attribution rule

**User direction summary:** Mia clarified that personal conversational naming and public project attribution serve different purposes. For this Next Chapter submission, every narrative reference should use `Mia`, and every full-name attribution should use `Mia Smith`. The rule applies specifically to this project and should not be generalized to unrelated organizations, websites, platforms, or conversations.

**Why the exact prompt is not reproduced:** The original instruction contains name forms that Mia explicitly asked to remove from this project's documentation. Preserving those forms here would contradict the approved project-specific naming rule.

**Human decision:** Mia wants to be presented as an individual applicant, separate from another applicant, using her legal name for this submission.

**Response and outcome:** Codex audited all project Markdown, standardized narrative references, corrected the README author line, added durable naming instructions, and updated the Prompt Library, AI Usage Log, Build Log, workflow, and scope documentation.

**Verification:** Search all project Markdown for excluded name forms; confirm the author is `Mia Smith`; preserve all pending Part 9 documentation work; re-run relative-link, formatting, README-count, and documentation-only scope checks.

## Prompt 17 — Preserve unsuccessful prompts and explain why they did not work

**Date and stage:** July 23, 2026 — prompt-history strategy refinement

**AI tool:** Codex

**Task type:** Iteration, reflection, and documentation improvement

**Exact user prompt:**

> Another thing I was just thinking is that lets remember to also document bad prompts and explanation of why it was a bad prompt going back to the project requirements also stating what prompts didn't work. Could you update the prompt history with this realization?

**Requirement clarification:** Part 9 does not explicitly require a section labeled “bad prompts.” It asks for selected prompts that demonstrate Mia's thinking, and it identifies iteration, debugging, and verification as signs of strong AI collaboration. Preserving prompts that did not work—along with the reason, correction, and verified result—is strong evidence of those behaviors.

**Why this realization matters:** A prompt history made up only of polished successes can hide the actual problem-solving process. An unsuccessful or incomplete prompt becomes useful evidence when the record explains:

1. What result Mia expected.
2. What the AI actually produced.
3. Which instruction, constraint, assumption, or acceptance criterion was missing or unclear.
4. How Mia questioned, corrected, or rewrote the prompt.
5. Whether the revised prompt produced a better result.
6. How the final result was independently verified.

**Existing project evidence:** Prompts 4 through 6 already show this progression. The first image request did not constrain the technical output sufficiently, the second prompt improved the visual direction but still missed exact dimensions and filenames, and the next prompt narrowed the correction to precise export requirements.

**Human decision:** Mia wants unsuccessful prompts preserved as learning evidence rather than omitted from the project story.

**Outcome:** Added unsuccessful-prompt evidence to the Part 9 map and expanded the ongoing recording standard so future weak, incomplete, failed, or partially successful prompts include the reason and correction path.

## Prompt 18 — Detect and correct the missing unsuccessful-prompt ratings

**Date and stage:** July 23, 2026 — documentation verification and human-oversight evidence

**AI tool:** ChatGPT/Codex

**Task type:** Independent review, follow-up, correction, and AI orchestration

**Exact verification prompt:**

> Chat remember that I want to show the rating 5/5 of my prompting that we are documentation. So please review that you did show a rating also for prompts that did not give me a good outcome.

**What Mia independently noticed:** The Prompt Library explained why several prompts did not work, but it did not display an explicit numeric rating for those examples. This meant the approved rating framework had been implemented for strong prompts but not consistently applied to unsuccessful prompts.

**AI response and limitation:** Codex reviewed the library and confirmed the omission. It proposed a complete `1/5` through `5/5` scale and explicit ratings for both successful and unsuccessful examples. Codex did not change the documentation until Mia evaluated and approved the correction.

**Exact approval and orchestration prompt:**

> Chat I do approve of the gap update and I would like to make sure we document this conversation and how I saw something that we need to clearly verify showing my independent thinking and how I am not allowing AI to direct and make decisions for me but actually understanding and knowing how to really utilize my AI tools by being the orchestrator and being able to orchestrate multiple AI tools across the platform.

**Human decision and reasoning:** Mia approved the rating correction and required the record to preserve how the correction happened. She did not accept the earlier documentation merely because AI reported it as complete. She reviewed the actual file, identified a missing requirement, asked for verification, considered the proposed ratings, and authorized the final update.

**Multi-tool orchestration evidence:** Mia assigns different responsibilities to ChatGPT, Codex, Gemini, and Claude; carries relevant context between their separate interfaces when needed; evaluates their outputs; and decides what enters the project. The tools are not represented as automatically connected to one another. Mia is the connecting decision-maker and project orchestrator.

**Outcome:** Expanded the rating definitions from `1/5` through `5/5`, clarified that prompt quality and AI outcome quality are different measurements, added explicit ratings to the strong Gemini examples and every unsuccessful example, and strengthened the AI Usage Log and README description of human oversight.

**Verification required:** Confirm that every selected precise-execution and unsuccessful example has an explicit rating, all ratings include a reason, no AI outcome is treated as verified merely because the prompt was highly rated, and all documentation checks continue to pass.

## Prompt 19 — Require visible AI-art disclosure even when technical provenance may be lost

**Date and stage:** July 23, 2026 — visual-asset provenance and disclosure decision

**AI tools discussed:** Gemini, ChatGPT/Codex, and OpenAI image generation

**Task type:** Curiosity, responsible AI use, provenance verification, and human-directed requirement change

**Exact provenance question:**

> Chat this is awesome that you can also generate images because I always seem to run into the problem using Gemini that he never names the files correctly that I ask and the sizing is always off so know that you can be precise will make my life a lot easier when I need precision and not just beautiful images to look at. One big thing I want to make sure that you also show in your images is that it was actually AI generated by some kind of sign. With using Gemini in image generation you will see a small star like image in the lower right corner of the image and that sign actually protects me as showing anyone viewing the image that I did not create or copy the image but that I orchestrated an AI generated image. Do you show some kind of proof that when you create an image it clearly shows it was AI generated?

**AI response and verified distinction:** ChatGPT/Codex checked current official OpenAI guidance and explained that OpenAI-generated images include C2PA Content Credentials and SynthID provenance signals, but these signals are not necessarily visible to a viewer. C2PA metadata can be removed during processing, and cropping or resizing may affect detectable provenance. A visible badge is disclosure rather than cryptographic proof, so the strongest practice combines visible disclosure, preserved originals, final-file verification, and documented evidence.

**Exact final decision:**

> Chat I love this!!! We are really learning how to work together and building a strong foundation. I love the idea that we do not take Gemini's identification that the image was AI generated but that we disclose that the images that we create will always state that these images were AI generated and orchestrated by me and since we possibly could be cropping original AI generated images and possibly lose the C2PA and SynthID verification lets always state that these images were AI generated directed by me to protect me.

**Human decision:** Mia established a generator-independent final-asset rule. Every final AI-created image must visibly state `AI-generated artwork — Directed by Mia`. A Gemini mark, C2PA metadata, or SynthID signal can provide additional provenance, but none replaces the required visible disclosure.

**Implementation boundary:** The project will preserve original generated files, apply exact dimensions and the visible disclosure to final project-ready files, verify supported provenance signals on the final exports, and report the result honestly. A missing signal after processing will not be misrepresented as proof that an image was not AI-generated.

**Requirement change:** The earlier “no readable text” rule now has one approved exception: the required AI-generation disclosure. Exact sizing is no longer the only unresolved asset requirement; disclosure placement, final-file provenance verification, and display testing are also pending.

**Files affected:** `AGENTS.md`, `README.md`, `docs/prompt_history.md`, `docs/BUILD_LOG.md`, `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`, `docs/archive/AI_USAGE_LOG.md`, `docs/archive/ASSET_GENERATION_BRIEF.md`, `docs/archive/PROJECT_PLAN.md`, `docs/archive/PROJECT_REQUIREMENTS_AND_SCOPE.md`, and `docs/archive/SECOND_COLLECTION_AUDIT.md`.

Prompt 20 — Redesign the AI workflow before implementation

Date and stage: July 23, 2026 — pre-implementation workflow and resource planning

AI tools and models: Gemini Pro, ChatGPT Instant 5.5, Claude Code, Codex, and Gemini 2.5 Flash

Task type: Planning, constraint analysis, multi-tool orchestration, continuity preservation, and documentation review

Context and initiating concern: Before beginning application implementation, Mia recognized that the repository-capable ChatGPT/Codex environment was nearing its available usage limit. Approximately 6% of that environment's usage remained after the planning, requirements, architecture, asset, and documentation work. Rather than begin implementation with a high risk of losing repository access partway through the build, Mia paused and reconsidered how responsibilities should be distributed across her available AI tools.

Mia's orchestration decision: Mia preserved the detailed project handoff and reassigned repository-aware implementation to Claude Code inside Visual Studio Code. She assigned Gemini Pro as the continuing collaborator for requirements interpretation, architecture review, Teaching Mode, verification planning, explanation of tradeoffs, reflective follow-up, and reviewer-facing documentation audits. She retained ChatGPT Instant 5.5 for interview rubber-ducking and brainstorming with Mia.

The revised responsibility split is:

Mia: Project orchestrator, context owner, reviewer, and final decision-maker.

Gemini Pro: Requirements interpretation, architecture review, Teaching Mode, verification planning, explanation of tradeoffs, reflective follow-up, and reviewer-facing documentation audits.

ChatGPT Instant 5.5: Interview rubber-ducking and brainstorming with Mia.

Claude Code: Repository-aware implementation, code inspection, local testing, debugging, and implementation evidence inside Visual Studio Code.

Gemini 2.5 Flash: Visual-asset generation when required, followed by independent inspection and verification.

Codex: Repository inspection or implementation only when Mia intentionally selects it and sufficient usage is available; it is no longer treated as the only implementation path.

Why this was a constraint-driven pivot: The change was not based on abandoning the existing plan or accepting a lower-quality workflow. Mia identified a resource constraint before it became a project failure, preserved the completed reasoning and documentation, and redesigned the workflow so that one tool's usage limit would not become a single point of failure.

Human-controlled context transfer: Gemini Pro, ChatGPT Instant 5.5, Claude Code, Codex, and Gemini 2.5 Flash are separate tools and are not represented as automatically sharing project knowledge. Mia determines what context each tool receives, preserves approved decisions in project documentation and handoffs, compares outputs, questions inconsistencies, and decides what enters the repository.

Response summary and outcome: ChatGPT Instant 5.5 helped Mia brainstorm and develop the framing of the decision as a Constraint-Driven AI Orchestration Pivot, an AI Workflow Pivot Before Implementation, and a Multi-Tool AI Orchestration Decision. Mia then rejected simply pasting those narratives into several files without reviewing their existing structures. She required a full documentation-structure review so the pivot could be recorded differently in each affected file without unnecessary duplication or structural inconsistency.

Human decision: Mia approved the multi-tool workflow and required the pivot to be documented through structure-matched updates to the existing project records. She explicitly chose not to rewrite the existing documentation, not to add artificial edits to unrelated files, and not to update DOCUMENTATION_WORKFLOW.md because the standing documentation process itself did not change.

What this demonstrates: This decision shows planning, risk identification, resource management, tool selection, continuity preservation, independent judgment, and human-led AI orchestration before implementation began.

Verification boundary: At the time of this entry, the orchestration plan and responsibility assignments are documented decisions. Claude Code implementation results have not yet been reviewed through this project record. Future claims about code changes, tests, debugging, or repository state must be supported by actual repository evidence supplied by Mia or verified through a connected repository-capable tool.

Files affected: AGENTS.md, README.md, docs/prompt_history.md, docs/BUILD_LOG.md, and docs/archive/AI_USAGE_LOG.md.

Files intentionally not affected: docs/archive/DOCUMENTATION_WORKFLOW.md, requirements, privacy, project-planning, interview, asset, audit, evidence, filename-map, and image-prompt documents. The pivot does not change their current subject matter or approved project requirements.

Related commit: None recorded. Mia will review and place the documentation updates before deciding when to commit them.

Next action: Supply the approved project handoff to Claude Code, begin the write-save-revisit implementation, preserve real implementation prompts and debugging evidence, use Gemini Pro for requirements interpretation, architecture review, Teaching Mode, verification planning, explanation of tradeoffs, reflective follow-up, and reviewer-facing documentation audits, and continue using ChatGPT Instant 5.5 for interview rubber-ducking and brainstorming with Mia.

## Ongoing Recording Standard

For every material interaction, add:

1. Sequential prompt number and descriptive title.
2. Date and AI tool/model when confirmed.
3. User purpose and exact prompt when it is important evidence.
4. Expected result and actual AI output.
5. What worked and what did not work.
6. Why an unsuccessful or partial prompt underperformed.
7. Follow-up question, correction, or rewritten prompt.
8. Mia's decision and reasoning.
9. Files changed and verification performed.
10. Open questions or next action.

Sensitive diary content, passwords, secrets, access tokens, and unrelated personal information must never be copied into this record.
