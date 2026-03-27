## Chosen Problem
Helping City staff review procurement risks and opportunities with less manual contract reading.

## User
Primary user: procurement analyst or contract review specialist in a City department.
Secondary user: procurement manager who needs fast visibility into expiring or high-risk contracts.

## Why this one
- It maps directly to a scored pillar problem and shows clear public-sector impact in staff efficiency.
- It supports a concrete Sunday demo: upload/select a contract, extract key terms, surface risk tags, and present a review recommendation panel.
- It can be built with currently available materials in this repo: `02_data/source_inventory.csv`, `evidence_log.md`, and `procurement-examples/`.

## Why not the others
- Resident service navigation is strong but depends on current 311 routing context that is harder to validate with public data alone.
- The broad fiscal-transparency concept is compelling but likely too wide for a single weekend unless heavily narrowed.
- Procurement review has the cleanest one-user, one-workflow scope with realistic build boundaries.

## Risks
- **Data quality risk:** contract metadata and document text may disagree; extraction output must be traceable to source text.
- **OCR risk:** scanned PDFs can produce noisy text that breaks date/amount parsing.
- **Adoption risk:** no confirmed departmental champion in this workflow yet.
- **Governance risk:** the tool must remain decision-support only and avoid legal/compliance determinations.

## Initial MVP Boundary
- In scope: expiration-window flagging, missing-field alerts, high-value contract flag, and plain-language contract summary.
- Out of scope: automated award decisions, legal determinations, and claims of official City procurement authority.

