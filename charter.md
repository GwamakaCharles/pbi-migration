# Project charter: reporting tools review and Power BI migration

Version 0.4, 7 Oct 2026. This version removes the licence work, because the bank already pays for the Power BI licences. The platform tickets move earlier.

| Role | Person |
|---|---|
| Project owner and lead | Gwamaka C. Mwamwaja – Data Warehouse and BI Lead |
| Sponsor | Shani B. Kinswaga – Chief Financial Officer (CFO) |
| IT lead | Halfan I. Semindu – IT |
| Group oversight | Thagaran Govender – Group Chief Technology Officer (CTO), Digital |

## 1. Background

On 6–7 Oct 2026 the CFO asked IT to review all tools that the bank uses for analysis and reports. Examples are Qlik in Finance, robotics in Risk and an Internal Audit tool. The name of the Internal Audit tool is not confirmed.

Reports from different units give different results for the same figures. The review must also help to decrease IT costs. Power BI across the bank is one possible solution.

The thread agreed these actions:
- Halfan I. Semindu examines Qlik with Kelvin R. Rugashumba (Finance), robotics with Colman S. Riwa (Risk) and the Internal Audit tool with Salha A. Othman.
- Gwamaka C. Mwamwaja speaks with all stakeholders and presents a report to the CFO.
- Thagaran Govender asked to include the subsidiaries. Gwamaka C. Mwamwaja speaks with Exim Uganda, Exim Djibouti and Exim Comoros.

**Data platform now.** The data warehouse is an on-premises PostgreSQL database with a Kimball star schema. Dagster and dbt load it every day from Finacle and the loan system (LMS). The UAT environment is the UAT server, with branch `main` of the ETL repository. The production environment is the production server, with branch `production`.

The live marts are `dim_customer`, `fact_account_transaction`, `fact_loan_daily_balance`, `fact_loan_portfolio_mpf` and `fact_customer_channel_usage`. The mart `fact_loan_portfolio_mpf` supplies Power BI now. The ATOZ trial balance (TB) mart and the Loan Arrears early warning (EWI) mart are in test. The Data Upload Portal holds controlled manual data. Access to production source systems is read-only.

## 2. Objectives

1. Make a full inventory of tools and reports, with their users.
2. Explain why reports do not agree, and correct the causes.
3. Make the data warehouse the single source, with one agreed definition for each metric in certified Power BI semantic models.
4. Retire the tools that the bank does not need, if Power BI can do their functions.
5. Prepare an approach that the subsidiaries can use again.

## 3. Scope

**In scope**
- Units of Exim Bank Tanzania that make analysis or reports: Finance, Risk, Internal Audit, Credit, Channels, Treasury and Compliance.
- The tool inventory, the reports catalogue, data lineage and the analysis of discrepancies.
- Data warehouse gap closure for in-scope reports.
- Power BI platform, governance and certified semantic models.
- Migration of in-scope reports, parallel run, reconciliation, sign-off and retirement of old tools.
- Discovery with the subsidiaries now. Rollout in Phase 4.

**Out of scope**
- Changes to source systems.
- Write access to production source systems.
- Reports that units decide to retire. The catalogue records them, but nobody rebuilds them.
- Build work for a subsidiary before Group approval.
- Power BI licence work. The bank already pays for the Power BI licences.

## 4. Deliverables

| # | Deliverable | Phase | Location |
|---|---|---|---|
| 1 | Reporting Tools Inventory and Reports Catalogue | 0 | [`inventory/`](inventory/) |
| 2 | Findings report with coverage, gaps and recommendation | 0 | [`findings/`](findings/) |
| 3 | KPI Dictionary with owner sign-off | 1 | [`kpi/`](kpi/) |
| 4 | Power BI platform design and governance standard | 1 | [`platform/`](platform/) |
| 5 | Data warehouse marts for the agreed gaps | 1–2 | [`warehouse/`](warehouse/) |
| 6 | Certified semantic models with RLS | 1–2 | [`waves/`](waves/) |
| 7 | Migrated reports for each wave, with UAT sign-off | 2 | [`waves/`](waves/) |
| 8 | Parallel-run reconciliations, sign-offs and retirement records | 3 | [`waves/`](waves/) |
| 9 | Subsidiary rollout approach and pilot | 4 | [`waves/subsidiaries/`](waves/subsidiaries/) |

## 5. Success measures

- Each in-scope report is live on Power BI from the data warehouse, retired, or marked "Not migrated" with a reason.
- Each KPI has one definition, one owner and one certified source.
- Reports that overlap agree within the tolerances during the parallel run.
- Risk robotics and Internal Audit read from the data warehouse, not from production source systems.
- The users of each wave get instruction before go-live.

## 6. Assumptions

- The units send their written returns by Fri 16 Oct 2026.
- Unit contacts attend the sessions in the week of 19 Oct 2026.
- One person (Gwamaka C. Mwamwaja) does the plan, with a maximum of two or three tickets on one day.
- Power BI is available to the bank. The bank already pays for the Power BI licences.
- IT can give read-only access to more source systems where a gap needs it.
- Unit heads nominate metric owners and UAT testers.
- The subsidiary rollout comes after Tanzania and needs Group approval.

## 7. Risks

The RAID log ([`raid.md`](raid.md)) records the risks and the actions.

## 8. Governance

| Role | Person | Responsibilities |
|---|---|---|
| Sponsor | Shani B. Kinswaga (CFO) | Approves the recommendation, scope and budget. Decides disputes about Finance metrics. |
| Group oversight | Thagaran Govender (Group CTO, Digital) | Group alignment. Approves the subsidiary rollout. |
| IT lead | Halfan I. Semindu | IT coordination, security reviews, procurement and escalation. |
| Project owner | Gwamaka C. Mwamwaja | Plan, backlog, data warehouse and Power BI work, stakeholders and status reports. |
| Unit contacts | Kelvin R. Rugashumba (Finance), Colman S. Riwa (Risk), Salha A. Othman (Internal Audit), others to confirm | Requirements, metric ownership, UAT and sign-off. |
| Subsidiary contacts | Dennis Ssembajjo (Uganda), Dhanunjaya C. Sivalingappa (Djibouti), Karim Bacari (Comoros) | Discovery input and local rollout. |

Sprints are one week, Monday to Friday. Sprint 1 is Wed 7 – Fri 9 Oct 2026. The sponsor gets a status update each Friday.

## 9. Timeline

Working days are Monday to Friday. The public holidays in the plan are Wed 14 Oct, Wed 9 Dec, Fri 25 Dec, Sat 26 Dec, Fri 1 Jan and Tue 12 Jan. The year-end freeze is 21 Dec 2026 – 1 Jan 2027.

| Phase | Window | Main outputs |
|---|---|---|
| Phase 0 – Discovery and inventory | Wed 7 – Mon 26 Oct 2026 | Mart list, source map and Power BI inventory from 7 Oct. Rows from the written returns by 16 Oct. Unit sessions: Finance 19 Oct, Risk 20 Oct, Internal Audit 21 Oct, Channels 22 Oct. Subsidiary calls 13–16 Oct. Coverage 23 Oct. Inventory complete 26 Oct. |
| Findings report | Tue 27 Oct – Mon 2 Nov 2026 | Migration plan 27 Oct. Draft 28 Oct. Review with Halfan I. Semindu 29 Oct. Presentation to the CFO Mon 2 Nov. |
| Phase 1 – Platform, governance and KPI core | Mon 19 – Fri 30 Oct 2026 | Certified semantic model standard 19 Oct, read-only role 20 Oct, data gateway 22 Oct, name rules, access model and tenant settings 23 Oct, workspaces 26 Oct, pipeline 27 Oct, RLS 28 Oct, KPI Dictionary core 30 Oct. |
| Phase 2 – Build and migrate by wave | Mon 2 Nov – Fri 11 Dec 2026 | Wave 1 Finance 2–13 Nov. Wave 2 Risk 9–20 Nov. Wave 3 Internal Audit 16–27 Nov. Wave 4 other units 30 Nov – 11 Dec. |
| Phase 3 – Parallel run, sign-off and retirement | Tue 3 Nov – Fri 18 Dec 2026 | Finance parallel run over the Nov close and Qlik decision 4 Dec. Risk sign-off 4 Dec. Internal Audit tool decision 10 Dec. Other units sign-off 14 Dec. Post-migration report 18 Dec. |
| Year-end freeze | 21 Dec 2026 – 1 Jan 2027 | No changes. Check after year-end on Fri 8 Jan 2027. |
| Phase 4 – Subsidiaries | Approach 15 Dec 2026, pilot 11–29 Jan 2027 | Rollout approach and entity design. Pilot live and signed off by Fri 29 Jan 2027. |

### Milestones

| Milestone | Date |
|---|---|
| PBI-0 Discovery and inventory complete | Mon 26 Oct 2026 |
| PBI-1 Findings report presented to the CFO | Mon 2 Nov 2026 |
| PBI-2 Power BI platform, governance and KPI core complete | Fri 30 Oct 2026 |
| PBI-3 Wave 1 Finance build complete | Fri 13 Nov 2026 |
| PBI-4 Wave 2 Risk complete | Fri 20 Nov 2026 |
| PBI-5 Wave 3 Internal Audit complete | Fri 27 Nov 2026 |
| PBI-6 Finance parallel run and Qlik decision | Fri 4 Dec 2026 |
| PBI-7 Wave 4 other units complete | Fri 11 Dec 2026 |
| PBI-8 Sign-off and retirement complete | Fri 18 Dec 2026 |
| PBI-9 Subsidiary pilot complete | Fri 29 Jan 2027 |

The findings report scope decides the data warehouse gap closure tickets. Change or remove those tickets after Mon 2 Nov 2026 if the scope changes.
