# SaaS Subscription Business Requirements & Process Mapping

**Business Analyst portfolio project — Adham AlHers**
[Portfolio home](#) · [LinkedIn](https://www.linkedin.com/in/adhamalhers/)

## Problem statement
A SaaS company (CloudSuite, fictional for this exercise) wants to launch a new self-serve tiered pricing plan and needs a BA to define requirements, map the new billing process, and flag risks before development starts.

## Business context
Ireland is home to major SaaS EMEA HQs — this kind of pricing/process BA work (defining requirements for a billing change, coordinating Product/Engineering/Finance/Support) is a common junior-to-mid BA task at companies with an Irish presence.

## Why this project has no dataset
This is the point. A Data Analyst portfolio proves you can find a story in data. A Business Analyst portfolio needs to prove something different: that you can operate from stakeholder conversations, ambiguity, and process alone — before there's any data to analyze. This project is built entirely from requirements-gathering and process-design artifacts, deliberately mirroring what a BA actually delivers before engineering writes a single line of code.

## Tools
Word/docx for the BRD and user stories · Excel for the RACI matrix and risk log · Python (matplotlib) for the process swimlane diagrams, standing in for Miro/Lucidchart.

## Repository structure
```
├── docs/
│   ├── BRD_SaaS_Pricing.docx/.pdf     # Business Requirements Document
│   └── user_stories.docx/.pdf         # 7 user stories with acceptance criteria
├── excel/
│   └── RACI_Risk_Log.xlsx             # RACI matrix + 7-item risk log, both formatted
└── diagrams/
    ├── process_current_state.png      # Current manual, multi-day plan-change process
    └── process_future_state.png       # Future self-serve, instant process
```

## Step-by-step approach
1. **BRD first** — `docs/BRD_SaaS_Pricing.docx` defines stakeholders, current-state pain points, the proposed 3-tier pricing structure (Starter/Growth/Scale), explicit in-scope/out-of-scope boundaries, and success metrics — all before any process or engineering design work.
2. **User stories** — `docs/user_stories.docx` translates the BRD into 7 engineering-ready stories in standard format, each with concrete, testable acceptance criteria (not vague — e.g. "unlocked within 60 seconds of confirmation").
3. **Process maps** — `![Current state process map](./diagrams/process_current_state.png)` and `![Future state process map](./diagrams/process_future_state.png)` are swimlane diagrams (Customer / Sales-Support / Finance / Billing System) showing exactly how the process changes and where the current bottleneck sits.
4. **RACI matrix** — `excel/RACI_Risk_Log.xlsx` (sheet 1) assigns Responsible/Accountable/Consulted/Informed across 10 rollout tasks and 6 roles (Product, Engineering, Finance, Support, Sales, BA).
5. **Risk log** — same workbook (sheet 2), 7 identified risks with likelihood, impact, mitigation, and owner — including the proration edge cases and EUR/GBP/USD currency handling risks named in the project brief.

## Key insight
The single highest-leverage requirements-gathering decision in this project wasn't a number — it was resolving an ambiguity before any design work started: should existing annual customers be **auto-migrated** to the new tiers, or **given an explicit choice** with advance notice? The BRD and user stories commit to the latter (30-day notice + customer choice, see US-06), directly because Sales flagged churn risk at renewal as their top concern in stakeholder discussions (Section 2 of the BRD). That single resolved ambiguity shapes 3 of the 7 user stories and 2 of the 7 logged risks.

## Recommendation
Proceed to engineering discovery using the BRD and user stories as the baseline scope, with the two "Assumptions" in BRD Section 8 (payment provider proration API support, Finance system feed compatibility) resolved as the first two technical-discovery questions — both are launch-date-blocking dependencies owned outside this BA's direct control.

## Business impact
Signals BA maturity beyond spreadsheets: requirements-gathering, cross-functional coordination (Product/Engineering/Finance/Support/Sales), and producing artifacts a real engineering team could start building from directly.

---
*Company and product name (CloudSuite) are fictional, created for this portfolio exercise. All artifacts (BRD, user stories, RACI matrix, risk log, process maps) are original work product, not templates.*
