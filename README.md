# Nykaa Marketing Campaign Performance Comparison Dashboard

An interactive executive dashboard built in **Microsoft Excel** using **Power Query**, **Power Pivot (DAX)**, and **Dynamic Pivot Charts** to evaluate marketing ROI, customer acquisition costs (CPA), and channel mix efficiency.

## 📌 Business Problem
Digital campaigns often span multiple platforms simultaneously (e.g., Instagram, YouTube, and WhatsApp in a single campaign). Simply splitting rows per platform inflates spend and revenue totals, while averaging pre-calculated percentages distorts overall KPIs. 

This project solves both challenges by modeling **Single vs. Multi-Channel Strategy** performance alongside weighted DAX aggregations.

## 🛠️ Tools & Advanced Excel Techniques
* **Power Query (ETL & Feature Engineering):**
  * Standardized currency and integer data types and created calculated columns (`Net_Profit`, `Daily_Spend`).
  * Engineered a custom `Channel_Mix` dimension using `List.Count(Text.Split([Channel_Used], ","))` to categorize campaigns into **Single Channel**, **Multi-Channel (2 Channels)**, and **Multi-Channel (3 Channels)** with zero double-counting.
* **Power Pivot & DAX Modeling:**
  * Loaded cleaned data directly into the Excel Data Model (`Only Create Connection`) to optimize workbook performance.
  * Wrote weighted DAX measures (`Total Spend`, `Total Revenue`, `Weighted CPA`, `Overall ROI %`, `ROAS`) to ensure accurate totals across all filter states.
* **Dashboard Design & Interactivity:**
  * **5 Dynamic KPI Cards:** Linked directly to Data Model measures for real-time executive tracking.
  * **Dual-Axis Combo Charts:** Contrasted high-volume Revenue/ROI metrics against Spend/CPA baselines on secondary axes.
  * **Conditional Formatting Heatmap:** Cross-tabulated `Customer Segment` × `Channel Mix` ROI % to highlight high-converting audience combinations.
  * **Synchronized Slicers:** Connected `Campaign Type`, `Customer Segment`, and `Channel Mix` slicers across all underlying Pivot Tables.

## 📈 Key Findings
1. **Multi-Channel Efficiency:** Multi-Channel (3 Channels) campaigns outperformed Single-Channel campaigns in both overall ROI and lower Weighted CPA.
2. **Top-Performing Channels:** **Social Media** and **Influencer** campaigns delivered the highest Return on Ad Spend (**ROAS > 1,400**).
3. **Audience Sweet Spot:** **Working Women** engaging with **2-Channel** campaigns generated the highest segment-level ROI (**155,617%**).
