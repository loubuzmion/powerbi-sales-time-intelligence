# powerbi-sales-time-intelligence
# 📈 Power BI Sales & Time Intelligence Analysis

An exploratory retail sales analytics project built in Power BI, featuring a custom relational Date table, advanced DAX time intelligence measures, and multi-year trend forecasting (2015–2018).

---

## 👥 Project Context & My Contribution
This was a collaborative 3-person team project analyzing a multi-year retail transaction dataset (`MissionXLouExcelFile.xlsx`)[cite: 13, 14]. 

* **My Role & Contributions:** I independently designed and executed the **Time Intelligence Analysis** component of the project. This included building the relational Date dimension, writing advanced DAX time intelligence calculations (`TOTALYTD`, `SAMEPERIODLASTYEAR`, `PREVIOUSMONTH`), structuring monthly/yearly performance dashboards, and presenting key operational recommendations.

---

## 🗄️ Data Model & Relational Architecture
To enable time intelligence calculations in Power BI, raw transactional data must connect to a continuous calendar dimension:
1. **Custom Date Table Creation (DAX):** 
   ```dax
   Date = CALENDAR(MIN(Sales[InvoiceDate]), MAX(Sales[InvoiceDate]))
