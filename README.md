# 🛒 E-Commerce Sales Dashboard — Power BI

Interactive Power BI dashboard analysing **₹4.37L of Indian e-commerce sales (2018)** across states, categories and payment modes.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-blue?style=flat)

---

## 📊 Key Metrics

| Metric | Value |
|---|---|
| Total Sales | ₹4,37,771 |
| Total Profit | ₹36,963 |
| Quantity Sold | 5,615 |
| Profit Margin | 8.4% |
| Orders / Customers | 500 / 336 |

---

## 📂 Data

| File | Rows | Key Columns |
|---|---|---|
| `Orders.csv` | 500 | Order ID, Order Date, CustomerName, State, City |
| `Details.csv` | 1,500 | Order ID, Amount, Profit, Quantity, Category, Sub-Category, PaymentMode |

Joined on **Order ID** (1 : many). Covers 19 states, 25 cities, 3 categories, 17 sub-categories.

---

## ✨ Dashboard Features

- KPI cards — Sales, Profit, Quantity, AOV
- Sales by State (top performers)
- Profit by Category & Sub-Category
- Payment mode breakdown
- Monthly profit trend
- Slicers for state, category and quarter

---

## 🧮 Sample DAX

```dax
Total Sales   = SUM(Details[Amount])
Total Profit  = SUM(Details[Profit])
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
AOV           = DIVIDE([Total Sales], DISTINCTCOUNT(Details[Order ID]), 0)
```

---

## 🔍 Insights

- **Electronics** leads revenue (₹1.66L), but **Clothing** gives the highest profit (₹13.3K).
- **Maharashtra** and **Madhya Pradesh** drive the largest share of orders.
- **Furniture** is the weakest category on both revenue and profit.
- **COD** is still heavily used — scope to push digital payments.

---

## 🚀 How to Run

1. Clone the repo.
2. Open `DashboardEcommerce.pbix` in Power BI Desktop.
3. Update the CSV source paths if prompted → **Refresh**.

---

**Riyan Shaikh** · Aspiring Data Analyst · [@riyanshaikh07](https://github.com/riyanshaikh07)
