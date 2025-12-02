# Business-Insights-360


### 🏬 Company Overview
- AtliQ Hardware(imaginary company) is a rapidly growing electronics company specializing in hardware products, including PC accessories, printers, and more. Over the years, AtliQ has expanded significantly, establishing a strong global presence in key regions such as APAC, North America, Latin America, and the European Union.

The company distributes its products through two primary sales platforms:
- Brick-and-Mortar Stores – Partnering with physical retail outlets like Croma and Best Buy.
- E-Commerce Platforms – Selling through online giants like Amazon and Flipkart.
  
Moreover, AtliQ operates through multiple sales channels:
- Retailers – Third-party sellers, both online and offline, that stock and sell AtliQ’s products.
- Direct Stores – AtliQ’s own branded stores, where consumers can purchase directly.
- Distributors – In restricted markets like China and South Korea, AtliQ collaborates with large distributors to ensure product availability.

Note: AtliQ’s customers are retailers and distributors, while the consumers are the end users.

### 🔎 Problem Statement
- As a rapidly growing company, AtliQ Hardware's reliance on scattered Excel sheets for analytics has led to inefficient decision-making, resulting in significant losses, particularly during its Latin American expansion. Meanwhile, competitors leveraging advanced data analytics have gained an edge, leaving AtliQ struggling to keep up with outdated methods. To improve transparency in data-driven decisions and stay competitive, AtliQ has launched a data analytics project to enhance decision-making and strategic growth.

### 🎯 Project Objective
- To develop an intuitive dashboard that delivers actionable insights for finance, sales, marketing, and supply chain teams, along with an executive and key performers view. This will enhance transparency, improve data accessibility, and empower stakeholders to make informed, data-driven decisions for strategic growth and efficiency.

### 🛢 Data Overview
AtliQ Hardware has provided two SQL databases and three Excel files for analysis.

The three Excel files are:

- Operating Expenses
- Targets (available only for FY 2022)
- Market Share (limited to the Personal Computer division)

The two databases contain the following tables:

gdb041:

- Fact tables: fact_forecast_monthly, fact_sales_monthly
- Dimension tables: dim_customer, dim_market, dim_product
  
gdb056:

- Contains freight_cost, gross_price, manufacturing_cost, post_invoice_deductions, and pre_invoice_deductions
  
AtliQ’s fiscal year runs from September to August, and the dataset covers actual sales from **September 1, 2017**, to **December 31, 2021**.

NOTE: Since this is a bootcamp project, the data files cannot be shared.


### 🧹️ Data Cleaning & Transformation
Standardized & Trimmed Data:
- Removed leading and trailing spaces from text fields.
- Standardized naming conventions for consistency.

Data Structuring & Optimization:
- Created a dim_date table for better time-based analysis.
- Append fact_sales_monthly and fact_forecast_monthly into a single table -> fact_actual_estimates, to simplify calculations.
- Added calculated fields in fact_actual_estimates using data from relevant tables 
- Disabled load for tables that were used to derive calculations in fact_actual_estimates to optimize performance and reduce the Power BI report size.

### Quick Refresh Key Business Metrics :-

| **Business Term**             | **Definition** |
|------------------------------|----------------|
| **Gross Revenue / Gross Sales** | Total revenue generated from selling products before any deductions like discounts or costs. |
| **Pre-Invoice Deduction**       | Discounts applied before the invoice is generated, usually negotiated or promotional discounts. |
| **Net Invoice Sales**           | Gross Revenue minus Pre-Invoice Deductions; the revenue amount that appears on the final invoice. |
| **Post-Invoice Deduction**      | Deductions applied after the invoice is generated, such as rebates, returns, allowances, or adjustments. |
| **Net Sales**                   | Net Invoice Sales minus Post-Invoice Deductions; actual revenue realized by the company. |
| **Manufacturing Cost**          | Total cost to produce each product, including raw materials, labor, and overhead expenses. |
| **Freight Cost**                | Cost to transport products from factories to warehouses, stores, or customers. |
| **COGS (Cost of Goods Sold)**   | Total cost of producing and delivering products: Manufacturing Cost + Freight Cost + other direct costs. |
| **Gross Margin**                | Profit remaining after subtracting COGS from Net Sales. Formula: Gross Margin = Net Sales − COGS. |
| **Gross Margin %**              | Percentage of profit earned relative to Net Sales. Formula: (Gross Margin / Net Sales) × 100. |
| **Operational Expense (OPEX)**  | Costs required to run the business: salaries, rent, utilities, admin, logistics, support, etc. |
| **Marketing Spend**             | Budget spent on promotion, advertising, campaigns, branding, and customer acquisition. |
| **Net Profit**                  | Final profit after subtracting OPEX + Marketing Spend + other expenses from Gross Margin. |
| **Forecast Quantity**           | Number of units the company expects to sell during a specific period. |
| **Sold Quantity**               | Actual number of units sold in the period. |
| **Forecast Accuracy**           | How close the forecast quantity is to actual units sold. Higher % indicates better planning. |
| **Net Error**                   | Difference between forecasted and actual sales, showing overestimation or underestimation. |
| **Absolute Error**              | Absolute difference between forecasted and actual units sold; ignores direction. |

| **Gross Margin** | Profit left after subtracting **direct costs** (manufacturing + freight) from gross revenue. |

---------------------------------------------------------------------------------------------------------------------------------------------------------------


