# 🛒 Retail Sales & Customer Analytics Dashboard | Power BI Project

A complete **5-dashboard Power BI analytics suite** built on a multi-country retail dataset (USA, Canada, Mexico), covering customers, products, sales, returns, and store/regional performance. Designed to give stakeholders a 360° view of business performance — from high-level KPIs down to store-level and product-level detail.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data%20Analysis-2E8B57?style=for-the-badge)

---

## 📌 Project Overview

This project analyzes a retail company's operations across **three countries (USA, Canada, Mexico)**, using customer, product, sales/transaction, returns, store, and regional data. The goal was to design an interactive, decision-ready BI suite that answers key business questions:

- Who are our customers, and what does our customer base look like?
- Which products and brands drive the most sales and profit?
- Where and why are returns happening?
- Which stores and regions are performing best (and worst)?
- What is our overall sales, profit, and margin trend over time?

The result is **5 interconnected dashboards**, each focused on a specific business function, plus a summary/KPI dashboard tying everything together.

---

## 📊 Dashboards Included

| # | Dashboard | Focus |
|---|-----------|-------|
| 1 | **Sales Performance (Fact) Dashboard** | Overall KPIs — total sales, net sales, profit, margin, returns; monthly trends; top stores/products; profit by region |
| 2 | **Customer Analytics Dashboard** | Customer demographics, membership tiers, gender split, account growth trend, sales by age group |
| 3 | **Product Performance Dashboard** | Top products & brands by sales, profit by recyclability, low-fat product sales |
| 4 | **Return Analysis Dashboard** | Return rate by store/country/brand, top returned products, return sales trend by month |
| 5 | **Store & Regional Performance Dashboard** | Store-level sales/profit, performance by store type, country, district, and region |

📁 See [`/screenshots`](./screenshots) for full-size images of each dashboard.

---

## 🗂️ Dataset

The project uses a relational retail dataset with the following tables:

| Table | Description |
|-------|-------------|
| `customer` | Customer demographics — name, location, income, education, occupation, membership card |
| `product` | Product catalog — brand, name, SKU, retail price, cost, weight, recyclable/low-fat flags |
| `region` | Sales district and region mapping |
| `store` | Store details — type, location, size (sqft), open/remodel dates |
| `transactions_1997_1998` | Sales transactions — date, product, customer, store, quantity |
| `returns_1997_1998` | Product returns — date, product, store, quantity |

**Time period:** 1997–1998
**Geography:** USA, Canada, Mexico
**Scale:** 10,000+ customers, 1,500+ products, 20+ stores, 7 regions

> Note: This is a sample/demo retail dataset used for portfolio and learning purposes.

---

## 🛠️ Tools & Skills Used

- **Power BI Desktop** — data modeling, DAX measures, report design
- **Power Query** — data cleaning and transformation
- **DAX** — calculated columns and measures (profit margin, return rate, YoY trends, etc.)
- **Data Modeling** — star schema relationships across fact and dimension tables

---

## 💡 Key Insights

- USA is the largest market by customer count and sales volume, followed by Canada and Mexico.
- Bronze-tier membership dominates the customer base (~55%), suggesting an opportunity for tier-upgrade campaigns.
- The North West region and Store 13 lead in profit contribution.
- Return rate holds steady around **0.99%**, with select products/brands driving disproportionate returns — a target list for quality review.
- Overall profit margin sits at **~59.7%**, with sales showing a seasonal uptick toward Q4.

---

## 📁 Repository Structure

```
retail-powerbi-dashboard/
│
├── README.md                          # This file
├── PROJECT_REPORT.md                  # Detailed write-up: methodology, insights, recommendations
├── retail_dashboard.pbix              # Power BI project file
│
├── screenshots/
│   ├── 01_sales_performance_dashboard.png
│   ├── 02_customer_analytics_dashboard.png
│   ├── 03_product_performance_dashboard.png
│   ├── 04_return_analysis_dashboard.png
│   └── 05_store_regional_performance_dashboard.png
│
└── data/                              # (optional — only include if licensing allows)
    ├── customer.csv
    ├── product.csv
    ├── region.csv
    ├── store.csv
    ├── transactions_1997_1998.csv
    └── returns_1997_1998.csv
```

---

## 🚀 How to Use

1. Clone this repository
   ```bash
   git clone https://github.com/<your-username>/retail-powerbi-dashboard.git
   ```
2. Open `retail_dashboard.pbix` in **Power BI Desktop** (free download from Microsoft)
3. Explore each dashboard tab using the filters/slicers provided (Country, State, Product, Date, etc.)

Alternatively, view the static screenshots in the [`/screenshots`](./screenshots) folder or check the published report link below.

---

## 🔗 Live Report

🔗 **Published Power BI Report:** *[add your Publish-to-Web link here]*

---

## 👤 Author

**[Your Name]**
Data Analyst | Power BI Developer
📧 [your-email@example.com] | 🔗 [LinkedIn](https://linkedin.com/in/your-profile) | 🌐 [Portfolio](https://your-portfolio.com)

---

## 📄 License

This project is for educational/portfolio purposes. Dataset is a publicly available sample retail dataset used for learning and demonstration.
