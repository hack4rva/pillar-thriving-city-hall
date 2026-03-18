# Verification TODO — A Thriving City Hall

Top 10 claims to verify before the hackathon (March 27, 2026). Assign each to a team member and log the result in `evidence_log.md`.

---

## Priority Verifications

### 1. rva.gov sitemap availability
**Claim:** rva.gov publishes a sitemap.xml that can be used to discover all department and service pages.
**How to verify:** Check https://www.rva.gov/sitemap.xml — does it exist? If so, how many pages does it index?
**Impact if false:** Teams building a rva.gov search layer must crawl manually from department landing pages rather than using a sitemap.
**Evidence log ID:** E-016
**Status:** [x] Verified 2026-03-18 — **CLAIM IS FALSE.** https://www.rva.gov/sitemap.xml returns HTTP 404. No sitemap exists. Teams must crawl department landing pages manually.

---

### 2. Drupal Search API facet parameters
**Claim:** The search URL pattern https://www.rva.gov/search?search={query}&page={n}&f[0]=business_unit:{id} is correct and returns JSON-parseable results.
**How to verify:** Test the URL with a known query and a known department slug; inspect the response format.
**Impact if false:** Search integration approach may need to change.
**Evidence log ID:** E-006
**Status:** [x] Verified 2026-03-18 — **CLAIM IS PARTIALLY INCORRECT.** URL pattern works as /?search={query}&page={n} with zero-based pagination. Response is HTML only (not JSON). The f[0]=business_unit:{id} facet parameter is NOT visible in the HTML and appears non-functional. Search integration via JSON is not possible with this endpoint.

---

### 3. RVA311 2025 volume (208,216 requests)
**Claim:** RVA311 received 208,216 total service requests in 2025.
**How to verify:** Find the source document (City annual report, press release, Council presentation). The rubric document cites this figure but doesn't give a URL.
**Impact if false:** Demo credibility if this number is wrong or cannot be sourced.
**Evidence log ID:** E-004
**Status:** [x] Verified 2026-03-18 — **CLAIM IS LIKELY INCORRECT.** The Feb 26, 2025 City Council presentation by Pete Breil (Director of Citizen Service & Response) reports 2024 figures: 203,000 calls received, 75,200 requests created in RVA311. No figure of 208,216 appears anywhere in the official documents or news coverage. WRIC reports ~204,000 calls. The figure 208,216 is unverified and should be removed from demos unless sourced. Source: https://richmondva.legistar.com/View.ashx?GUID=C050E3F8-7CC4-4663-BA8F-362608460B56&ID=13777233&M=F

---

### 4. City Contracts dataset column bug confirmation
**Claim:** The City Contracts Socrata API (xqn7-jvv2) returns only 8 of 9 columns. The CSV download returns all 9.
**How to verify:** Query both the SODA API and download the CSV; compare column counts and identify the missing column.
**Impact if false:** Teams may not need to use CSV workaround.
**Evidence log ID:** E-008 and E-009
**Status:** [x] Verified 2026-03-18 — **CLAIM IS INCORRECT.** Both SODA API and CSV return the same 9 columns: agency_department, contract_number, contract_value, supplier, procurement_type, description, type_of_solicitation, effective_from, effective_to. No column bug exists as of this date. CSV download URL confirmed working. Teams do not need a CSV workaround.

---

### 5. SAM.gov API free key availability and rate limits
**Claim:** SAM.gov provides free API access with no cost, and a key can be obtained via sam.gov registration.
**How to verify:** Visit https://open.gsa.gov/api/entity-api/ and confirm key registration process and rate limits.
**Impact if false:** Cross-source contract finder may require paid API access or have tighter rate limits than expected.
**Evidence log ID:** E-014
**Status:** [x] Verified 2026-03-18 — **CLAIM IS VERIFIED WITH IMPORTANT CAVEATS.** API key is free (no monetary cost). Key obtained from sam.gov/profile/details. Rate limits: non-federal users without a role = 10 requests/day (very low). Non-federal with role = 1,000/day. Teams should register in advance. The 10 req/day limit for basic accounts is a significant constraint for hackathon demos.

---

### 6. AvePoint Citizen Services platform — no public API confirmation
**Claim:** AvePoint Citizen Services (Richmond's RVA311 platform) does not expose a public API for service requests.
**How to verify:** Check AvePoint product documentation at https://www.avepoint.com/products/citizen-services. Look for API documentation.
**Impact if false:** (Unlikely to be wrong, but confirming eliminates a potential project blocker.)
**Evidence log ID:** E-002
**Status:** [x] Verified 2026-03-18 — **CLAIM IS PLAUSIBLE BUT UNCONFIRMED.** The AvePoint product page (avepoint.com/products/citizen-services) returns 404. The case study confirms BizTalk server integration with Cityworks but does not reference a public API. No public API documentation found. Treat as no public API available for hackathon purposes.

---

### 7. rva.gov department slug list
**Claim:** There are over 40 department slugs accessible via the business_unit facet parameter in rva.gov search.
**How to verify:** Inspect rva.gov search page HTML for facet values; or query the search API without a business_unit filter and examine the facet response.
**Impact if false:** The number of departments affects the scope of a category taxonomy project.
**Evidence log ID:** E-017
**Status:** [x] Verified 2026-03-18 — **CLAIM CANNOT BE CONFIRMED.** No facet filter options or business_unit parameters are exposed in the rva.gov search page HTML. The 40+ department slug claim is unverified. Teams should not rely on this parameter.

---

### 8. Historical RVA311 Socrata data date range
**Claim:** The historical SeeClickFix Socrata dataset (vgg4-hjn8) contains data from January 2014 through August 2015 only.
**How to verify:** Query the SODA API: https://data.richmondgov.com/resource/vgg4-hjn8.json?$select=min(created_at),max(created_at)
**Impact if false:** May affect how useful the historical data is for understanding current category patterns.
**Evidence log ID:** E-001
**Status:** [x] Attempted 2026-03-18 — **CANNOT VERIFY.** The SODA $select query returned HTTP 400 (Bad Request). The date range claim (Jan 2014–Aug 2015) could not be confirmed via API. Alternative: manually check the dataset page at data.richmondgov.com or try a different query format.

---

### 9. eVA Virginia procurement dataset URL on data.virginia.gov
**Claim:** Virginia eVA procurement data is available as a CSV download on data.virginia.gov.
**How to verify:** Search https://data.virginia.gov for "eVA" or "procurement" and find the current dataset URL.
**Impact if false:** Cross-source finder approach may need adjustment.
**Evidence log ID:** E-018
**Status:** [x] Verified 2026-03-18 — **CLAIM IS VERIFIED.** Multiple annual datasets confirmed at data.virginia.gov: 2018, 2022, 2023, 2024, 2025. CSV download confirmed (~1.1 GB for 2024). Dataset uses CKAN API (not Socrata SODA). Also accessible via eva.virginia.gov/eva-open-data.html. Direct CSV: https://data.virginia.gov/dataset/570f4ddb-7dca-4e2f-a329-ffad0e295e7a/resource/25a59527-f14a-475d-b8da-af0155015887/download/eva_procurement_data_2024.csv

---

### 10. Pete Briel as Director of 311 / formal champion status
**Claim:** Pete Briel is the Director of 311 at Richmond City government and is a candidate for post-hackathon champion.
**How to verify:** Check City of Richmond staff directory or press coverage.
**Impact if false:** The continuation pathway for the service navigation problem needs to be re-identified.
**Evidence log ID:** E-011
**Status:** [x] Verified 2026-03-18 — **CLAIM IS VERIFIED (with spelling correction).** Name is **Pete Breil** (not Briel). Title: Director of Citizen Service & Response, City of Richmond, Virginia. Email: peter.breil@rva.gov. LinkedIn: linkedin.com/in/petebreil/. Confirmed as Richmond's first Director of this department (appointed 2018 by Mayor Stoney). Presented RVA311 update to City Council on Feb 26, 2025. Strong candidate as post-hackathon champion.
