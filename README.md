#  Product Master Data Quality Audit
### A Master Data Management (MDM) Project | Manufacturing Domain

---

##  Project Overview

This project simulates a **real-world Master Data Quality Audit** for a manufacturing company's product catalog — the kind of work done daily in MDM roles at companies like Schneider Electric, Siemens, ABB, and Honeywell.

The dataset contains **100 product records** across categories like Sensors, Drives, Electrical, Pumps, and Controllers. Approximately 30% of records contain intentional data quality issues — mirroring what analysts find in live ERP/PIM systems.

---

##  Business Problem

Poor product master data leads to:
- ❌ Revenue loss from incorrect pricing
- ❌ Order failures due to blocked or duplicate products
- ❌ Reporting errors from missing or inconsistent fields
- ❌ Customer dissatisfaction from wrong product information

This audit identifies, categorizes, and prioritizes data issues — and recommends corrective actions.

---

## What's Inside

| File | Description |
|------|-------------|
| `MDM_Product_Data_Quality_Audit.xlsx` | Full audit workbook with 3 sheets |

### Sheet 1 — Raw Data
100 product records with fields:
`Product_ID | Product_Name | Category | Status | Price | Discount% | Created_Date | Last_Modified | Completeness_Score`

Colour coded:
-  **Green** = Clean records
-  **Yellow** = Warnings (duplicates, missing fields, format issues)
-  **Red** = Critical errors (negative prices, invalid values)

### Sheet 2 — Data Quality Audit
Every issue logged with:
- **Issue Type** — what kind of error it is
- **Severity** — Critical / High / Medium / Low
- **Description** — what the problem means for the business
- **Recommended Action** — how to fix it

### Sheet 3 — Summary Dashboard
- Overall Data Quality Score
- Issue breakdown by type and severity
- 6 key governance recommendations

---

##  Issues Found & Categorized

| Issue Type | Count | Severity |
|---|---|---|
| Missing Product Name | 8 | High |
| Duplicate Record | 6 | Medium |
| Invalid Price (0 or negative) | 6 | Critical / High |
| Wrong Date Format | 4 | Medium |
| Future Created Date | 3 | High |
| Invalid Discount (>100% or negative) | 3 | Critical / High |
| Text in Price Field | 3 | High |
| Invalid Status Value | 3 | High |
| Last Modified Before Created | 3 | High |
| Missing Last Modified Date | 3 | Low |
| Missing Category | 1 | Medium |

**Overall Data Quality Score: 70%** *(target: ≥ 80%)*

---

## 🛠️ Tools Used

- **Microsoft Excel** — Data audit, issue flagging, dashboard
- **Data Governance concepts** — Completeness, validity, consistency, uniqueness
- **MDM domain knowledge** — Product lifecycle, status management, pricing rules

---

##  Key Recommendations

1. Fix all **Critical issues** immediately — negative prices and discounts >100% directly impact revenue
2. Enforce **unique key constraints** on Product Name to prevent duplicates
3. Standardise all dates to **ISO 8601 format** (YYYY-MM-DD) at source system level
4. Make **Product Name and Category mandatory fields** with system-level validation
5. Restrict **Status values** to only Active/Blocked through dropdown validation
6. Run this audit **monthly** as part of ongoing data governance

---

## 👩‍💼 About This Project

I'm Yashika, a Master Data Analyst with experience in **SAP MM/SD, Stibo PIM, and Salesforce (BFO)** — working on product data lifecycle management in a B2B manufacturing environment.

This project is based on the types of data quality issues I encounter in real MDM work — translated into a shareable, anonymized format.

📧 Connect with me on [LinkedIn](https://www.linkedin.com/in/yashikadudeja22/)

---

*Built as part of my Data Analytics portfolio | 2026*
