# Multi-Application Category Research Roadmap

**Decision date:** August 8, 2026  
**Repository:** `yashumani/app-opportunity-research`  
**Status:** Active research program

## 1. Decision

This repository is not the source repository for one application. It is the research and investment-control layer for a **portfolio of potential applications**.

The portfolio will begin with ten cross-platform application categories, generate several product concepts inside each category, test the strongest concepts cheaply, and create a separate production repository only when a concept earns a formal GO decision.

### Repository boundaries

- **This repository owns:** market research, competitor data, app reviews, pain-point analysis, opportunity scoring, pricing hypotheses, cost models, validation evidence, and investment decisions.
- **Future product repositories own:** product requirements, architecture, source code, tests, deployment, operations, and product-specific documentation.
- Research may produce multiple applications over time. It should therefore remain independent from every application codebase.

---

## 2. Portfolio funnel

The planned funnel is:

| Stage | Target volume | Required output |
|---|---:|---|
| Category landscape | 10 categories | Cross-platform demand, economics, barriers, and preliminary ranking |
| Concept generation | 3–5 per category | Approximately 30–50 focused application concepts |
| Evidence shortlist | 1 per category | Up to 10 concepts with competitor and complaint evidence |
| Validation portfolio | 5 concepts | Landing page, concierge test, prototype, or paid pilot |
| Prototype portfolio | 2–3 concepts | Repeated-use proof and real pricing evidence |
| Product build | 1 or more, sequentially | Separate product repository after GO approval |

The objective is not to force one winner. More than one product may eventually be built, but capital is released **sequentially**, not across ten simultaneous builds.

---

## 3. Category tracks

### Wave 1 — highest risk-adjusted opportunity

1. **Business, Productivity & Utilities**
2. **Education, Language & Professional Coaching**
3. **Health, Fitness & Nutrition**

These tracks combine proven willingness to pay with reasonably narrow target segments. Business and Education can be validated with low-cost concierge or asynchronous prototypes. Health has excellent category economics but requires more trust, accuracy, privacy, and policy work.

### Wave 2 — strong focused utility opportunities

4. **Travel, Navigation & Local Discovery**
5. **Shopping, Resale & Seller Tools**
6. **Finance, Budgeting & Investing**

These categories contain many successful narrow utilities. Research should avoid broad marketplaces or regulated money movement and instead prioritize execution, intelligence, workflow, and read-only analysis.

### Wave 3 — attractive but technically or competitively expensive

7. **AI Assistants & Vertical Agents**
8. **Creator, Photo & Video Tools**

AI is treated primarily as a horizontal capability inside a domain product. Creator tools are investigated only through profession-specific, outcome-based workflows with controlled inference costs.

### Observe-first categories

9. **Entertainment, Streaming & Short Drama**
10. **Social, Dating & Communities**

These are major markets but poor first-build candidates because content, network effects, moderation, safety, and paid acquisition can dominate engineering cost. Research may identify adjacent tools, but no consumer platform build should begin without proprietary distribution, community, or content.

---

## 4. Standard category dossier

Every category will use the same research template so comparisons remain consistent.

### 4.1 Market and platform map

- Current category size and growth signals.
- Top 20 meaningful iOS applications.
- Top 20 meaningful Android applications.
- Top web services, including web-first alternatives.
- Mobile versus web role in the customer journey.
- Monetization models: subscriptions, commerce, advertising, usage, lead generation, transactions, enterprise contracts, or hybrid.

### 4.2 Competitor intelligence

For each relevant competitor:

- Company, product, platform, geography, and target audience.
- App-store rating and ranking/download indicators.
- Web-traffic or search-demand indicators where available.
- Pricing, trial, annual discount, free tier, and paywall timing.
- Core promise and positioning.
- Feature and workflow map.
- Distribution channels and visible growth loops.
- Data, content, community, network, or integration advantages.
- Important limitations in the available evidence.

### 4.3 Review and complaint mining

Target **500–1,500 pieces of user evidence per category** where collection is technically and legally feasible. Sources may include app reviews, support forums, Reddit discussions, product communities, public issue trackers, and review sites.

Each complaint should be tagged by:

- Product and platform.
- Date and rating where available.
- Customer segment or use case.
- Pain-point cluster.
- Severity and frequency.
- Current workaround.
- Whether the problem is a missing feature, broken workflow, trust issue, price issue, performance issue, support issue, or distribution/content problem.
- Evidence of willingness to pay or switch.

Do not treat one dramatic review as market validation. The analysis must show recurrence across independent users and preferably multiple competitors.

### 4.4 Concept generation

Generate 3–5 concepts per category. Each concept must state:

- Exact target customer.
- Job to be done.
- Existing behavior or workaround.
- Narrow initial wedge.
- Why incumbents underserve it.
- Core workflow and minimum usable feature set.
- Mobile role, web role, and any integrations.
- Monetization hypothesis.
- Defensibility beyond model access or UI.
- Distribution hypothesis.
- Principal technical, operational, regulatory, and unit-economic risks.

### 4.5 Cost and unit economics

Estimate at four levels:

1. **Validation:** interviews, review mining, landing page, manual service, or clickable prototype.
2. **Functional proof:** one end-to-end workflow with real users.
3. **Founder-assisted commercial MVP:** founder owns product/data/QA and contracts specialized work.
4. **Professional commercial MVP:** production mobile/web product with backend, payments, analytics, QA, privacy, monitoring, and release.

Model costs at:

- 100 active users/customers.
- 1,000 active users/customers.
- 10,000 active users/customers.
- Average and 90th-percentile usage.

Include model/API inference, data providers, storage, media processing, support, marketplace/payment fees, security/compliance, and customer acquisition—not only engineering.

### 4.6 Validation design

Every shortlisted concept receives a cheap experiment with:

- Testable hypothesis.
- Target participant profile.
- Recruitment channel.
- Prototype or concierge workflow.
- Price shown to participants.
- Activation, repeat-use, payment, and qualitative trust metrics.
- Predefined pass, revise, and kill thresholds.

---

## 5. Opportunity scoring framework

Each concept will be scored from 0–10 on the following dimensions. Scores require written evidence, not intuition alone.

| Dimension | Weight | Meaning |
|---|---:|---|
| Problem frequency and severity | 15% | How often the pain occurs and how costly/frustrating it is |
| Proven willingness to pay | 15% | Existing spend, switching behavior, or real payment evidence |
| Differentiation and unmet need | 12% | Evidence that current products fail materially |
| Reachable target segment | 10% | Ability to identify and contact the customer |
| Distribution controllability | 10% | Organic, direct-sales, partnership, community, SEO, or product-led path |
| Retention potential | 10% | Recurring need, accumulated data/context, habit, workflow lock-in |
| Build feasibility | 8% | Ability to deliver a credible MVP with available skills and capital |
| Unit economics | 8% | Margin after APIs, content, support, fees, and acquisition |
| Founder-market fit | 5% | Domain knowledge, credibility, access, and execution advantage |
| Regulatory/safety simplicity | 4% | Lower legal, policy, privacy, and harm risk receives a higher score |
| Expansion potential | 3% | Adjacent customers, workflows, or products after wedge validation |

### Score interpretation

- **8.0–10.0:** strong candidate for validation.
- **7.0–7.9:** validate only with a sharply defined wedge.
- **6.0–6.9:** research or observe; do not fund a full MVP.
- **Below 6.0:** reject unless new evidence materially changes the thesis.

A high category score does not automatically make every concept in that category attractive.

---

## 6. Capital-release gates

### Gate 0 — desk research

**Budget ceiling:** approximately $300–$1,000 per category, depending on data/tool access.

Required evidence:

- Cross-platform competitor map.
- Repeated complaint clusters.
- At least three focused concepts.
- Preliminary cost and distribution model.

### Gate 1 — problem and price validation

**Cumulative budget ceiling:** approximately $2,500–$3,000 per shortlisted concept.

Required evidence:

- 10–20 qualified customer conversations or equivalent behavioral evidence.
- Repeated pain across independent sources.
- A price-bearing offer.
- At least 3–5 users willing to pay, prepay, sign a pilot, deposit, or repeatedly use a concierge version.

Compliments, survey interest, and “I would use this” do not pass the gate.

### Gate 2 — functional proof

**Cumulative budget ceiling:** approximately $10,000–$12,000 for most concepts before clear traction; media-heavy concepts may require a separately approved ceiling.

Required evidence:

- The core workflow works end to end.
- Users return without repeated founder persuasion.
- Measured time, money, accuracy, confidence, or outcome improvement.
- Real payment or a credible organizational commitment.
- Acceptable preliminary variable cost.

### Gate 3 — commercial MVP

Release larger development capital only after Gate 2. Before proceeding:

- Lock the first persona, workflow, and pricing hypothesis.
- Define 90-day activation and retention targets.
- Complete a feature-level engineering estimate.
- Model average and heavy-user unit economics.
- Confirm platform policy, legal, privacy, and data-provider constraints.
- Create a separate private product repository.

### Gate 4 — growth

No paid-growth scaling until:

- Cohort retention is measured.
- Contribution-margin LTV can support observed CAC.
- Support and reliability are stable.
- The product's differentiation persists after real use.

---

## 7. Product-repository creation rule

A dedicated repository is created only after a concept receives a GO decision. Naming should describe the product rather than the research category, for example:

- `executive-operations-brief`
- `analytics-communication-coach`
- `south-asian-nutrition-tracker`
- `travel-disruption-assistant`
- `reseller-margin-intelligence`

At creation, the research repo should contain a decision record linking to the new product repository and preserving:

- Evidence summary.
- Selected customer and problem.
- Approved MVP scope.
- Budget ceiling.
- Success and kill metrics.
- Known risks and excluded scope.

The product repository should not duplicate the full market-research archive.

---

## 8. Immediate work sequence

### Sprint 1 — Business, Productivity & Utilities

- Build a 20–30 product competitor set across narrative BI, spreadsheet copilots, operational reporting, small-business dashboards, alerts, invoicing/field tools, document workflow, and adjacent utilities.
- Separate enterprise BI from SMB workflow products.
- Identify review evidence around setup effort, trust, hallucination, metric governance, alert fatigue, mobile usability, integrations, pricing, and executive reporting.
- Produce 3–5 concepts and one validation experiment.

### Sprint 2 — Education & Professional Coaching

- Map role-play, interview, language-speaking, presentation, communication, and job-specific coaching products.
- Test whether role-specific outcomes create stronger pricing and retention than generic AI tutoring.

### Sprint 3 — Health, Fitness & Nutrition

- Map general trackers and culturally/sport/life-stage-specific products.
- Prioritize trust, correction workflows, adherence, and underserved food/activity data.
- Define a strict general-wellness boundary before prototype work.

After Wave 1, the scorecard will be recalibrated before Wave 2 begins.

---

## 9. Decision principle

The repository will not select a product because it is fashionable, because a competitor earned substantial revenue, or because an AI model generated a compelling idea.

A product earns investment only when four things align:

> **Repeated painful problem + reachable customer + credible differentiated workflow + economics supported by actual behavior.**
