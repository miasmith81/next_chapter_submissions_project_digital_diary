# Project Requirements and Scope

## Project title

**Next Chapter Submissions Project — A Digital Diary**

## Mission brief

Build a digital diary prototype that gives people experiencing mental-health challenges a place to record feelings and possible triggers while the experience is still fresh. Users can revisit what they wrote later for personal reflection or choose to discuss it with a therapist.

This application is a journaling prototype. It is not therapy, diagnosis, medical advice, emergency monitoring, or a crisis-response service.

## Admissions requirements

The submission must include:

- A working web application
- HTML
- CSS
- JavaScript
- A public GitHub repository
- A working GitHub Pages deployment
- `index.html` with correctly connected CSS and JavaScript
- No private or sensitive information
- A README containing the project name, live demo, problem, value, project plan, features, technologies, AI tools, and local-running instructions
- A prompt-history file demonstrating planning, curiosity, iteration, debugging, and verification
- Multiple meaningful commits
- Clear project structure
- Features that demonstrate value
- Code the creator can explain

## Smallest demonstration of value

The prototype proves its value when a user can:

1. Write an entry
2. Save the entry
3. Revisit the entry later

## Approved admissions architecture

- HTML
- CSS
- JavaScript
- GitHub Pages
- Browser `localStorage` for prototype persistence

## Scope limitations

- `localStorage` is browser- and device-specific.
- Entries do not synchronize across devices.
- Clearing browser data can remove saved entries.
- A JavaScript login screen would not create real authentication.
- The prototype must not claim production-level confidentiality.
- Users should enter only non-sensitive demonstration content.

## Preserved visual direction

- Purple, blue, and white gradient palette
- Inter for interface text
- Caveat for handwritten diary text
- Glassmorphism styling
- Floating background, entrance, and content animations
- Animated diary that begins closed and opens into pages
- Page-turn interaction
- Taped polaroid-style decorative frames
- Responsive desktop and mobile experience

## MVP features

- Editable diary name stored in the current browser
- New-entry form
- Optional entry title and mood
- Save an entry to browser storage
- Render saved entries in chronological order
- Revisit entries after refreshing or reopening the site
- Empty state for a new diary
- Delete-my-entries control with confirmation
- Responsive mobile and desktop layouts
- Clear prototype and storage limitations

## Features postponed beyond the admissions MVP

- Cloud database
- Express backend
- User accounts
- Real authentication and authorization
- Cross-device synchronization
- Custom image upload infrastructure
- Therapist accounts or automatic sharing
- Social or shared diary features

## Possible production iteration

A later production version may use React, a secure backend, Neon PostgreSQL, authenticated accounts, per-user authorization, protected sessions, and a professional privacy/security review.

