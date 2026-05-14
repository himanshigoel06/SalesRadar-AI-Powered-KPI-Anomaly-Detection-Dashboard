# 📡 SalesRadar — AI-Powered KPI Anomaly Detection Dashboard

A dynamic, interactive Power BI dashboard designed to automatically detect unusual patterns in sales and profit KPIs — and explain their root causes using Power BI's built-in AI intelligence.

---

# 📌 Short Description / Purpose

The SalesRadar Dashboard is a visually rich, 2-page Power BI report that enables business users to monitor KPIs, uncover hidden anomalies, and understand what's driving unusual performance — without manual investigation.

It leverages Power BI's AI-powered Anomaly Detection to automatically flag unexpected spikes and drops in sales and profit, and surfaces root-cause explanations by region, category, and sub-category — helping teams respond faster and make smarter, data-driven decisions.

---

# 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

- 📊 Power BI Desktop — Main data visualization platform used for report creation
- 📂 Power Query — Data transformation and cleaning layer for reshaping raw data
- 🧠 DAX (Data Analysis Expressions) — Used for calculated measures, KPIs, and conditional logic
- 🤖 Power BI AI — Anomaly Detection — Built-in intelligence to automatically detect and explain anomalies
- 📅 Date Intelligence (CALENDARAUTO) — Dynamic date table for time-based analysis
- 📁 File Format — `.pbix` for development and `.png` for dashboard previews

---

# 📂 Data Source

## Source:
Kaggle — Superstore Sales Dataset

A comprehensive retail dataset containing **9,994 rows** of transactional data across **4 years (2014–2017)**, covering:

- Orders
- Sales
- Profit
- Discount
- Quantity

### Customer Segments
- Consumer
- Corporate
- Home Office

### Product Categories
- Furniture
- Technology
- Office Supplies

### Geography
49 US states across 4 regions:
- West
- East
- South
- Central

---

# ✨ Features / Highlights

## 🔴 Business Problem

Sales and operations teams often struggle to manually identify when and why KPIs behave unusually.

Key questions include:

- Which days had unexpectedly high or low sales — and why?
- Which regions or categories are driving profit anomalies?
- Which products are consistently loss-making?

These insights are time-consuming to uncover using raw data alone.

---

## 🎯 Goal of the Dashboard

To deliver an AI-powered BI tool that:

- Automatically detects anomalies in sales and profit trends
- Explains root causes by region, category, and sub-category
- Identifies loss-making products and discount impact on profit
- Enables filtering by year, region, and category for deeper analysis

---

# 📊 Walkthrough of Key Visuals

# 📄 Page 1 — Sales & Anomaly Detection

### KPI Cards (Top)
- Total Profit: **286.40K**
- Total Orders: **5,009**
- Total Sales: **2.30M**
- Profit Margin: **12.47%**

### Interactive Slicers
Filter by:
- Year
- Region
- Category

### Total Sales by Date (Line Chart + AI Anomaly Detection)
- Automatically flags **47 anomalies** across 2014–2017
- Red markers indicate unusual spikes/drops
- Clicking anomalies reveals AI-generated root-cause explanations with confidence scores

### Total Sales by Sub-Category (Bar Chart)
Top 5 sub-categories:
- Phones
- Chairs

### Total Sales by State (Map Visual)
Geographic bubble map showing state-wise sales concentration.

---

# 📄 Page 2 — Profit Analysis

### KPI Cards (Top)
- Total Profit
- Total Orders
- Total Discount: **1.56K**
- Loss Orders: **1,871**

### Total Profit by Region (Bar Chart)
- West region leads at **108K**
- Central region lowest at **40K**

### Discount vs Profit by Sub-Category (Scatter Plot)
Shows relationship between:
- High discounts
- Lower profit margins

### Loss-Making Sub-Categories (Bar Chart)
- Tables: **-17.7K**
- Bookcases: **-3.5K**
- Supplies: **-1.2K**

### Total Profit by Date (Line Chart + AI Anomaly Detection)
AI flags unusual profit spikes and drops with detailed root-cause analysis.

---

# 💡 Business Impact & Insights

## 📈 Anomaly Response
Teams can instantly identify when and why sales spiked.

Example:
> Sales on 11-Nov-2014 were 25% above expected range, driven by Office Supplies in West region (93% AI confidence)

---

## 📉 Loss Prevention
Tables sub-category is losing **-17.7K**, indicating urgent discount strategy review.

---

## 🌍 Regional Strategy
- West & East regions dominate sales and profit
- Central region underperforming

---

## 🏷️ Discount Impact
Sub-categories with high discount levels show significant margin erosion risk.

---

## 📅 Seasonal Planning
Q4 consistently shows sales spikes, confirming holiday season demand patterns.

---

# 🔢 DAX Measures

```DAX
Total Sales = SUM(Superstore[Sales])

Total Profit = SUM(Superstore[Profit])

Total Orders = DISTINCTCOUNT(Superstore[Order ID])

Profit Margin % =
DIVIDE(
    SUM(Superstore[Profit]),
    SUM(Superstore[Sales])
) * 100

Total Discount = SUM(Superstore[Discount])

Loss Orders =
CALCULATE(
    COUNT(Superstore[Order ID]),
    Superstore[Profit] < 0
)
```

---

# 📸 Screenshots

## 📄 Page 1 — Sales & Anomaly Detection

![Sales & Anomaly Detection](https://github.com/himanshigoel06/SalesRadar-AI-Powered-KPI-Anomaly-Detection-Dashboard/blob/main/Sales%26Anamoly%20Detection.png?raw=true)

---

## 📄 Page 2 — Profit Analysis

![Profit Analysis](https://github.com/himanshigoel06/SalesRadar-AI-Powered-KPI-Anomaly-Detection-Dashboard/blob/main/Profit%20Analysis.png?raw=true)

---

## 🤖 AI Anomaly Detection in Action

![AI Anomaly Detection](https://github.com/himanshigoel06/SalesRadar-AI-Powered-KPI-Anomaly-Detection-Dashboard/blob/main/AI%20Anomaly%20Detection%20in%20Action.png?raw=true)

---

## 🔍 AI Root Cause Analysis — 4 Drivers Identified

![AI Root Cause Analysis](https://github.com/himanshigoel06/SalesRadar-AI-Powered-KPI-Anomaly-Detection-Dashboard/blob/main/AI%20Root%20Cause%20Analysis%20%E2%80%94%204%20Drivers%20Identified.png?raw=true)

---

# 📁 Project Files

| File | Description |
|------|-------------|
| `SalesRadar.pbix` | Main Power BI dashboard file |
| `README.md` | Project documentation |
| `screenshots/` | Dashboard preview images |

---

# 👩‍💻 Author

## Himanshi Goel

Senior Analyst | Power BI Enthusiast | Data Analytics Professional

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!
