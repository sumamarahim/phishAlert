# phishAlert - MVP Documentation

## 1. Project Title
**phishAlert** – A Browser Extension to Detect Phishing and Spam Emails

## 2. Objective
To develop a browser-based extension that automatically analyzes email content in real-time and flags potential phishing and spam emails to protect users from cyber threats.

## 3. Target Users
- General Gmail users (initially)
- Non-technical individuals vulnerable to phishing
- Small businesses without dedicated cybersecurity tools

## 4. Core Problem Statement
Phishing and spam emails are becoming increasingly sophisticated and frequent. Many users unknowingly fall victim due to a lack of awareness or proper detection tools. Current email platforms do not always detect every malicious email.

## 5. Proposed Solution (MVP Scope)
A Chrome browser extension that:
- Scans the content of opened Gmail emails.
- Detects phishing or spam content using AI or heuristic techniques.
- Displays a visual warning if the email is suspicious.
- Operates locally with minimal permissions.

## 6. Key MVP Features

| Feature | Description |
|--------|-------------|
| **Email DOM Extraction** | Extract subject, body, sender from opened Gmail emails. |
| **Phishing/Spam Detection Engine** | Run AI-based or regex-based checks for known patterns (e.g., fake links, urgent language, spoofed addresses). |
| **Real-Time Warning Display** | Show warning banner or icon if email is suspicious. |
| **User Feedback Option** | Allow users to confirm or correct detection (optional for MVP). |
| **Background Script** | Handles API communication and permission management. |

## 7. Non-MVP (Future) Features
- Integration with external APIs (e.g., VirusTotal, Google Safe Browsing)
- Detailed phishing/spam explanation to user
- Dashboard with statistics
- Multi-email provider support (Outlook, Yahoo)
- User training or reporting module

## 8. Technology Stack

| Layer | Tool/Framework |
|-------|----------------|
| **Frontend** | JavaScript, HTML/CSS, Chrome Extension APIs |
| **AI/Detection** | OpenAI API / Custom ML Model (fallback to regex rules) |
| **Backend (optional)** | Firebase/Supabase for feedback logging (optional) |
| **Communication** | `chrome.runtime` for background-foreground messaging |

## 9. User Flow (MVP)
1. User opens Gmail.
2. Extension detects email opened.
3. Extension extracts email data.
4. AI/regex engine processes the data.
5. If threat is found, warning banner appears.
6. User closes or ignores the warning.

## 10. Success Criteria
- Can detect basic phishing patterns with >70% accuracy.
- Seamless integration into Gmail UI.
- No lag or blocking behavior in Gmail.
- Warning is visible and understandable by general users.

## 11. Constraints and Assumptions
- Gmail DOM structure may change—must be flexible.
- Users will grant minimal permissions.
- Limited usage of OpenAI or external APIs due to cost (can fall back to regex).

## 12. Initial Development Timeline

| Week | Milestone |
|------|-----------|
| 1 | Setup basic Chrome extension structure |
| 2 | DOM scraping and Gmail email detection |
| 3 | Implement AI-based or regex-based detection logic |
| 4 | Display phishing warning UI |
| 5 | Test across email scenarios |
| 6 | Final bug fixing, packaging, and documentation |

## 13. Open Questions
- Should detection happen entirely client-side or also involve a backend?
- What fallback detection to use if AI fails?
- What metrics/logs should be collected for improvement?
