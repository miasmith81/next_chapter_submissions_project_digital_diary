# Project Plan

## Phase 0 - Repository and Documentation

- Confirm repository, local path, branch, and remote.
- Add `AGENTS.md` and the complete documentation set.
- Verify Codex loads the repository instructions.
- Make the first meaningful documentation commit.

## Phase 1 - Smallest Working Value

- Build an accessible entry form.
- Read and validate form values.
- Save entries to `localStorage`.
- Load and render saved entries.
- Verify persistence after refresh and browser reopen.

**Acceptance criterion:** A user can write, save, and revisit an entry.

## Phase 2 - Data Behavior and Safety

- Store dates consistently.
- Display entries oldest-first inside the diary.
- Add the empty state and diary-name setting.
- Add clear-all/delete with confirmation.
- Safely render user-provided text.
- Add the prototype/privacy notice.

## Phase 3 - Diary Structure

- Build closed front cover and owner page.
- Convert saved entries into diary pages.
- Add New Entry page and back cover.
- Handle odd page counts.

## Phase 4 - Page-Turn Interaction

- Implement forward/backward page turns.
- Add keyboard navigation and visible controls.
- Prevent form controls and scrollable text from turning pages accidentally.
- Add swipe-versus-scroll axis locking on mobile.

## Phase 5 - Visual Identity

- Apply gradients, fonts, glassmorphism, binding, gutters, and shadows.
- Preserve Mausi's decision to accept Gemini's visible AI watermark.
- Correct image dimensions from 928 x 1152 to exactly 1024 x 1280.
- Independently verify final exports and sequential filenames.
- Add approved files to `assets/frames/`.
- Implement image rotation and wraparound.

## Phase 6 - Responsive Behavior and Accessibility

- Test at 375px, 390px, 768px, and 1280px.
- Verify keyboard access, focus visibility, contrast, and labels.
- Respect reduced-motion preferences where practical.
- Verify long entries scroll without breaking pages.

## Phase 7 - Verification and Debugging

- Test write, validation, save, reload, revisit, delete, and empty state.
- Test malformed and long content.
- Verify equal page dimensions.
- Verify swipe and vertical scroll do not conflict.
- Record real bugs and fixes.
- Complete Interview Questions 7 and 8 with evidence.

## Phase 8 - Documentation and Deployment

- Complete every README requirement.
- Curate the strongest prompts.
- Update tool/model records.
- Deploy through GitHub Pages.
- Test the live link on desktop and mobile.
- Perform the final checklist audit.

## Commit Strategy

Use small meaningful commits, such as:

- `docs: add project scope and interview preparation`
- `feat: add diary entry form and validation`
- `feat: persist and render diary entries`
- `feat: add editable diary name and empty state`
- `feat: build animated diary page structure`
- `fix: separate mobile swipe gestures from entry scrolling`
- `style: apply responsive diary visual system`
- `docs: add verification evidence and live demo`

Do not commit broken code merely to increase commit count.
