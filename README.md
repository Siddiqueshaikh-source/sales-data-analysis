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
best_cat      = cat["Sales"].idxmax()
best_cat_marg = cat["Margin %"].idxmax()
best_region   = reg["Sales"].idxmax()
best_reg_marg = reg["Margin %"].idxmax()
weak_reg      = reg["Margin %"].idxmin()
best_month    = df.groupby("Month Name")["Sales"].sum().idxmax()
worst_month   = df.groupby("Month Name")["Sales"].sum().idxmin()
top_product   = top_products["Sales"].idxmax()
best_year     = yearly["Sales"].idxmax()
hi_disc = df.loc[df["Discount"] >= 0.3]
no_disc = df.loc[df["Discount"] == 0]
hi_margin = hi_disc["Profit"].sum() / hi_disc["Sales"].sum() * 100
no_margin = no_disc["Profit"].sum() / no_disc["Sales"].sum() * 100

print(f"1. Overall: ${total_sales:,.0f} in sales and ${total_profit:,.0f} profit ({overall_margin:.1f}% margin) across {total_orders:,} orders.")
print(f"2. '{best_cat}' drives the most sales; '{best_cat_marg}' has the best profit margin.")
print(f"3. Top product by sales: '{top_product}'.")
print(f"4. Loss-making sub-categories: {', '.join(loss_makers.index) if len(loss_makers) else 'none'}.")
print(f"5. '{best_region}' is the biggest region by sales; '{best_reg_marg}' has the best margin and '{weak_reg}' the weakest.")
print(f"6. Sales peak in {best_month} and are lowest in {worst_month}; {best_year} was the strongest year.")
print(f"7. Orders with 30%+ discount earn a {hi_margin:.1f}% margin versus {no_margin:.1f}% with no discount.")

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
