# Next Chapter Submissions Project — A Digital Diary

A responsive digital diary prototype that helps users record feelings and possible triggers while experiences are fresh, then revisit entries for personal reflection or optional discussion with a therapist. Built with HTML, CSS, JavaScript, animated page turns, and browser-based storage.

## Live Demo

**Deployment pending.** The GitHub Pages link will be added here after the application is built, deployed, and verified.

<!-- Replace the line above with the final link:
[View the live project](https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/)
-->

## Mission Brief

The mission of this project is to provide a familiar digital space where someone experiencing a difficult emotional moment can record what they are feeling and what may have contributed to it. The user can revisit the entry later for personal reflection or choose to discuss it with a therapist.

This admissions project is a functional prototype. It is not therapy, medical advice, diagnosis, emergency monitoring, or a crisis-response service.

## Problem

After a difficult emotional experience, someone may not remember exactly how they felt or what may have triggered the moment. Without those details, it can be harder to process the experience and explain it later during a conversation with a therapist.

## Value

The application gives users a place to record their personal feelings while an experience is still fresh. Later, they can revisit what they wrote. If they choose to share the information with a therapist, it may help them discuss what happened, recognize possible patterns, and explore helpful coping strategies together.

## Smallest Demonstration of Value

The application first proves its value when a user can:

1. Write a diary entry.
2. Save the entry.
3. Revisit the entry later.

## Project Plan

Development is organized into small, verifiable phases:

1. Establish the repository and documentation foundation.
2. Build and verify the write-save-revisit data flow.
3. Add the empty state, diary name, and responsible deletion controls.
4. Render saved entries dynamically as diary pages.
5. Add the animated book and page-turn interactions.
6. Apply the approved visual identity and decorative images.
7. Verify desktop, mobile, keyboard, storage, and accessibility behavior.
8. Deploy through GitHub Pages and complete the submission audit.

See the detailed [Project Plan](./docs/PROJECT_PLAN.md).

## Features

### Completed

- Initial project structure
- Requirements and scope review
- Static-site architecture decision
- Project documentation foundation
- Admissions interview preparation for Questions 1–6
- Privacy and browser-storage limitation analysis

### MVP features being built

- Write a diary entry
- Validate required entry content
- Save entries in the current browser
- Revisit entries after refreshing or reopening the application
- Display entries in chronological order
- Show an empty state for a new diary
- Personalize the diary with a user-entered name
- Delete saved prototype entries with confirmation
- Responsive desktop and mobile layouts
- Accessible controls and keyboard navigation

### Visual and interaction features planned

- Closed front and back diary covers
- Animated opening and closing behavior
- Forward and backward page turns
- Purple, blue, and white visual palette
- Glassmorphism interface styling
- Handwritten diary typography
- Decorative polaroid-style images
- Mobile swipe navigation that does not interfere with vertical scrolling

### Future production features

- Secure server-side authentication
- Per-user authorization
- Secure backend and database storage
- Cross-device synchronization
- Professional privacy, security, and data-retention review

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Web Storage API (`localStorage`) for prototype persistence
- Git and GitHub
- GitHub Pages
- Visual Studio Code

## AI Tools Used

### Claude

Claude was used during the original diary project and created a detailed handoff covering the existing visual design, animation, architecture, known bugs, and reusable decisions.

### ChatGPT and Codex

ChatGPT/Codex serves as the lead planning and implementation collaborator for the admissions rebuild. It has helped compare the original architecture with the submission rubric, organize the project into verifiable phases, rubber-duck interview questions, investigate storage limitations, and create the documentation foundation.

I preserve my own voice, challenge recommendations, make the final decisions, and verify important claims before including AI-assisted work in the project.

Additional AI tools will be listed only after they make a real, documented contribution.

See the [AI Usage Log](./docs/AI_USAGE_LOG.md) and [Prompt History](./prompt-history.md).

## Running the Project Locally

This is a static HTML, CSS, and JavaScript project. It does not require a package installation or build command.

1. Clone the repository:

   ```bash
   git clone https://github.com/miasmith81/next_chapter_submissions_project_digital_diary.git
   ```

2. Open the project folder in Visual Studio Code.
3. Install the **Live Server** Visual Studio Code extension if it is not already installed.
4. Right-click `index.html` and select **Open with Live Server**.
5. Open the local address displayed by Live Server in your browser.

## Project Structure

```text
next_chapter_submissions_project_digital_diary/
├── assets/                       Images and other visual assets
├── css/                          Application styles
├── docs/
│   ├── AI_USAGE_LOG.md
│   ├── INTERVIEW_PREP.md
│   ├── PRIVACY_AND_LIMITATIONS.md
│   ├── PROJECT_PLAN.md
│   └── PROJECT_REQUIREMENTS_AND_SCOPE.md
├── js/                           Application JavaScript
├── BUILD_LOG.md                  Development decisions and lessons
├── index.html                    Application entry page
├── LICENSE
├── prompt-history.md             Curated AI collaboration history
└── README.md
```

## Prototype Storage and Privacy Limitations

Diary entries in this admissions prototype are stored in the current browser using `localStorage`.

- Entries remain after an ordinary refresh or browser restart.
- Entries are tied to the current browser profile and device.
- Entries do not synchronize across devices.
- Clearing the browser's site data can remove entries.
- Browser storage must not be described as production-secure storage for sensitive mental-health information.
- Users should enter only non-sensitive demonstration content.

A username and password screen written entirely in client-side JavaScript would not provide real authentication. That functionality is intentionally postponed until a future version with a secure backend.

Read the complete [Privacy and Limitations](./docs/PRIVACY_AND_LIMITATIONS.md) document.

## Documentation

- [Build Log](./BUILD_LOG.md)
- [Prompt History](./prompt-history.md)
- [AI Usage Log](./docs/AI_USAGE_LOG.md)
- [Interview Preparation](./docs/INTERVIEW_PREP.md)
- [Privacy and Limitations](./docs/PRIVACY_AND_LIMITATIONS.md)
- [Project Plan](./docs/PROJECT_PLAN.md)
- [Project Requirements and Scope](./docs/PROJECT_REQUIREMENTS_AND_SCOPE.md)

## Development Status

The project is currently in the documentation and MVP-foundation stage. Feature descriptions will be updated as functionality is implemented and verified. Interview answers about bugs, testing, and completed work will be based on real development evidence rather than written in advance.

## Author

Mia Smith — [miasmith81](https://github.com/miasmith81)

## License

See [LICENSE](./LICENSE) for license information.
