# Meeting #5 — Business Opportunity Scoring Framework (BOS)

**Project:** AI Employee Project
**Version:** v1.0.0
**Status:** 🔒 Locked — Final

---

## 🎯 Objective

Design a transparent, explainable, evidence-based scoring system that ranks businesses by opportunity, in line with the company constitution: AI never guesses, every score is explainable, every recommendation has evidence.

---

## 🏗 Final Scoring Architecture

### Step 1 — Opportunity Score

```
Opportunity Score = (Website Opportunity × 55%)
                   + (Contact Readiness × 25%)
                   + (Project Potential × 20%)
```

**Website Opportunity (55%)** — the highest-weighted factor, since websites are the core service. Measures: no website, outdated design, poor mobile experience, slow loading, weak branding, poor navigation, missing booking, missing modern features.

**Contact Readiness (25%)** — measures how easy the business is to reach, using public information only: public email, public phone, contact form, social media messaging.

**Project Potential (20%)** — measures whether the finished website would make a strong portfolio piece. Evidence-based only: image quality, branding quality, visual appeal, available public assets, business presentation. No subjective opinions allowed.

### Step 2 — Business Health Multiplier

Business Health is **not** part of the Opportunity Score — it multiplies the final result, preserving the Meeting #3 architecture.

```
Opportunity Score → Business Health Multiplier → Business Opportunity Score (Final)
```

| Business Health Tier | Multiplier |
|---|---|
| Excellent | ×1.20 |
| Good | ×1.00 |
| Weak | ×0.60 |
| Poor | ×0.30 |

*(The exact Business Health calculation is finalized in Meeting #6.)*

### Final Score Rule
The Business Opportunity Score is always capped at 100.

---

## 📜 Company Rules Approved

| Rule | Description |
|---|---|
| **K — Explainability** | Every score must reference the exact BIR fields that produced it. No black-box scoring. |
| **L — Evidence-Based Project Potential** | Project Potential must use measurable evidence, never guessing. |
| **M — No Double Counting** | Business Health and Contact Readiness must never reuse the same signal. |
| **N — Report Freshness** | 🟢 0–30 days: continue normally. 🟡 31–60 days: quick refresh. 🟠 61–90 days: regenerate BIR before ranking. 🔴 90+ days: remove from active pipeline until re-researched. |
| **O — Tie-Breaking** | 1) Higher Contact Readiness → 2) Higher Website Opportunity → 3) Higher Business Health Tier → 4) Most Recently Researched → 5) Original discovery order. Fully deterministic. |
| **P — Score Cap** | Business Opportunity Score can never exceed 100. |
| **Q — Missing Critical Data** | Scout never invents missing values. Mark report Incomplete → attempt another search → if still incomplete, flag for human review before scoring. |

---

## 📊 Priority Bands

| Score | Priority |
|---|---|
| 80–100 | High |
| 60–79 | Medium |
| 40–59 | Low |
| 20–39 | Very Low |
| 0–19 | Do Not Contact (Automatic) |

---

## ✅ Architecture Decisions Locked

- Website Opportunity receives the highest weighting.
- Business Health remains a multiplier, never a weighted category.
- Every score must be explainable, referencing exact BIR fields.
- Every recommendation must have evidence.
- Reports become stale over time and lose priority accordingly.
- Tie-breaking is fully deterministic across five levels.
- Businesses with insufficient data cannot be scored — never guessed.

---

## 📌 Outstanding Work → Meeting #6

1. **Business Health Formula** — precise weighting of Rating, Review Count, Review Freshness, Business Activity, and Profile Completeness into the Excellent/Good/Weak/Poor tiers.
2. **BIR → Score Mapping Table** — the master table enforcing Rule K, linking every scoring input back to a specific BIR field.

Once complete, Employee #2 (Architect) can safely depend on the scoring system.

---

## 📌 Version Update

- **v1.0.0** — Locked. Business Opportunity Score architecture, Rules K–Q, Priority Bands, and tie-breaking system finalized.

---
*This document is part of the AI Employee Project meeting archive.*
