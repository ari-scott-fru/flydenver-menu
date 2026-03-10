# DEN Airport Blog — Prototype Specification

> **Purpose:** This document provides everything Claude needs to build a working prototype of the Denver International Airport (DEN) blog. It covers strategy, design direction, content structure, and technical implementation details. Use this as a skill file — read it fully before generating any code.

---

## 1. Project Overview

Denver International Airport (flydenver.com) is launching a blog as an owned "newsroom" to tell DEN's story on its terms. The blog replaces the current press-release-only approach with a strategic content hub that drives SEO, feeds social/newsletter distribution, and showcases DEN's strong photography and videography assets.

**Key goals:**
- Reclaim search authority on DEN-related topics (DEN has high domain authority but third-party bloggers currently outrank them)
- Create a multimedia-rich content experience that leverages DEN's photography/videography
- Build topical authority for AI Overview visibility
- Serve as the source that feeds newsletters, social media, and other distribution channels
- Provide genuinely useful content driven by what users are actually searching for

---

## 2. Design Reference & Aesthetic Direction

### Primary Reference: ONT Airport Blog (flyontario.com/blog)
The Ontario International Airport blog is the design benchmark. Key qualities to emulate:
- Clean, modern editorial layout with large hero images
- Card-based post grid on the index page
- Strong visual hierarchy — photography-forward
- Readable long-form article template with generous whitespace
- Category filtering/tagging system
- Professional but approachable tone

### DEN Brand Context
- **Site:** flydenver.com
- **Personality:** DEN leans into its iconic, slightly playful identity — the tent-roof architecture, the Blucifer mustang, the conspiracy theories, the public art. The blog should feel authoritative but have personality.
- **Color palette:** Use DEN's existing brand colors from flydenver.com (deep navy, white, accent colors). You can sample from the live site or use a sophisticated navy + white + warm accent scheme.
- **Typography:** Editorial and clean. Use a distinctive serif or semi-serif for headlines (something with character, not generic) paired with a highly readable sans-serif for body text. Import from Google Fonts.
- **Photography:** The prototype should use placeholder images that represent the kind of high-quality airport photography DEN produces — terminal interiors, mountain views, architectural details, food/dining. Use Unsplash airport/Denver images or solid color placeholders.

### Design Principles
- **Photography-first:** Hero images are large and cinematic. The blog should feel like a travel magazine, not a corporate announcement board.
- **Generous whitespace:** Let content breathe. This is an airport with dramatic architecture — the design should echo that sense of space.
- **Mobile-responsive:** Most airport users will browse on mobile devices while traveling.
- **Fast-scanning:** Travelers want answers quickly. Use clear headings, key takeaways, and scannable formatting within articles.

---

## 3. Content Architecture

### 3.1 Content Categories

Build the prototype with these categories as filterable tags:

| Category | Description | Example Posts |
|---|---|---|
| **Travel Tips** | Practical guides for navigating DEN | "Your Complete Guide to DEN Security Wait Times", "How to Get From DEN to Downtown Denver" |
| **Eat & Drink** | Dining guides, restaurant spotlights | "Best Restaurants Near Gate B40", "The Ultimate DEN Dining Guide by Concourse" |
| **Parking & Transport** | Getting to/from DEN | "DEN Parking: Every Option Explained", "A-Line vs. Rideshare vs. Shuttle — Which is Right for You?" |
| **Art & Culture** | DEN's famous art, architecture, and yes — the conspiracies | "The Real Story Behind Blucifer", "A Self-Guided Tour of DEN's Public Art" |
| **Inside DEN** | Behind-the-scenes, construction updates, sustainability | "Inside the Great Hall Renovation", "How DEN is Building a More Sustainable Airport" |
| **News** | Expanded press releases, new routes, policy updates | "Turkish Airlines Launches Nonstop to Istanbul", "New Security Checkpoint Updates" |

### 3.2 Content Types

The prototype should demonstrate three distinct post templates:

**1. Evergreen Guide (primary type)**
- Long-form (1,500–2,500 words)
- Table of contents sidebar or jump links
- FAQ section with structured data potential
- "Last updated" date displayed prominently
- Example: "The Complete Guide to Parking at DEN"

**2. News/Announcement**
- Medium-form (500–1,000 words)
- Press-release expansion with added context and traveler impact
- Related posts sidebar
- Example: "New Nonstop Flights to Istanbul on Turkish Airlines"

**3. Long-form Feature / Deep Dive (quarterly)**
- Magazine-style (2,500–4,000 words)
- Heavy multimedia: embedded video, photo galleries, pull quotes
- Chapter-style navigation
- Example: "Building the Future: Inside DEN's $2B Great Hall Transformation"

### 3.3 Sample Posts to Include in Prototype

Build the prototype with at least 6 sample post cards on the index page. Use these titles (or similar) to demonstrate the content mix:

1. **"Your Complete Guide to DEN Security Wait Times"** — Travel Tips (Evergreen)
2. **"The Best Places to Eat at DEN, Gate by Gate"** — Eat & Drink (Evergreen)
3. **"Every Parking Option at DEN, Explained"** — Parking & Transport (Evergreen)
4. **"The Secrets of DEN: Art, Architecture & Conspiracy Theories"** — Art & Culture (Evergreen)
5. **"Turkish Airlines Launches Denver's Longest Nonstop Flight"** — News
6. **"Inside the Great Hall: What Travelers Need to Know in 2026"** — Inside DEN (Feature)
7. **"DEN Lounges: Your Complete Guide to Relaxing Before Your Flight"** — Travel Tips (Evergreen)
8. **"How to Get From DEN to Downtown Denver"** — Parking & Transport (Evergreen)

---

## 4. Page Templates to Build

### 4.1 Blog Index Page (Homepage)
- **Hero section:** Featured/pinned post with large cinematic image, headline, excerpt, category badge
- **Category filter bar:** Horizontal pill-style filters (All, Travel Tips, Eat & Drink, Parking & Transport, Art & Culture, Inside DEN, News)
- **Post grid:** 2–3 column responsive card grid. Each card includes:
  - Featured image (landscape ratio, ~16:9)
  - Category badge (colored pill)
  - Headline
  - Excerpt (2 lines max)
  - Publication date
  - Estimated read time
- **Sidebar or bottom section:** Newsletter signup CTA ("Get DEN travel tips in your inbox")
- **Pagination or "Load more" button**

### 4.2 Article Detail Page
Build at least one full article page (the security wait times guide is a good candidate). Include:
- **Hero image:** Full-width or contained, cinematic
- **Article header:** Category badge, headline, subtitle/excerpt, author, date, read time
- **Share buttons:** Social sharing strip
- **Table of contents:** Sticky sidebar or in-article jump links (for evergreen guides)
- **Body content:** Rich typography with subheadings, pull quotes, inline images, tip/callout boxes
- **FAQ section:** Expandable accordion (for SEO structured data)
- **Related posts:** 3-card row at bottom
- **Newsletter CTA:** Inline or bottom-of-article signup

### 4.3 Navigation Context
The blog lives at flydenver.com/blog. The prototype should include a minimal nav bar that contextualizes the blog within the larger DEN site:
- DEN logo (left)
- "Blog" title or breadcrumb
- Search icon
- Link back to flydenver.com

---

## 5. SEO & Structured Data Notes

The prototype should demonstrate SEO-aware patterns (even if not fully functional):

- **URL structure:** `/blog/[category]/[post-slug]` (show in breadcrumbs)
- **Meta elements:** Include `<title>` and meta description in the article template
- **Schema.org markup:** Include JSON-LD for Article and FAQPage schema in the article template (can be commented out or displayed as a code sample)
- **Internal linking:** Article body should include contextual links to other blog posts
- **"Last updated" dates:** Displayed prominently on evergreen content
- **FAQ accordions:** Structured for potential FAQ rich snippet capture

---

## 6. Technical Implementation

### Stack
- Build as a **single-file React component (.jsx)** using Tailwind CSS utility classes
- Use Google Fonts for typography (import via `<link>` in a style tag or `@import`)
- Use placeholder images from Unsplash (airport/Denver themed) or solid gradient placeholders
- Include smooth transitions and micro-interactions (hover states on cards, scroll animations if feasible)
- Make it fully responsive (mobile-first)

### State Management
- Use React `useState` for:
  - Active category filter
  - Current view (index vs. article detail)
  - Newsletter email input
  - FAQ accordion open/close states
  - Mobile nav toggle

### Interaction Requirements
- Clicking a category filter should filter the post grid
- Clicking a post card should navigate to the article detail view
- "Back to blog" should return to the index
- FAQ items should toggle open/close
- Newsletter form should show a success state on submit
- Smooth scroll to sections via table of contents links

---

## 7. Content Distribution Callouts

The prototype should visually hint at the blog's role in the broader content ecosystem. Include one or more of:
- A "Subscribe to the DEN Newsletter" CTA that references the blog feeding email
- Social share buttons on articles
- A small "Follow DEN" social links strip
- An "Also available on" or distribution note somewhere subtle

---

## 8. Sample Article Content

For the article detail page, use this sample content for **"Your Complete Guide to DEN Security Wait Times"**:

**Category:** Travel Tips
**Headline:** Your Complete Guide to DEN Security Wait Times
**Subtitle:** Everything you need to know about getting through security at Denver International Airport — including real-time tips, the best times to fly, and how to speed up the process.
**Author:** DEN Travel Team
**Date:** March 2026
**Read Time:** 8 min read
**Last Updated:** March 2026

**Sections to include:**
1. Current Security Checkpoint Locations (North, South, Bridge)
2. Average Wait Times by Time of Day (include a simple chart/visual)
3. Tips for Getting Through Faster (TSA PreCheck, CLEAR, packing tips)
4. The Best Times to Fly from DEN
5. What to Expect During Great Hall Construction
6. FAQs (expandable):
   - "What is the busiest day at DEN?"
   - "Can I use TSA PreCheck at DEN?"
   - "Which security checkpoint is fastest?"
   - "How early should I arrive at DEN?"

Use realistic but clearly fictional placeholder data for wait times. Include a tip/callout box style element and at least one inline image break.

---

## 9. Launch Strategy Context (for informational awareness)

This context helps Claude understand the broader picture — it does not need to be reflected in the UI unless helpful:

- **Cadence:** ~2 posts/month ongoing, with a pre-launch batch of ~10 posts so the blog launches with substance
- **SEO priority topics** (from GA4/GSC/SEMrush research): security wait times, parking, dining by gate, car rentals, conspiracy theories/art/architecture, lounges, transportation options, amenities
- **DEN's domain authority advantage:** flydenver.com has strong DA, but third-party sites are outranking them on their own topics. The blog is designed to reclaim those rankings.
- **AI Overview opportunity:** Building topical authority through comprehensive, well-structured content creates eligibility for Google AI Overview citations
- **Tech:** WordPress post type already exists on flydenver.com — just needs a template. This prototype informs that template design.

---

## 10. Prototype Deliverable Checklist

When building, ensure the prototype includes:

- [ ] Blog index page with hero, category filters, and post card grid
- [ ] At least one full article detail page with rich formatting
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Category filtering interaction
- [ ] Navigation between index and article views
- [ ] Newsletter signup CTA
- [ ] FAQ accordion on article page
- [ ] Table of contents / jump links on article page
- [ ] Social share buttons
- [ ] Distinctive, non-generic design that reflects DEN's brand personality
- [ ] Placeholder content that demonstrates the content strategy (mix of evergreen, news, features)

---

*This specification was created to give Claude full context for building a high-fidelity blog prototype for Denver International Airport. The prototype should demonstrate both the design vision and the content strategy so stakeholders can evaluate the concept before WordPress template development begins.*
