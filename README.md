# Profile Card Component

A responsive, accessible Profile Card component built using semantic HTML5, modern CSS, and vanilla JavaScript. 

## Core Features

- **Semantic Architecture:** Utilizes HTML5 landmark elements including <article>, <aside>, <main>, and <nav> to ensure proper document structure and SEO.
- **Accessibility Compliance:** - Full keyboard navigation support with visible focus indicators.
    - ARIA-live regions for dynamic time updates to notify screen readers.
    - High color contrast meeting WCAG AA standards.
    - Descriptive alternative text for all visual media.
- **Responsive Design:** Implements a fluid "Bento Grid" layout that transitions from a horizontal desktop view to a vertical stack at 928px.
- **Testability:** Includes specific data-testid attributes for stable integration with automated testing frameworks.

## Technical Stack

- HTML5: Semantic markup.
- CSS3: Flexbox, CSS Grid, and custom responsive breakpoints.
- JavaScript: Vanilla JS for real-time Date.now() millisecond updates.

## Required Data Attributes

The following data-testid attributes are implemented for automated testing:

- test-profile-card: The root container.
- test-user-name: The user's full name.
- test-user-bio: The short biography paragraph.
- test-user-time: The live epoch time in milliseconds.
- test-user-avatar: The profile image element.
- test-user-social-links: The container for social navigation links.
- test-user-hobbies: The list of user hobbies.
- test-user-dislikes: The list of user dislikes.

## Implementation Details

### Time Synchronization
The component displays the current epoch time in milliseconds. This is handled via a JavaScript interval that updates the text content of the test-user-time element every 100ms to ensure precision.

### Social Links
All social links are configured with target="_blank" and rel="noopener noreferrer" to ensure security and performance when navigating to external domains.

## Installation

1. Clone the repository.
2. Open index.html in any modern web browser.
3. No build steps or dependencies are required.

## Accessibility Audit Summary

- Focus Management: All interactive elements are reachable via the Tab key.
- Screen Readers: Used aria-label on icon-only buttons to provide context for non-visual users.
- Live Regions: The millisecond counter uses aria-live="polite" to ensure updates are announced according to user preference without disrupting the flow.