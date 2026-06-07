# Week 1 Final Report: E-Commerce Data Analysis
**Organization:** WeIntern Pvt Ltd
**Project:** Week 1 Assignment
**Prepared By:** Shanika Jith
---
### 1. Title and Objective
* **Project Title:** E-Commerce Data Cleaning, KPI Analysis, and Visualization Pipeline.
* **Objective:** My goal for this project was to clean a raw e-commerce dataset using Python, calculate key business metrics (KPIs), and create clear charts to help the company make better business decisions.
---
### 2. Dataset Overview
* **The Raw Data:** The initial dataset had **541,909 rows** containing transaction details like order numbers, product descriptions, quantities, prices, dates, and customer IDs.
* **Data Issues:** When I first checked the data, I found a lot of missing values, unformatted dates, duplicates, and negative numbers for prices and quantities that needed to be fixed before analysis.
---
### 3. Data Cleaning Summary
To clean the data systematically, I took the following steps:
* **Missing Customer IDs:** I found **135,080 missing values** in the `CustomerID` column. Instead of deleting them and losing sales data, I labeled them as `"Guest Customer"`.
* **Missing Descriptions:** There were **1,454 rows** with empty product names. I filled these with `"Unknown Item Description"`.
* **Duplicate Rows:** I found and removed **5,268 exact duplicate rows** so they wouldn't mess up our sales totals.
* **Data Validation:** 
  - I deleted **10,587 rows** with negative product quantities because they represented canceled orders.
  - I removed rows with negative unit prices.
  - I converted the `InvoiceDate` column into a standard date format (`YYYY-MM-DD`).
* **Final Clean Dataset:** After cleaning, I had **526,052 clean rows** left, which I saved as `cleaned_ecommerce.csv`.
---
### 4. KPI Summary
Here are the main business metrics I calculated from the cleaned data:

| Business KPI | Value |
| :--- | :--- |
| **Total Revenue** | $10,642,110.80 |
| **Total Orders** | 20,726 unique transactions |
| **Average Order Value (AOV)** | $513.47 per order |
| **Total Units Sold** | 5,645,017 items |
| **Top Category** | Novelty / Craft Supplies |
| **Top Product (by Revenue)** | PAPER CRAFT, LITTLE BIRDIE |

---
### 5. Trend Analysis
* **Observation:** When looking at the monthly sales data, revenue stays mostly steady from January through September. However, sales suddenly skyrocket in late October and peak in November.
* **What it means:** This huge spike at the end of the year is almost certainly due to holiday shopping or successful year-end marketing promotions.
---
### 6. Customer Insights
* **Observation:** Registered members bring in **83.5% of total revenue**, while guest checkouts only account for **16.5%**.
* **What it means:** This shows excellent loyalty among our registered customers. Instead of spending a lot of money trying to find new customers, the marketing team should focus on keeping our registered members happy and finding ways to get guests to sign up for accounts.
---
### 7. Visualization Section
I created and saved four charts in the project folder to show these findings visually:
1. `monthly_sales_trend.png` (Line chart showing sales growth over the months).
2. `customer_revenue_share.png` (Pie chart showing how much revenue comes from registered vs. guest users).
3. `top_10_products_bar.png` (Bar chart ranking the top 10 best-selling items by volume).
4. `dashboard_mockup.png` (A single dashboard image that combines the KPI table and all charts together).
All charts include clear titles, labeled axes, and readable text blocks.
---
### 8. Key Findings
* **Registered Users Matter Most:** Over 80% of our money comes from users who have an account.
* **Q4 Holiday Spike:** The fourth quarter (especially November) is by far the most profitable time of the year.
* **Popular Products:** Novelty craft items, especially the "PAPER CRAFT, LITTLE BIRDIE", drive a large portion of our unit sales.
---
### 9. Recommendations
* **Get Guests to Sign Up:** Offer a small discount (like free shipping or 10% off) during checkout to encourage the 16.5% of guest buyers to create an account.
* **Prepare for Q4 Stock:** Since sales double at the end of the year, the warehouse team needs to stock up on inventory and ensure servers can handle the website traffic before October starts.
* **Promote Best Sellers:** Put top-selling items like craft supplies on the homepage banner to make them easier for users to find and buy.
---
### 10. Limitations or Assumptions
* **Canceled Orders:** I assumed all negative quantities were canceled orders or errors, so I removed them to focus only on actual completed sales.
* **Guest Tracking:** Because guests don't have user IDs, I treated every guest checkout as a completely different person, even though some might be the same person buying multiple times.
