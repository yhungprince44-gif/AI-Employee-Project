# Meeting #3 — Opportunity Scoring & Prioritization

**Project:** AI Employee Project
**Employee:** Employee #1 — Business Research Analyst
**Status:** ✅ Complete

---

## 🎯 Focus of This Meeting

Resolving the open question from Meeting #2: **how does Employee #1 decide which businesses are actually worth the team's time**, not just which ones need a new website.

## ✅ Decisions Made

- Employee #1 will use a **Business Opportunity Score out of 100**, replacing simple "good/bad website" judgments.
- The score is split into **two components**, not one:
  1. **Website Score** — quality of the current website (design, speed, mobile, booking, contact info).
  2. **Business Score** — health of the business itself (rating, review count, activity, photo quality, engagement).
- **Business Score acts as a multiplier on Website Opportunity, not an equal-weighted average.** A weak or poorly-reviewed business should scale the final score *down*, even if the website opportunity is huge — because a great website cannot fix a business customers don't trust.
- Resolved: given two businesses that both need a website, the one with the **stronger business health (higher rating, more reviews, active engagement)** is prioritized first. A struggling business with poor reviews is deprioritized, not excluded — it may still get a low-effort template later, but isn't worth premium effort.

## 📜 Rules Approved

### Rule #4 — Discovery Source
Search starts with **Google Maps**.

### Rule #5 — Target Business Categories
- Restaurants & Cafés
- Hotels & Apartments
- Barbers & Hair Salons

### Rule #6 — Market Priority
- **Primary market:** 🇬🇧 United Kingdom
- **Expansion markets:** 🇦🇺 Australia, 🇨🇦 Canada

### Rule #7 — Scoring Formula
```
Final Opportunity Score = Website Opportunity Score × Business Health Multiplier
```

**Business Health Multiplier bands:**

| Business Health | Criteria | Multiplier |
|---|---|---|
| Excellent | 4.5★+, 100+ reviews, active | 1.2× |
| Good | 4.0–4.4★, 30+ reviews | 1.0× |
| Weak | 3.0–3.9★, few reviews | 0.6× |
| Poor | Below 3.0★, or many complaints | 0.3× |

*(Final score is capped at 100.)*

## 💡 Ideas Discussed

**Original 100-point checklist proposal** (superseded by the multiplier model above, kept for reference):

| Check | Points |
|---|---|
| No website | +30 |
| Website looks outdated | +20 |
| Poor mobile experience | +15 |
| No online booking (where relevant) | +10 |
| Missing contact information | +5 |
| Slow loading | +10 |
| Weak branding / poor visuals | +10 |

**Key strategic shift:** Employee #1 no longer only asks *"Can I improve the website?"* — it also asks *"Is this a business worth helping?"* This moves Employee #1 from a website critic to a business strategist.

**Worked example:**
- Business A: No website, 4.9★, 600 reviews, always busy → Website Opportunity 90 × 1.2 → **100 (capped). Top priority.**
- Business B: No website, 2.3★, 18 reviews, many complaints → Website Opportunity 90 × 0.3 → **27. Low priority.**

## 🔄 Open Questions

- None outstanding — prioritization logic for Meeting #2's open question is now resolved.
- Future: define exact thresholds/edge cases for the Business Health bands as real data comes in.

## ✅ Action Items

- [ ] Begin building Employee #1's scoring engine in Python (planned free-tier stack: OpenStreetMap/Overpass API for discovery, Google PageSpeed Insights API for website scoring, Playwright for feature/visual checks, Claude for report generation).
- [ ] Every future meeting will produce a summary in this format (Decisions, Rules, Ideas, Action Items, Open Questions, Version Updates) and be added to the GitHub repository.
- [ ] Next process gap identified: once a business is qualified and prioritized, **someone must actually build the website** (added as a future step — options: no-code builders, Claude-built HTML/CSS with free hosting, or a future "Employee #2" automation).

## 📌 Version Updates

- **v1.2** — Introduced two-part scoring model (Website Score × Business Health Multiplier), locked in discovery source, target categories, and market priorities. Resolved prioritization open question from Meeting #2.

---
*This document is part of the AI Employee Project meeting archive.*
