# sales-data-analysis
Exploratory data analysis of retail sales data using Python (Pandas, Matplotlib, Seaborn): data cleaning, KPIs, product, category and regional performance, monthly trends, and discount impact on profit.
# Sales Data Analysis

Exploratory data analysis of a retail sales dataset using Python to find
what drives sales and profit, and where the business can improve.

## Objective
- Understand overall performance (sales, profit, orders)
- Find top-performing products, categories and regions
- Analyze monthly sales trends and seasonality
- Check how discounts affect profit

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Dataset
Retail "Superstore" sales data, downloaded from Kaggle ([dataset name and link]).

- **File:** `SuperStoreData-230102-093001.xlsx`
- **Size:** 9994 rows and 21 columns
- **Time period:** 2014-01-03 to 2017-12-30  
- **Key columns:** Order ID, Order Date, Ship Date, Customer ID, Segment, Region,
  State, Category, Sub-Category, Product Name, Sales, Quantity, Discount, Profit
## What I did
1. **Cleaned the data:** removed duplicates, handled missing values, converted dates
2. **Created new columns:** year, month, shipping days, profit margin
3. **Calculated KPIs:** total sales, profit, margin, orders, average order value
4. **Explored the data** by product, category, sub-category, region, segment and time
5. **Tested discounts:** compared profit margin across discount levels

## Key findings
1. Overall: $2,297,201 in sales and $286,397 profit (12.5% margin) across 5,009 orders.
2. 'Technology' drives the most sales; 'Technology' has the best profit margin.
3. Top product by sales: 'Canon imageCLASS 2200 Advanced Copier'.
4. Loss-making sub-categories: Tables, Bookcases, Supplies.
5. 'West' is the biggest region by sales; 'West' has the best margin and 'Central' the weakest.
6. Sales peak in Nov and are lowest in Feb; 2017 was the strongest year.
7. Orders with 30%+ discount earn a -37.3% margin versus 29.5% with no discount.

## Charts
![Category](Sales%20data%20analysis/charts/02_category.png)
![Monthly trend](Sales%20data%20analysis/charts/06_monthly_trend.png)
![Discount vs margin](Sales%20data%20analysis/charts/08_discount_margin.png)

## Recommendations
- **Review loss-making products:** [Sub-category names] lose money overall. The business
  should check supplier costs and pricing, or reduce stock of these items.
- **Limit deep discounts:** Orders with discounts of 30% or more earn a [X]% margin,
  compared with [X]% for orders with no discount. Setting an approval rule for
  discounts above [20 or 30]% would protect profit.
- **Plan for peak months:** Sales are highest in [month] and lowest in [month]. Stock,
  staffing and marketing should be planned around these periods.
- **Focus on strong regions:** [Region] brings the most sales, while [region] has the
  weakest margin and should be investigated.
## Files
- [`Sales_Data_Analysis.ipynb`](Sales%20data%20analysis/Sales_Data_Analysis.ipynb): full analysis with code, tables and charts
- [`charts/`](Sales%20data%20analysis/charts): saved visualizations used in this README

## Author
Siddique Shaikh | B.Sc. Data Science & Analytics
