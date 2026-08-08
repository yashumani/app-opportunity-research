# Shared Cost Model — From Validation to Marketplace

**Research date:** 2026-08-08  
**Purpose:** Provide one comparable cost framework for all four app domains, including development, deployment, AI usage, marketplace fees, operating run-rate, and break-even thinking.

## 1. Key conclusion

The marketplace account fees are trivial. The meaningful cost drivers are:

1. Engineering hours and QA.
2. Media/AI inference, especially voice and video.
3. Customer acquisition.
4. Ongoing maintenance/support.
5. Privacy/security/compliance for sensitive domains.

The cheapest technically viable product is the **Vertical AI / Business** concept because it can keep calculations deterministic and use the LLM only for interpretation. The most expensive to operate at scale is **Creator / Video**, because generation cost rises nearly linearly with seconds generated and retries.

## 2. Comparable domain economics

| Domain | Validation | Founder-assisted commercial MVP | Professional commercial MVP | Early variable AI cost per active customer | Suggested early price | Risk-adjusted rank |
|---|---:|---:|---:|---:|---:|---:|
| Vertical AI / Business | $0-$2.5K | $15K-$35K | $40K-$100K | ~$2-$8/workspace/mo | $49-$199+/workspace/mo | 1 |
| Education / Coaching | $0-$2.5K | $15K-$35K | $40K-$95K | ~$2.25-$4/user/mo async voice | $14.99-$24.99/user/mo | 2 |
| Health / Nutrition | $0-$3K | $20K-$45K | $60K-$140K | ~$3-$10/heavy user/mo | $14.99-$24.99/user/mo | 3 |
| Creator / Photo / Video | $0-$3K | $30K-$75K | $85K-$180K | Highly usage dependent; video can exceed $10/user/mo | $49-$199+ B2B | 4 |

These are planning estimates based on current 2026 market rates and deliberately constrained MVP scopes. They are not vendor quotes.

## 3. Labor-rate assumptions

Current benchmarks:

- Clutch: many mobile app development companies list **$25-$49/hour**, most reviewed projects fall between **$10K-$49,999**, and the reported average reviewed project cost is around **$90.8K**.
- Upwork: mobile developer median hourly rates around **$18-$39/hour**, with experienced/specialized developers often pricing higher.

### Model bands

| Delivery model | Blended planning rate | What founder owns |
|---|---:|---|
| Founder-heavy + targeted freelancers | $20-$35/hr external work | Product, research, architecture, some implementation, QA |
| Offshore/nearshore small team | $25-$50/hr | Product owner + acceptance testing |
| Senior specialist team | $50-$100+/hr | Product direction |
| US agency | $100-$200+/hr possible | Mostly product oversight |

## 4. Marketplace fees and release requirements

### Apple

- Apple Developer Program: **$99/year**.
- Small developers may qualify for reduced App Store commission under Apple's Small Business Program; verify eligibility and current territorial rules before launch.

### Google Play

- Developer registration: commonly **$25 one-time**.
- New personal developer accounts created after November 13, 2023 must meet closed-testing requirements before production access: currently **at least 12 testers continuously opted in for 14 days**.

### Shared store-launch budget

| Item | Cost |
|---|---:|
| Apple account | $99/year |
| Google account | ~$25 one-time |
| Store screenshots/creative | $0 founder-made to $500-$2K outsourced |
| Privacy policy/terms | $0 template/self-draft to $1K-$5K+ legal review |
| QA/test devices | $0 if existing devices to $500-$2K |
| Localization | Optional; $100s-$1Ks |
| **Bare account fees** | **~$124 initially** |
| **Realistic release-prep allowance** | **$1K-$7K+ depending legal/design/QA** |

## 5. Baseline production software stack

| Service | Early planning cost |
|---|---:|
| Supabase Pro | ~$25/month starting tier |
| Expo EAS Starter | ~$19/month; Production ~$199/month if needed |
| RevenueCat | $0 through first $2,500 monthly tracked revenue, then 1% |
| Domain/email | ~$10-$50/month combined depending provider |
| Error monitoring | $0-$50/month initially |
| Product analytics | $0-$100/month initially |
| Object storage/CDN | Usually low initially; media apps scale faster |
| CI/CD | Often included/free at low usage |
| **Text-heavy app baseline** | **~$75-$400/month before AI/support** |

## 6. AI pricing strategy

Use model routing:

- Deterministic code for arithmetic, formulas, and lookups.
- Low-cost model for extraction/classification/simple summaries.
- Mid-tier model for complex reasoning.
- Premium model only when a high-value request justifies it.
- Cache stable context and repeated outputs.

Video must be usage-capped because generation is charged per second and retries compound cost.

## 7. Total cash by stage

### Stage A — research / validation

Typical spend:

- Landing page/domain: $50-$300.
- Prototype/design tools: $0-$300.
- Interview incentives: $200-$1,000.
- Review/data collection: $0-$500.
- Small ad/message tests: $200-$1,000.

**Budget ceiling: $2,500-$3,000.**

### Stage B — concierge proof

**Budget ceiling: $5K-$12K cumulative** for most concepts; creator/video can need slightly more.

### Stage C — commercial MVP

- Business: **$15K-$35K founder-assisted**.
- Education: **$15K-$35K**.
- Health: **$20K-$45K**.
- Creator: **$30K-$75K**.

Include a **15-25% contingency** for integration/review/rework risk.

### Stage D — full v1 / growth

Do not pre-budget this as mandatory. Typical cumulative product spend can reach $75K-$250K+ depending domain.

## 8. Founder-time economics

Track founder hours as an opportunity cost even if no cash changes hands.

Example: 400 founder hours × $75/hour internal opportunity value = **$30,000** implicit labor.

## 9. Revenue/store-fee examples

Assume 15% store commission purely for comparison.

| Monthly subscription | Net after 15% store fee | Subscribers needed for ~$10K net before other costs |
|---:|---:|---:|
| $9.99 | $8.49 | ~1,178 |
| $14.99 | $12.74 | ~785 |
| $19.99 | $16.99 | ~589 |
| $49 | $41.65 | ~241 |
| $79 | $67.15 | ~149 |
| $149 | $126.65 | ~79 |

This is why vertical B2B is strategically attractive: meaningful recurring revenue can be reached with hundreds rather than thousands of customers.

## 10. Gross-margin targets

Internal planning targets after API/storage/payment variable costs:

- Vertical business: **80%+** technical gross margin.
- Education async voice: **65-80%+**.
- Health photo analysis: **55-75% initially**.
- Video-heavy creator: use credits to protect **60%+** margin.

## 11. CAC/LTV rule

Do not scale ads until paid retention exists. Measure visitor → signup → activation → trial → paid → retention, then compare CAC to contribution-margin LTV rather than headline subscription price.

## 12. Go/no-go financial rules

1. **No more than $2.5K-$3K before problem validation.**
2. **No more than ~$10K-$12K cumulative before repeated usage or paid pilot evidence.**
3. **Do not spend $30K+ because users say they would pay; require actual payment/commitment.**
4. **Model the 90th-percentile user for AI/media cost.**
5. **Do not offer unlimited video or expensive realtime voice until observed usage proves unit economics.**
6. **Do not add a second major connector/workflow until the first retains users.**
7. **Kill or change an idea when acquisition + variable cost + churn cannot support pricing.**

## Sources

- Clutch: https://clutch.co/directory/mobile-application-developers/pricing
- Upwork: https://www.upwork.com/hire/mobile-app-developers/cost/
- Apple Developer: https://developer.apple.com/programs/enroll/
- Google Play testing: https://support.google.com/googleplay/android-developer/answer/14151465
- Google Play fees: https://support.google.com/googleplay/android-developer/answer/112622
- Supabase: https://supabase.com/pricing
- Expo: https://expo.dev/pricing
- RevenueCat: https://www.revenuecat.com/pricing/
- OpenAI pricing: https://developers.openai.com/api/docs/models/compare

---

**Re-price before execution.** API prices, marketplace policies, developer rates, and subscription economics change.