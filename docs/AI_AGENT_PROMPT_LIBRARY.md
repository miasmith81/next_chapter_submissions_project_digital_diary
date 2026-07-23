# AI Agent Prompt Library

## Purpose

This document is a curated library of prompts that demonstrate how Mausi directs AI agents throughout the project. It is different from `prompt-history.md`:

- `prompt-history.md` is the chronological record of material project interactions.
- This library organizes the strongest reusable prompts by purpose and includes selected prompts that did not work as expected, what was learned, and how they were improved.

The goal is to show prompt quality, agent selection, iteration, verification, and Mausi's role as the project orchestrator.

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
10. How Mausi revised or redirected the agent
11. Verification performed
12. Reuse guidance

Do not include passwords, authentication codes, access tokens, private diary entries, or other sensitive information.

## Recurring Prompts

### 1. Live Documentation Sync

**Best agent:** Codex  
**Use when:** A material coding, design, verification, or project-management task is completed  
**Why Codex:** Codex can inspect the repository, identify the files affected by the work, and update the documentation beside the code.

**Reusable prompt:**

> Review the work completed in this task and update every affected project document before declaring the task complete. At minimum, consider `prompt-history.md`, `docs/AI_AGENT_PROMPT_LIBRARY.md`, `docs/AI_USAGE_LOG.md`, `BUILD_LOG.md`, `README.md`, `docs/PROJECT_PLAN.md`, and any relevant requirements, audit, privacy, interview, or evidence file. Record the exact prompt when it is important evidence, the AI agent and model when known, what I accepted or rejected, the files changed, and how the result was verified. Do not create artificial edits in documents that were not affected. Do not include secrets or private diary content.

**Expected result:** Relevant documentation is synchronized with the actual project state.

**Verification:** Review the repository changes and confirm that unfinished work is still marked pending.

### 2. Teaching-Mode Rubber Duck

**Best agent:** ChatGPT  
**Use when:** Mausi wants to develop her own explanation before receiving a polished answer  
**Why ChatGPT:** It can ask focused follow-up questions, reflect Mausi's meaning, and help refine an answer without replacing her voice.

**Reusable prompt:**

> Work with me in Teaching Mode and rubber-duck this question one step at a time. Ask me focused questions before refining my answer. Preserve my meaning, tone, and personal reasoning. Clearly separate my original answer from your suggested refinement, explain why the revision is stronger, and let me make the final decision. Do not invent project evidence or describe features we have not built and verified.

**Expected result:** A professional explanation grounded in Mausi's own thinking and real project evidence.

### 3. Execution With Documentation and Verification

**Best agent:** Codex  
**Use when:** A clearly defined repository change is ready to be implemented  
**Why Codex:** It can inspect the current files, make the scoped change, run relevant checks, and update the documentation.

**Reusable prompt:**

> Work in Execution Mode. Inspect the current repository and implement only the defined task: [INSERT TASK]. Preserve unrelated work and existing project decisions. After implementation, run the checks appropriate to the change, inspect the resulting differences, and update all affected documentation. Report exactly what changed, what was tested, what remains pending, and any limitation you could not independently verify.

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

**Expected result:** A clean, explainable milestone ready for Mausi's review.

## Prompts That Produced Precise Execution

### Exact Gemini Image-Size Correction

**Agent/model:** Gemini Flash; exact interface version should be recorded when submitted  
**Project stage:** Second image-collection correction  
**Complete prompt:** `docs/prompts/GEMINI_EXACT_SIZE_PROMPT.md`

**Why it is strong:**

- States the exact pixel width and height repeatedly.
- Defines what does not count as success.
- Requires separate PNG exports rather than a collage.
- Includes a final self-check while still requiring independent verification.
- Limits the task to correcting dimensions instead of unnecessarily redesigning the approved artwork.

**Status:** Awaiting final Gemini output and independent file inspection.

### Second Gemini Collection Brief

**Agent/model:** Gemini 1.5 Flash, as identified in the supplied report  
**Complete prompt:** `docs/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`

**What worked:** It produced a cohesive portrait collection with the requested painterly purple and lavender direction and recognizable themes.

**What still required correction:** The downloaded files used generic names and measured 928 x 1152 rather than the reported 1024 x 1280.

**Lesson:** A detailed creative prompt can improve visual accuracy, but exported-file metadata must still be verified independently.

### Documentation Restoration Request

**Agent:** Codex  
**Original prompt:**

> Chat please give me all the docs and make sure you are give me the most up to date because for some reason i no longer have a docs folder with all the docs

**What made it effective:** It clearly stated the missing artifact, completeness requirement, and current-version requirement.

**Result:** Codex reconstructed the documentation set from the current project record, clearly disclosed unavailable source evidence, created a ZIP, and passed an archive-integrity test.

**Stronger reusable version:**

> Reconstruct the complete current documentation bundle from the latest verified project record. Include all root documentation, the complete `docs` hierarchy, prompts, audits, and available evidence. Do not claim that a missing source file is included. Record this restoration in the prompt history and build log, create a fresh ZIP, list its contents, and run an archive-integrity test before giving me the download link.

## Prompts That Did Not Work as Expected

### First Gemini Placeholder-Image Prompt

**Agent:** Gemini; exact model not confirmed  
**Expected result:** Twelve project-ready images expressing the approved emotional themes.

**Actual result:** Gemini produced 12 cohesive abstract landscape images, but they did not meet the later portrait 4:5 requirement, requested scenes, sequential naming, or purple-led visual direction.

**Why it underperformed:** The original request communicated the emotions but did not constrain orientation, exact dimensions, filenames, individual scene assignments, and technical delivery strongly enough.

**Improvement:** The second prompt added an exact 12-image scene list, portrait direction, shared palette and style, content boundaries, separate-file requirements, and sequential names. See `docs/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`.

**Lesson:** Creative intent and technical acceptance criteria must both be explicit.

### Second Gemini Prompt — Partial Technical Miss

**Agent/model:** Gemini 1.5 Flash, as identified in the supplied report  
**Expected result:** Correct scenes, cohesive portrait artwork, sequential filenames, and exact 1024 x 1280 exports.

**Actual result:** Visual requirements improved substantially, but the actual files were 928 x 1152 and retained generic Gemini filenames. Gemini's accompanying report incorrectly stated that the dimensions and filenames passed.

**What changed next:** Codex independently inspected the files, defined the `frame01.png` through `frame12.png` mapping, and created a narrowly focused exact-size correction prompt.

**Lesson:** Self-reported compliance is not verification. Check the actual files.

### Client-Side Username and Password Assumption

**Agent:** ChatGPT/Codex  
**Initial idea:** Add a username and password screen to make localStorage diary entries secure.

**Why the idea did not work:** A login interface written entirely in browser JavaScript would be cosmetic. JavaScript on the site could still access the stored entries, and there would be no server-side authentication or per-user authorization.

**Improved direction:** Treat localStorage as admissions-prototype persistence, use non-sensitive demonstration content, disclose the limitation clearly, and postpone real authentication until a secure backend exists.

**Lesson:** A familiar interface is not proof of security.

## Current Prompt-Capture Request

**Agent:** Codex  
**Date:** July 22, 2026  
**Category:** Documentation-system improvement

**Exact user prompt:**

> Chat I want this prompt to Codex to be stored in an AI Agents prompt doc. I want to create a AI Agent doc that records recurring prompts, prompts that gave me precise execution, and maybe show a few prompts that did not work as well as I was expecting

**Outcome:** Created this curated AI Agent Prompt Library, connected it to the repository documentation workflow, and preserved the request in the chronological prompt history.

## Future Entries

Add future prompts only when they teach something useful about:

- Selecting the right agent or model
- Moving between Teaching Mode and Execution Mode
- Improving precision
- Correcting a failed or partial result
- Verifying AI claims
- Conserving tokens by avoiding unnecessary duplicate work
- Preserving human judgment and final decision authority
