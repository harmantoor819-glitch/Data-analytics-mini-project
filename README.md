# Food Delivery Business Analytics and Performance Optimization System
**Business Analytics Mini Project | Academic Year 2025–2026**

![Project Status](https://img.shields.io/badge/Project_Status-Clean_&_Production_Ready-success)
![Technology](https://img.shields.io/badge/Core_Trio-Excel_|_Python_|_HTML5_Dashboard-blue)
![Analytics](https://img.shields.io/badge/Analytics-Descriptive_|_Diagnostic_|_Predictive_|_Prescriptive-orange)

An end-to-end, intermediate-level Business Analytics system evaluating **2,000 multi-city food delivery orders** across 5 metropolitan hubs (Bangalore, Mumbai, Delhi NCR, Hyderabad, Pune). 

The system operates on a clean, streamlined **Core Trio architecture**:
1. 📊 **Microsoft Excel Dashboard:** Deep spreadsheet modeling, dynamic logical formulas (`IF`, `AND`, `OR`, `VLOOKUP`), and statistical IQR outlier calculation.
2. 🐍 **Python Analytics Engine:** Preprocessing, statistical computing, correlation diagnostics ($r = -0.424$), 3-Month Moving Average Demand Forecast, and publication charts.
3. ⚡ **Interactive Web Dashboard (`dashboard.html`):** Standalone zero-setup UI with real-time filters, animations, and Chart.js visualizations that opens with a single double-click.

---

## 📁 Clean Project Architecture

```
Food_Delivery_Analytics/
├── data/
│   ├── raw_food_orders.csv            <- Raw operational dataset (2,008 rows with duplicates & noise)
│   ├── cleaned_food_orders.csv        <- Cleaned primary dataset (2,000 verified rows)
│   ├── food_orders.csv                <- Primary dataset mirror
│   ├── customers.csv                  <- Customer Master (300 records with loyalty tiers & demographics)
│   ├── restaurants.csv                <- Restaurant Master (20 partner brands with commission rates)
│   ├── delivery_partners.csv          <- Delivery Partner Master (30 riders with vehicles & ratings)
│   └── order_items.csv                <- Granular Order Item breakdown (3,994 line items)
├── excel/
│   └── food_delivery_analysis.xlsx    <- Full Excel workbook (Executive Dashboard, IQR stats, Pivots & formulas)
├── output/
│   ├── charts/
│   │   ├── monthly_order_trend.png               <- Monthly orders & revenue trend
│   │   ├── city_performance_comparison.png       <- City-wise revenue benchmark
│   │   ├── delivery_time_outliers_boxplot.png     <- IQR outlier detection boxplot
│   │   ├── customer_rating_distribution.png      <- Customer review breakdown
│   │   ├── rating_vs_delay_diagnostic.png        <- Speed bracket vs rating degradation
│   │   └── peak_hour_demand_heatmap.png          <- Hourly demand heatmap across days of week
│   ├── summary_kpis.json             <- Machine-readable executive KPI dictionary
│   ├── descriptive_stats.csv         <- Formatted statistical measures & IQR thresholds
│   └── business_recommendations.txt  <- 6 actionable prescriptive strategies
├── scripts/
│   ├── generate_data.py               <- Reproducible dataset generator
│   ├── build_excel_workbook.py        <- Automated openpyxl workbook builder
│   └── build_web_dashboard.py         <- Standalone animated HTML dashboard compiler
├── analysis.py                        <- Python analytics pipeline (Descriptive, Diagnostic, Predictive, Prescriptive)
├── dashboard.html                     <- Standalone Interactive Web Dashboard (Zero setup, double-click to run)
├── PROJECT_REPORT.md                  <- Academic Project Report
├── VIVA_QUESTIONS.md                  <- 25+ Viva Voce questions & model answers
└── README.md                          <- Project overview & execution guide
```

---

## 🚀 How to Run the Working Trio

### 1. View the Interactive Dashboard (Zero Commands Needed) 🌟
1. Open the folder: `C:\Users\anshu\Desktop\Food_Delivery_Analytics`
2. **Double-click `dashboard.html`** in your file explorer.
3. It opens immediately in Chrome or Edge with:
   - **4 Core Tabs:** Executive Dashboard, Diagnostic Analytics, Predictive Forecast, and Prescriptive Strategy.
   - **Interactive Control Bar:** Live City, Cuisine, and Order Status filters that update all charts and KPIs in real time.
   - **Modern UI/UX:** Clean styling, CSS animations, and zero third-party banners.

### 2. Run the Python Analytics Engine
To re-run the backend statistical computations, calculate correlation metrics, generate the 3-Month Moving Average forecast, and update the PNG chart files in `output/charts/`:
```bash
python analysis.py
```

### 3. Open the Microsoft Excel Workbook
Open [`excel/food_delivery_analysis.xlsx`](file:///c:/Users/anshu/Desktop/Food_Delivery_Analytics/excel/food_delivery_analysis.xlsx) to inspect:
- **`Executive_Dashboard` Sheet:** KPI summary cards, monthly trend chart, and city platform revenue chart.
- **`Cleaned_Orders` Sheet:** 2,000 orders with live formulas demonstrating `IF`, nested `IF`, `AND`, `OR`, `NOT`, `IFERROR`, `VLOOKUP`, and `CONCATENATE`.
- **`Statistical_Analysis` Sheet:** Mean, Median, Mode, Quartiles ($Q_1$, $Q_3$), IQR, and outlier thresholds.
- **`Pivot_Summaries` Sheet:** Multi-dimensional summaries across City, Cuisine, and Customer Loyalty Tiers.

---

## 📊 Core Business Metrics Summary

| Business Metric | Value | Business Definition & Interpretation |
| :--- | :---: | :--- |
| **Total Orders Placed** | **2,000** | Full order volume across the 12-month evaluation period. |
| **Delivered Orders** | **1,881** | Successfully fulfilled orders (**94.05% fulfillment rate**). |
| **Cancelled Orders** | **98** | Order cancellations (**4.90% cancellation rate**). |
| **Gross Merchandise Value (GMV)** | **₹12.41 Lakhs** | Total customer gross spend on food items. |
| **Net Platform Revenue** | **₹2.59 Lakhs** | Platform earnings from commission + delivery fees (**20.90% take rate**). |
| **Average Order Value (AOV)** | **₹620.50** | Mean transaction ticket size. |
| **Average Delivery Time** | **35.16 mins** | Door-to-door delivery latency (Median: **33.80 mins**). |
| **Average Customer Rating** | **3.65 / 5.0** | Overall customer satisfaction score. |
| **Statistical IQR Upper Bound** | **55.90 mins** | Statistical upper bound ($Q_3 + 1.5 \times \text{IQR}$) for normal delivery. |
| **Forecasting Accuracy (MAPE)** | **8.36%** | 3-Month Moving Average Demand Forecast evaluation error. |
