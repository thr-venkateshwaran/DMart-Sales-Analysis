# D-Mart Style Retail Sales Analysis (2021-2022)

A practice project analysing a sample retail sales dataset (527 sales records, 44 products, 5 categories, 3 sales channels, 23 locations) to answer business questions a manager would ask. Built with Google Sheets / Excel. SQL and Power BI parts are coming next.

Note: This is a sample practice dataset, not real D-Mart company data.

## Business Questions
1. How did sales, cost, profit and margin change from 2021 to 2022?
2. What does the monthly trend look like?
3. Which products sell and earn the most and least?
4. Which categories earn the most profit and margin?
5. Which products sell well but earn low margin?
6. Which sales channel is best?
7. How are Cash and Online payments used?
8. Which locations matter most?
9. What should management do?

## Dataset
- Source: https://www.kaggle.com/datasets?search=Dmart
- Period: January 2021 to December 2022
- Columns: date, product, quantity, sale type, location, payment mode, category, purchase price, sale price, amounts
- Limitations: no customer or order ID, profit is gross profit only (sales minus purchase cost), no expenses such as shipping or fees

## What I Did
1. Checked the data: rows, columns, data types, missing values, duplicates
2. Split the data into two tables: products and sales
3. Joined them back using XLOOKUP on Product ID
4. Calculated profit as Quantity x (Sale Price - Purchase Price)
5. Built pivot tables for year, month, category, product, channel, location and payment mode
6. Wrote insights in Finding / So what / Action format

## Key Insights
- Sales grew 14.33% (187,284 to 214,128) but profit grew 27.30% (30,315 to 38,593). Margin rose from 16.19% to 18.02%.
- Category03 sales fell 62.22% while the other four categories grew. All six Category03 products declined.
- California and Texas give 41.15% of sales and 42.48% of profit.
- Wholesaler sales grew 40% in 2022 while Online sales stayed flat.
- Product44 and Product23 sell well but earn only 7.41% and 5.66% margin, against a company average of 17.17%.
- Cash and Online payments are almost equally used (264 vs 263 records).

Full list of 8 insights is in the Insights tab of the Excel file and in insights.csv.

## Data Issues I Found and Fixed
- Date swap: When loading data into Google Sheets, day and month were swapped for some dates, so monthly totals were wrong while yearly totals still looked right. I found it by checking monthly numbers against the source data, then fixed it.
- AI margin error: An AI tool gave wrong profit margins for categories (copied from one unrelated row). I recalculated them (for example Category04 is 18.46%, not 25.37%).
- Wrong label: "Orders" was used for row counts. The data has no order ID, so I renamed it "Sales Records".

## How I Used AI
I used AI tools to help draft tables and insights. I verified every number against the source data and corrected the errors listed above.

## Files
- DMart_Sales_Analysis.xlsx: full analysis (findings, category, product, channel, location, payment mode, insights)
- sales.csv: sales transactions
- products.csv: product details
- insights.csv: written insights

## Next Steps
- Answer the same questions with SQL
- Build a Power BI dashboard

## About Me
Name: Thiru venkateshwaran.M
LinkedIn profile: www.linkedin.com/in/thiru-venkateshwaran-40466b326
