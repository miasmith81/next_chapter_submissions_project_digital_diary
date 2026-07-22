# Project Plan

## Professional build sequence

### Phase 0 — Repository and documentation foundation

- Confirm the repository name, local path, `main` branch, and GitHub remote.
- Confirm GitHub CLI authentication without exposing credentials.
- Add the documentation set.
- Review and complete the README foundation.
- Add `.gitignore` if needed.
- Make the first meaningful documentation commit.

### Phase 1 — Smallest working value

- Build an accessible entry form in `index.html`.
- Read the form values in JavaScript.
- Validate required entry content.
- Save entries to `localStorage`.
- Load and render saved entries.
- Verify persistence after refresh and browser reopen.

**Acceptance criteria:** A user can write, save, and revisit an entry.

### Phase 2 — Data behavior and safety controls

- Store dates consistently.
- Display entries oldest-first inside the diary.
- Create the empty state.
- Add the diary-name setting.
- Add clear-all/delete-my-entries with confirmation.
- Escape or safely render user-provided text.
- Add the prototype/privacy limitation notice.

### Phase 3 — Diary structure

- Build the closed front cover.
- Build the owner page.
- Convert saved entries into diary pages dynamically.
- Add the New Entry page.
- Build the closed back cover.
- Handle odd page counts with a filler page.

### Phase 4 — Page-turn interaction

- Implement forward and backward page turns.
- Add keyboard navigation.
- Add visible previous/next controls.
- Prevent form controls and scrollable entry text from turning pages accidentally.
- Add swipe-versus-scroll axis locking on mobile.

### Phase 5 — Visual identity

- Apply the approved gradient, fonts, glassmorphism, and diary colors.
- Add the binding, gutter shadows, page shadow, and page-turn shadow.
- Add decorative placeholder-image rotation.
- Preserve equal page dimensions.

### Phase 6 — Responsive behavior and accessibility

- Test at 375px, 390px, 768px, and 1280px.
- Verify keyboard access and focus visibility.
- Verify readable contrast and labels.
- Respect reduced-motion preferences where practical.
- Verify long entries scroll without breaking the page.

### Phase 7 — Verification and debugging

- Test write, validation, save, reload, revisit, delete, and empty state.
- Test malformed or very long entry content.
- Verify that all pages have equal dimensions.
- Verify mobile swipe and vertical scroll do not conflict.
- Record real bugs and fixes in `BUILD_LOG.md`.
- Add evidence to Interview Questions 7 and 8.

### Phase 8 — Documentation and deployment

- Complete every required README section.
- Curate the strongest prompt-history entries.
- Update AI tool/model records.
- Deploy through GitHub Pages.
- Test the live link on desktop and mobile.
- Add the live link to the README.
- Perform the final submission-checklist audit.

## Commit strategy

Make small, meaningful commits after verified milestones. Examples:

- `docs: add project scope and interview preparation`
- `feat: add diary entry form and validation`
- `feat: persist and render diary entries`
- `feat: add editable diary name and empty state`
- `feat: build animated diary page structure`
- `fix: separate mobile swipe gestures from entry scrolling`
- `style: apply responsive diary visual system`
- `docs: add verification evidence and live demo`

Do not commit broken code merely to increase the commit count.

