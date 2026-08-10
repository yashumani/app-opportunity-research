# My Seventh Meal — Complete Development and Launch Plan

**Plan date:** August 10, 2026  
**Status:** Active delivery plan  
**Brand status:** `My Seventh Meal` remains provisional until final store, domain, and trademark clearance  
**Product type:** General-wellness nutrition, activity, and progress application  
**Platforms:** iPhone, Android, and a supporting web experience  
**Source repository:** A dedicated private product repository named `my-seventh-meal-app`  
**Research repository:** `yashumani/app-opportunity-research`

> **Product promise:** Photograph a meal, confirm what the camera cannot see, and track calories and macros with more confidence.

> **Product principle:** AI proposes. The user confirms. A deterministic nutrition engine calculates. The product remembers.

---

## 1. Executive plan

The first working application foundation already exists. It includes onboarding, camera or gallery entry, mock meal analysis, review and clarification, transparent nutrition ranges, local saving, the Today screen, Recipes, Progress, Profile, manual entry, and light/dark appearance.

The next job is not to add every possible health feature. The next job is to replace the mock parts with a trustworthy, private, measurable meal-analysis system and prove that the core experience works for real people.

The recommended delivery path is:

1. Put the existing starter in its own private product repository.
2. Run it on real iPhones and Android phones and fix the basic experience.
3. Build a private image-analysis service and compare three recognition approaches.
4. Connect structured food data and a deterministic nutrition calculator.
5. Add household recipes, repeated-meal memory, manual search, and packaged-food scanning.
6. Add accounts, privacy controls, export, deletion, subscriptions, and activity connections.
7. Test with a small alpha group, then a larger beta group.
8. Submit only after the app meets explicit trust, speed, cost, privacy, and retention gates.

### Planning window

A realistic founder-assisted plan is **approximately 24 weeks from repository setup to a launch candidate**. A single engineer working part-time will likely need longer. A focused two-person product/engineering team can shorten the schedule, but the quality gates should not be skipped.

### Expected remaining cash range

- **Founder-assisted commercial launch:** approximately **$20,000–$55,000**, including contingency.
- **Professional small team:** approximately **$60,000–$140,000**.

The lower range assumes the founder owns product decisions, analytics, data definitions, acceptance testing, research, and a meaningful portion of implementation or coordination.

---

## 2. Definition of the first successful release

The first public release is successful when a user can:

1. Open the app without being forced to create an account immediately.
2. Photograph a meal, choose a photo, scan a packaged product, or enter food manually.
3. Review likely foods and correct anything wrong.
4. Answer no more than a few useful questions.
5. Receive a clearly labeled calorie and macro estimate or range.
6. Understand why the result is uncertain.
7. Save the meal in under 45 seconds for the normal photo flow.
8. Save a regular meal or household recipe for faster future logging.
9. See daily and weekly nutrition progress without shaming language.
10. Control photo retention, export data, and delete the account and associated data.

The application must remain useful when:

- Camera permission is denied.
- Photo recognition fails.
- The user has a small phone.
- The user uses larger accessibility text.
- The connection is slow or temporarily unavailable.
- A meal contains several components or hidden ingredients.
- The user does not know an exact portion.

---

## 3. Release scope

## 3.1 Must-have features for version 1.0

### Getting started

- Guest experience before account creation.
- Goal selection: understand meals, manage weight, increase protein, build consistency, or support fitness.
- Dietary preference and measurement-unit setup.
- Plain-language explanation of estimates and limitations.

### Meal logging

- Take a photo.
- Choose a photo.
- Manual food search and entry.
- Packaged-food barcode lookup.
- Recent meals and one-tap repeat.
- Favorites.
- Editable meal items, portions, preparation, and ingredients.
- “I’m not sure” option for every clarification question.

### Photo meal estimate

- One to three likely food or dish suggestions.
- Confidence or uncertainty information.
- Question ranking that asks only what materially changes the estimate.
- Structured calculation of calories, protein, carbohydrates, fat, and fiber.
- Transparent range when uncertainty remains.
- Explanation of the main source of uncertainty.
- Manual fallback and full correction.

### Recipe and memory

- Create a household recipe from ingredients and yield.
- Save a corrected meal as a regular meal.
- Save normal serving sizes.
- Reuse leftovers.
- Version a recipe when it changes.
- Suggest a previously saved recipe when a similar meal is detected.

### Daily and weekly experience

- Today view with estimated totals and targets.
- Protein and fiber progress.
- Recent meals.
- Weekly logging consistency.
- Weight trend.
- Step and activity summary when connected.
- Neutral, practical weekly observation.

### Accounts and trust

- Continue with Apple, Google, or email.
- Restore purchases.
- Export meals, recipes, goals, and progress.
- Delete account and associated data in the app.
- Public web page for deletion requests.
- Photo-retention choice.
- Methodology and limitations page.
- Report incorrect nutrition.
- Support contact.

### Commercial features

- Free tier with manual logging and a limited photo allowance.
- Paid plan with a larger photo allowance, recipe memory, weekly insights, and activity connection.
- Transparent paywall after the user experiences the product value.
- RevenueCat entitlement management.

### Supporting web experience

- Landing page.
- Pricing page.
- Privacy policy.
- Terms.
- Methodology and limitations.
- Support and contact.
- Account deletion request page.
- Internal review console for food mappings and reported errors.

## 3.2 Version 1.1 candidates

- Voice meal logging.
- Family recipe sharing.
- Better restaurant-meal support.
- Expanded micronutrients where source quality is sufficient.
- More detailed activity trends.
- Meal reminders personalized by behavior.
- Improved offline queueing.

## 3.3 Explicitly out of scope for the first release

- Disease diagnosis or treatment.
- Medication advice.
- Diabetes, kidney disease, pregnancy, eating-disorder, or other condition-management programs.
- Users under 18.
- Live clinician or dietitian marketplace.
- Public social feed.
- Competitive leaderboards.
- Full workout-program library.
- Automatic grocery ordering.
- Unlimited photo analysis.
- Medical-grade accuracy claims.
- Standalone Apple Watch or Wear OS application.

---

# 4. Twenty-four-week delivery roadmap

Week numbers begin when the dedicated product repository is created and the starter code is pushed.

## Phase 0 — Product repository and working baseline

**Target:** Week 1  
**Goal:** Turn the starter package into a normal, testable product codebase.

### Work

- Create the private repository `my-seventh-meal-app`.
- Push the existing Expo/React Native starter.
- Protect the default branch and require review before merging.
- Add a simple branch and pull-request workflow.
- Install dependencies and run project verification and TypeScript checks.
- Create development, test, and production environment templates.
- Run the app on:
  - one recent iPhone,
  - one compact iPhone,
  - one recent Android phone,
  - one lower-cost or smaller Android device,
  - web browser.
- Record screenshots and the first device-specific defects.
- Confirm the app identifiers, owner account, and signing approach.

### Exit gate

- The starter launches successfully on iOS, Android, and web.
- The full mock journey can be completed without a blocker.
- No secret keys are committed.
- Automated checks run on every pull request.
- The product repository, not the research repository, becomes the source of truth for code.

---

## Phase 1 — Experience foundation and device quality

**Target:** Weeks 2–3  
**Goal:** Make the current mock experience feel reliable before connecting real services.

### Work

- Refine the welcome, goal, capture, review, questions, result, and Today screens.
- Add clear loading, retry, no-result, offline, and permission-denied states.
- Make the camera optional and manual entry equally visible.
- Add safe-area, keyboard, and small-screen handling.
- Test larger accessibility text and screen-reader labels.
- Add basic event names for the user journey without sending meal or health content.
- Add local draft recovery so a user does not lose a meal when the app closes.
- Add plain-language methodology and privacy placeholders.
- Confirm that all health language is neutral and general-wellness focused.

### Exit gate

- The core journey works on the agreed device matrix.
- No important action depends only on color.
- Buttons and text remain usable with larger text.
- Every permission denial has a practical alternative.
- The mock photo-to-save journey is understandable without explanation from the team.

---

## Phase 2 — Private backend and image pipeline

**Target:** Weeks 3–5  
**Goal:** Create the safe path between the phone and meal-analysis providers.

### Work

- Create a small backend service and database.
- Add anonymous development sessions before full accounts.
- Compress images on the phone.
- Remove unnecessary image metadata.
- Use short-lived signed uploads to private storage.
- Keep provider keys on the server only.
- Add automatic raw-photo deletion after analysis by default.
- Add optional photo retention only after explicit user choice.
- Normalize provider responses into one internal meal-analysis format.
- Add request IDs, timing, provider, and cost metadata without logging the meal image or sensitive content.
- Add retry limits and graceful provider failure.

### Exit gate

- A test image travels through the private pipeline without exposing service keys.
- The image follows the intended retention setting.
- The app still supports manual entry if analysis fails.
- Sensitive content does not appear in normal analytics or error logs.
- The team can switch providers without rebuilding the screens.

---

## Phase 3 — Meal-analysis provider bake-off

**Target:** Weeks 4–7  
**Goal:** Select the best analysis approach using evidence rather than marketing claims.

### Approaches to compare

1. Passio Nutrition-AI.
2. LogMeal.
3. A general vision model followed by our own food and recipe matching.

A hybrid approach may win—for example, a specialist provider for packaged foods and simple dishes, with our own confirmation and recipe system for mixed home-cooked meals.

### Validation set

Start with **60 carefully documented meals**, then expand to at least **200 meals before public beta**.

The set should include:

- Single foods.
- Multi-item plates.
- Mixed dishes.
- Soups and sauces.
- Breakfasts.
- Restaurant meals.
- Packaged foods.
- Repeated household meals.
- Vegetarian and non-vegetarian meals.
- Low-light and imperfect photos.
- Several phone-camera models.

For the strongest accuracy reference, record known ingredients, recipe yield, and weighed portions for a subset.

### Measures

- Correct item or component in the top three suggestions.
- Number of edits required.
- Number of clarification questions.
- Time from photo to review result.
- Time from photo to saved meal.
- Provider failure rate.
- Performance on mixed meals.
- Cost per meal.
- Privacy and retention terms.
- Ease of correcting ingredients and quantities.
- User trust after seeing the result.

### Provider-selection gate

- At least 80% of validation meals have the correct main item or components in the top three.
- Median two or fewer useful clarification questions.
- Median photo-to-saved-meal time of 45 seconds or less during a guided usability test.
- Every result remains editable.
- Clear path to an average AI/photo cost below $4 per ordinary active paid user per month.
- No unacceptable image-retention, privacy, or contractual condition.

If no approach passes, do not disguise the failure. Narrow the supported meal types, improve the confirmation flow, or delay the photo feature while manual and recipe logging continue.

---

## Phase 4 — Structured nutrition engine

**Target:** Weeks 6–9  
**Goal:** Stop relying on mock nutrition values and create reproducible calculations.

### Work

- Connect USDA FoodData Central through the backend.
- Create canonical food, serving, ingredient, recipe, and nutrient records.
- Store source and version for every calculation.
- Build unit conversion for grams, ounces, cups, tablespoons, teaspoons, pieces, and servings.
- Create recipe yield and per-serving calculations.
- Support an uncertainty range for estimated portions.
- Map confirmed analysis results to structured food records.
- Add curated recipe templates for common mixed meals.
- Add a food-quality flag when data is incomplete or unreliable.
- Add nutrition regression tests.
- Add an internal review tool for incorrect mappings and reports.

### Exit gate

- Calories and macros are produced by structured data and code, not invented by a language model.
- Every saved result has a calculation version and traceable source.
- Common unit conversions are tested.
- Recipe totals and per-serving values reproduce expected results.
- Low-quality or missing data is clearly identified rather than silently displayed as precise.

---

## Phase 5 — Complete meal-logging system

**Target:** Weeks 8–12  
**Goal:** Make the app useful beyond the first photo demonstration.

### Work

- Manual food search.
- Packaged-food barcode scanning.
- Recent foods.
- Favorites.
- One-tap repeat.
- Household recipe builder.
- Recipe yield and serving editing.
- Save a corrected photo meal as a regular meal.
- Leftover logging.
- Meal time and meal label.
- Edit and delete logged meals.
- Offline-friendly access to recent meals and recipes.
- Sync queue for temporary connection loss.
- “Report incorrect nutrition” flow.

### Exit gate

- A user can log meals without a photo.
- Repeated meals are materially faster than the first log.
- The recipe builder is understandable without nutrition expertise.
- Failed scans never trap the user.
- Saved history remains consistent after restart and sync.

---

## Phase 6 — Today, Recipes, Progress, and activity

**Target:** Weeks 10–14  
**Goal:** Turn meal logging into a useful weekly habit.

### Work

- Today totals and ranges.
- Protein and fiber progress.
- Meal history.
- Frequent meals and household recipes.
- Weekly consistency.
- Weight tracking and trend.
- Step and workout-minute connection through Apple Health and Android Health Connect.
- Clear permission explanation and opt-in.
- No heart-rate interpretation or medical recommendation.
- One or two neutral weekly observations.
- Reminder controls.
- Accessible chart summaries in text.

### Exit gate

- The dashboard remains useful when activity is not connected.
- Users can understand a weekly summary without reading a chart.
- Health permissions are requested only when the user initiates the connection.
- Meal or health data is not used for advertising.
- The app never presents activity or weight trends as a diagnosis.

---

## Phase 7 — Accounts, privacy, deletion, and subscriptions

**Target:** Weeks 13–16  
**Goal:** Make the product commercially and operationally ready.

### Work

- Guest mode.
- Email account creation.
- Sign in with Apple.
- Google sign-in.
- Account linking and recovery.
- Consent and privacy records.
- In-app account deletion.
- Public web account-deletion request page.
- Data export.
- Revocation of connected health permissions.
- Subscription products and entitlements.
- Restore purchases.
- Free usage allowance and clear limit messaging.
- Paywall shown after value is demonstrated.
- No misleading countdown, hidden price, or difficult cancellation language.
- Privacy policy, terms, methodology, and support pages.

### Pricing test

Start with a simple hypothesis rather than many tiers:

- **Free:** manual logging, basic progress, and a limited number of photo estimates.
- **Pro monthly:** approximately $14.99.
- **Pro annual:** approximately $119.99.

These are testing prices, not permanent decisions.

### Exit gate

- Account deletion removes the account and associated data, subject only to clearly disclosed legitimate retention.
- A deletion request also works from the public website.
- Export produces a useful, readable file.
- Subscription status and restore-purchase behavior are correct on iOS and Android.
- The paywall clearly states price, billing period, renewal, and cancellation.
- Privacy disclosures match actual behavior and every third-party service.

---

## Phase 8 — Private alpha

**Target:** Weeks 16–19  
**Goal:** Prove the core experience with real users before store-scale testing.

### Cohort

- 20–30 adults.
- Mix of iPhone and Android users.
- Mix of simple, mixed, home-cooked, packaged, and restaurant meals.
- At least four weeks for the earliest users when possible.

### Research activities

- First-use observation.
- Seven-day meal-logging diary.
- Weekly interview or survey.
- Review of all analysis corrections.
- Review of support requests and confusion.
- Review of cost by user and meal type.
- Accessibility testing with larger text and at least one screen-reader user if possible.

### Alpha targets

- 60% or more of qualified testers save a first meal.
- 35% or more log at least three meals in the first 24 hours.
- Median photo-to-save time is 45 seconds or less.
- Median clarification questions are two or fewer.
- Fewer than 5% of photo attempts end without a usable path forward.
- At least 25% of activated testers are still logging during week two.
- No critical privacy or data-loss issue.

These are internal decision thresholds, not market forecasts.

---

## Phase 9 — Store beta

**Target:** Weeks 19–22  
**Goal:** Test real signed builds, store installation, subscriptions, and broader device coverage.

### Cohort

- 75–100 beta users.
- TestFlight for iOS.
- Google Play closed testing for Android.
- Include at least the required tester duration and count when the Google developer account is subject to the new-personal-account rule.

### Work

- Store-signed builds.
- Subscription sandbox and production configuration.
- Push notification testing.
- Deep-link testing.
- Upgrade and reinstall testing.
- Account deletion and export testing.
- Privacy-label and Data Safety reconciliation.
- Health-app declaration review.
- Device and OS coverage.
- Performance, crash, and slow-network testing.
- Customer-support process.

### Beta targets

- 99.5% or better crash-free users.
- No repeatable data-loss issue.
- All account, purchase, restore, export, and deletion paths pass.
- Average technical cost is within the approved model.
- At least 25 paying beta users or equivalent paid commitments.
- No critical security, privacy, nutrition-data, or store-policy finding.
- Clear evidence that a meaningful segment returns because repeated meals become easier.

---

## Phase 10 — Launch candidate and marketplace submission

**Target:** Weeks 23–24  
**Goal:** Submit a release that can be supported responsibly.

### App Store and Play Store package

- Final name and icon.
- Screenshots for compact and large phones.
- App description that accurately matches the health declaration.
- Privacy policy.
- Terms.
- Support URL and contact information.
- Account deletion URL.
- Nutrition methodology and limitations.
- Review account or demo mode for app reviewers.
- Subscription descriptions.
- Data Safety form.
- Apple privacy details.
- Google Health apps declaration.
- Age rating.
- Release notes.
- App-review notes explaining photo analysis, ranges, and general-wellness boundary.

### Final launch gate

Do not submit or release publicly until:

- Core provider gate passes.
- Nutrition calculations are deterministic and versioned.
- Median photo-to-saved-meal time is 45 seconds or less.
- Manual fallback works.
- Account deletion works in the app and on the web.
- Privacy and store declarations match reality.
- No medical-grade or disease-treatment claim appears in the product or marketing.
- No critical security issue remains.
- Support ownership and incident response are defined.
- Operating cost can be supported by the intended pricing.

---

# 5. The first 30 days

This is the immediate sequence after the private product repository exists.

## Week 1

1. Push the starter package.
2. Install dependencies and run all checks.
3. Launch on iPhone, Android, and web.
4. Record the first device defects.
5. Create development and test environments.
6. Confirm the provisional app identifiers.
7. Add pull-request checks and branch protection.
8. Establish the defect and decision log.

## Week 2

1. Fix the current core journey on compact and large screens.
2. Add loading, offline, permission-denied, retry, and no-result experiences.
3. Add draft recovery.
4. Define the internal `MealAnalysis` response format.
5. Define photo retention and deletion behavior.
6. Create the 60-meal provider-evaluation set and data-capture template.

## Week 3

1. Create the backend skeleton.
2. Add anonymous development sessions.
3. Add private signed image upload.
4. Strip unnecessary image metadata.
5. Add provider adapter placeholders.
6. Add latency and cost tracking that excludes sensitive meal content.

## Week 4

1. Connect Passio in the test environment.
2. Connect LogMeal in the test environment.
3. Connect a general-vision proof in the test environment.
4. Run the first 20-meal comparison.
5. Review failure patterns with the product and nutrition reviewer.
6. Adjust the clarification-question approach before the full 60-meal test.

### First-month deliverable

A working private development build that analyzes a real image through at least two providers, normalizes the result, displays an editable review, records performance and cost, and safely falls back to manual entry.

---

# 6. User-experience work plan

The user experience will be developed in this order:

1. Welcome and product explanation.
2. Goal selection.
3. Capture choice.
4. Camera and photo picker.
5. Processing and waiting state.
6. Recognition review.
7. Clarification questions.
8. Result and uncertainty explanation.
9. Save and regular-meal memory.
10. Today.
11. Manual search and barcode.
12. Recipe builder.
13. Weekly progress.
14. Profile, privacy, export, and deletion.
15. Subscription and upgrade.

For every screen, review:

- What is the one main action?
- What can go wrong?
- What happens without permission?
- What happens without connectivity?
- What happens on a small phone?
- What happens with larger text?
- What does a first-time user misunderstand?
- Is the wording supportive and honest?

### Product-language rules

Use:

- Estimated range.
- Help us refine this meal.
- Main uncertainty.
- Use your usual recipe.
- I’m not sure.
- You are building consistency.

Avoid:

- Exact, guaranteed, perfect, or medically accurate.
- Good food, bad food, cheating, clean, guilty, or failed.
- Fear-based weight messaging.
- Artificial urgency in subscriptions.

---

# 7. Data, AI, and nutrition rules

1. A vision model may suggest foods, components, preparation cues, and useful questions.
2. A model does not directly become the final source of calories or macros.
3. Confirmed foods map to structured food or recipe records.
4. Nutrition math is code-based, reproducible, tested, and versioned.
5. A range is used when portion or recipe uncertainty remains.
6. The source and primary uncertainty are available to the user.
7. A correction can improve the user’s future experience.
8. A provider-specific response never leaks directly into the interface.
9. Third-party keys never live inside the mobile application.
10. The team keeps a fixed validation set so provider upgrades can be compared safely.

---

# 8. Privacy and safety plan

### Default privacy position

- No advertising business model using meal, weight, activity, or health data.
- Raw meal photos deleted after analysis by default.
- User can opt in to retain photos.
- No meal names, photos, weight, or health details in ordinary analytics events.
- No sensitive content in crash reports.
- Encryption in transit and at rest.
- Private storage with short-lived access.
- Minimal permissions.
- Guest use before account creation when practical.
- Easy consent withdrawal and health-connection removal.
- Data export and complete account deletion.

### Required reviews before beta

- Data inventory.
- Data-flow diagram.
- Vendor list and retention terms.
- Threat model.
- Privacy-policy review.
- Account deletion test.
- Incident-response plan.
- Health and general-wellness claim review.
- Marketplace declaration review.

### Safety boundary

The application provides general-wellness tracking. It does not diagnose, treat, prevent, or manage disease. It does not recommend medication changes or claim medical-grade nutrition accuracy from a photograph.

---

# 9. Device and accessibility plan

### Minimum practical device matrix

- Compact iPhone.
- Current standard iPhone.
- Large iPhone.
- Current Google Pixel or similar Android flagship.
- Current Samsung Galaxy.
- Mid-range or lower-cost Android phone.
- Small Android screen.
- Chrome, Safari, and Edge web views for supporting surfaces.

### Required conditions

- Light and dark appearance.
- Default and large text.
- Screen reader.
- Reduced motion.
- Slow connection.
- Temporary offline state.
- Camera denied.
- Photo library denied.
- Health permission denied.
- Subscription restoration.
- Fresh install and upgrade from previous build.

### Accessibility acceptance

- Controls have readable labels.
- Important information is not color-only.
- Touch targets are comfortable.
- Charts have text summaries.
- Larger text does not hide actions or overlap content.
- Focus order is logical.
- Motion can be reduced.

---

# 10. Quality and testing plan

### Automated checks

- Type checking.
- Formatting and linting.
- Unit tests for calculations and conversions.
- Tests for provider-response normalization.
- Tests for recipe yield and serving calculations.
- Tests for entitlement logic.
- Tests for deletion and export requests.
- Build checks for Android, iOS, and web.

### Human testing

- Usability sessions.
- Real-device testing.
- Meal-analysis review.
- Accessibility review.
- Subscription and restore-purchase testing.
- Account recovery and deletion testing.
- Slow-network and failed-provider testing.
- Privacy and security review.

### Defect priorities

- **P0:** privacy breach, data loss, account exposure, wrong purchase entitlement, app cannot launch, dangerous health claim.
- **P1:** core meal flow blocked, incorrect saved result, deletion failure, frequent crash, no usable fallback.
- **P2:** confusing screen, moderate visual issue, minor performance problem.
- **P3:** cosmetic improvement or low-impact enhancement.

No P0 or unresolved high-risk P1 issue may remain at public release.

---

# 11. Product and business measurements

### Core journey

- Install to first saved meal.
- Time to first saved meal.
- Photo attempt to usable review.
- Review to saved meal.
- Number of clarification questions.
- Number of edits.
- Manual fallback usage.
- Analysis failure rate.

### Habit and value

- Three meals logged in the first 24 hours.
- Days logged in week one.
- Repeated-meal use.
- Recipe saves.
- Weekly review opens.
- D7 and D30 retention.
- Users who say they would be disappointed to lose the product.

### Commercial

- Paywall views after value experience.
- Trial or free-to-paid conversion.
- Monthly versus annual choice.
- Refunds.
- Restore-purchase success.
- Revenue per active user.
- Contribution after provider and store costs.

### Quality and cost

- Crash-free users.
- Slow requests.
- Provider latency.
- Cost per analysis.
- Cost per active user.
- 90th-percentile heavy-user cost.
- Correction clusters by meal type.
- Support contacts per 100 active users.

Analytics events must use anonymous identifiers and categorical metadata rather than raw food, photo, weight, or health content.

---

# 12. Team plan

A lean team can begin with:

| Role | Responsibility |
|---|---|
| Founder / product owner | Product decisions, target customer, prioritization, pricing, acceptance, customer research |
| Product and UX lead | Flows, screens, content, accessibility, usability, design system |
| Lead mobile/full-stack engineer | Mobile app, backend coordination, releases, technical quality |
| Part-time backend/integration support | Image pipeline, provider adapters, nutrition services, storage |
| Nutrition-data reviewer | Food mappings, recipes, calculation test cases, methodology wording |
| Part-time QA/accessibility reviewer | Device matrix, regression, accessibility, store readiness |
| Privacy/security reviewer | Data flow, deletion, vendors, threat review, incident preparation |
| Beta coordinator/support | Tester recruitment, feedback, support, issue triage |

One experienced person may cover more than one engineering role. Nutrition and privacy work should still receive independent review before public launch.

---

# 13. Budget by stage

These are planning ranges, not vendor quotations.

| Stage | Founder-assisted cash range |
|---|---:|
| Repository, device baseline, design refinement | $0–$3,000 |
| Backend, image pipeline, provider comparison | $2,000–$8,000 |
| Nutrition engine, search, barcode, recipes | $5,000–$14,000 |
| Accounts, privacy, subscriptions, activity | $5,000–$12,000 |
| Alpha, beta, release preparation | $3,000–$8,000 |
| Legal, privacy, security, or specialist review | $1,000–$5,000+ |
| **Subtotal** | **$16,000–$50,000+** |
| Recommended contingency | **15–25%** |
| **Planning ceiling** | **approximately $20,000–$55,000** |

### Early monthly run-rate

- Backend, storage, and monitoring: approximately $100–$500 during beta.
- Analysis providers: usage dependent; target average below $4 per ordinary paid active user per month.
- Support and maintenance: depends on founder involvement.
- RevenueCat: free through its current tracked-revenue threshold, then percentage-based.
- Store commissions and taxes: modeled separately in pricing and cash-flow planning.

### Capital rule

Do not authorize the full commercial budget merely because the prototype looks good. Release the budget at the gates in this plan.

---

# 14. Decision gates

## Gate A — Working baseline

Pass when the starter runs across the device matrix and the mock journey is reliable.

## Gate B — Analysis approach

Pass when the provider or hybrid approach meets recognition, question, speed, privacy, and cost requirements.

## Gate C — Real nutrition system

Pass when calculations are structured, reproducible, versioned, and tested.

## Gate D — Private alpha

Pass when real users can repeatedly log meals, trust the explanation, and continue into week two without critical issues.

## Gate E — Paid beta

Pass when signed builds, subscriptions, deletion, export, privacy, and store declarations work; costs are acceptable; and real users pay or commit.

## Gate F — Public release

Pass only when the release checklist is complete and the team can support incidents, reviews, refunds, and user questions.

Every gate produces one decision:

- **GO:** continue as planned.
- **REVISE:** narrow or change the workflow and repeat the gate.
- **KILL:** stop meaningful investment because the value, trust, cost, or distribution case does not work.

---

# 15. Marketplace and policy checklist

### Apple

- Privacy policy in App Store Connect and inside the app.
- Clear purpose strings for camera, photos, notifications, and health access.
- In-app account deletion when accounts exist.
- Equivalent privacy-preserving login option when third-party login is used.
- Health data not used for advertising or unrelated data mining.
- Methodology and limitations for health-related accuracy claims.
- In-app purchase for digital subscription functionality.
- Review notes and a test account or demo path.

### Google Play

- Privacy policy.
- Data Safety form for testing and production tracks.
- Accurate Health apps declaration.
- In-app account deletion and a public web deletion resource when accounts exist.
- Closed testing and production-access requirements where applicable to the developer account.
- Store description consistent with the declared health functionality.
- Correct permissions and Health Connect declarations.
- Subscription and billing-policy compliance.

Policy details change. Recheck all requirements in the final release month.

---

# 16. First 90 days after launch

## Days 1–14

- Watch crashes, analysis failures, deletion, purchase, and support issues daily.
- Respond to reviews and support.
- Pause campaigns if reliability or costs are unstable.
- Fix trust-breaking problems before adding features.

## Days 15–30

- Review activation, first-day logging, D7 retention, and provider cost.
- Improve the largest confusion and correction clusters.
- Run one paywall or onboarding test at a time.
- Publish methodology and known-limit improvements.

## Days 31–60

- Improve repeated-meal and recipe memory.
- Expand the validation dataset.
- Add only the highest-demand version 1.1 feature.
- Begin structured referral or creator testing only when retention is acceptable.

## Days 61–90

- Decide whether to expand cuisine coverage, voice logging, family recipes, or coach support.
- Reforecast unit economics.
- Review trademark and brand decision if still provisional.
- Make a formal **scale, focus, reposition, or stop** decision.

---

# 17. Immediate owner actions

The next concrete actions are:

1. Create the private GitHub repository `my-seventh-meal-app`.
2. Add the GitHub app/connector to that repository.
3. Push the completed starter package.
4. Run it on at least one iPhone and one Android phone.
5. Create the 60-meal provider-comparison set.
6. Open development accounts for Expo, the backend host, USDA FoodData Central, Passio, and LogMeal.
7. Approve the default photo-retention rule: delete after analysis unless the user chooses to save.
8. Begin Phase 1 device and experience fixes.
9. Begin Phase 2 private backend and signed-upload work.
10. Hold the first Gate A review before provider integration expands.

---

## Current authoritative references

- Expo project and Router documentation: https://docs.expo.dev/get-started/create-a-project/ and https://docs.expo.dev/router/introduction/
- Expo build and submission: https://docs.expo.dev/deploy/build-project/ and https://docs.expo.dev/submit/introduction/
- USDA FoodData Central API: https://fdc.nal.usda.gov/api-guide/
- Passio Nutrition-AI platform: https://www.passio.ai/platform
- LogMeal quantity estimation and ingredient editing: https://logmeal.com/api/quantity-estimation/ and https://docs.logmeal.com/docs/guides-features-ingredients-edition
- Apple App Review Guidelines: https://developer.apple.com/app-store/review/guidelines/
- Apple account deletion: https://developer.apple.com/support/offering-account-deletion-in-your-app/
- Google Play Data Safety: https://support.google.com/googleplay/android-developer/answer/10787469
- Google Play account deletion: https://support.google.com/googleplay/android-developer/answer/13327111
- Google Play Health apps declaration: https://support.google.com/googleplay/android-developer/answer/14738291
- RevenueCat pricing: https://www.revenuecat.com/pricing

---

**Planning note:** The timeline and budget are management estimates. Provider prices, marketplace rules, and technical dependencies should be rechecked before each major gate.