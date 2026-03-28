# A Thriving City Hall — Hackathon Challenge

This file defines the two practical problem statements for this pillar and the top-rated blue sky vision. Read this before reading anything else in the repository.

---

## The Two Problems You're Solving

### Problem 1: Helping Residents Find the Right City Service or Next Step

**Score: 27/32 — Strong (highest-scoring targeted statement in this pillar)**

**Statement:**
How might we use technology to help Richmond residents quickly determine the right next step when interacting with City services — whether finding information or submitting a request — so that issues are routed correctly the first time while working within existing City systems and minimizing additional staff workload?

**Why this problem matters:**
Residents come to rva.gov or RVA311 with a real need but don't know which department handles it, which request type applies, or whether they need information, a form, or a service request. The City's information architecture is department-centric, not citizen-centric. Residents submit the wrong request type, contact staff directly, or abandon the process. The result: miscategorized requests, staff time spent on redirects, and residents who give up.

**Build toward:**
- Resident service navigation tool — plain language description → right department and next step
- 311 category guide or chatbot — helps residents pick the correct request type before submitting
- City website plain-language search helper — makes rva.gov content actually findable
- Staff-facing triage tool — helps 311 agents categorize ambiguous incoming requests

**Key constraints:**
- Must work with rva.gov and RVA311 — not replace them
- Must use verified City information only — do not invent answers
- Must refuse to answer confidently when information is unclear, outdated, or conflicting
- Must not claim to be an official City service or represent City determinations
- Post-2018 RVA311 data does not exist in any public API — do not build on it

**Critical technical landscape:**
- **rva.gov:** Drupal 8+ on Acquia. Search URL: `https://www.rva.gov/search?search={query}`
- **RVA311:** AvePoint Citizen Services on Dynamics 365, launched June 2018. **No public API.**
- **Historical Socrata 311 dataset (vgg4-hjn8):** SeeClickFix data only, January 2014–August 2015. Not representative of current request types or volume.
- **2025 volume:** ~208,000 RVA311 requests across 50+ categories in 7 department groups

#### Participant guide: connecting to the rubric (if you chose this problem)

Optional prompts — judges score from [`RUBRIC.md`](../../RUBRIC.md), not this list.

- **Impact:** Help residents reach the **right** next step (info vs request type vs department) without inventing City answers.
- **User Value:** A resident or 311-facing flow where miscategorized requests would plausibly drop.
- **Feasibility:** Work with verified City sources; no fake RVA311 API; say “don’t know” when data is missing.
- **Innovation:** Plain-language routing, triage aids, or search that beats raw site search alone.
- **Execution:** Demo path is credible and labeled when static or mock.
- **Equity and inclusion:** Reach residents who struggle most with digital City navigation.

**What often works well:** Navigation helper, category guide, or staff triage support grounded in real rva.gov / public facts.

**What to avoid:** Claiming official City status, confident answers you cannot verify, or implying live 311 integration you don’t have.

*Try asking yourself:* Could someone stuck on the wrong form find the right channel without us guessing policy?

---

### Problem 2: Helping City Staff Review Procurement Risks and Opportunities

**Score: 22/32 — Needs work (data pre-staging required)**

**Statement:**
How might we use technology to help Richmond staff identify valid, compliant, and cost-effective purchasing contracts across City, state, and federal sources so that procurement decisions require less manual review while maintaining legal compliance and transparency?

**Why this problem matters:**
City staff rely on multiple contract sources — City contracts, VITA state contracts, GSA federal contracts, cooperative purchasing agreements. Key details (expiration dates, renewal windows, pricing terms) are buried in PDFs or spread across different systems. No unified view of upcoming renewals exists. Staff manually scan PDFs and databases to make informed procurement decisions.

**Build toward:**
- Procurement contract risk dashboard — surfaces expiring contracts from Socrata data
- Contract PDF extractor — pulls key terms from procurement documents
- Multi-source contract explorer — visualizes spending or contract data across City/state/federal sources
- Staff decision-support tool — helps staff triage or compare contracts before a decision

**Key constraints:**
- Must support staff judgment, not replace it — no automated award or compliance decisions
- Must use publicly available contract data — do not build on internal City systems
- Must be scoped tightly enough to demo in a weekend
- Must not make legal compliance determinations

**Data sources:**
- **City Contracts Socrata (xqn7-jvv2):** Use the CSV download — the API has a known bug returning only 8 of 9 columns. CSV: `data.richmondgov.com/api/views/xqn7-jvv2/rows.csv?accessType=DOWNLOAD`
- **SAM.gov:** Federal contracts and debarment data. Free API key required.
- **eVA (Virginia electronic procurement):** CSV export available at data.virginia.gov
- **VITA statewide contracts:** `vita.cobblestonesystems.com/public/` — web only, no API
- **GSA Schedules:** Federal supply schedules via SAM.gov

**Data gaps (teams must address before building):**
- Sample procurement PDFs not pre-staged — teams need to find and download representative samples
- No named departmental champion has committed to this problem
- VITA portal has no API — scraping or manual extraction required

#### Participant guide: connecting to the rubric (if you chose this problem)

Optional prompts — [`RUBRIC.md`](../../RUBRIC.md) is authoritative for judges.

- **Impact:** Reduce manual hunting across contracts (expirations, terms, risk signals) while **supporting** staff judgment.
- **User Value:** A procurement or finance role with a concrete saved step (e.g. expiring list, PDF field extraction demo).
- **Feasibility:** Public data only; no automated legal/compliance **decisions**; scope matches a weekend.
- **Innovation:** Cross-source views, risk surfacing, or extraction UX that’s honest about PDF messiness.
- **Execution:** Working slice on real Socrata CSV or a small real PDF set.
- **Equity and inclusion:** Transparency angles that help oversight and residents understand spending **without** misrepresenting official reporting.

**What often works well:** Contract dashboard from Socrata, compare or triage UI, careful PDF prototype with disclaimers.

**What to avoid:** Legal determinations, award recommendations, or pretending full multi-source automation is production-ready.

*Try asking yourself:* Could staff trust this as a **starting point** for review, not a verdict?

---

## The Blue Sky Vision

### Making Fiscal Responsibility More Visible — 21/27 — Strong ★

**Statement:**
How might we use technology to make Richmond's fiscal decisions, contract awards, and budget spending more visible and understandable to residents and oversight bodies so that public accountability is strengthened and trust in City government is improved?

**Why this scored well:**
Strong data foundation. The City Contracts Socrata dataset, SAM.gov, eVA, and related procurement data are all publicly available. A transparency dashboard or contract explorer built on these sources is a compelling weekend project.

**Hackathon path if you're aiming at this vision:**
Build a public-facing transparency explorer using the Socrata contracts dataset, with plain-language descriptions of contract categories, vendor patterns, and spending trends. Avoid claiming the tool represents official City financial reporting — label it exploratory.

The blue sky is the ceiling. Problem 2 (Procurement Risks) is the practical floor. A team that builds a staff-facing procurement tool and adds a public-facing transparency layer will have a strong pitch for both the Pillar Award and the Moonshot Award.

**Rubric connection (blue sky):** Aligns with **Problem 2** (contracts, spending visibility) and public accountability framing. Use the Problem 2 participant guide; add resident-readable layers only with clear “exploratory / not official reporting” labels.

---

## Pillar Award: official scoring mechanics

**Authoritative rubric:** [`RUBRIC.md`](../../RUBRIC.md) at the hackathon root.

**Participant guides** under each problem are optional team prompts — **not** binding on judges.

| Category | Weight |
|----------|--------|
| **Impact** (targeted civic problem) | **5** |
| **User Value** | 4 |
| **Feasibility** / implementability | 3 |
| **Innovation** / originality | 3 |
| **Execution** / prototype quality | 3 |
| **Equity and inclusion** | 3 |

Read **`RUBRIC.md`** for full definitions and anchors.

**Score formula:** Sum of (category score 1–5 × weight). Maximum 105.

**Tiebreaker:** User Value score.

**General tips** (full detail in `RUBRIC.md`): Civic usefulness over complexity; flag fragile assumptions; slides-only → low Execution; unverified integrations → lower Feasibility.
