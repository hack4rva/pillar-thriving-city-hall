# Post-Event Research Index — A Thriving City Hall

**Pillar:** A Thriving City Hall
**GitHub:** [hack4rva/pillar-thriving-city-hall](https://github.com/hack4rva/pillar-thriving-city-hall)
**Problem Statements:**
- PS1: Resident Service Navigation — Help residents find the right City service or department quickly
- PS2: Procurement Risk & Opportunity Review — Help City staff identify valid, compliant contracts

**For AI agents:** Read this file to locate any post-event research artifact. Do not list the directory.

---

## Shared Research (Cross-Demo, Per Problem Statement)

| Dir | JTBD | Pain Points | Prior Art |
|-----|:----:|:-----------:|:---------:|
| [`_shared-service-navigation/`](_shared-service-navigation/) | ✅ | ✅ | ✅ |
| [`_shared-procurement/`](_shared-procurement/) | ✅ | ✅ | ✅ |

These files synthesize the problem statement across all demos in that PS. Read them before reading any per-project file.

---

## Per-Project Research Inventory

| Project | Problem Statement | JTBD | Pain | Prior Art | Solution Ideas |
|---------|------------------|:----:|:----:|:---------:|:--------------:|
| [`civicpulse-ai/`](civicpulse-ai/) | PS2: Procurement | ✅ | ✅ | ✅ | ✅ |
| [`hey804/`](hey804/) | PS1: Service Navigation | ✅ | ✅ | ✅ | ✅ |
| [`mira/`](mira/) | PS2: Procurement | ✅ | ✅ | ✅ | ✅ |
| [`rva-contract-lens/`](rva-contract-lens/) | PS2: Procurement | ✅ | ✅ | ✅ | ✅ |
| [`rva-help/`](rva-help/) | PS1: Service Navigation | ✅ | ✅ | ✅ | ✅ |
| [`text-311/`](text-311/) | PS1: Service Navigation | ✅ | ✅ | ✅ | ✅ |
| [`vendor-contract-mgmt/`](vendor-contract-mgmt/) | PS2: Procurement | ✅ | ✅ | ✅ | ✅ |
| [`city-activity-transparency-system/`](city-activity-transparency-system/) | PS2: Procurement | — | — | — | ✅ |

**Note:** `city-activity-transparency-system` is a post-event idea (not a hackathon demo); it has only solution ideas.

---

## Research Answers (`_research-answers/`)

Parallel AI queries that answered the JTBD open questions. Read `QUERY_MAP.md` to see which file answers which question.

| File | Problem Statement | Questions Answered |
|------|------------------|-------------------|
| [`QUERY_MAP.md`](_research-answers/QUERY_MAP.md) | Both | Full map of JTBD questions → query files |
| [`sn_q1_system_data.md`](_research-answers/sn_q1_system_data.md) | PS1 | 311 platform, API, taxonomy, Socrata data, misroute rate, hours, chatbot |
| [`sn_q2_usage_equity.md`](_research-answers/sn_q2_usage_equity.md) | PS1 | User research, phone/app/web split, smartphone access, languages, equity |
| [`sn_q3_prior_art.md`](_research-answers/sn_q3_prior_art.md) | PS1 | Third-party API access, existing chatbots, comparable cities |
| [`proc_q1_system_data.md`](_research-answers/proc_q1_system_data.md) | PS2 | Contract mgmt system, storage, Socrata data, VITA API, vendor portal |
| [`proc_q2_staffing_equity.md`](_research-answers/proc_q2_staffing_equity.md) | PS2 | Procurement staff count, verification time, equity, turnover |
| [`proc_q3_prior_art.md`](_research-answers/proc_q3_prior_art.md) | PS2 | AI procurement tools, prior modernization attempts |

---

## Agent Reading Sequence

```
1. Read this file (INDEX.md) — orient
2. For PS1 context: _shared-service-navigation/jtbd_analysis.md
3. For PS2 context: _shared-procurement/jtbd_analysis.md
4. For a specific project: <project>/jtbd_analysis.md → <project>/pain_points.md
5. For answered research questions: _research-answers/QUERY_MAP.md → relevant query file
```
