# Power BI migration: project documents

This repository holds the plan and the documents of the Exim Bank Tanzania project to review the reporting tools and move reports to Power BI on the data warehouse.

- Project board: [Project 6 – Exim Reporting & Power BI Migration](https://github.com/users/GwamakaCharles/projects/6)
- Issues: [all plan issues](https://github.com/GwamakaCharles/pbi-migration/issues?q=label%3Apbi-migration)
- Milestones: [PBI-0 to PBI-9](https://github.com/GwamakaCharles/pbi-migration/milestones)
- Old ETL issue numbers: [`issue-number-map.md`](issue-number-map.md)
- Owner: Gwamaka C. Mwamwaja

Each issue on the board has an **Output** section. That section links to a file or a folder here, on the `main` branch.

## Layout

| Path | Contents |
|---|---|
| [`charter.md`](charter.md) | The project charter: purpose, scope, governance and timeline. |
| [`raid.md`](raid.md) | The RAID log: risks, assumptions, issues and decisions. |
| [`inventory/`](inventory/) | The Reporting Tools Inventory and the Reports Catalogue (CSV files), the mart list, the source-to-staging map, the robotics input map and the open items. |
| [`findings/`](findings/) | The findings report, the root-cause notes, the CFO presentation and the post-migration report. |
| [`kpi/`](kpi/) | The KPI Dictionary (CSV file), the parallel-run tolerances and the sign-off template. |
| [`platform/`](platform/) | Power BI platform records: grants, data gateway, workspaces, pipeline, RLS matrix, standards, tenant settings and the runbook. |
| [`warehouse/`](warehouse/) | Records of the data warehouse gap closure: tests, comparisons, promotions and new sources. The dbt and Dagster code stays in the ETL repository. |
| [`waves/`](waves/) | One folder for each migration wave: `finance/`, `risk/`, `internal-audit/`, `other-units/` and `subsidiaries/`. |
| [`meetings/`](meetings/) | The interview guide, the meeting notes template and the session notes. |

## Rules

1. Keep one term for one thing. Use the names in the KPI Dictionary and the Reports Catalogue.
2. Write "To confirm" for each value that is not known. Do not guess.
3. Do not put passwords, keys, tokens or customer data in this repository.
4. Do not put sample outputs with customer data in the repository.
5. Record each defect as an issue in this repository with the labels `pbi-migration` and `defect`. Add the issue to Project 6.
6. Record each decision in [`raid.md`](raid.md).
7. Change files on a branch and merge them to `main` through a pull request.

## Abbreviations

| Abbreviation | Meaning |
|---|---|
| CFO | Chief Financial Officer |
| CTO | Chief Technology Officer |
| EWI | Early Warning Indicator |
| GL | General Ledger |
| IA | Internal Audit |
| KPI | Key Performance Indicator |
| RAID | Risks, Assumptions, Issues and Decisions |
| RLS | Row-Level Security |
| TB | Trial Balance |
| UAT | User Acceptance Test |
