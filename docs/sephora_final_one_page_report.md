# Sephora Digital BI Project - Final One-Page Report

## Project Summary
This BI case study evaluated digital commerce performance across `app`, `desktop_web`, and `mobile_web` to identify the highest-impact opportunities for conversion and revenue growth.

## Business Objective
Determine where Sephora's digital journey loses the most value and prioritize actions that improve:
- conversion rate,
- revenue per session (RPS),
- operational focus across digital channels.

## Scope and Method
- Built a SQL metric layer using session-level ecommerce data.
- Analyzed funnel progression (`Product Views -> Add To Cart -> Checkout Starts -> Orders`).
- Compared channel performance and personalization impact.
- Built executive-facing dashboards in Tableau.

## Core KPIs
- Session to Order Rate = `orders / sessions`
- Revenue per Session = `revenue / sessions`
- Average Order Value (AOV) = `revenue / orders`
- Funnel stage rates:
  - View to Cart
  - Cart to Checkout
  - Checkout to Order

## Key Findings
1. **App is the strongest channel**
   - Session-to-order rate: **6.68%**
   - Revenue per session: **$4.95**
2. **Mobile web is the largest opportunity gap**
   - Session-to-order rate: **2.15%**
   - Revenue per session: **$1.48**
3. **Largest funnel friction is mobile web cart -> checkout**
   - Cart-to-checkout rate: **62.60%**
4. **Personalization outperforms non-personalized experience**
   - Conversion: **4.76% vs 2.70%** (+2.06 pp)
   - RPS: **$3.52 vs $1.99**

## Recommendations
1. Prioritize mobile web checkout simplification (shorter forms, clearer payment flow, express pay prominence).
2. Expand personalization on high-traffic pages and categories.
3. Use app performance patterns as a benchmark for web optimization.
4. Establish weekly channel x source KPI monitoring with owners and thresholds.

## Next Test (Execution-Ready)
- **A/B Test:** mobile web checkout simplification
- **Changes:** shorter forms + express pay prominence
- **Success Metric:** **+0.5 to +1.0 percentage points** in session-to-order rate

## Deliverables Produced
- SQL analysis scripts and reproducible metric logic
- Executive KPI, Funnel, and Personalization Tableau dashboards
- Tableau story with Intro -> KPI -> Funnel -> Personalization -> Recommendations
- BI planning documentation and interview-ready narrative

## Project Outcome
The project provides a decision-ready roadmap to improve digital conversion and revenue efficiency by focusing first on mobile checkout friction and scaling personalization where uplift is strongest.
