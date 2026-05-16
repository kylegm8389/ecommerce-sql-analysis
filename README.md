# E-Commerce Customer & Sales Analysis

A SQL analytics project built to demonstrate real-world querying skills using a public e-commerce dataset. All analysis is written in SQL via a Kaggle notebook, with Python used for visualisation.

---

## Business Problem

Retailers need to understand who their most valuable customers are, how revenue is trending, and which products are performing well or poorly. This project answers 11 business questions across four key areas:

- **Customer value** — who is spending the most and where are they coming from?
- **Revenue trends** — how is the business growing month on month?
- **Product performance** — which products are rated highest and returned most?
- **Channel effectiveness** — which acquisition channels produce the most valuable customers?

---

## Project Structure

```
ecommerce-sql-analysis/
├── ecommerce_analysis.ipynb    # Full analysis notebook
└── README.md
```

---

## Analysis Summary

| # | Business Question | SQL Techniques |
|---|---|---|
| 1 | Which countries generate the most revenue? | `GROUP BY`, `SUM`, bar & pie charts |
| 2 | Which acquisition channels bring in the highest value customers? | `GROUP BY`, `ORDER BY` |
| 3 | How does spend differ across membership tiers and devices? | Multi-column `GROUP BY` |
| 4 | Are there customers who have never placed an order? | `LEFT JOIN`, `IS NULL` |
| 5 | How much revenue comes from the top 20% of customers? | CTE, `NTILE()`, `CASE WHEN` |
| 6 | How has revenue trended month on month? | CTE, `LAG()`, MoM growth % |
| 7 | How does each customer's spend compare to their country average? | `AVG() OVER (PARTITION BY)` |
| 8 | Who are the top customers within each membership tier? | `RANK() OVER (PARTITION BY)` |
| 9 | Which products are rated highest within each category? | `RANK() OVER (PARTITION BY)` |
| 10 | Which products have the highest return rates per category? | `RANK() OVER (PARTITION BY)` |
| 11 | Which channel and tier combination drives the highest order value? | `INNER JOIN`, `AVG`, `COUNT` |

---

## Key Findings

| Finding | Business Insight |
|---|---|
| Top 20% of customers drive 60% of revenue | Retaining high value customers is critical — losing a small number has outsized impact |
| Revenue shows a consistent upward trend | Business is in a healthy growth phase across the full period |
| Acquisition channel affects average order value | Marketing budget should be weighted toward highest value channels |
| Return rates vary significantly by product | High return items should be reviewed for quality or description issues |
| Spend patterns differ across countries | Localised marketing strategies may improve conversion by market |

---

## Skills Demonstrated

- **Joins** — `INNER JOIN` and `LEFT JOIN` across multiple tables
- **Aggregation** — `SUM`, `COUNT`, `AVG`, multi-column `GROUP BY`
- **CTEs** — chained common table expressions for multi-step analysis
- **Window functions** — `LAG()`, `RANK()`, `NTILE()`, `PARTITION BY`
- **Conditional logic** — `CASE WHEN`, `IS NULL`
- **Visualisation** — matplotlib bar charts, pie charts, dual-axis time series, grouped bar charts

---

## Dataset

[E-Commerce Customer Behavior and Sales 2020–2026](https://www.kaggle.com/datasets/meruvakodandasuraj/e-commerce-customer-behavior-and-sales-20202026) — available publicly on Kaggle.

Four tables used: `customers`, `orders`, `product_summary`, `monthly_revenue`

---

## How to Run

Open the notebook directly on Kaggle — no local setup required:

👉 [View on Kaggle](https://www.kaggle.com/code/kylemarshall10/e-commerce-project)

Or download `ecommerce_analysis.ipynb` and run locally with:

```bash
pip install pandas pandasql matplotlib
jupyter notebook ecommerce_analysis.ipynb
```

---

## Author

Kyle Marshall · [LinkedIn](https://www.linkedin.com/in/kyle-marshall-665434160) · [GitHub](https://github.com)
