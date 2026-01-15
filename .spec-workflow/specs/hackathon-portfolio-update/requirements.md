# Requirements Document

## Introduction

This feature adds a new portfolio entry showcasing the user's role as organizer of the **Blockchain@NTU x Base Hackathon**, a significant blockchain event held at AWS Singapore on August 26, 2025. The hackathon brought together 200 builders worldwide and was sponsored by Base, Virtuals Protocol, Sogni AI, and AWS. This entry will highlight the user's leadership and event organization capabilities in the Web3/blockchain space.

## Alignment with Product Vision

This update aligns with the portfolio's purpose of showcasing the user's expertise and accomplishments in blockchain technology, Web3, and community building. It demonstrates leadership beyond just technical skills.

## Requirements

### Requirement 1: Portfolio Entry in index.html

**User Story:** As a portfolio visitor, I want to see the hackathon organization experience prominently displayed in the projects section, so that I can understand the user's leadership and event organization capabilities.

#### Acceptance Criteria

1. WHEN a visitor views the portfolio projects section THEN the system SHALL display a new hackathon entry with the same visual structure as existing projects (carousel on left, description on right)
2. WHEN the hackathon entry is displayed THEN the system SHALL include:
   - Event name: "Blockchain@NTU x Base Hackathon"
   - Role: Organizer
   - Key stats: 200 builders worldwide, held in Singapore
   - Sponsors: Base, Virtuals, Sogni
3. IF images are available for the hackathon THEN the system SHALL display them in a Bootstrap carousel matching existing project carousels

### Requirement 2: Links and Buttons Consistency

**User Story:** As a portfolio visitor, I want to see consistent button and link styling, so that I have a seamless browsing experience.

#### Acceptance Criteria

1. WHEN the hackathon entry includes links THEN the system SHALL use pipe-separated text links format: `<a>Link 1</a> | <a>Link 2</a>` matching existing portfolio entries
2. WHEN an external link (news article, event page) is included THEN the system SHALL open in a new tab using `target="_blank"`
3. IF a "Learn More" page exists THEN the system SHALL link to it using the same pattern as other projects (e.g., `hackathon.html`)

### Requirement 3: News Article Reference

**User Story:** As a portfolio visitor, I want to access the official news article about the hackathon, so that I can verify the accomplishment and learn more details.

#### Acceptance Criteria

1. WHEN the hackathon entry is displayed THEN the system SHALL include a link to the NTU CCTF news article: `https://www.ntu.edu.sg/cctf/news-events/news/detail/blockchain-ntu-x-base-hackathon-finals-successfully-conclude--showcasing-student-innovation`
2. WHEN a user clicks the news article link THEN the system SHALL open the article in a new browser tab

## Non-Functional Requirements

### Code Architecture and Modularity
- **Single Responsibility Principle**: The new entry should be self-contained HTML block that can be added/removed without affecting other portfolio items
- **Modular Design**: Follow existing portfolio item structure exactly for maintainability
- **Clear Interfaces**: Use consistent Bootstrap classes and carousel IDs to avoid conflicts

### Performance
- Images for the hackathon carousel should be optimized (507x234 dimensions matching existing portfolio images)
- No additional JavaScript libraries required; uses existing Bootstrap carousel functionality

### Security
- All external links should use `target="_blank"` with `rel="noopener"` for security best practices

### Reliability
- Entry must render correctly on all screen sizes (responsive design using existing Bootstrap grid classes)
- Carousel navigation (prev/next buttons, indicators) must function identically to existing carousels

### Usability
- Entry placement should be prominent (near top of portfolio section) given it showcases leadership/organization skills
- Visual hierarchy should match existing projects with bold achievement line and clear description
