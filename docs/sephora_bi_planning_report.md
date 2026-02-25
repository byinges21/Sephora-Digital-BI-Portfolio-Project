# Sephora - BI Planning Report

## 1. Stakeholder Requirements Document

### Project Title
Digital Performance & Personalization Dashboard - Sephora Ecommerce

### Project Background
Sephora's digital teams need clearer visibility into channel performance and funnel behavior across `app`, `desktop_web`, and `mobile_web`. Leadership wants data-backed direction on where to focus optimization efforts to increase conversion and revenue efficiency.

### Business Problem
Current reporting does not clearly show:
- which channel drives strongest conversion and revenue per session,
- where users drop off most in the funnel,
- whether personalization is delivering measurable uplift.

### Project Goal
Design an accessible BI dashboard that identifies conversion bottlenecks and personalization impact, and translates findings into prioritized business actions.

### Key Stakeholders
Primary:
- Digital Analytics Manager
- Product Manager (Web/App)
- Digital Merchandising Lead

Secondary:
- Marketing Analytics Analyst
- Content Strategy Analyst
- Engineering Analytics Partner

Dashboard viewers:
- Digital leadership
- Product, Marketing, and Merchandising partners

### Stakeholder Needs & Expectations
- Clear KPI visibility (sessions, orders, revenue, conversion, AOV, RPS)
- Channel comparison (`app`, `desktop_web`, `mobile_web`)
- Funnel-stage diagnostics
- Personalization performance comparison
- Time trend views
- Executive-friendly, clean visuals

### Success Criteria (Stakeholder Perspective)
Dashboard is successful if it:
- clearly highlights top and bottom channel performance,
- identifies the highest-friction funnel stage,
- quantifies personalization uplift,
- supports prioritization of an optimization roadmap.

## 2. Project Requirements Document

### Data Sources
Anonymized session-level ecommerce dataset with:
- `session_date`
- `channel`
- `traffic_source`
- `campaign`
- `is_personalized`
- `sessions`
- `product_views`
- `add_to_cart`
- `checkout_starts`
- `orders`
- `revenue`

### Data Definitions
- Channels: `app`, `desktop_web`, `mobile_web`
- Personalization flag:
  - `1` = personalized experience
  - `0` = non-personalized experience
- Funnel:
  - `Product Views -> Add To Cart -> Checkout Starts -> Orders`

### Deliverables
- KPI summary by channel
- Funnel conversion and drop-off analysis by channel
- Channel x traffic source performance view
- Personalization impact analysis
- Time-series trend view
- Tableau story with:
  - Intro
  - Executive KPI Overview
  - Funnel Performance
  - Personalization Impact
  - Recommendations & Next Steps

### Functional Requirements
Dashboard must:
- filter by channel, traffic source, personalization type, and date,
- display conversion and monetization KPIs,
- support comparison across channels and personalization groups,
- include an actionable recommendation view.

### Non-Functional Requirements
- Clean, uncluttered layout
- Consistent metric formatting (`$`, `%`, counts)
- High readability and clear labels
- Shareable via Tableau Public and GitHub link

### Metrics
Primary:
- Session to Order Rate = `orders / sessions`
- Revenue per Session = `revenue / sessions`
- Revenue
- Orders

Secondary:
- View to Cart Rate = `add_to_cart / product_views`
- Cart to Checkout Rate = `checkout_starts / add_to_cart`
- Checkout to Order Rate = `orders / checkout_starts`
- AOV = `revenue / orders`

### Risks & Dependencies
- Metric definition drift across sheets
- Inconsistent formatting or labeling
- Misinterpretation of personalization as causal without test design
- Dataset granularity limits (simulated data)

## 3. Strategy Document

### BI Stage 1: Capture
- Validate schema and field types
- Confirm KPI formulas and funnel sequence
- Standardize date and segmentation dimensions

### BI Stage 2: Analyze
Key analyses:
- Channel KPI comparison (conversion, RPS, revenue)
- Funnel leak identification by channel and stage
- Traffic source quality by channel
- Personalized vs non-personalized uplift
- Time trend movement by date interval

Derived metrics:
- Personalization Uplift (conversion and RPS delta)
- Funnel Friction Index (largest stage drop-off by channel)
- Channel Efficiency Ranking

### BI Stage 3: Monitor
Dashboard design principles:
- Executive-first layout
- Clear insight callouts per dashboard
- Consistent color logic (baseline vs personalized)

Monitoring strategy:
- Weekly KPI check by channel
- Funnel friction watchlist (focus on mobile_web checkout)
- Personalization uplift trend tracking

### Implementation Plan
1. Build and validate SQL metric layer
2. Create Tableau dashboard pages
3. Add story narrative and recommendations
4. QA metric consistency and formatting
5. Publish to Tableau Public
6. Link Tableau in GitHub README

### Expected Impact
- Faster prioritization of high-impact digital optimizations
- Better alignment across Product, Marketing, and Merchandising
- Improved conversion and revenue efficiency focus

## 4. Questions About Missing Information
1. Should KPI targets be absolute (e.g., +1.0 pp conversion) or relative (% lift)?
2. Should mobile_web optimization be prioritized over all other initiatives by default?
3. Are campaign-level insights required in the executive view or only drill-down?
4. Should personalization results be framed as directional only unless A/B tested?
5. What benchmark defines acceptable channel performance (internal target vs channel average)?
6. Do stakeholders need downloadable exports (PNG/PDF/CSV) from Tableau Public?
