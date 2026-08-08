# Domain 1 — Vertical AI / Business Operations

**Recommendation:** PRIORITY 1  
**Working concept:** AI KPI & Operations Brief for SMB / mid-market teams  
**Example wedge:** Connect Google Sheets/CSV → define metrics → generate evidence-backed morning brief → flag anomalies → maintain decision/action history.

## 1. Why this domain is attractive

Business apps are less glamorous than consumer AI, but that is part of the opportunity. RevenueCat's 2026 subscription dataset shows:

- Business is one of the categories most strongly oriented toward pure subscription monetization (76.5% subscriptions-only).
- Median Day-14 revenue per install is about $0.31, above the overall median.
- Only 19.1% of Business apps in the dataset are classified as AI-powered, far below Photo & Video (61.4%) and Productivity (41.1%).
- Business apps tend to monetize more slowly than high-impulse consumer apps, which means the go-to-market model should rely on targeted sales, pilots, referrals, and professional communities rather than hoping for viral App Store discovery.

The strongest thesis is **not** “build another BI tool.” It is to remove the manual interpretation and communication layer that currently sits between dashboards/spreadsheets and decisions.

## 2. Customer problem hypothesis

Target customers:

- Founder-led businesses with financial/operations reporting in Sheets.
- Small finance, sales-ops, supply-chain, marketing, and operations teams.
- Agencies reporting recurring client KPIs.
- Managers who receive multiple spreadsheets or dashboards but still need a human analyst to explain what changed.

Recurring pains to validate:

1. Data exists, but no one has time to interpret it every morning/week.
2. Existing dashboards show numbers but do not tell the user what changed or why.
3. Generic chatbots can hallucinate metrics or lose the organization's definitions.
4. Teams repeatedly write the same commentary for leadership.
5. Metric definitions differ across departments.
6. Alerting tools create noise because they lack business context.

## 3. Proposed differentiated product

### Core v1

- Email / Google / Microsoft login.
- CSV upload and Google Sheets connection.
- Metric dictionary: name, formula, source, owner, expected direction, thresholds.
- Scheduled refresh.
- Deterministic metric calculations outside the LLM.
- AI explanation layer using only validated calculated results.
- Daily/weekly executive brief.
- Anomaly and threshold alerts.
- Evidence links back to source rows/ranges.
- Chat follow-ups such as “why is conversion down?”
- Action log / notes attached to anomalies.

### Defensibility

The moat should be **governed context**, not model access:

- Persisted metric definitions.
- Source lineage.
- Calculation engine.
- Historical narratives and resolved incidents.
- Organization-specific vocabulary.
- Alert feedback loop (“useful / not useful”).
- Role-specific briefs.

This directly addresses RevenueCat's 2026 finding that AI apps monetize strongly early but retain worse: recurring utility and organization-specific context are needed to make the product sticky.

## 4. Competitive position

Do not compete head-on with Power BI, Tableau, Looker, ChatGPT, or generic spreadsheet copilots. Instead position as a **narrative and monitoring layer** that can sit above lightweight data sources first.

### Initial wedge

**“Turn the spreadsheet your business already uses into a trusted daily operating brief.”**

Why this wedge is attractive:

- Minimal migration friction.
- Easy demonstration.
- Customers already understand Sheets/Excel.
- Fast time-to-value.
- Can later expand to BigQuery, Snowflake, SQL Server, HubSpot, Shopify, QuickBooks, Stripe, etc.

## 5. MVP architecture

| Layer | Recommended early choice | Reason |
|---|---|---|
| Mobile | React Native + Expo | One iOS/Android codebase |
| Web | Next.js / React | Admin, configuration, richer analysis |
| API | Python FastAPI or TypeScript | Mature ecosystem |
| Database/Auth | Supabase/Postgres | $25/month production entry point; auth included |
| Background jobs | Managed queue/cron | Scheduled refresh and briefs |
| File storage | Supabase/S3 compatible | CSVs, exports |
| AI | GPT-5.6 Luna/Terra routing | Low-cost extraction + stronger reasoning when needed |
| Billing | RevenueCat for mobile; Stripe for web/B2B | Cross-platform subscription management |
| Analytics | PostHog/Firebase | Funnel/retention measurement |
| Error monitoring | Sentry/Firebase Crashlytics | Production support |

## 6. Development effort and cost

### Functional proof-of-concept

Scope: Google Sheet/CSV → three metrics → one daily brief → web/mobile result.

- Estimated effort: 150-300 hours.
- Contractor blended rate assumption: $20-$45/hour.
- Cash cost: **$3,000-$13,500**.
- Founder-assisted target: **$3,000-$7,500**.

### Commercial MVP

Scope includes authentication, organization/workspace model, secure connectors, metric dictionary, scheduled jobs, AI brief, alerts, billing, analytics, error handling, privacy controls, QA, App Store/Play Store release.

Estimated effort:

| Workstream | Hours |
|---|---:|
| Product discovery / specification | 60-100 |
| UX/UI | 100-160 |
| Mobile app | 220-350 |
| Web admin | 160-260 |
| Backend/auth/data model | 220-320 |
| Google Sheets/CSV ingestion | 100-160 |
| Metric engine + lineage | 120-220 |
| AI narrative + evaluation | 100-180 |
| Alerts/notifications | 50-90 |
| Billing | 40-70 |
| QA/security/release | 120-200 |
| **Total** | **1,290-2,110 hours** |

At a $25-$49/hour development-company benchmark, that implies a theoretical labor envelope around **$32K-$103K**. A founder taking ownership of product definition, data logic, prompt/evaluation work, acceptance testing, documentation, and some implementation can cut cash spend materially.

**Founder-assisted commercial MVP planning target: $15K-$35K.**  
**Professional team planning target: $40K-$100K.**

## 7. AI unit economics

A business narrative app can be inexpensive to operate if calculations are deterministic and the LLM only interprets structured results.

### Example user-month

Assume one paid workspace generates:

- 60 briefs/analyses per month.
- Average request: 8,000 input tokens + 1,500 output tokens.

Using GPT-5.6 Luna ($1/M input; $6/M output):

- Input per analysis: ~$0.008.
- Output per analysis: ~$0.009.
- Total per analysis: ~$0.017.
- 60 analyses: **~$1.02/month**.

Using GPT-5.6 Terra ($2.50/M input; $15/M output):

- Input per analysis: ~$0.020.
- Output per analysis: ~$0.0225.
- Total per analysis: ~$0.0425.
- 60 analyses: **~$2.55/month**.

Even allowing for retries, embeddings, summaries, and occasional premium-model escalation, a **$2-$8 AI cost per active workspace per month** is realistic for a well-engineered early product.

This is attractive against potential pricing of $49-$199/month per workspace.

## 8. Monthly operating model

### 100 paying workspaces

Assume $79/month average subscription = $7,900 MRR.

Potential monthly variable/fixed software costs:

| Item | Planning range |
|---|---:|
| Supabase / database / storage | $25-$100 |
| AI usage | $200-$800 |
| Email/notifications | $20-$100 |
| Monitoring/analytics | $0-$100 |
| RevenueCat (if mobile revenue tracked) | 1% after threshold |
| Misc. SaaS | $50-$150 |
| **Technical run-rate before human support** | **~$300-$1,300/month** |

The biggest early expense is likely not compute; it is customer acquisition, onboarding, support, and continued development.

## 9. Pricing hypothesis

Test three tiers:

- **Solo:** $29-$49/month — 1 workspace, limited sources.
- **Team:** $79-$149/month — more sources, alerts, scheduled briefs, multiple users.
- **Business:** $199-$499/month — integrations, permissions, audit history, branded reporting, priority support.

A mobile App Store subscription is optional. For B2B, web billing may be strategically preferable where platform rules allow it, because the primary sales motion is likely web/demo driven.

## 10. Major risks

- Customers may view the product as a feature inside BI tools rather than a standalone product.
- Wrong narrative = lost trust. Every claim needs evidence and reproducibility.
- Connector maintenance can grow quickly.
- B2B sales cycles can be slower than consumer app conversion.
- Security expectations rise when business data becomes sensitive.
- Large AI/BI vendors can copy superficial features.

### Risk reduction

Start with one connector (Sheets), one target persona, and one repeatable use case. Do not build ten connectors before customers pay.

## 11. Validation experiment

1. Recruit 10 managers/business owners who already review recurring spreadsheets.
2. Ask for a sanitized weekly/daily report.
3. Manually generate the “AI operating brief” for 2 weeks.
4. Measure: Did they open it? Did it identify something useful? Did they reply/act? Did they request continuation?
5. Ask for $49-$99/month to continue.

**Go signal:** 3+ of the first 10 agree to pay or sign a pilot before a full app exists.

## 12. Domain score

| Dimension | Score / 10 |
|---|---:|
| Proven willingness to pay | 8 |
| Competition | 6 |
| Ease of differentiation | 8 |
| Build feasibility | 8 |
| Variable cost economics | 9 |
| Regulatory simplicity | 8 |
| Founder-market fit | 10 |
| Distribution controllability | 8 |
| **Weighted view** | **8.4 / 10** |

## Sources

- RevenueCat, State of Subscription Apps 2026: https://www.revenuecat.com/state-of-subscription-apps
- Sensor Tower, State of Mobile 2026: https://sensortower.com/press/press-release-boosted-by-gen-ai-services-consumers-spent-more-money-in-apps-than-games-for-first-time
- OpenAI model pricing: https://developers.openai.com/api/docs/models/compare
- Supabase pricing: https://supabase.com/pricing
- RevenueCat pricing: https://www.revenuecat.com/pricing/
- Expo pricing: https://expo.dev/pricing
- Clutch Mobile App Pricing Guide 2026: https://clutch.co/directory/mobile-application-developers/pricing
- Upwork mobile developer cost guide: https://www.upwork.com/hire/mobile-app-developers/cost/
