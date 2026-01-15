# Requirements Document

## Introduction

Add two new portfolio projects to the website:
1. **x402data** - The "Stripe Dashboard" for x402 Ecosystem - financial analytics platform
2. **Moonstack** - Prediction market with NFT Beagles on Base L2

Both need portfolio entries in index.html and dedicated detail pages.

## Requirements

### Requirement 1: x402data Portfolio Entry

**User Story:** As a portfolio visitor, I want to see the x402data project showcased, so that I understand the user's expertise in building analytics platforms for Web3.

#### Acceptance Criteria

1. WHEN a visitor views the portfolio section THEN the system SHALL display x402data entry with carousel and description
2. WHEN the entry is displayed THEN it SHALL include:
   - Title: "x402data"
   - Tagline: "The Stripe Dashboard for x402 Ecosystem"
   - Description of financial intelligence layer for x402 micropayment protocol
   - Key stats: $600M+ transaction volume, 72K+ AI agents, 960+ API endpoints
   - Image: x402.png (already exists)
3. WHEN links are displayed THEN the system SHALL include link to https://x402data.org/

### Requirement 2: x402data Detail Page

**User Story:** As a portfolio visitor, I want to click "Learn More" on x402data, so that I can see full project details.

#### Acceptance Criteria

1. WHEN user clicks "Learn More" THEN the system SHALL navigate to x402data.html
2. WHEN the detail page loads THEN it SHALL include:
   - Full carousel with x402.png image
   - Overview explaining the problem/solution
   - Key features for API Providers and Agent Operators
   - Tech stack and links to live site

### Requirement 3: Moonstack Portfolio Entry

**User Story:** As a portfolio visitor, I want to see the Moonstack project showcased, so that I understand the user's blockchain development skills.

#### Acceptance Criteria

1. WHEN a visitor views the portfolio section THEN the system SHALL display Moonstack entry with carousel and description
2. WHEN the entry is displayed THEN it SHALL include:
   - Title: "Moonstack"
   - Tagline: "Prediction Market Powered by Beagles & Options"
   - Role: Full Stack Blockchain Developer
   - Tech: Solidity, Next.js, Base L2, ERC-721
   - Images: moon1.jpg, moon2.jpg, moon3.jpg, moon4.jpg
3. WHEN links are displayed THEN the system SHALL include:
   - Demo Video: https://www.youtube.com/watch?v=ym3LKuCT4Rw
   - Learn More: moonstack.html

### Requirement 4: Moonstack Detail Page

**User Story:** As a portfolio visitor, I want to click "Learn More" on Moonstack, so that I can see full project details.

#### Acceptance Criteria

1. WHEN user clicks "Learn More" THEN the system SHALL navigate to moonstack.html
2. WHEN the detail page loads THEN it SHALL include:
   - Carousel with moon1-4.jpg images
   - Overview of prediction market concept
   - Moongle NFT explanation (AI-generated Beagle avatars)
   - Technical achievements (ERC-721, gas optimization, dynamic metadata)
   - Demo video button
   - Links to moonstack.fun and Base app

## Non-Functional Requirements

### Code Architecture and Modularity
- Follow existing portfolio item HTML structure exactly
- Use same CSS classes as existing entries
- Images use centered styling with object-fit: cover

### Performance
- Images optimized for web display
- Fixed height (234px) for consistent carousel behavior

### Usability
- Links and buttons follow existing pipe-separated pattern
- External links open in new tab with target="_blank"
