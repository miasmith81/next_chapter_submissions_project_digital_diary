# Live Documentation Workflow

## Standing Rule

Mausi should not have to prompt ChatGPT/Codex to update documentation after every material change. Documentation is part of the work itself and must be updated before a material task is considered complete.

## Source of Truth

The repository documentation is the durable submission record. Conversation context and platform memory may help continuity, but neither replaces project files committed with the repository.

At the beginning of future work, inspect the current repository documentation before relying on remembered details.

The direct project root contains the repository's only `README.md`. Archived documentation uses `docs/archive/ARCHIVE_INDEX.md`, and archived evidence uses `docs/archive/evidence/EVIDENCE_INDEX.md`.

## Documentation Triggers

Update documentation whenever:

- A new AI prompt is written or submitted.
- An AI tool or model produces output.
- Mausi accepts, rejects, revises, or supersedes a requirement.
- An AI recommendation is challenged or independently verified.
- A file is added, renamed, resized, removed, or integrated.
- Architecture, scope, privacy, design, or build order changes.
- A bug is discovered, fixed, verified, or deferred.
- A test, audit, commit, deployment, or live verification occurs.
- Feature status changes.

## Documents to Consider

Update every affected document without creating artificial edits in unrelated files.

- `prompt-history.md` - prompts, iterations, response summaries, verification, and decisions
- `docs/archive/AI_AGENT_PROMPT_LIBRARY.md` - curated reusable prompts, precise examples, partial results, improvements, and lessons
- `docs/archive/AI_USAGE_LOG.md` - tool, model, assigned task, accepted/rejected output, and human judgment
- `BUILD_LOG.md` - chronological work, unexpected results, decisions, lessons, tests, and commits
- `README.md` - public-facing features, AI contributions, structure, and current status
- `docs/archive/PROJECT_PLAN.md` - remaining work and phase status
- `docs/archive/PROJECT_REQUIREMENTS_AND_SCOPE.md` - approved scope and requirement changes
- `docs/archive/ASSET_GENERATION_BRIEF.md` - asset requirements and approval state
- `docs/archive/INTERVIEW_PREP.md` - real evidence that strengthens interview answers
- Audit and evidence files - independent findings, reports, manifests, screenshots, and test results

## Prompt-Capture Standard

Each material prompt record should include:

1. Date and stage
2. AI tool and exact model when known
3. Mode or task type
4. Goal
5. Complete prompt or stable link to it
6. Why it was structured that way
7. Response summary
8. Follow-up or iteration
9. What Mausi accepted
10. What Mausi rejected or changed
11. Verification method and result
12. Files affected
13. Related commit when available

## End-of-Work Check

Before finishing a material task:

1. Identify requirements, decisions, prompts, files, and statuses that changed.
2. Update every relevant document.
3. Preserve useful original AI reports as evidence.
4. Separate AI claims from independently verified facts.
5. Record Mausi as the final decision-maker.
6. Leave unfinished work marked pending.
7. Rebuild and test the downloadable bundle when working outside the repository.

**Rule adopted:** July 22, 2026
