# Design Document

## Overview

Add two new portfolio projects (x402data and Moonstack) following the exact HTML structure and styling patterns established by existing portfolio entries like DonorSpark and the Base Hackathon entry.

## Code Reuse Analysis

### Existing Components to Leverage
- **Portfolio Item Structure**: `index.html` lines 700-742 (Base Hackathon pattern)
- **Detail Page Template**: `ntuxbasehackathon.html` or `donorspark.html`
- **Image Styling**: `style="height: 234px; object-fit: cover; object-position: center;"`

### Integration Points
- **index.html**: Insert new portfolio items within `portfolio-container` div
- **Root directory**: Create new detail pages (x402data.html, moonstack.html)

## Architecture

```
index.html
├── x402data portfolio entry (new)
├── moonstack portfolio entry (new)
├── Base Hackathon entry (existing)
└── Other portfolio items...

/x402data.html (new detail page)
/moonstack.html (new detail page)
```

## Components

### Component 1: x402data Portfolio Entry (index.html)

```html
<div class="container row col-lg-10 portfolio-item align-items-center">
  <div id="x402dataIndicators" class="carousel slide col-lg-6" data-ride="carousel">
    <ol class="carousel-indicators">
      <li data-target="#x402dataIndicators" data-slide-to="0" class="active"></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img class="d-block w-100" style="height: 234px; object-fit: cover; object-position: center;" src="assets/img/portfolio/x402.png" alt="x402data Dashboard">
      </div>
    </div>
    <a class="carousel-control-prev" href="#x402dataIndicators" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#x402dataIndicators" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
  <div class="col-lg-6 d-flex flex-column justify-content-center">
    <h3>x402data</h3>
    <p>
      <b>The "Stripe Dashboard" for the x402 Ecosystem</b><br>
      Building the financial intelligence layer for the x402 micropayment protocol. Replacing manual block explorer searches with a real-time analytics suite for $600M+ transaction volume across 72K+ autonomous AI agents and 960+ API endpoints.
    </p>
    <p>
      <a href="https://x402data.org/" target="_blank">Live Site</a> |
      <a href="x402data.html">Learn More</a>
    </p>
  </div>
</div>
```

### Component 2: Moonstack Portfolio Entry (index.html)

```html
<div class="container row col-lg-10 portfolio-item align-items-center">
  <div id="moonstackIndicators" class="carousel slide col-lg-6" data-ride="carousel">
    <ol class="carousel-indicators">
      <li data-target="#moonstackIndicators" data-slide-to="0" class="active"></li>
      <li data-target="#moonstackIndicators" data-slide-to="1"></li>
      <li data-target="#moonstackIndicators" data-slide-to="2"></li>
      <li data-target="#moonstackIndicators" data-slide-to="3"></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img class="d-block w-100" style="height: 234px; object-fit: cover; object-position: center;" src="assets/img/portfolio/moon1.jpg" alt="Slide 1">
      </div>
      <div class="carousel-item">
        <img class="d-block w-100" style="height: 234px; object-fit: cover; object-position: center;" src="assets/img/portfolio/moon2.jpg" alt="Slide 2">
      </div>
      <div class="carousel-item">
        <img class="d-block w-100" style="height: 234px; object-fit: cover; object-position: center;" src="assets/img/portfolio/moon3.jpg" alt="Slide 3">
      </div>
      <div class="carousel-item">
        <img class="d-block w-100" style="height: 234px; object-fit: cover; object-position: center;" src="assets/img/portfolio/moon4.jpg" alt="Slide 4">
      </div>
    </div>
    <a class="carousel-control-prev" href="#moonstackIndicators" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#moonstackIndicators" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
  <div class="col-lg-6 d-flex flex-column justify-content-center">
    <h3>Moonstack</h3>
    <p>
      <b>Prediction Market Powered by Beagles & Options</b><br>
      Full Stack Blockchain Developer. Built a next-gen prediction market on Thetanuts Finance's options protocol with gamified NFT mechanics. Users mint AI-generated "Moongle" Beagle avatars that evolve based on platform activity.
    </p>
    <p>
      <a href="https://www.youtube.com/watch?v=ym3LKuCT4Rw" target="_blank">Demo Video</a> |
      <a href="moonstack.html">Learn More</a>
    </p>
  </div>
</div>
```

### Component 3: x402data Detail Page (x402data.html)

Follow `ntuxbasehackathon.html` template structure:
- Header with navigation
- Section title with "Back" link
- Carousel with x402.png
- Two-column layout:
  - Left: Overview, Problem, Solution, Key Features
  - Right: Live Site link, Tech Stack, Skills

### Component 4: Moonstack Detail Page (moonstack.html)

Follow same template:
- Carousel with moon1-4.jpg
- Overview of prediction market and Moongle NFTs
- Technical achievements (ERC-721, gas optimization)
- Links: Demo video, moonstack.fun, Base app
- Tech Stack: Solidity, Next.js, Base L2, ERC-721

## Data Models

### x402data Content
```
Title: x402data
Tagline: The "Stripe Dashboard" for the x402 Ecosystem
URL: https://x402data.org/
Image: assets/img/portfolio/x402.png
Skills: x402, Blockchain, Analytics
Features:
  - Real-time revenue tracking for API Providers
  - Top customer identification
  - Multi-chain growth trends (Base, Solana)
  - Expense monitoring for Agent Operators
  - Vendor breakdowns and budget alerts
```

### Moonstack Content
```
Title: Moonstack
Tagline: Prediction Market Powered by Beagles & Options
Role: Full Stack Blockchain Developer
URLs:
  - https://moonstack.fun/
  - https://base.app/app/moonstack.fun/
Demo: https://www.youtube.com/watch?v=ym3LKuCT4Rw
Images: moon1.jpg, moon2.jpg, moon3.jpg, moon4.jpg
Tech Stack: Solidity, Next.js, Base L2, ERC-721
Features:
  - Moongle NFT minting (AI-generated Beagle avatars)
  - Dynamic trait evolution based on activity
  - Gas-optimized ERC-721 smart contract
  - Custom royalty standards
```

## Testing Strategy

### Manual Testing
1. Verify portfolio entries display correctly in index.html
2. Test carousel navigation for both entries
3. Verify all links open correctly (new tab for external)
4. Test detail pages load and display properly
5. Check responsive design on mobile/tablet
