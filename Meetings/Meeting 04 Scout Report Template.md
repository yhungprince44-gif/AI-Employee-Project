# Scout — Business Intelligence Report Template (v2)

**Rule:** Every field below must be filled with a real value or `Unknown / Not Found`. Scout never guesses. If a field cannot be confirmed from a real source (Google Maps, the business's own website/socials), it is marked `Unknown / Not Found` — never estimated.

**Data Source Rule:** Every data point must be traceable. Scout logs where each core fact came from (Google Maps / Business Website / Instagram / Facebook), so the report can be audited later.

**Public Info Only Rule:** Phone and Email must be publicly listed (Google Maps, website, or social bio). Scout never uses private or scraped-from-unrelated-source contact info.

---

## Section 0 — Eligibility Gate
*(Must pass before Scout continues to Section 1. If it fails, Scout stops and logs the reason — no report is built.)*

| Field | Value / Format |
|---|---|
| Country | Must be 🇬🇧 UK, 🇦🇺 Australia, or 🇨🇦 Canada — else STOP |
| Category | Must be Restaurant/Café, Hotel/Apartment, or Barber/Hair Salon — else STOP |
| Eligible? | YES / NO |
| Date Researched | DD/MM/YYYY |

---

## Section 1 — Business Information

| Field | Value / Format |
|---|---|
| Business Name | Text |
| Category | Text (e.g. Restaurant, Hotel, Barber) |
| Country | Text |
| City | Text |
| Full Address | Text |
| Phone Number | Text or `Unknown / Not Found` |
| Email | Text or `Unknown / Not Found` |
| Website URL | Text or `None` |
| Instagram | Link or `Unknown / Not Found` |
| Facebook | Link or `Unknown / Not Found` |
| Google Rating | Number (e.g. 4.7) or `Unknown / Not Found` |
| Number of Reviews | Number |
| Opening Hours | Text or `Unknown / Not Found` |
| Photo Count on Google | Number |
| Photo Quality | Poor / Average / Good |
| Business Description | Text (from Google/website "About") |
| Main Services Offered | List |
| Data Source (per field above) | Google Maps / Business Website / Instagram / Facebook |

### Business Health Score (drives the multiplier in Section 5)

| Field | Value / Format |
|---|---|
| Rating Band | 4.5★+ / 4.0–4.4★ / 3.0–3.9★ / Below 3.0★ |
| Review Volume | 100+ / 30–99 / 10–29 / Under 10 |
| Recent Activity | Posted/reviewed in last 30 days? YES / NO |
| Business Health Tier | Excellent / Good / Weak / Poor (per Meeting #3 bands) |

---

## Section 2 — Website Analysis
*(Skip this entire section and mark it `N/A — No Website` if Has Website = NO)*

| Field | Value / Format |
|---|---|
| Has Website? | YES / NO |
| Website Design Score | 0–10 |
| Mobile Experience Score | 0–10 |
| Page Load Speed Score | 0–10 |
| Trust Score | 0–10 |
| Has Online Booking? | YES / NO / Not Applicable |
| Has Online Menu / Catalog? | YES / NO / Not Applicable |
| Has WhatsApp Button? | YES / NO |
| Has Live Chat? | YES / NO |
| Has Contact Form? | YES / NO |
| Has Google Maps Embed? | YES / NO |
| Has Customer Testimonials? | YES / NO |
| Has FAQ Section? | YES / NO |
| Overall Website Quality | Poor / Average / Good |
| Website Opportunity Score | 0–100 (per Meeting #2/#3 rubric) |

---

## Section 3 — Competitor Research

**Search Method (fixed, no guessing):** Search Google Maps for the same Category within a 2-mile / 3km radius of the business address. Take the top 3 results by review count, excluding the business itself.

| Field | Value / Format |
|---|---|
| Competitors Found (count) | Number |
| Competitor 1 — Name / Website / Rating | Text |
| Competitor 2 — Name / Website / Rating | Text |
| Competitor 3 — Name / Website / Rating | Text |
| Average Competitor Website Quality | Poor / Average / Good |
| Does This Business Fall Behind Competitors? | YES / NO |
| Gap Summary | 1–2 sentences on what competitors offer that this business doesn't |

---

## Section 4 — Improvement Ideas

| Field | Value / Format |
|---|---|
| Missing Features to Add | List (from Section 2 checklist gaps) |
| Design Improvement Notes | Text |
| Recommended Website Type | Booking Site / Menu + Ordering Site / Portfolio Site / Full Business Site / Landing Page |
| Estimated Build Complexity | Low / Medium / High |

---

## Section 5 — Final Recommendation

| Field | Value / Format |
|---|---|
| Business Health Multiplier | 1.2× / 1.0× / 0.6× / 0.3× (from Business Health Tier above) |
| Final Opportunity Score | Website Opportunity Score × Business Health Multiplier (capped at 100) |
| Should We Contact This Business? | YES / NO |
| Priority Level | High / Medium / Low |
| Reason (1 sentence, consultant tone) | Text |

---

## No-Guessing Enforcement Rules

1. If a data point isn't found through Google Maps, the business's website, or its social media, Scout enters `Unknown / Not Found` — it does not estimate or assume.
2. A field marked `Unknown / Not Found` in Section 1 (Phone or Email) automatically lowers the **Contactability** factor used in prioritization — it does not block the report from being completed.
3. Section 2 is only filled if `Has Website? = YES`. If NO, Section 2 is marked `N/A — No Website` in full, and the business auto-qualifies per the Meeting #2 rule.
4. Every score (0–10 or 0–100) must be based on the checklist criteria defined in Meetings #2 and #3 — never a subjective feeling.
5. This exact template is used for every business, with no fields skipped or renamed, so Employee #2 (Architect) can consume it without needing to ask Scout any follow-up questions.
6. If Section 0 (Eligibility Gate) fails, Scout does not proceed to Sections 1–5 at all. It logs the business name, address, and failure reason only — saving time and API calls on ineligible leads.
