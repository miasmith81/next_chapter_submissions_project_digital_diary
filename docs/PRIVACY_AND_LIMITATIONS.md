# Privacy and Prototype Limitations

## Prototype Status

This admissions project demonstrates functionality and responsible technical judgment. It is not a production-secure platform for sensitive mental-health records.

## Browser Storage

Entries are planned to be stored using `localStorage`.

- Data remains after ordinary refreshes and browser restarts.
- Data is tied to the current browser profile and device.
- Data does not synchronize across devices.
- Clearing browser site data can remove entries.
- JavaScript running on the site can read the stored data.
- Browser storage must not be described as securely isolating multiple users.

## Authentication Limitation

A username and password screen implemented only in client-side JavaScript would be cosmetic. It would not create secure authentication, server-side sessions, or per-user authorization. This feature is intentionally postponed until a secure backend exists.

## Responsible User Messaging

The prototype should state that:

- It is not therapy, diagnosis, medical advice, emergency monitoring, or crisis support.
- Users should enter only non-sensitive demonstration content.
- Entries remain only in the current browser and device.
- Users control whether they discuss an entry with a therapist.

## Project Documentation Safety

- Do not include passwords, tokens, credentials, private diary entries, authentication codes, or sensitive information in code, commits, prompts, screenshots, or documentation.
- Use fabricated demonstration entries for testing and screenshots.
- Never overstate what was encrypted, secured, authenticated, or verified.

## Future Production Requirements

- Secure server-side authentication
- Per-user authorization
- Protected backend and database storage
- Appropriate encryption
- Cross-device synchronization
- Data deletion and retention controls
- Privacy, security, and legal review
- Incident-response planning
