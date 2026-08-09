# App Opportunity Research

**Last updated:** August 9, 2026  
**Purpose:** Research, compare, validate, and financially gate multiple potential application businesses across iOS, Android, and the web.

## What this repository is

This is a **portfolio research repository**, not the codebase for one application.

It is intended to produce multiple evidence-backed product opportunities over time. Market research, competitor data, app-review mining, pricing analysis, cost models, experiments, and investment decisions remain here. When an opportunity earns a formal GO decision, its application is created in a separate private product repository.

## Current cross-platform landscape

The first portfolio map covers ten commercially important categories across the Apple App Store, Google Play, and the web.

- [`research/00-top-10-cross-platform-categories.md`](./research/00-top-10-cross-platform-categories.md) — full category landscape, platform leaders, opportunity ranking, cost bands, and category briefs.
- [`market-data/top-10-cross-platform-category-scorecard-2026.csv`](./market-data/top-10-cross-platform-category-scorecard-2026.csv) — machine-readable category scorecard.
- [`decisions/category-research-roadmap.md`](./decisions/category-research-roadmap.md) — portfolio funnel, standard research method, scoring system, and capital-release gates.
- [`sources/2026-market-source-registry.md`](./sources/2026-market-source-registry.md) — source hierarchy, links, limitations, and evidence rules.

### Two rankings are intentionally maintained

The categories with the most current money and attention are not necessarily the best categories for a new entrant.

| Market-power rank | Category | New-entrant rank | Portfolio view |
|---:|---|---:|---|
| 1 | Social, Dating & Communities | 10 | Massive market; severe network, safety, moderation, and acquisition barriers |
| 2 | Entertainment, Streaming & Short Drama | 9 | Strong spend; content and paid-distribution economics dominate |
| 3 | AI Assistants & Vertical Agents | 6 | Strong demand; pursue only through a focused workflow and proprietary context |
| 4 | Shopping, Resale & Seller Tools | 5 | Favor seller intelligence and workflow tools over a new marketplace |
| 5 | Creator, Photo & Video Tools | 7 | Proven subscriptions but highly AI-saturated and inference-cost exposed |
| 6 | Business, Productivity & Utilities | 1 | **Best risk-adjusted starting category** |
| 7 | Finance, Budgeting & Investing | 8 | Strong willingness to pay; trust, data, security, and regulation raise the barrier |
| 8 | Health, Fitness & Nutrition | 3 | Excellent subscription economics; higher privacy, policy, and accuracy obligations |
| 9 | Education, Language & Professional Coaching | 2 | Strong outcome-specific and habit-based opportunities |
| 10 | Travel, Navigation & Local Discovery | 4 | Attractive focused utilities; real-time data and seasonality matter |

AI is treated primarily as a **capability inside a domain product**, not as a complete category thesis. A vertical finance, health, travel, education, or business agent should be evaluated first through the economics and customer problem of that domain.

## Active candidate build plans

### Project Aahar — Health, Fitness & Nutrition

A nutrition-first general-wellness application for South Asian adults. The proposed wedge is fast photo-assisted meal logging with targeted confirmation questions, transparent nutrient ranges, deterministic calculations, and household recipe memory.

- [`plans/health-fitness-nutrition/01-project-aahar-build-plan.md`](./plans/health-fitness-nutrition/01-project-aahar-build-plan.md) — product scope, user journeys, AI and nutrition architecture, privacy/compliance boundary, delivery phases, costs, metrics, launch plan, and GO/REVISE/KILL gates.
- [`plans/health-fitness-nutrition/02-project-aahar-mvp-backlog.csv`](./plans/health-fitness-nutrition/02-project-aahar-mvp-backlog.csv) — phase-by-phase executable backlog with owners, dependencies, acceptance criteria, and investment gates.

**Current status:** Phase 0 validation plan only. A separate product repository and commercial build are not approved until the concept passes the documented gates.

## Existing first-pass domain studies

These reports predate the broader ten-category map and are now treated as initial dossiers within the portfolio:

- [`research/01-vertical-ai-business.md`](./research/01-vertical-ai-business.md)
- [`research/02-education-coaching.md`](./research/02-education-coaching.md)
- [`research/03-health-nutrition.md`](./research/03-health-nutrition.md)
- [`research/04-creator-photo-video.md`](./research/04-creator-photo-video.md)
- [`financial-models/shared-cost-model.md`](./financial-models/shared-cost-model.md)

They will be revised as deeper competitor, pricing, review, and validation evidence is collected.

## Portfolio funnel

The research program is designed to reduce 10 broad markets to a small number of investable products:

1. **10 category tracks**
2. **3–5 concepts per category** — approximately 30–50 concepts
3. **One evidence-backed shortlist per category**
4. **Five low-cost validation experiments**
5. **Two or three concierge/prototype candidates**
6. **Separate product repository only after a GO decision**

More than one application may ultimately be built, but development capital is released sequentially rather than spread across ten simultaneous builds.

## Research order

### Wave 1

1. Business, Productivity & Utilities
2. Education, Language & Professional Coaching
3. Health, Fitness & Nutrition

### Wave 2

4. Travel, Navigation & Local Discovery
5. Shopping, Resale & Seller Tools
6. Finance, Budgeting & Investing

### Wave 3

7. AI Assistants & Vertical Agents
8. Creator, Photo & Video Tools

### Observe first

9. Entertainment, Streaming & Short Drama
10. Social, Dating & Communities

## Standard category research package

Every category should eventually contain:

- Top iOS, Android, and web products.
- Pricing, trials, monetization, target segment, positioning, and distribution.
- A feature and workflow matrix.
- 500–1,500 pieces of review/support/community evidence where feasible.
- Complaint clusters with frequency, severity, workaround, and willingness-to-pay implications.
- Three to five differentiated product concepts.
- Founder-assisted and professional build estimates.
- API/infrastructure economics at 100, 1,000, and 10,000 active users.
- Regulatory, privacy, safety, content, and platform-policy risks.
- A low-cost validation experiment with explicit pass, revise, and kill thresholds.

## Investment gates

### Gate 0 — desk research

Build the competitor map, complaint clusters, concept set, and preliminary economics.

### Gate 1 — problem and price validation

Do not spend more than approximately **$2,500–$3,000 per shortlisted concept** before repeated pain and real willingness-to-pay evidence exists.

### Gate 2 — functional proof

Do not spend more than approximately **$10,000–$12,000 cumulatively for most concepts** before users repeat the workflow and real payment or pilot evidence appears.

### Gate 3 — commercial MVP

Only after Gate 2 should the project receive a feature-level estimate, privacy/policy review, approved budget, formal GO record, and separate product repository.

## Core principle

A category is not selected because it is trending, because an incumbent earns substantial revenue, or because an AI-generated concept sounds compelling.

A product earns investment only when four things align:

> **Repeated painful problem + reachable customer + credible differentiated workflow + economics supported by actual behavior.**

## Important research limitations

Third-party mobile revenue and download figures are estimates rather than audited company financial statements. Store rankings change frequently and underrepresent products monetized through advertising, commerce, bookings, payments, lending, brokerage, enterprise contracts, or web subscriptions. Website traffic indicates demand and habit, not necessarily profitability. Every shortlisted concept must be re-verified before capital is committed.
