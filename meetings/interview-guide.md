# Stakeholder Interview Guide

- **Unit or entity:** [ ]
- **Contacts:** [ ]
- **IT attendee:** Halfan I. Semindu, if available
- **Date:** [ ]
- **Time:** 60 minutes (45 minutes for a subsidiary call)
- **Read first:** the written return of the unit and its rows in [`../inventory/`](../inventory/)

## Start (5 minutes)
- The Chief Financial Officer (CFO) asked for a review of the tools for analysis and reports. The aims are figures that agree across reports and a lower IT cost. Power BI on the data warehouse is one possible solution.
- This session confirms what the unit uses and makes. Nobody stops a tool at this stage.
- The output is rows in the Reporting Tools Inventory and the Reports Catalogue. The unit gets a copy to confirm.

## 1. Tools and users (10 minutes)
1. Which tools do you use for analysis and reports (for example Qlik, robotics, Excel, Access)?
2. Who uses each tool? How many people build reports, and how many only read them?
3. Where is the tool (on-premises server, vendor cloud or desktop)?
4. Which functions of the tool must you keep (for example schedules, data entry or audit tests)?

## 2. Reports (15 minutes)
For each report:
1. What is the name of the report?
2. How often do you make it (daily, weekly, monthly, quarterly, annual or on request)?
3. Who gets it, inside and outside the bank?
4. Is it a regulatory return, or a report for the Board or a Board committee?
5. Who owns it, and who makes it?
6. How much time does it take for each cycle?
7. Do you still need it? Can it merge with another report?

## 3. Data sources and method (15 minutes)
For each report:
1. Which sources supply data to it: Finacle, the loan system (LMS), cards, channels, HR, manual Excel or other?
2. How do you get the data: database query, system extract, file from another unit or manual entry?
3. Is the method automated, manual or a mix? Which steps are manual?
4. When do you take the extract (for example end of day or the next morning)?
5. Do you make manual adjustments? Who approves them?
6. Can the data warehouse supply the figures? The data warehouse has customers, accounts and transactions, the loan portfolio and channel usage now. The trial balance and the loan arrears marts are in test.

## 4. Discrepancies and problems (10 minutes)
1. Which of your figures are different from figures from other units? Give examples with dates.
2. What causes the difference (definition, time, source, filters or adjustments)?
3. Which metric definitions do you own or use? Can you be the owner in the KPI Dictionary (Key Performance Indicator)?
4. Which tasks take the most time or cause the most errors now?
5. What must Power BI give you before you can stop the current tool?

## End (5 minutes)
- Confirm the list of tools and reports. Agree who completes each "To confirm" item, and when.
- For Internal Audit: confirm the independence, read-only access and query log requirements.
- For Risk: confirm which robotics inputs can come from data warehouse views.
- For Finance: confirm the Qlik functions that Power BI does not have.
- Tell the next steps: the inventory is complete on Mon 26 Oct 2026, and the CFO gets the findings report on Mon 2 Nov 2026.

## Subsidiary calls (45 minutes)
Use sections 1–4 at a high level: main tools, main reports (with the regulatory reports), the core system and the loan system, and known discrepancies. Also ask about local server location, data residency and local regulations for a later rollout.
