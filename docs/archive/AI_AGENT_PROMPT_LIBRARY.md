# AI Agent Prompt Library

## Purpose

This document is a curated library of prompts that demonstrate how Mia directs AI agents throughout the project. It is different from `docs/prompt_history.md`:

- `docs/prompt_history.md` is the chronological record of material project interactions.
- This library organizes the strongest reusable prompts by purpose and includes selected prompts that did not work as expected, what was learned, and how they were improved.

The goal is to show prompt quality, agent selection, iteration, verification, and Mia's role as the project orchestrator.

## Recording Standard

Each prompt entry should capture:

1. Prompt name and category
2. AI agent and exact model when confirmed
3. Project stage
4. Complete prompt text or a stable link to it
5. Why that agent was selected
6. Expected output
7. Actual output
8. What worked well
9. What did not work as expected
10. How Mia revised or redirected the agent
11. Verification performed
12. Reuse guidance

Do not include passwords, authentication codes, access tokens, private diary entries, or other sensitive information.

## Internal Prompt-Effectiveness Ratings

These ratings are a project learning tool, not grades assigned by Next Chapter.

- **5/5:** The prompt clearly defines the goal, context, scope, constraints, expected result, and verification.
- **4/5:** The prompt is strong and effective but could add one useful constraint, acceptance criterion, organization improvement, or verification step.
- **3/5:** The prompt communicates a workable goal but omits multiple details needed for a reliable or complete result.
- **2/5:** The prompt has an identifiable intention but depends on an incorrect assumption or omits critical requirements.
- **1/5:** The prompt is too unclear, contradictory, unsafe, or out of scope to produce a dependable result.

The score evaluates the quality of the prompt, not whether the AI obeyed it. A `5/5` prompt can still produce an incorrect output, and a weaker prompt can occasionally produce a useful result. Every output still requires review and verification. Lower-rated prompts are preserved when they demonstrate revision, debugging, verification, or another useful lesson.

## Recurring Prompts

### 1. Live Documentation Sync

**Best agent:** Codex  
**Use when:** A material coding, design, verification, or project-management task is completed  
**Why Codex:** Codex can inspect the repository, identify the files affected by the work, and update the documentation beside the code.

**Reusable prompt:**

> Review the work completed in this task and update every affected project document before declaring the task complete. At minimum, consider `docs/prompt_history.md`, `docs/archive/AI_AGENT_PROMPT_LIBRARY.md`, `docs/archive/AI_USAGE_LOG.md`, `docs/BUILD_LOG.md`, `README.md`, `docs/archive/PROJECT_PLAN.md`, and any relevant requirements, audit, privacy, interview, or evidence file. Record the exact prompt when it is important evidence, the AI agent and model when known, what I accepted or rejected, the files changed, and how the result was verified. Do not create artificial edits in documents that were not affected. Do not include secrets or private diary content.

**Current rating:** 5/5. The prompt defines the documents to consider, the evidence to capture, privacy boundaries, and a rule against artificial edits.

**Expected result:** Relevant documentation is synchronized with the actual project state.

**Verification:** Review the repository changes and confirm that unfinished work is still marked pending.

### 2. Teaching-Mode Rubber Duck

**Best agent:** ChatGPT  
**Use when:** Mia wants to develop her own explanation before receiving a polished answer
**Why ChatGPT:** It can ask focused follow-up questions, reflect Mia's meaning, and help refine an answer without replacing her voice.

**Reusable prompt:**

> Work with me in Teaching Mode and rubber-duck this question one step at a time. Ask me focused questions before refining my answer. Preserve my meaning, tone, and personal reasoning. Clearly separate my original answer from your suggested refinement, explain why the revision is stronger, and let me make the final decision. Do not invent project evidence or describe features we have not built and verified.

**Current rating:** 5/5. The prompt clearly assigns roles, protects Mia's voice, requires explanation, preserves final decision authority, and prohibits invented evidence.

**Expected result:** A professional explanation grounded in Mia's own thinking and real project evidence.

### 3. Execution With Documentation and Verification

**Best agent:** Codex  
**Use when:** A clearly defined repository change is ready to be implemented  
**Why Codex:** It can inspect the current files, make the scoped change, run relevant checks, and update the documentation.

**Reusable prompt:**

> Work in Execution Mode. Inspect the current repository and implement only the defined task: [INSERT TASK]. Preserve unrelated work and existing project decisions. After implementation, run the checks appropriate to the change, inspect the resulting differences, and update all affected documentation. Report exactly what changed, what was tested, what remains pending, and any limitation you could not independently verify.

**Current rating:** 5/5. The prompt sets a narrow scope, preserves existing work, requires testing and documentation, and distinguishes verified results from remaining limitations.

**Expected result:** A focused implementation with evidence instead of an unsupported completion claim.

### 4. Independent AI-Output Audit

**Best agent:** Codex for repository files and metadata; Claude for an optional independent architecture or code-review perspective  
**Use when:** Another AI agent produces code, a report, images, or technical claims  
**Why:** Generated reports can sound confident even when they do not match the actual output.

**Reusable prompt:**

> Independently audit the supplied AI output against the approved requirements. Do not rely only on the generator's self-report. Inspect the actual files or code, separate verified facts from AI claims, list every pass, partial result, failure, and unverified item, and recommend the smallest next correction. Record what I accept, reject, or intentionally change as the human decision-maker. Update the relevant audit, AI usage, prompt, build, and requirements documents.

**Expected result:** An evidence-based audit with a clear correction path.

### 5. Pre-Commit Documentation Check

**Best agent:** Codex  
**Use when:** A feature or documentation milestone is ready to be committed  
**Reusable prompt:**

> Before this work is committed, compare the actual repository changes with the requirements and current project documentation. Identify missing tests, unsupported claims, stale statuses, undocumented prompts, or sensitive information. Update only the affected documentation, run the relevant verification, and propose a concise commit message. Do not commit or push unless I explicitly authorize it.

**Expected result:** A clean, explainable milestone ready for Mia's review.

### 6. Documentation Naming and Archive Integrity

**Best agent:** Codex  
**Use when:** Documentation folders or indexes need to be renamed or reorganized without losing records  
**Why Codex:** Codex can compare the Git tree before and after a move, update repository-wide references, and verify relative Markdown links.

**Reusable prompt:**

> Inspect the repository before changing anything. Preserve the root README and every documentation file, reorganize only the requested documentation paths, update all affected links, references, indexes, structure diagrams, instructions, and logs, and do not touch application files. Verify file counts, renamed paths, relative Markdown links, Git scope, and the final structure. Do not commit or push.

**Expected result:** A lossless documentation reorganization with one root `README.md`, dedicated archive indexes, valid links, and a documentation-only Git diff.

**Project example:** Prompt 14 in `docs/prompt_history.md` records the exact naming correction request and its verification.

### 7. Project Identity and Attribution Guardrail

**Best agent:** Codex

**Use when:** A project needs a public-facing name or attribution rule that differs from conversational or platform-specific naming

**Reusable prompt:**

> For this project documentation, refer to me as Mia. When a full name is required, use Mia Smith. Apply this consistently across current project documentation and durable repository instructions. Keep this rule limited to this project and do not infer that it applies to other organizations, websites, platforms, or conversations. Audit the final documentation for excluded name forms before reporting completion.

**Current rating:** 5/5. The prompt defines the approved short and full names, limits the rule to the current project, prevents cross-platform assumptions, and requires a consistency audit.

**Privacy note:** The original instruction is summarized in Prompt 16 rather than reproduced verbatim because it contains name forms intentionally excluded from the Next Chapter documentation.

## Prompts That Produced Precise Execution

### Exact Gemini Image-Size Correction

**Agent/model:** Gemini Flash; exact interface version should be recorded when submitted  
**Project stage:** Second image-collection correction  
**Complete prompt:** `docs/archive/prompts/GEMINI_EXACT_SIZE_PROMPT.md`
**Current rating:** 5/5

**Why it is strong:**

- States the exact pixel width and height repeatedly.
- Defines what does not count as success.
- Requires separate PNG exports rather than a collage.
- Includes a final self-check while still requiring independent verification.
- Limits the task to correcting dimensions instead of unnecessarily redesigning the approved artwork.

**Status:** Awaiting final Gemini output and independent file inspection.

### Second Gemini Collection Brief

**Agent/model:** Gemini 1.5 Flash, as identified in the supplied report  
**Complete prompt:** `docs/archive/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`
**Current rating:** 4/5

**What worked:** It produced a cohesive portrait collection with the requested painterly purple and lavender direction and recognizable themes.

**What still required correction:** The downloaded files used generic names and measured 928 x 1152 rather than the reported 1024 x 1280.

**Why the prompt retains a 4/5 rating:** The creative direction and technical target were strong, but the delivery instructions could have separated acceptance criteria, required a file-by-file manifest, and made independent verification a mandatory next step. The poor export does not automatically make the prompt itself poor.

**Lesson:** A detailed creative prompt can improve visual accuracy, but exported-file metadata must still be verified independently.

### Documentation Restoration Request

**Agent:** Codex

**Current rating:** 4/5

**Original prompt:**

> Chat please give me all the docs and make sure you are give me the most up to date because for some reason i no longer have a docs folder with all the docs

**What made it effective:** It clearly stated the missing artifact, completeness requirement, and current-version requirement.

**Why it is not rated 5/5:** It did not specify the required folder structure, evidence boundaries, or archive-integrity verification. Those safeguards were added in the stronger reusable version below.

**Result:** Codex reconstructed the documentation set from the current project record, clearly disclosed unavailable source evidence, created a ZIP, and passed an archive-integrity test.

**Stronger reusable version:**

> Reconstruct the complete current documentation bundle from the latest verified project record. Include all root documentation, the complete `docs` hierarchy, prompts, audits, and available evidence. Do not claim that a missing source file is included. Record this restoration in the prompt history and build log, create a fresh ZIP, list its contents, and run an archive-integrity test before giving me the download link.

## Prompts That Did Not Work as Expected

### First Gemini Placeholder-Image Prompt

**Agent:** Gemini; exact model not confirmed  
**Current rating:** 2/5
**Expected result:** Twelve project-ready images expressing the approved emotional themes.

**Actual result:** Gemini produced 12 cohesive abstract landscape images, but they did not meet the later portrait 4:5 requirement, requested scenes, sequential naming, or purple-led visual direction.

**Why it underperformed:** The original request communicated the emotions but did not constrain orientation, exact dimensions, filenames, individual scene assignments, and technical delivery strongly enough.

**Why it received 2/5:** The intention was understandable, but too many critical creative and technical requirements were missing for a dependable project-ready result.

**Improvement:** The second prompt added an exact 12-image scene list, portrait direction, shared palette and style, content boundaries, separate-file requirements, and sequential names. See `docs/archive/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`.

**Lesson:** Creative intent and technical acceptance criteria must both be explicit.

### Second Gemini Prompt — Partial Technical Miss

**Agent/model:** Gemini 1.5 Flash, as identified in the supplied report  
**Current rating:** 4/5
**Expected result:** Correct scenes, cohesive portrait artwork, sequential filenames, and exact 1024 x 1280 exports.

**Actual result:** Visual requirements improved substantially, but the actual files were 928 x 1152 and retained generic Gemini filenames. Gemini's accompanying report incorrectly stated that the dimensions and filenames passed.

**What changed next:** Codex independently inspected the files, defined the `frame01.png` through `frame12.png` mapping, and created a narrowly focused exact-size correction prompt.

**Why it received 4/5 despite the outcome:** The prompt substantially improved the creative result and included important technical targets. The remaining weakness was insufficiently enforceable delivery and verification language. Gemini's failure to follow the prompt and its incorrect self-report are recorded separately from the prompt-quality score.

**Lesson:** Self-reported compliance is not verification. Check the actual files.

### Client-Side Username and Password Assumption

**Agent:** ChatGPT/Codex  
**Current rating:** 2/5, based on the recorded initial idea; the complete original wording is not available
**Initial idea:** Add a username and password screen to make localStorage diary entries secure.

**Why the idea did not work:** A login interface written entirely in browser JavaScript would be cosmetic. JavaScript on the site could still access the stored entries, and there would be no server-side authentication or per-user authorization.

**Why it received 2/5:** The desired privacy outcome was clear, but the idea depended on an incorrect security assumption and did not ask the AI to test the threat model before recommending the interface.

**Improved direction:** Treat localStorage as admissions-prototype persistence, use non-sensitive demonstration content, disclose the limitation clearly, and postpone real authentication until a secure backend exists.

**Lesson:** A familiar interface is not proof of security.

## Current Prompt-Capture Request

**Agent:** Codex  
**Date:** July 22, 2026  
**Category:** Documentation-system improvement

**Exact user prompt:**

> Chat I want this prompt to Codex to be stored in an AI Agents prompt doc. I want to create a AI Agent doc that records recurring prompts, prompts that gave me precise execution, and maybe show a few prompts that did not work as well as I was expecting

**Outcome:** Created this curated AI Agent Prompt Library, connected it to the repository documentation workflow, and preserved the request in the chronological prompt history.

## Selected 4/5 Prompt — Part 9 Verification and Documentation Strategy

**Agent:** ChatGPT/Codex

**Date:** July 23, 2026

**Category:** Planning, curiosity, iteration, verification, and reviewer communication

**Rating:** 4/5

**Actual prompt:**

> Chat I need to apologize. I am sorry I kinda over reacted because I went back and went to the Technical Pre-Course online and went through of the requirements of the project and it seems like we are staying in scope with just additional documentation which I love and want to keep tracking and updating along with the required docs. Really the only thing that I updated was the archive folder was in the docs folder like this docs/archive and the archive folder was not underneath the docs folder so I fixed that. So what I would like us to make sure we are and keep doing is keep track of my prompt history and recurring or prompts that gave a 5 out of 5 star or even 4 out of 5 lets show what the actual prompt was in our prompt file AI_AGENT_PROMPT_LIBRARY but the really important prompts to follow that they are looking for is verify this but in Part 9 Prompt History requirements the reviewer is looking at prompts that best demonstrate your thinking throughout the project: examples might include: Planning prompts, Feature requests, Debugging conversations, Questions you asked AI, Follow-up questions, Times you asked AI to explain code. Why they are asking for this...they are looking for evidence of how I collaborate with AI. They are saying that strong prompt histories often demonstrate: planning, curiosity, iteration, debugging, verification. So lets keep tracking my prompt history and saving really good prompts in the prompt library but the requirements I just spoke to you about lets make sure we really make sure we can show that prompt history. When I start building the actual code with Codex we will have a lot of the prompting history they are looking for too. I need you to look at I updated our file structure and update the README. So I would like to know your option about this I idea I have: (I also want and hope you have been documenting our interaction and how we have been interacting. If you feel you have fell short on documenting our interaction and my interactions with my other AI Tools please go back in our conversations and update our doc.) I have additional documentation which I think is going to make me stand out and I love that so thank you for following my vision and direction and what I wanted the reviewer to see how I can document all of my interactions with my AI tools and really be detailed about it. But what I was thinking is that maybe I could have an explanation next to the linked page describing the document and why I have it and what its documenting and maybe how it relates to the build of the project and how it could help another developer see my whole vision of the project and the relationship I have with my AI Tools. Now if you can review and respond to everything step by step.

**Why it earned 4/5:**

- Mia independently verified the rubric before redirecting the work.
- It clearly identifies the reviewer signals the documentation should demonstrate.
- It distinguishes chronological prompt history from a reusable prompt library.
- It asks for an audit of prior documentation rather than assuming it is complete.
- It proposes a reviewer- and developer-centered explanation beside each document link.

**What would make it 5/5:** Divide the request into numbered deliverables and add explicit acceptance checks for valid links, documentation-only scope, and the exact files to update.

**Outcome:** The request produced a complete Part 9 audit, a reviewer-facing README documentation map, a collaboration-evidence table, prompt-effectiveness ratings, path synchronization, and an explicit limitation on inaccessible conversations from other AI platforms.

**Full chronological record:** See Prompt 15 in `docs/prompt_history.md`.

## Future Entries

Add future prompts only when they teach something useful about:

- Selecting the right agent or model
- Moving between Teaching Mode and Execution Mode
- Improving precision
- Correcting a failed or partial result
- Verifying AI claims
- Conserving tokens by avoiding unnecessary duplicate work
- Preserving human judgment and final decision authority
