# Project Aahar — Health, Fitness & Nutrition App Build Plan

**Plan date:** August 9, 2026  
**Status:** Candidate plan — pre-validation, not yet approved for full product development  
**Category:** Health, Fitness & Nutrition  
**Working title:** Project Aahar  
**Primary market:** South Asian adults in the United States  
**Initial platforms:** iOS and Android, supported by a web landing page and internal administration console  
**Future product repository:** `south-asian-nutrition-app` after the concept passes the investment gates in this plan

> **Working product promise:** Track Indian and South Asian home-cooked meals in under 45 seconds, receive transparent calorie and macro ranges, and build a sustainable nutrition-and-activity routine without pretending that a food photo is perfectly accurate.

The working title is temporary. Complete a trademark, domain, App Store, and Google Play name search before adopting a final brand.

---

## 1. Executive decision

Build one **nutrition-first general-wellness application** for South Asian adults who currently struggle to log homemade meals accurately in mainstream calorie trackers.

The initial product will combine three tightly connected jobs:

1. **Nutrition:** fast, culturally accurate meal logging using a photo, targeted confirmation questions, household recipes, and deterministic nutrient calculations.
2. **Fitness adherence:** lightweight step and activity tracking rather than a full workout-program marketplace.
3. **Health progress:** weight and habit trends presented as general-wellness information, without diagnosing, treating, or managing disease.

The app will not begin as a broad “all-in-one health super-app.” Its wedge is the frustrating, high-frequency task of logging South Asian home-cooked food. Fitness and progress features exist to support retention and outcomes, not to dilute the initial promise.

### Product principle

> **AI proposes. The user confirms. A deterministic nutrition engine calculates. The product remembers.**

The language model must never be the final calculator of calories, protein, carbohydrates, fat, fiber, or micronutrients.

---

## 2. Target customer

### Initial target segment

- Age 18 and older.
- South Asian adults living in the United States.
- English-speaking initial release.
- Eats Indian or South Asian homemade food at least four times per week.
- Is trying to manage weight, calories, protein, macros, or overall meal consistency.
- Currently uses, abandoned, or considered products such as MyFitnessPal, Lose It!, Cronometer, MacroFactor, HealthifyMe, Cal AI, or manual notes/spreadsheets.
- Is frustrated by ambiguous entries such as “curry,” “dal,” “rice plate,” or generic restaurant estimates.

### Secondary segments after validation

- South Asian fitness coaches managing client meal compliance.
- Households that cook shared recipes.
- Indian students and professionals living abroad.
- Users mixing South Asian and Western meals.
- Other cuisines with similar homemade mixed-dish ambiguity.

### User problem statement

> “I want to track what I eat, but my home-cooked meals are not standardized. A photo cannot reveal oil, ghee, cream, sugar, flour, or precise portions, and manual recipe entry takes too long. Existing apps either make me guess or give me a precise-looking number that I do not trust.”

---

## 3. Differentiated value proposition

### Primary value proposition

**Track a familiar South Asian meal quickly without sacrificing honesty about uncertainty.**

### Differentiators

1. **Confirmation-first photo logging**  
   The system asks only the highest-impact questions: portion, oil/ghee, key ingredient, cooking style, and recipe variant.

2. **Transparent confidence and ranges**  
   The app shows an estimated range when inputs remain uncertain rather than a falsely precise calorie number.

3. **South Asian food ontology**  
   Dishes are represented by region, cooking method, ingredient family, and household variation—not collapsed into generic “curry.”

4. **Household recipe memory**  
   Once a user corrects the family’s poha, rajma, biryani, sabzi, dal, or roti recipe, the product reuses that configuration.

5. **Deterministic nutrient calculation**  
   Nutrients are calculated from structured ingredients and portions using traceable data sources.

6. **Nutrition plus adherence**  
   The app emphasizes protein, fiber, calorie range, meal consistency, steps/activity, and weekly progress rather than only weight loss.

7. **No advertising business model using health data**  
   The initial business model is subscription-based. Health, meal, weight, and activity data are not used for targeted advertising.

---

## 4. Product scope

## 4.1 Must-have commercial MVP

### Account and onboarding

- Email, Apple, and Google authentication.
- Age confirmation: 18+ for the first release.
- Country, dietary preference, cuisine preference, height, weight, optional goal weight, activity level, and goal.
- User may select a suggested calorie target or enter a target supplied by a coach or professional.
- The methodology and limitations of any suggested target are disclosed.
- Consent to privacy policy, terms, and health-data processing.

### Meal logging

- Camera capture and photo upload.
- AI returns one to three likely dishes/components.
- Structured confirmation flow:
  - Dish/ingredient confirmation.
  - Portion selection or optional gram weight.
  - Oil, ghee, butter, cream, sugar, coconut milk, or other high-impact ingredient confirmation.
  - Cooking method and household variation.
- Manual search and manual meal entry.
- Recent meals, favorites, and one-tap copy.
- Meal time and meal label.
- Edit and delete meal.

### Nutrition calculation

- Calories, protein, carbohydrates, fat, and fiber in the primary interface.
- Micronutrients available only when underlying data quality is sufficient.
- Source and confidence indicator.
- Estimated range where portion or recipe uncertainty remains.
- Deterministic calculation from structured food and recipe records.
- No diagnosis, treatment, medication, or disease-management recommendation.

### Recipe and household memory

- Create a recipe from ingredients and yield.
- Save household version of a dish.
- Save serving sizes.
- Reuse leftovers.
- Learn from corrections at the user or household level.
- Version recipes when ingredients or yield change.

### Daily and weekly dashboard

- Calories and macro range versus target.
- Protein and fiber progress.
- Meal consistency.
- Weight trend.
- Weekly adherence summary.
- Neutral language; no shaming, fear, or extreme-diet messaging.

### Fitness adherence

- Manual activity minutes in the first alpha.
- Read-only step and workout-minute integration with Apple HealthKit and Android Health Connect before public launch if privacy review and implementation quality are adequate.
- No heart-rate diagnosis, medical interpretation, or treatment logic.

### Subscription and account controls

- Free and paid entitlement management through RevenueCat.
- Restore purchases.
- Subscription status.
- In-app data export request.
- In-app account and data deletion.
- Photo-retention preference.

### Reliability and support

- Offline-friendly recent-meal access where practical.
- Crash/error monitoring without sending meal, weight, health, or photo content to monitoring tools.
- In-app feedback and “report incorrect nutrition” flow.
- Support site and contact channel.

## 4.2 Explicitly out of scope for version one

- Diabetes, hypertension, PCOS, kidney disease, pregnancy, eating-disorder, or other condition-management programs.
- Medical diagnosis, risk scoring, treatment, symptom checking, or medication advice.
- Live dietitian or clinician consultations.
- AI-generated medical meal plans.
- Full workout-program marketplace.
- Social feed, public profiles, challenges, or competitive leaderboards.
- Users under 18.
- Restaurant menu scraping at scale.
- Automatic grocery ordering.
- Wearable heart-rate interpretation.
- Apple Watch or Wear OS standalone applications.
- More than one launch language.
- “Unlimited” photo analysis without an observed unit-cost model.

---

## 5. Core user journeys

## 5.1 First-day activation

1. User installs the app.
2. Creates an account and confirms age.
3. Selects goal: maintain, lose, gain, improve protein, or improve consistency.
4. Selects vegetarian/non-vegetarian and regional cuisine preferences.
5. Sets or accepts a calorie/protein target.
6. Logs the first meal by photo or manual entry.
7. Confirms dish, portion, and high-impact ingredients.
8. Sees a nutrition range and source/confidence explanation.
9. Saves the meal or household recipe.

**Activation definition:** user completes onboarding, sets a goal, and logs at least three meals within the first 24 hours.

## 5.2 Photo-to-log flow

1. Capture or select photo.
2. Client compresses and strips unnecessary metadata.
3. Server stores the image using a short-lived signed upload.
4. Vision model proposes dish/component candidates and uncertainty tags.
5. Question engine asks two to four high-impact questions.
6. Structured mapper links answers to canonical foods and recipe templates.
7. Nutrition engine calculates nutrients and uncertainty range.
8. User reviews, edits, and saves.
9. Corrections update the user’s reusable meal/recipe profile.

## 5.3 Household recipe flow

1. User selects “Create my recipe.”
2. Adds ingredients through search, barcode, or manual entry.
3. Enters total cooked yield or number of servings.
4. App calculates nutrients deterministically.
5. User saves recipe as “My home rajma,” “Mom’s poha,” etc.
6. Future photo recognition can propose that household recipe.

## 5.4 Weekly review flow

1. App summarizes logging consistency, average calorie range, protein, fiber, steps/activity, and weight trend.
2. It highlights one or two neutral, actionable observations.
3. User may choose a next-week habit such as “add protein at breakfast” or “log dinner five days.”
4. No medical or disease-specific recommendation is generated.

---

## 6. AI and nutrition-engine design

## 6.1 Pipeline

### Stage A — visual candidate generation

Input: compressed meal image plus optional user context.  
Output: structured candidates only:

- Possible dishes/components.
- Visible portion cues.
- Cooking-method cues.
- Uncertainty flags.
- Questions that would materially change the nutrient calculation.

The model must not return the final nutrition values.

### Stage B — clarification prioritization

Select the smallest set of questions with the greatest expected impact, such as:

- One or two rotis?
- Paneer or tofu?
- Approximately how much rice?
- Was the curry made with cream/coconut milk?
- How much oil or ghee was used in the full recipe?
- Homemade or restaurant version?

Target: median of two questions, maximum four for the ordinary flow.

### Stage C — structured food mapping

Map the confirmed meal to:

- Canonical dish.
- Recipe template version.
- Ingredient records.
- Serving amount.
- Preparation method.
- Data provenance.

### Stage D — deterministic nutrient calculation

- Sum nutrient values from structured ingredients.
- Divide by confirmed yield/serving.
- Apply portion range when exact weight is unavailable.
- Return base estimate plus lower/upper range.
- Version calculation logic and source records for reproducibility.

### Stage E — correction learning

Store:

- User-confirmed dish.
- User’s household recipe ID.
- Common serving size.
- Repeated correction pattern.
- Confidence improvement over time.

Do not train a global model directly on private user data without explicit consent and a separate privacy decision.

## 6.2 Model-routing policy

- Use a cost-optimized multimodal model for ordinary meal classification.
- Escalate only ambiguous, multi-dish meals to a stronger model.
- Use a low-cost text model for question selection and structured normalization.
- Cache repeated household meals and recipe mappings.
- Re-run visual analysis only when the user requests it or the first result fails.
- Maintain a provider abstraction so the product is not permanently coupled to one AI vendor.

## 6.3 Quality evaluation dataset

Before public beta, create a controlled dataset containing:

- At least 500 meal photos.
- At least 100 high-frequency South Asian dishes.
- Multiple lighting conditions and plate styles.
- Mixed meals, thalis, leftovers, restaurant food, and home food.
- Ground-truth dish labels.
- Weighed or recipe-based reference portions for a subset.
- Expert-reviewed nutrient calculations for the structured subset.

Evaluate separately:

- Correct dish present in top three candidates.
- Portion-question quality.
- High-impact ingredient-question recall.
- Final calculation reproducibility.
- Difference between photo-only estimate and confirmed structured estimate.
- Performance across vegetarian and non-vegetarian meals.

---

## 7. Food-data strategy

## 7.1 Data layers

1. **USDA FoodData Central** for foundational and branded nutrient data.
2. **Curated South Asian ingredient records** for ingredients not represented cleanly in the base source.
3. **Curated recipe templates** for common dishes and regional variants.
4. **Household/user recipes** calculated from ingredients and yield.
5. **User corrections** that personalize recurring meals.
6. **Source/confidence metadata** attached to every calculated result.

USDA FoodData Central provides REST search/details endpoints, requires an API key, currently documents a default limit of 1,000 requests per hour per IP, and publishes its data in the public domain under CC0. Cache permitted reference data and never expose the API key in the mobile client.

## 7.2 Initial curated data target

### Validation prototype

- 40–60 common dishes.
- 100–150 ingredients.
- 10 representative mixed plates.

### Closed beta

- 100–150 dishes.
- 300–500 ingredients/variants.
- Regional tags.
- Vegetarian/non-vegetarian variants.
- Basic restaurant versus household distinctions.

### Public version one

- 200–300 validated dish templates.
- User recipe builder to cover the long tail.
- Versioned calculation records and source notes.

## 7.3 Data-quality controls

- Every recipe template has an owner, source, version, date, ingredient list, yield, and review status.
- Changes require regression tests against known totals.
- Duplicate food entries are merged or explicitly distinguished.
- Micronutrients are hidden when source completeness is insufficient.
- Reported errors enter a data-quality queue.
- A nutrition-data specialist or registered dietitian reviews methodology, claims, and a representative sample before public release.

---

## 8. Safety, privacy, and compliance boundary

## 8.1 General-wellness boundary

The FDA’s January 2026 general-wellness guidance distinguishes low-risk software intended to maintain or encourage a healthy lifestyle from functions intended for diagnosis, cure, mitigation, prevention, or treatment of disease. Version one must remain on the general-wellness side of that boundary.

### Product-language rules

Use:

- “Estimate.”
- “General wellness.”
- “May help you track.”
- “Calculated from the ingredients and portions you confirmed.”

Do not use:

- “Diagnoses.”
- “Treats.”
- “Prevents disease.”
- “Medical-grade accuracy.”
- “Safe for diabetes/PCOS/pregnancy” without a separately reviewed regulated product strategy.

## 8.2 Apple requirements to design for

Apple’s App Review Guidelines state that medical apps that could provide inaccurate data may receive greater scrutiny and require disclosure of the data and methodology supporting health-measurement accuracy claims. Apple also restricts the use of health and fitness data for advertising and requires accurate handling of HealthKit data.

Plan requirements:

- Disclose nutrition-estimation methodology and limitations.
- Do not claim photo-only precision.
- Use HealthKit only for health and fitness purposes.
- Request only required HealthKit permissions.
- Do not place sensitive health data in advertising or analytics systems.
- Keep all store metadata consistent with the app’s actual general-wellness functionality.

## 8.3 Google Play requirements to design for

Google requires all published apps—including closed/open testing apps—to complete the Health apps declaration. This product will declare at least:

- **Nutrition and Weight Management**.
- **Activity and Fitness** if step/workout integration is included.

The declaration, store description, privacy policy, and in-app functionality must agree.

## 8.4 FTC health-data obligations

The FTC’s amended Health Breach Notification Rule explicitly applies to many health apps and similar technologies that are not covered by HIPAA. The company needs a documented incident-response and breach-notification process before public launch.

## 8.5 Privacy architecture

- Collect the minimum information needed for the product.
- Encrypt in transit and at rest.
- Use signed URLs for photos.
- Strip unnecessary image metadata.
- Default meal-photo retention target: delete raw photos after analysis within 30 days unless the user explicitly chooses to retain them.
- Separate identity data from meal/health records through clear access controls.
- Do not write meal descriptions, weight, health metrics, or photos into analytics event payloads.
- Redact sensitive data from application logs.
- Maintain consent, export, deletion, and administrative-access audit trails.
- Define deletion SLAs for primary data, derived data, backups, and third-party processors.
- Maintain a vendor/data-flow register.
- Conduct a lightweight threat model before closed beta and a professional security/privacy review before public launch.

## 8.6 Safety and eating-behavior design

- No shame, fear, or punishment language.
- No encouragement of extreme restriction, purging, or unsafe rapid weight loss.
- Do not generate aggressive calorie targets.
- Let users hide weight-centric elements where practical.
- Provide an easy path to pause goals and reminders.
- Escalate concerning support reports to a defined safety process.
- Keep the initial audience 18+.

This plan is product and engineering guidance, not legal advice. Obtain qualified legal/privacy review before launch.

---

## 9. Technical architecture

## 9.1 Recommended stack

| Layer | Recommended choice | Rationale |
|---|---|---|
| Mobile | React Native with Expo | One iOS/Android codebase and rapid beta distribution |
| Web | Next.js | Landing page, support, privacy pages, and internal/admin console |
| API | Python FastAPI | Strong ecosystem for data, nutrition calculations, and AI orchestration |
| Authentication/database | Supabase Auth + PostgreSQL | Managed auth, relational data, row-level security, and low initial cost |
| Object storage | Supabase Storage or S3-compatible storage | Signed uploads and explicit retention controls |
| Background processing | Managed queue/worker or serverless job system | Photo analysis, data imports, deletion, and weekly summaries |
| AI orchestration | Provider-abstracted service | Model routing, structured output validation, caching, and vendor flexibility |
| Subscription | RevenueCat | Cross-platform entitlements and purchase-state handling |
| Product analytics | Privacy-configured PostHog or Firebase | Funnel/retention events without health content |
| Error monitoring | Sentry or Crashlytics | Reliability monitoring with strict redaction |
| CI/CD | GitHub Actions + Expo EAS | Automated tests, builds, and staged releases |
| Secrets | Server-side secret manager | No AI, USDA, or infrastructure keys in the client |

## 9.2 Environments

- Local development.
- Shared development.
- Staging with synthetic/test health data.
- Production.

Production data must never be copied into development. Test accounts and store-review accounts must use synthetic data.

## 9.3 Core services

1. Identity and consent service.
2. Food and recipe catalog service.
3. Meal-analysis orchestration service.
4. Deterministic nutrition-calculation service.
5. Goals and progress service.
6. Activity-integration service.
7. Subscription/entitlement service.
8. Notification service.
9. Data export/deletion service.
10. Internal data-quality/admin service.

## 9.4 Core entities

- `users`
- `profiles`
- `consents`
- `goals`
- `foods`
- `food_nutrients`
- `recipe_templates`
- `recipes`
- `recipe_ingredients`
- `meals`
- `meal_items`
- `meal_photos`
- `meal_analysis_runs`
- `meal_confirmations`
- `user_food_corrections`
- `weight_logs`
- `activity_summaries`
- `subscriptions`
- `data_export_requests`
- `deletion_requests`
- `audit_events`
- `nutrition_quality_issues`

---

## 10. Delivery phases and schedule

The schedule assumes one strong full-stack/mobile engineer, founder product/data ownership, part-time design, part-time nutrition-data review, and release-focused QA. A solo part-time build will take materially longer.

## Phase 0 — problem and price validation: Weeks 1–3

### Deliverables

- Competitor map of 15–20 nutrition-tracking products.
- At least 500 review/support/community observations.
- Twenty target-user interviews.
- Fifteen to twenty participants in a seven-day meal diary study.
- Clickable confirmation-flow prototype.
- Landing page with real price options.
- Manual/concierge nutrition result for sample meals.

### Gate 1 pass criteria

- At least 70% of diary participants show repeated difficulty with current South Asian meal logging.
- Prototype reduces median logging time or correction burden meaningfully versus the current workflow.
- At least five target users provide a paid deposit, preorder, or explicit paid-pilot commitment at $9.99/month or more.
- No evidence that one incumbent already solves the complete problem well for the same segment.

### Kill/reframe condition

Fewer than five serious paid commitments after twenty qualified users, or users value generic convenience more than culturally accurate confirmation.

## Phase 1 — product, data, and risk design: Weeks 4–6

### Deliverables

- Approved PRD and scope boundary.
- UX flows and design system.
- Data model and architecture decision record.
- Privacy data-flow map.
- Threat model.
- General-wellness language guide.
- First 40–60 curated dishes and ingredients.
- Evaluation-dataset specification.
- API/provider proof tests.

### Gate 2A pass criteria

- Technical proof that the model can return structured dish candidates reliably enough to justify a prototype.
- Nutrition engine reproduces known recipe totals within defined rounding tolerance.
- Privacy and compliance review finds no unresolved blocker within the chosen scope.

## Phase 2 — functional proof: Weeks 7–10

### Build

- Mobile photo capture.
- Signed upload.
- Candidate identification.
- Clarification flow.
- Structured food mapping.
- Deterministic nutrient calculation.
- Save/edit meal.
- Minimal dashboard.
- Internal data-quality console.

### Test group

15–30 users for two weeks.

### Gate 2B pass criteria

- Median photo-to-saved-meal time: **45 seconds or less**.
- Correct dish/component appears in the top three candidates for **at least 75%** of evaluation meals.
- Median clarification count: **two or fewer**.
- At least 60% of test users log on five or more days during the test.
- At least five users pay to continue.
- Estimated AI/photo cost demonstrates a credible path below **$4 per active paid user per month** for ordinary usage.

## Phase 3 — commercial MVP: Weeks 11–18

### Build

- Production authentication and onboarding.
- Manual search and meal entry.
- Recipe builder and household memory.
- Goals and daily/weekly dashboard.
- Weight logs.
- Read-only activity integration if approved.
- Notifications.
- RevenueCat subscriptions.
- Restore purchases.
- Export and deletion.
- Analytics and monitoring with redaction.
- Support, privacy, terms, methodology, and limitation pages.
- CI/CD and staging environment.

### Exit criteria

- Feature-complete release candidate.
- Automated tests for nutrition calculations.
- No critical privacy/security findings.
- Store metadata and health declarations drafted.
- Data-quality review completed for launch catalog.

## Phase 4 — closed beta and hardening: Weeks 19–22

### Beta target

- 50–100 users.
- At least four weeks of usage for the earliest cohort.
- TestFlight distribution for iOS.
- Google Play closed test for Android.
- For a new Google personal developer account, schedule the required tester window into the release plan; current guidance requires at least 12 testers opted into the closed test for 14 days before applying for production access.

### Beta goals

- Crash-free sessions above 99.5%.
- P95 meal-analysis response within 10 seconds, excluding weak-network upload time.
- D7 retention at or above 35%.
- D30 retention at or above 20% for users with enough observation time.
- At least 40% of active users log meals on five or more days per week.
- Trial-to-paid conversion at or above 25%, with a stretch target near the Health & Fitness benchmark of 37.7%.
- Refund rate below 5%.
- AI, storage, and other direct technical variable costs below 30% of net subscription revenue.

## Phase 5 — marketplace launch: Weeks 23–24+

### Launch requirements

- App Store and Google Play listings.
- Accurate Health apps declaration.
- App privacy disclosures.
- Subscription terms and restore-purchase flow.
- Support site.
- Methodology and limitation statement.
- Incident-response and breach-notification procedure.
- Production monitoring and on-call ownership.
- Final accessibility and device testing.
- Creator/partner launch content.

Public launch occurs only after Gate 3 approval below.

---

## 11. Team and responsibilities

| Role | Initial allocation | Primary responsibility |
|---|---:|---|
| Founder/product lead | 0.5–1.0 FTE | Customer research, product scope, data logic, acceptance testing, pricing, partnerships |
| Senior mobile/full-stack engineer | 1.0 FTE | React Native, API, database, integrations, CI/CD, reliability |
| UX/UI designer | 0.2–0.4 FTE | Onboarding, photo confirmation, dashboard, accessibility, paywall |
| Nutrition-data specialist / dietitian reviewer | Project-based | Recipe methodology, data-quality sampling, claims and limitation review |
| QA engineer | 0.2 FTE during MVP; 0.5 FTE near launch | Device matrix, regression, subscriptions, deletion, offline/error states |
| Privacy/security counsel/reviewer | Project-based | Data flow, policies, HBNR readiness, store declarations, threat findings |
| Growth/content partner | Part-time before beta | Waitlist, creators, community partnerships, educational content |

The founder should own the metric definitions, data-quality framework, evaluation scorecard, and release gates rather than outsourcing product judgment.

---

## 12. Budget and capital gates

These are planning ranges, not vendor quotations.

## 12.1 Stage-level cash plan

| Stage | Cash ceiling | Rule |
|---|---:|---|
| Phase 0 validation | $1,000–$3,000 | No full engineering build |
| Functional proof | $6,000–$15,000 cumulative | Continue only after paid/problem evidence |
| Founder-assisted commercial MVP | $20,000–$45,000 cumulative | Founder owns product, data, QA, and part of implementation |
| Professional small-team MVP | $60,000–$140,000 | Use only after strong validation and approved financing |
| Contingency | 15–25% | Integration, data, review, and rework risk |

### Hard capital rule

Do not authorize more than **$45,000 of founder-funded cash** before the closed beta proves repeated use, acceptable variable cost, and real paid conversion.

## 12.2 Early monthly operating plan

| Cost | Early planning range |
|---|---:|
| Database, storage, API hosting, queue | $75–$400/month |
| Analytics, monitoring, email/notifications | $25–$200/month |
| AI/photo processing | Approximately $3–$10 per heavy active paid user initially |
| RevenueCat | $0 through first $2,500 monthly tracked revenue, then 1% of tracked revenue under current pricing |
| Nutrition data/content QA | $300–$2,000/month depending cadence |
| Support and bug-fix reserve | $500–$2,500/month after public launch |
| Legal/security review | Periodic project cost, not ordinary monthly SaaS |
| Marketing/acquisition | Separate experiment budget |

### Unit-cost target

- Beta target: direct AI/photo cost below $6 per paid active user per month.
- Launch target: below $4 for ordinary usage.
- Mature target: below 20% of net subscription revenue.

No “unlimited AI scans” promise should be made before observed usage supports it.

---

## 13. Pricing and monetization hypothesis

Test prices rather than assuming one price.

### Free

- Manual food search and entry.
- Basic dashboard.
- Limited photo analyses per month.
- Limited saved recipes.

### Pro hypothesis

- **$14.99/month**.
- **$119.99/year**.
- Up to approximately 90–100 photo analyses/month during the initial pricing model.
- Unlimited manual entries.
- Household recipes, correction memory, weekly insights, and activity integration.

### Pro Plus / Family — later experiment

- **$24.99/month** or annual equivalent.
- Multiple household profiles or shared recipes.
- Higher scan allowance.
- Coach/export tools only after demand appears.

### Price-validation cells

During Phase 0, test:

- $9.99/month.
- $14.99/month.
- $19.99/month.

Measure reservation/payment behavior rather than asking only “Would you pay?”

### Example 1,000-subscriber planning model

At $14.99/month:

- Gross monthly subscription revenue: approximately $14,990.
- At a 15% store-fee planning assumption: approximately $12,742 before taxes/refunds.
- At $4 direct AI/photo cost per active user: approximately $4,000.
- Remaining before infrastructure, support, acquisition, content, taxes, and payroll: approximately $8,742.

This is a scenario, not a forecast. If average AI cost rises toward $8–$10 per user, pricing, usage allowances, model routing, or the product design must change before paid acquisition scales.

---

## 14. Product and business KPI scorecard

## 14.1 Validation KPIs

- 20 qualified interviews.
- 15–20 completed seven-day diary participants.
- 500+ review/support observations.
- Five paid commitments.
- At least 70% report repeated South Asian meal-logging friction.

## 14.2 Product-quality KPIs

- Correct dish/component in top three: 75%+ at proof stage; 85%+ for high-frequency launch dishes.
- Median clarification questions: two or fewer.
- Median meal-log completion: 45 seconds or less.
- P95 analysis service response: 10 seconds or less after upload.
- Crash-free sessions: 99.5%+.
- Repeat-meal correction rate decreases over time.
- Nutrition calculations reproducible from stored inputs and source versions.

## 14.3 Engagement KPIs

- Activation: onboarding plus three meals in 24 hours.
- D1 retention: 55%+.
- D7 retention: 35%+.
- D30 retention: 20%+ before public launch.
- At least 40% of active users log on five or more days per week.
- At least 25% of active users reuse a saved meal or household recipe weekly.

## 14.4 Monetization KPIs

- Trial start during first session for users shown the paywall.
- Trial-to-paid: 25% minimum beta target; 37.7% category-benchmark stretch target.
- Refund rate below 5%.
- Direct variable technical cost below 30% of net revenue in beta and below 20% after optimization.
- CAC payback target below three months before scaling paid acquisition.

## 14.5 Privacy and safety KPIs

- Zero sensitive health/meal content intentionally sent to analytics.
- Zero production secrets in the mobile bundle.
- Export and deletion tests pass before release.
- All store declarations match the implemented features.
- All accuracy-related claims have documented methodology and limitations.
- Zero unresolved critical/high security findings at public launch.

---

## 15. Go, revise, and kill gates

## Gate 1 — problem and price

**GO:** five or more paid commitments and repeated diary evidence.  
**REVISE:** pain exists but users prefer a recipe utility or coach tool rather than a tracker.  
**KILL:** insufficient repeated pain or willingness to pay.

## Gate 2 — functional proof

**GO:** logging speed, dish recall, repeated use, and unit-cost targets are met.  
**REVISE:** classification is useful but the confirmation flow is too slow; narrow the dish set or focus on household recipes.  
**KILL:** users still prefer manual tracking or AI cost/quality cannot support pricing.

## Gate 3 — closed beta

Public marketplace launch requires all of the following:

- 50+ qualified beta users.
- 25+ paid users or equivalent paid-pilot commitments.
- D30 retention of at least 20% for eligible cohorts.
- Direct variable cost below 30% of net revenue with an identified path below 20%.
- No unresolved critical privacy, safety, store-policy, or nutrition-data issue.
- At least 60% of surveyed retained users would be “very disappointed” or strongly resistant if the product disappeared, or equivalent strong qualitative evidence.

## Gate 4 — separate product repository and growth budget

After Gate 2 approval, create the dedicated private product repository. After Gate 3, approve public launch and a limited acquisition budget. Do not scale ads until retention and contribution-margin LTV support the observed CAC.

---

## 16. Go-to-market plan

## 16.1 Initial acquisition channels

- South Asian fitness and meal-prep creators.
- Indian diaspora fitness communities.
- Local gyms and independent coaches.
- Recipe creators who can contribute validated household recipes.
- LinkedIn/Instagram/TikTok educational content demonstrating why photo-only estimates are uncertain.
- Search content for specific dishes, emphasizing recipe variability rather than claiming one universal calorie number.
- Referral loop around shared household recipes.

## 16.2 Launch message

Avoid “AI can perfectly scan your meal.”

Use:

> “Finally, a nutrition tracker that understands your meal may be homemade, regional, and different from everyone else’s—and asks before it guesses.”

## 16.3 Beta cohort strategy

Recruit users with different needs:

- Vegetarian and non-vegetarian.
- Weight loss, maintenance, muscle/protein goals.
- North and South Indian food patterns.
- Home-cooked and mixed restaurant/home meals.
- Android and iOS.
- New trackers and experienced macro trackers.

---

## 17. Major risks and mitigation

| Risk | Likely impact | Mitigation |
|---|---|---|
| Food photo cannot reveal hidden ingredients | Incorrect estimates and loss of trust | Confirmation questions, ranges, household recipes, source disclosure |
| South Asian cuisine is too broad | Data-quality backlog grows endlessly | Launch with 100–150 high-frequency dishes plus user recipe builder |
| AI inference is too expensive | Poor gross margin | Model routing, caching, scan allowances, image compression, reuse corrections |
| Users stop logging after novelty | Weak retention | Recent meals, recipe memory, weekly insights, low-friction logging, habit goals |
| Product appears medically authoritative | Store/regulatory risk | General-wellness boundary, careful claims, methodology, legal review |
| Sensitive health data leaks through vendors/logs | Enforcement and trust damage | Data minimization, redaction, vendor review, threat model, incident plan |
| Large incumbent adds regional foods | Feature differentiation shrinks | Household correction memory, confidence/provenance, culture-specific ontology, community data-quality loop |
| Product scope becomes a super-app | Cost and timeline expansion | Nutrition-first roadmap; defer workouts, social, clinicians, and disease programs |
| Eating behavior becomes harmful | User safety and reputational risk | Neutral UX, no extreme targets, 18+ launch, safety review and support protocol |
| App-store declaration mismatch | Release rejection | Maintain one feature inventory mapped to store description, privacy policy, and declarations |

---

## 18. First 30-day execution plan

### Days 1–5

- Finalize target user screener.
- Identify 15–20 competitors.
- Collect first 500 reviews/support complaints.
- Create interview guide and meal-diary protocol.
- Draft landing-page value propositions.

### Days 6–10

- Run first ten interviews.
- Recruit diary participants.
- Build clickable photo-confirmation prototype.
- Define candidate price cells.

### Days 11–17

- Run seven-day meal diary.
- Manually produce confirmed nutrition results for sample meals.
- Record time, corrections, ambiguity, and trust scores.
- Continue remaining interviews.

### Days 18–23

- Test prototype against participants’ current tracker.
- Launch waitlist/reservation page.
- Ask for deposit, paid pilot, or founding membership—not only an opinion.

### Days 24–27

- Analyze pain clusters, meal types, logging time, correction rate, and pricing behavior.
- Produce Gate 1 scorecard.

### Days 28–30

- Make GO/REVISE/KILL decision.
- If GO, approve the Phase 1 budget and create the dedicated product repository.
- If REVISE, narrow to the strongest job—photo confirmation, household recipes, or coach compliance.
- If KILL, preserve findings and move capital to another category.

---

## 19. Immediate decisions and defaults

Unless research contradicts them, use these defaults:

| Decision | Default |
|---|---|
| Launch geography | United States |
| Language | English |
| Minimum age | 18 |
| Core niche | South Asian homemade meals |
| Core platform | iOS + Android React Native |
| Web role | Landing, support, administration; no full consumer web app initially |
| Primary monetization | Subscription |
| Medical scope | None; general wellness only |
| Photo philosophy | Confirmation and ranges, not false precision |
| Fitness scope | Steps/activity adherence, not full workout programming |
| Product-repo creation | After Gate 2 approval |
| Founder-funded cash ceiling before beta proof | $45,000 |

---

## 20. Authoritative source register

Re-verify every policy and price before execution.

- RevenueCat, State of Subscription Apps 2026: https://www.revenuecat.com/state-of-subscription-apps
- RevenueCat pricing: https://www.revenuecat.com/pricing
- USDA FoodData Central API Guide: https://fdc.nal.usda.gov/api-guide/
- FDA, General Wellness: Policy for Low Risk Devices, January 2026: https://www.fda.gov/regulatory-information/search-fda-guidance-documents/general-wellness-policy-low-risk-devices
- FTC Health Breach Notification Rule basics: https://www.ftc.gov/business-guidance/resources/health-breach-notification-rule-basics-business
- Apple App Review Guidelines: https://developer.apple.com/app-store/review/guidelines/
- Apple Developer Program: https://developer.apple.com/programs/
- Apple App Store Small Business Program: https://developer.apple.com/app-store/small-business-program/
- Google Play Health apps declaration: https://support.google.com/googleplay/android-developer/answer/14738291
- Google Play testing requirements: https://support.google.com/googleplay/android-developer/answer/14151465
- OpenAI API model documentation and pricing: https://developers.openai.com/api/docs/models

---

## 21. Final recommendation

Proceed with **Phase 0 validation**, not full development.

Project Aahar is a credible app concept because it addresses a frequent task, a clearly identifiable population, and a trust problem that generic photo-based calorie estimates do not fully solve. Its defensible product layer would be the combination of South Asian food structure, household recipe memory, transparent uncertainty, user corrections, and deterministic calculations.

The concept should receive a dedicated application repository and commercial-MVP budget only after users demonstrate repeated use and real payment behavior. The purpose of this plan is to make the path to a marketplace product concrete while ensuring that weak evidence stops the investment early.