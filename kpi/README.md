# KPI Dictionary

KPI means Key Performance Indicator. [`kpi-dictionary.csv`](kpi-dictionary.csv) has one row for each KPI. Each KPI has one agreed definition, one owner and one certified source. Reports must use the certified measure, not a local calculation.

| Step | Issue | Due date |
|---|---|---|
| Add each Finance, Risk and Internal Audit metric with Status Draft | [#39](https://github.com/GwamakaCharles/pbi-migration/issues/39) | Tue 27 Oct 2026 |
| Propose one definition for each Wave 1–3 KPI | [#43](https://github.com/GwamakaCharles/pbi-migration/issues/43) | Wed 28 Oct 2026 |
| Agree the Finance KPIs with Kelvin R. Rugashumba | [#46](https://github.com/GwamakaCharles/pbi-migration/issues/46) | Thu 29 Oct 2026 |
| Agree the Risk and Internal Audit KPIs with Colman S. Riwa and Salha A. Othman | [#48](https://github.com/GwamakaCharles/pbi-migration/issues/48) | Thu 29 Oct 2026 |
| Record the sign-offs and set Status Agreed | [#52](https://github.com/GwamakaCharles/pbi-migration/issues/52) | Fri 30 Oct 2026 |
| Define the parallel-run tolerances and the sign-off template (put them in this folder) | [#56](https://github.com/GwamakaCharles/pbi-migration/issues/56) | Tue 3 Nov 2026 |

## Columns

| Column | Contents |
|---|---|
| KPI | The business name of the KPI. |
| Definition | The definition that the owner agrees, in plain words. |
| Formula | The calculation, with filters, exclusions, signs and currency. |
| Grain | The level and time (for example "per account per day"). |
| Source mart | The data warehouse table (for example `fact_loan_daily_balance`). |
| Certified semantic model / measure | The Power BI model and measure name. |
| Owner | The business owner who signs the definition. |
| Refresh | Daily, Weekly, Monthly, On demand |
| Used in reports | The report names from the Reports Catalogue, separated by `;`. |
| Status | Draft, Under review, Agreed, Retired |
| Agreed date | The sign-off date (YYYY-MM-DD). |
| Notes | The old definitions from discovery and how the owner resolved them. |

## Rules

- A KPI goes to Status Agreed only with the recorded sign-off of its owner.
- A change to an agreed definition must use the change control process in the certified semantic model standard ([`../platform/`](../platform/)). Record the date and the reason.
- If two units used different definitions, keep the old definitions in Notes. Write which reports changed.
- The rows in the CSV file are examples only. Nobody agreed these definitions yet.
