# Logistics & Consignment Dispatch Analytics Dashboard

An end-to-end Microsoft Power BI operational dashboard developed to analyze freight billing, vehicle loading efficiency, and route realization across regional transport hubs.

---

## 📌 Business Overview
Freight and logistics operations frequently manage fragmented consignments where multiple customer invoices map to single Lorry Receipts (LRs). This report provides operational visibility into daily dispatch spikes, route tariff margins, and packing consolidation.

---

## 🛠️ Tech Stack & Skills
- **Tool:** Microsoft Power BI Desktop
- **Data Prep & ETL:** Power Query (type transformation, schema standardization)
- **Calculations:** DAX (Data Analysis Expressions)
- **Data Modeling:** Dimensional modeling principles

---

## 📊 Key Measures & DAX Logic
- **Total Freight Value:** `SUM(Table[VALUE])`
- **Total Freight Weight (Tonnage):** `SUM(Table[Total weight])`
- **Distinct Invoices & LRs:** `DISTINCTCOUNT(Table[Invoice No.])` & `DISTINCTCOUNT(Table[LR No])`

Consolidation Density:

Code snippet
Invoices per LR = DIVIDE([Total Invoices], [Total LRs], 0)
Weight per Case = DIVIDE([Total Weight], [Total Cases], 0)

🚀 Dashboard Pages & Features
Logistics & Revenue Overview:

Executive KPI summary cards (Value, Weight, Case counts, Active LRs).

Town-wise revenue and volume distribution.

Interactive date range slicers and top customer billing breakdowns.

Consignment & Route Deep Dive:

Realized freight rate per KG vs. contractual tariffs by town.

Consolidation efficiency across dispatch dates.

Searchable LR-to-Invoice audit grid for quick operations reconciliation.

📁 Repository Contents
Logistics_Analytics.pbix - Complete interactive Power BI report file.

Logistics_Analytics.pdf - High-resolution export of the multi-page report canvas.


- **Route Realization:**
  ```dax
  Effective Rate per KG = DIVIDE([Total Value], [Total Weight], 0)
