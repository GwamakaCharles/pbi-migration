# Inventory

This folder holds the inventory files of discovery (Phase 0).

| File | Contents | Issues |
|---|---|---|
| [`reporting-tools-inventory.csv`](reporting-tools-inventory.csv) | The Reporting Tools Inventory. One row for each tool, unit and entity. | [#14](https://github.com/GwamakaCharles/pbi-migration/issues/14), [#17](https://github.com/GwamakaCharles/pbi-migration/issues/17), [#19](https://github.com/GwamakaCharles/pbi-migration/issues/19), [#25](https://github.com/GwamakaCharles/pbi-migration/issues/25), [#28](https://github.com/GwamakaCharles/pbi-migration/issues/28) |
| [`reports-catalogue.csv`](reports-catalogue.csv) | The Reports Catalogue. One row for each report and entity. | [#13](https://github.com/GwamakaCharles/pbi-migration/issues/13), [#16](https://github.com/GwamakaCharles/pbi-migration/issues/16), [#19](https://github.com/GwamakaCharles/pbi-migration/issues/19), [#21](https://github.com/GwamakaCharles/pbi-migration/issues/21), [#25](https://github.com/GwamakaCharles/pbi-migration/issues/25), [#27](https://github.com/GwamakaCharles/pbi-migration/issues/27), [#28](https://github.com/GwamakaCharles/pbi-migration/issues/28), [#31](https://github.com/GwamakaCharles/pbi-migration/issues/31) |
| [`warehouse-marts.md`](warehouse-marts.md) | The list of the live marts in the data warehouse. | [#12](https://github.com/GwamakaCharles/pbi-migration/issues/12) |
| [`source-to-staging.md`](source-to-staging.md) | The map of staging tables to source systems, and the gaps. | [#15](https://github.com/GwamakaCharles/pbi-migration/issues/15), [#27](https://github.com/GwamakaCharles/pbi-migration/issues/27) |
| [`robotics-input-map.md`](robotics-input-map.md) | The map of each robotics input to a data warehouse table. | [#20](https://github.com/GwamakaCharles/pbi-migration/issues/20) |
| [`open-items.md`](open-items.md) | The open items with owners at the end of discovery. | [#28](https://github.com/GwamakaCharles/pbi-migration/issues/28) |

Put other discovery exports here (for example the Qlik export from [#17](https://github.com/GwamakaCharles/pbi-migration/issues/17)). Do not put customer data, passwords or keys here.

## Rules

- Use only figures from the owner team or from IT. Do not estimate user counts or report names.
- Write "To confirm" for each value that is not known.
- Keep the column names below. Keep values in a field with more than one value separated by `;`.

## Reporting Tools Inventory columns

| Column | Values |
|---|---|
| Tool | The tool name. Use "To confirm" in the name if it is not known. |
| Unit | Finance, Risk, Internal Audit, IT / Data, Credit, Channels, Treasury, Compliance, Other (to confirm) |
| Entity | Exim Bank Tanzania, Exim Uganda, Exim Djibouti, Exim Comoros |
| Owner | The business owner of the tool in the unit. |
| Users | The number of users or the user groups. |
| Hosting | On-premises, Vendor cloud / SaaS, Desktop, To confirm |
| Status | In use – under review, Target platform, To be retired, Retired, To confirm |
| Contact | The person who gave the information. |
| Notes | Functions that Power BI cannot do and other notes. |

## Reports Catalogue columns

| Column | Values |
|---|---|
| Report | The report name that the unit uses. |
| Unit | Same values as the inventory. |
| Entity | Same values as the inventory. |
| Tool | The tool name from the inventory. |
| Frequency | Daily, Weekly, Monthly, Quarterly, Semi-annual, Annual, Ad hoc, To confirm |
| Audience | Who gets the report (for example management, unit head, Asset and Liability Committee). |
| Regulatory/Board | Yes if the report goes to a regulator, the Board or a Board committee. Else No. |
| Data sources | Finacle, LMS, Cards, Payment gateway (HDPAY), USSD, WhatsApp, Internet banking, ATM, Sybrin, Agency, HR, Manual Excel, Data Upload Portal, Data warehouse, Other, To confirm |
| Production method | Automated, Manual, Hybrid |
| Warehouse coverage | Covered, Partial, Gap, Unknown |
| Known discrepancies | Differences against other reports and the possible cause. |
| Target Power BI report | The target Power BI report or app page, or "Retire" or "Not migrated". |
| Certified semantic model | Finance, Loans & Risk, Customers & Channels, Internal Audit, None yet |
| Migration wave | Wave 1 Finance, Wave 2 Risk, Wave 3 Internal Audit, Wave 4 Other units, Subsidiaries, Not migrated, To confirm |
| Action | Rebuild, Merge, Retire, To confirm |
| Effort | S, M, L, To confirm |
| Owner | The business owner of the report. |
| Status | Not assessed, Assessed, In design, In build, In UAT, Parallel run, Live on Power BI, Retired, Not migrated |
| Notes | Other notes. |

Replace the placeholder rows ("list to confirm") with one row for each real report. Then remove the placeholder rows.
