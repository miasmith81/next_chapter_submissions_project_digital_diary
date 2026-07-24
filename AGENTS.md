# Next Chapter Digital Diary - Project Agent Instructions

## Documentation is part of every material task

Before beginning project work, read:

- `docs/archive/DOCUMENTATION_WORKFLOW.md`
- `docs/prompt_history.md`
- `docs/BUILD_LOG.md`
- `docs/archive/AI_USAGE_LOG.md`
- Any requirement, plan, audit, or evidence file relevant to the task

Mia should not need to request documentation updates after every change. Before completing any material project task, update every affected living document.

The project root `README.md` is the repository's only file named `README.md`. Use `docs/archive/ARCHIVE_INDEX.md` and `docs/archive/evidence/EVIDENCE_INDEX.md` for the archived documentation indexes; do not create additional files named `README.md` below the root.

## Required behavior

- Capture every material AI prompt, response summary, follow-up, and outcome.
- Preserve complete prompts in `docs/prompt_history.md` or a linked file under `docs/archive/prompts/`.
- Update `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` when a prompt establishes a reusable workflow, produces especially precise execution, or provides a useful lesson from a partial or failed result.
- Record the AI tool, exact model when known, assigned responsibility, and why it was selected.
- Record what Mia accepted, rejected, revised, or superseded.
- Distinguish AI-generated claims from independently verified facts.
- Update `docs/BUILD_LOG.md` chronologically with decisions, unexpected results, tests, lessons, and commits.
- Update the README and project plan when public status or remaining work changes.
- Update requirement and audit documents when Mia changes a requirement.
- Preserve useful source reports and manifests under `docs/archive/evidence/`.
- Do not edit unrelated documentation merely to create activity.
- Do not mark work complete while required evidence or verification remains pending.
- Keep credentials, authentication codes, private diary entries, and sensitive personal information out of project documentation.

## Decision authority

Mia is the final decision-maker for project scope, design acceptance, requirement changes, AI-output approval, and submission content.

## Current AI orchestration

The project uses a human-directed multi-tool workflow. Do not assume that one AI tool owns every stage of the project.

- Mia is the project orchestrator, context owner, reviewer, and final decision-maker.
- Gemini Pro supports requirements interpretation, architecture review, Teaching Mode, verification planning, explanation of tradeoffs, reflective follow-up, and reviewer-facing documentation audits.
- ChatGPT Instant 5.5 supports interview rubber-ducking and brainstorming with Mia.
- Claude Code is the primary repository-aware implementation tool for the next build stage inside Visual Studio Code.
- Codex remains an optional repository-capable tool for inspection, implementation, testing, documentation synchronization, and evidence capture when Mia intentionally selects it and sufficient usage is available.
- Gemini 2.5 Flash may generate visual assets and visual iterations, but every output requires independent visual and technical verification.
- Do not assign interview rubber-ducking to Gemini Pro. That responsibility belongs to ChatGPT Instant 5.5.
- Do not assign requirements interpretation, architecture review, Teaching Mode, verification planning, explanation of tradeoffs, reflective follow-up, or reviewer-facing documentation audits to ChatGPT Instant 5.5 under the current orchestration plan. Those responsibilities belong to Gemini Pro.
- Distinguish Gemini Pro from Gemini 2.5 Flash. Gemini Pro supports reasoning, review, verification planning, and documentation auditing. Gemini 2.5 Flash supports image generation.
- The tools do not automatically share context. Mia controls handoffs and decides which approved requirements, constraints, decisions, and evidence are supplied to each tool.
- Do not describe a handoff summary, AI report, or conversation as repository verification.
- Do not claim that Claude Code, Codex, or another implementation tool changed or tested the repository unless the actual changes and results are available for inspection.
- Preserve the approved static HTML, CSS, and JavaScript architecture unless Mia explicitly changes it.
- Treat tool availability and remaining usage as project constraints. Do not create a single point of failure by assuming one AI environment will remain available for the complete build.
- Before implementation, read the supplied handoff and current project documentation. When the handoff conflicts with the repository or a later approved decision, stop and surface the conflict rather than silently choosing one.
- After implementation, report the files changed, behavior added, tests run, unexpected results, remaining limitations, and documentation that must be updated.
- Keep planning recommendations, brainstorming, interview practice, implemented changes, generated images, and independently verified results clearly distinguished.

## Project naming and attribution

- In Next Chapter project documentation, refer to the applicant as `Mia`.
- When a full name is required, use `Mia Smith`.
- Do not use a nickname or an alternate or hyphenated surname in this project's documentation.
- This project-specific rule does not define naming for other companies, websites, platforms, or conversations.

## Current visual-asset status

- Gemini 1.5 Flash produced the accepted second visual collection.
- Codex created and verified sequential copies named `frame01.png` through `frame12.png`.
- Mia intentionally accepted Gemini's lower-right platform mark as AI-generation disclosure.
- The actual supplied files remain 928 x 1152.
- Every final AI-created image must visibly state `AI-generated artwork — Directed by Mia`.
- Preserve C2PA and SynthID provenance when available, but verify the final post-crop or post-resize file before claiming either signal remains.
- If technical provenance is missing or cannot be verified, retain the visible disclosure and record the verification result honestly.
- Exact 1024 x 1280 sizing, visible-disclosure approval, provenance verification, and final repository integration are pending.

See `docs/archive/SECOND_COLLECTION_AUDIT.md` for evidence.
