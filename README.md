# E-Commerce Revenue & Customer Behaviour Analysis
### UK Online Retail | Dec 2010 – Dec 2011 | 541,909 Transactions

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## Business Problem

A UK-based online retailer operating across 38 countries had no clear visibility into which customers, products, and markets were truly driving revenue — or where product returns were quietly eroding profits. Without this understanding, marketing spend, inventory decisions, and retention efforts were being made without data to back them.

---

## Project Objective

This analysis was designed to answer five core business questions:

- Which months generate the most revenue, and what drives seasonality?
- Which products contribute the most to total revenue?
- Which countries represent the strongest markets — and which are underserved?
- Which customers are most valuable, and how are they distributed?
- Are high-value customers also the highest-risk customers in terms of returns?

---

## Dataset

**Source:** UCI Online Retail Dataset — available on [Kaggle](https://www.kaggle.com/datasets/vijayuv/onlineretail)

| Attribute | Detail |
|---|---|
| Records | 541,909 transactions |
| Period | December 2010 – December 2011 |
| Countries | 38 |
| Features | InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country |

> **Note:** `data.csv` is not included in this repository due to licensing. Download it from the Kaggle link above and place it in the root project folder as `data.csv` before running the notebook.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core analysis language |
| pandas | Data manipulation and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualizations |
| Jupyter Notebook | Interactive analysis environment |
| Power BI Desktop | Business dashboard |

---

## Project Workflow

```
1. Raw Data Ingestion          →  Load 541,909 transactions from CSV
2. Data Cleaning               →  Handle missing values, remove duplicates, filter invalid prices
3. Anomaly Detection           →  Identify negative quantities as return transactions (10,587 rows)
4. Feature Engineering         →  Create Revenue, TransactionType, InvoiceYear, InvoiceMonth
5. Exploratory Data Analysis   →  Monthly revenue trends, country and product breakdowns
6. Customer Segmentation       →  Pareto-based segmentation into High / Medium / Low Value
7. Return Analysis             →  Return ratio by country, product, and customer segment
8. Visualization               →  5 Python charts covering all key dimensions
9. Business Recommendations    →  Actionable insights derived from findings
```

---

## Key Findings

| # | Finding | Business Implication |
|---|---|---|
| 1 | Revenue peaks sharply in Sep–Nov 2011 | Plan inventory and marketing campaigns ahead of Q4 |
| 2 | UK contributes ~83% of total revenue | International markets are significantly underserved |
| 3 | Only 13 customers drive 20% of all customer revenue | VIP retention is the single highest-ROI action available |
| 4 | High Value customers have a 20.9% return ratio — 5x higher than other segments | Bulk order cancellations need individual investigation |
| 5 | Decorative and gift products dominate revenue | Premium gifting range should be prioritized in Q4 marketing |
| 6 | 10,587 return transactions identified via negative quantities | Separate return analysis is essential for accurate revenue reporting |

---

## Business Recommendations

**1. Build a VIP Retention Programme**
Only 13 customers are responsible for 20% of all customer revenue. Losing even two or three of them is a material financial risk. These customers should receive dedicated account management, early access to new products, and priority support.

**2. Investigate High Value Customer Returns Immediately**
A 20.9% return ratio among the most valuable customers is not a normal pattern — it almost certainly reflects bulk order cancellations or fulfilment issues. Each of these 13 customers should be reviewed individually to identify the root cause before more revenue is lost.

**3. Double Down on Q4 Inventory Planning**
Revenue spikes 3x between August and November driven by Christmas gifting demand. Stockouts during this window directly cost revenue. The gift and decorative product range — particularly the Regency Cakestand (£164K alone) — should be stocked with 60-90 days lead time.

**4. Invest in International Market Development**
Netherlands, EIRE, and Germany are the strongest international markets but together represent less than 10% of revenue. With targeted localisation and logistics investment, even modest growth in these markets represents significant incremental revenue.

---

## Visualizations

| Chart | Description |
|---|---|
| Monthly Revenue Trend | Area + line chart showing revenue across 13 months with peak annotation |
| Top 10 Products by Revenue | Horizontal bar chart sorted by revenue contribution |
| Revenue by Country | Bar chart with UK highlighted separately |
| Customer Segment Distribution | Bar chart showing count of High / Medium / Low Value customers |
| Return Ratio by Segment | Column chart showing average return ratio per customer segment |

> Power BI dashboard screenshots available in `/dashboard/screenshots/`

---

## Repository Structure

```
ecommerce-analysis/
│
├── README.md                            ← Project documentation (this file)
├── ecommerce-customer-behaviour-analysis.ipynb             ← Full analysis notebook
│
├── powerbi_data/                        ← Exported summary CSVs for Power BI
│   ├── monthly_revenue.csv
│   ├── top_products.csv
│   ├── revenue_by_country.csv
│   ├── customer_segments.csv
│   └── return_ratio_by_segment.csv
│
├── dashboard/                           ← Power BI files
│   ├── ecommerce_dashboard.pbix
│   └── screenshots/
│       └── dashboard_overview.png
│
└── .gitignore                           ← Excludes data.csv (raw dataset)
```

---

## How to Run

1. Download the UCI Online Retail Dataset from [Kaggle](https://www.kaggle.com/datasets/vijayuv/onlineretail)
2. Place the file as `data.csv` in the root project folder
3. Open `ecommerce-customer-behaviour-analysis.ipynb` in Jupyter Notebook
4. Run all cells from top to bottom
5. Summary CSVs will be exported to `/powerbi_data/` automatically (after the export cell is added)

---

## Author

**Saba**
Aspiring Data Analyst | Python · Power BI · SQL
[GitHub Profile](#) · [LinkedIn](#)
