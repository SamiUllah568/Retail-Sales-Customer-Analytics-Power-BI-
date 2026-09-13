# Project Report: Retail Sales & Customer Analytics (Power BI)

## 1. Objective

To design a business intelligence solution for a multi-country retail chain that consolidates customer, product, sales, return, and store data into a single, interactive analytics suite — enabling leadership to monitor performance, spot trends, and make data-driven decisions across markets (USA, Canada, Mexico).

## 2. Business Questions Addressed

1. What does our customer base look like, and how is it growing?
2. Which products and brands generate the most revenue and profit?
3. Where are returns concentrated, and which products/brands are underperforming on quality?
4. Which stores and regions are the strongest and weakest performers?
5. What is the overall trajectory of sales, profit, and margin over time?

## 3. Data Sources

| Table | Rows (approx.) | Key Fields |
|---|---|---|
| Customer | 10,000+ | demographics, income, membership card, homeowner status |
| Product | 1,500+ | brand, name, SKU, price, cost, recyclable/low-fat flags |
| Region | 7 regions / multiple districts | district → region mapping |
| Store | 20+ | type, size, location, open date |
| Transactions (1997–1998) | large fact table | date, product, customer, store, quantity |
| Returns (1997–1998) | fact table | date, product, store, quantity |

## 4. Methodology

- **Data Cleaning:** Standardized date formats, handled inconsistent state/province naming across countries, verified referential integrity between fact and dimension tables.
- **Data Modeling:** Built a star schema with `transactions` and `returns` as fact tables, linked to `customer`, `product`, `store`, and `region` dimension tables.
- **DAX Measures:** Created calculated measures for total sales, net sales, profit, profit margin, return rate, and return sales, along with time-intelligence measures for monthly trending.
- **Dashboard Design:** Grouped visuals by business function (customer / product / returns / store-region / overall sales) rather than cramming everything into one page, to keep each dashboard focused and readable.

## 5. Dashboard Breakdown

### 5.1 Sales Performance (Fact) Dashboard
Top-level KPI dashboard: total sales ($1.76M), net sales ($1.75M), total profit ($1.05M), profit margin (59.67%), return sales ($17.43K), return rate (0.99%). Includes monthly sales & profit trend, top 10 stores by sales, top 10 products by sales, and profit by region.

### 5.2 Customer Analytics Dashboard
10,281 total customers, average age 53. Breaks down customer base by country, state, city, membership card tier, gender, and account-open trend over time. Bronze membership dominates at ~55% of the customer base.

### 5.3 Product Performance Dashboard
1,560 total products, average retail price $2.12, average cost $0.854. Highlights top 10 products and brands by sales, profit split by recyclability, and sales split by low-fat classification.

### 5.4 Return Analysis Dashboard
$17.43K in return sales at a 0.99% overall return rate. Breaks down return rate by store, country, and brand, plus a monthly return sales trend and top 10 returned products.

### 5.5 Store & Regional Performance Dashboard
24 total stores, 22 districts, 7 regions. Shows top stores by sales, profit by store state, sales & profit by store type (supermarket, gourmet, small grocery, etc.), sales by country, and profit by district/region.

## 6. Key Insights

- **Geographic concentration:** USA drives the largest share of sales and customers, followed by Canada, then Mexico.
- **Membership mix:** Bronze-tier customers are the majority — a potential upsell opportunity toward Silver/Golden tiers.
- **Regional profit leader:** North West region and Store 13 lead in profitability.
- **Return hotspots:** A small set of products/brands account for a disproportionate share of returns — worth flagging for quality or supplier review.
- **Margins:** Overall profit margin is healthy at ~59.7%, with visible seasonal uplift toward Q4 (November–December).

## 7. Recommendations

1. Launch targeted campaigns to migrate Bronze members to higher tiers, since they represent the largest segment.
2. Investigate top-returned products/brands for quality or description-accuracy issues.
3. Study underperforming regions (e.g., Central West) to identify whether the issue is market size, store count, or execution.
4. Use the Q4 seasonal uplift pattern to plan inventory and staffing ahead of peak months.

## 8. Tools Used

- Power BI Desktop (data modeling, DAX, visualization)
- Power Query (ETL/data cleaning)
- DAX (measures and calculated columns)

## 9. Limitations

- Dataset covers only 1997–1998, so trends should be read as illustrative rather than reflecting current market conditions.
- Store table sample shown covers a subset of the full 24 stores; full detail is in the underlying data model.
