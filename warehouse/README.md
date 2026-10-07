# Data warehouse gap closure

This folder holds the records of the data warehouse work for the migration: tests, comparisons, promotions and new sources. The dbt models and the Dagster jobs stay in the ETL repository. You do not need access to the ETL repository to read these records.

The findings report on Mon 2 Nov 2026 confirms the scope of this work.

| Record | Issue | Due date |
|---|---|---|
| UAT tests of the ATOZ trial balance mart against the Finacle GL for 30 Sep 2026 | [#41](https://github.com/GwamakaCharles/pbi-migration/issues/41) | Fri 23 Oct 2026 |
| Promotion of the ATOZ trial balance mart to production | [#44](https://github.com/GwamakaCharles/pbi-migration/issues/44) | Mon 26 Oct 2026 |
| GL balances mart: comparison with the trial balance mart | [#53](https://github.com/GwamakaCharles/pbi-migration/issues/53) | Fri 30 Oct 2026 |
| Promotion of the Loan Arrears EWI mart to production | [#57](https://github.com/GwamakaCharles/pbi-migration/issues/57) | Wed 4 Nov 2026 |
| Data quality tests, freshness checks and failure alerts | [#60](https://github.com/GwamakaCharles/pbi-migration/issues/60) | Fri 6 Nov 2026 |
| Data Upload Portal templates for manual Finance inputs | [#65](https://github.com/GwamakaCharles/pbi-migration/issues/65) | Wed 11 Nov 2026 |
| Payment gateway (HDPAY) and USSD data | [#75](https://github.com/GwamakaCharles/pbi-migration/issues/75) | Wed 18 Nov 2026 |
| WhatsApp, internet banking and ATM data | [#82](https://github.com/GwamakaCharles/pbi-migration/issues/82) | Tue 24 Nov 2026 |
| Sybrin cheques and agency data | [#84](https://github.com/GwamakaCharles/pbi-migration/issues/84) | Thu 26 Nov 2026 |
| New sources for the Wave 4 units | [#85](https://github.com/GwamakaCharles/pbi-migration/issues/85) | Fri 27 Nov 2026 |
| Check after year-end: 31 Dec 2026 loads and trial balance | [#107](https://github.com/GwamakaCharles/pbi-migration/issues/107) | Fri 8 Jan 2027 |

USSD means Unstructured Supplementary Service Data. ATM means Automated Teller Machine.
