# 🌍 Global Superstore Sales & Profit Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-004E8C?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

> An end-to-end Power BI dashboard that turns the Global Superstore dataset into a single-page, decision-ready view of global sales, profitability, market performance, and shipping efficiency.

---

## 📌 Project Overview

The **Global Superstore Sales & Profit Analysis Dashboard** is an interactive, single-page Power BI report built on the Global Superstore transactional dataset (`Orders` table). It consolidates sales, profit, quantity, and shipping-cost data across countries, markets, regions, product categories, and customer segments into one KPI-driven view.

The dashboard is designed so a business stakeholder — a regional manager, category head, or operations lead — can open the file, apply a slicer, and immediately see where revenue is being generated, where it is profitable, and where operational costs are eating into margins.

---

## ❗ Business Problem

Retail organizations operating across multiple countries and markets often struggle to answer simple but critical questions quickly:

- Which countries and markets actually drive profitable growth, versus just high sales volume?
- Are certain product categories gaining or losing rank month-over-month?
- Is shipping cost disproportionately affecting certain customer segments?
- How does quarterly and yearly performance trend, and where are the inflection points?

Without a consolidated view, these questions require manual, time-consuming cross-referencing of raw transactional data. This dashboard solves that by centralizing sales, profit, quantity, and shipping metrics into a single interactive report.

---

## 🎯 Objectives

- Analyze global sales performance across countries and markets
- Evaluate profitability by market and region
- Monitor year-over-year and quarter-over-quarter growth trends
- Compare performance across customer segments
- Understand the impact of shipping cost on operations
- Identify high-performing and underperforming regions
- Support strategic, data-driven business decisions

---

## 🗂️ Dataset Information

| Attribute | Details |
|---|---|
| **Source Table** | `Orders` |
| **Dataset** | Global Superstore (retail transactional data) |
| **Grain** | Order-level transactions |
| **Key Dimensions** | Country, Region, Market, Category, Segment, Ship Mode, Order Date |
| **Key Measures** | Sales, Profit, Quantity, Shipping Cost |
| **Time Intelligence** | Date Hierarchy (Year → Quarter → Month) |

---

## ⚙️ Dashboard Features

- Single-page, high-density executive dashboard layout
- 4 KPI summary cards for at-a-glance performance monitoring
- 9 distinct chart types chosen to match the analytical question each answers
- 4 cross-filtering slicers for on-the-fly segmentation
- Consistent theming using a custom Power BI theme (dark-gradient accent)
- Fully interactive cross-highlighting between all visuals on the page

---

## 🧮 KPI Cards

| KPI | Description |
|---|---|
| 💰 **Total Sales** | Sum of all order sales revenue across the dataset |
| 📈 **Total Profit** | Sum of profit generated across all orders |
| 🧾 **Total Orders** | Count of distinct orders placed |
| 📦 **Total Quantity** | Total number of units sold |

---

## 📊 Dashboard Visuals

### 1. Sales by Country — Bar Chart
Ranks countries by total sales (`Sum(Sales)` by `Country`), making it easy to instantly spot the highest and lowest revenue-generating countries in the portfolio.

### 2. Monthly Category Sales — Ribbon Chart
Tracks `Sum(Sales)` by `Category` across the **Month** level of the date hierarchy. The ribbon format highlights rank changes between categories month-over-month, showing which category is "winning" at any point in the year.

### 3. Quarterly Sales vs Profit — Line & Clustered Column Combo Chart
Plots `Sum(Sales)` as columns and `Sum(Profit)` as a line, both by **Quarter**. This dual-axis view makes it easy to spot quarters where sales grew but profit didn't follow — a classic margin-compression signal.

### 4. Profit by Market — Funnel Chart
Ranks global `Market` segments by `Sum(Profit)`, visually narrowing from the most to least profitable market, useful for prioritizing where to invest further.

### 5. Category-wise Sales Distribution — Donut Chart
Shows `Sum(Sales)` by `Category` as a percentage of total sales, giving an immediate read on category mix.

### 6. Quantity Sold by Market — Treemap
Displays `Sum(Quantity)` by `Market` as proportionally sized blocks, making relative market size (by volume, not just revenue) easy to compare at a glance.

### 7. Shipping Cost by Customer Segment — Pie Chart
Breaks down `Sum(Shipping Cost)` by customer `Segment` (Consumer, Corporate, Home Office), surfacing which segment is the most expensive to serve logistically.

### 8. Sales & Profit Trend by Year — Line Chart
Plots `Sum(Sales)` and `Sum(Profit)` across the **Year** level of the date hierarchy, giving a clean long-term trend line for year-over-year growth analysis.

### 9. Regional Profit Comparison — Scatter Chart
Compares `Sum(Profit)` across `Region`, allowing quick visual identification of regional profitability outliers — both strong performers and underperformers.

---

## 🎛️ Interactive Filters (Slicers)

| Slicer | Field | Purpose |
|---|---|---|
| 🗓️ Quarter | `Order Date` (Quarter) | Filter the entire page to a specific quarter |
| 🌐 Market | `Market` | Focus analysis on one global market at a time |
| 📍 Region | `Region` | Drill into a specific region's performance |
| 🚚 Ship Mode | `Ship Mode` | Isolate performance by shipping method |

All slicers cross-filter every visual on the page simultaneously, enabling rapid, multi-dimensional "what-if" exploration without writing a single query.

---

## 💡 Business Insights

1. Sales performance varies significantly by country, with a small cluster of top countries contributing a disproportionately large share of total revenue.
2. Not every high-sales market is highly profitable — the Funnel chart reveals markets where profit lags well behind sales volume.
3. Product category rankings shift month-to-month, indicating seasonality in customer purchasing behavior across categories.
4. Certain quarters show sales growth without a corresponding rise in profit, pointing to potential discounting or cost-control issues.
5. Category-wise sales distribution shows an uneven mix, with one or two categories typically dominating overall revenue share.
6. Quantity sold does not always correlate with market size in revenue terms — some markets sell high volume at lower price points.
7. Shipping cost is not evenly distributed across customer segments, with one segment consistently more expensive to fulfill than others.
8. Year-over-year trends reveal whether growth is accelerating, plateauing, or declining, which is critical for forward planning.
9. Regional profit comparison highlights specific regions that consistently underperform relative to peers, warranting operational review.
10. Some regions show high profit despite modest sales volume, suggesting stronger margin discipline or product mix advantages.
11. Quarterly combo-chart analysis helps flag early-warning quarters where profit trends diverge from sales trends.
12. Segment-level shipping cost analysis can directly inform negotiations with logistics providers or shipping-mode policy changes.
13. The dashboard's slicer combination (Market + Region + Ship Mode + Quarter) enables root-cause analysis of localized performance dips.
14. Category and market-level insights together can guide inventory and stocking decisions for high-demand, high-margin product lines.
15. Overall, the dashboard demonstrates that sales volume and profitability are related but distinct stories — both must be tracked together for sound business decisions.

*(Note: These insights are illustrative of the type of findings this dashboard structure is designed to surface. Actual figures will depend on the underlying data at the time of analysis.)*

---

## 📈 Business Impact

This dashboard enables stakeholders to move from reactive, spreadsheet-based reporting to proactive, visual decision-making. By surfacing profitability gaps by market and region, flagging seasonal category shifts, and quantifying shipping cost by segment, the business can:

- Reallocate marketing and inventory investment toward genuinely profitable markets, not just high-revenue ones
- Renegotiate or adjust shipping strategy for the costliest customer segment
- Set realistic quarterly growth targets grounded in historical trend data
- Reduce the time-to-insight for regional and category performance reviews from days to minutes

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Report design and dashboard development |
| **DAX** | Calculated measures (Total Sales, Total Profit, Total Orders, Total Quantity) |
| **Power Query (M)** | Data cleaning and transformation |
| **Data Modeling** | Relationship and hierarchy design (Date Hierarchy, star-schema style modeling) |
| **Data Visualization** | Bar, Ribbon, Combo, Funnel, Donut, Treemap, Pie, Line, and Scatter charts |

---

## 🔄 Dashboard Workflow

```
Data Collection → Data Cleaning → Data Modeling → DAX Calculations → Dashboard Design → Business Insights
```

1. **Data Collection** — Sourced the Global Superstore `Orders` dataset
2. **Data Cleaning** — Handled inconsistencies and prepared fields in Power Query
3. **Data Modeling** — Built the Date Hierarchy and structured relationships for time intelligence
4. **DAX Calculations** — Authored KPI measures (Total Sales, Total Profit, Total Orders, Total Quantity)
5. **Dashboard Design** — Selected and configured 9 visuals plus 4 slicers on a single themed page
6. **Business Insights** — Translated visuals into actionable, stakeholder-ready findings

---

## 📁 Repository Structure

```
Global-Superstore-Sales-Profit-Dashboard/
│
├── Global_Superstore_Dashboard.pbix     # Power BI project file
├── README.md                            # Project documentation (this file)
├── /screenshots                         # Dashboard preview images
     └── dashboard_overview
---
---

---
## 🚀 Future Improvements

- Add a dedicated drill-through page for country-level and product-level deep dives
- Introduce forecasting visuals (e.g., sales/profit forecast using built-in Power BI forecasting)
- Add a dynamic "Top N" parameter for country and category rankings
- Incorporate row-level security (RLS) for regional stakeholder-specific views
- Add tooltips with mini-visuals for richer hover-based context
- Publish to Power BI Service with scheduled refresh for live data updates

---

## 🎓 Learning Outcomes

- Strengthened skills in DAX measure creation for core business KPIs
- Practiced choosing the right chart type for the right analytical question (e.g., funnel for ranked comparison, ribbon for rank-over-time)
- Improved data modeling skills using Power BI's built-in Date Hierarchy for time intelligence
- Gained experience designing a single-page executive dashboard that balances density with readability
- Developed a stronger business storytelling approach — translating charts into stakeholder-ready insights

---

## 🖼️ Screenshots
<img width="635" height="353" alt="image" src="https://github.com/user-attachments/assets/353c77e8-932a-474f-892e-25947357c68e" />
<img width="623" height="354" alt="image" src="https://github.com/user-attachments/assets/6d60457b-a68a-4acf-8945-901ba22d4858" />
<img width="640" height="353" alt="image" src="https://github.com/user-attachments/assets/55d6bd38-a80b-4700-bfdc-1326ed112acb" />
<img width="619" height="347" alt="image" src="https://github.com/user-attachments/assets/752185b9-3f2b-454b-aeb3-71783456b907" />

---

## 👤 Author

**Tushal Kamboj**
Aspiring Data Analyst | Power BI • SQL • Python
📧 kambojtushal740@gmail.com | 🔗 https://www.linkedin.com/in/tushal-kamboj | 💻 https://github.com/kambojtushal

---

## ✅ Conclusion

This project demonstrates the full lifecycle of business intelligence dashboard development — from raw data to a polished, insight-driven Power BI report. It reflects practical, job-ready skills in data modeling, DAX, and visual storytelling that are directly transferable to real-world data analyst and BI developer roles. Recruiters and hiring managers can use this project as evidence of the candidate's ability to independently take a raw dataset and turn it into a decision-support tool for business stakeholders.

---

⭐ *If you found this project useful or interesting, consider giving the repository a star!*
