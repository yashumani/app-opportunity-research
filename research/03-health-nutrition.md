# Domain 3 — Health / Nutrition

**Recommendation:** PRIORITY 3 — high upside, higher execution/compliance risk  
**Working concept:** Culturally accurate nutrition tracker for South Asian / Indian home-cooked meals  
**Initial wedge:** Fast food-photo logging plus ingredient/portion confirmation, transparent confidence ranges, family recipes, and correction learning.

## Why this domain is attractive

Health & Fitness currently has some of the strongest subscription economics in RevenueCat's 2026 dataset. The opportunity is not “another calorie scanner.” The wedge must solve a population-specific accuracy and workflow problem that generic databases/models handle poorly.

## Customer problem hypothesis

Target users:

- South Asian users tracking calories/macros.
- Families eating homemade mixed dishes.
- Users switching between Indian regional cuisines and Western meals.
- People frustrated by vague database entries such as “curry,” “dal,” or “rice plate.”

## Proposed product

- Food-photo capture.
- AI identifies likely dishes/components.
- Confirmation flow for uncertain ingredients and portions.
- Portion-size selector and optional weight input.
- Nutrition confidence interval rather than false precision.
- Regional food database.
- Family recipe builder.
- Saved meal templates and leftovers.
- Correction memory.
- Calorie/macronutrient goals and trends.
- Barcode/manual packaged-food search.

## Data strategy

Use a layered food model:

1. USDA / trusted packaged-food nutrition data.
2. Curated South Asian dish templates.
3. Ingredient-based recipe calculator.
4. User-specific corrections and household recipes.
5. Confidence/source score.

## Compliance boundary

Keep first release in **general wellness**, not diagnosis or treatment. Treat food, weight, wellness, and connected-health information as sensitive. Reassess FDA/FTC/platform requirements before any medical-function expansion.

## Commercial MVP cost

| Workstream | Hours |
|---|---:|
| User/food research | 120-200 |
| UX/UI | 140-220 |
| Mobile/camera flows | 280-440 |
| Backend/auth/data | 220-340 |
| Nutrition DB/recipe engine | 220-380 |
| Vision/AI pipeline | 180-320 |
| Personalization/corrections | 100-180 |
| Goals/trends | 80-140 |
| Billing/notifications/analytics | 70-120 |
| Privacy/security/compliance review | 100-200 |
| QA/device testing/store release | 160-260 |
| **Total** | **1,670-2,800 hours** |

**Founder-assisted commercial MVP target: $20K-$45K.**  
**Professional team target: $60K-$140K.**

## AI unit economics

Planning allowance for photo-assisted analysis: **$0.02-$0.08 per meal analysis** during early design. At 90 photo-assisted meals/month, that is roughly **$1.80-$7.20/month** before storage/retries/other services. A safer planning range is **$3-$10/active paid user/month** initially.

This makes caching, meal reuse, lightweight recognition, and deterministic nutrient calculations critical.

## Pricing hypothesis

- Free: manual search + limited photo scans.
- Plus: $9.99-$14.99/month.
- Pro: $19.99-$24.99/month.
- Annual: test $79-$149/year depending usage.

## Validation

Recruit 20 South Asian users who currently track calories/macros, log seven days of meals, compare current workflow to a confirmation-based prototype, catalogue corrections/ambiguity, and test paid reservation at $9.99/$14.99/$19.99.

**Go signal:** repeated evidence that current tools require substantial correction and at least five users commit to paying.

## Domain score

**Weighted view: 7.2 / 10**

## Sources

- RevenueCat: https://www.revenuecat.com/state-of-subscription-apps
- USDA FoodData Central: https://fdc.nal.usda.gov/api-guide
- FDA General Wellness guidance: https://www.fda.gov/regulatory-information/search-fda-guidance-documents/general-wellness-policy-low-risk-devices
- FTC Health Breach Notification Rule: https://www.ftc.gov/legal-library/browse/rules/health-breach-notification-rule
- Apple App Review Guidelines: https://developer.apple.com/app-store/review/guidelines/
- Google Play health declaration: https://support.google.com/googleplay/android-developer/answer/14738291
