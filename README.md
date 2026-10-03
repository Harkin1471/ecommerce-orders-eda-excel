# ecommerce-orders-eda-excel
Explanatorydata analysis of 1200 e-commerce orders using Excel : statistics, outliers, correlation and trends
# E-commerce Orders: Exploratory Data Analysis (Excel)

## Business question
What patterns, trends and outliers exist in 1,200 online orders (Jan 2023 to Jun 2025), and what should the business act on?

## Dataset
1,200 orders with 14 fields: product, quantity, unit price, order status, payment method, coupon code and referral source.

## Tools
Microsoft Excel: formulas, PivotTables, conditional formatting and charts.

## Method
1. Audited the data: no duplicates, no missing values apart from coupon codes (blank means no coupon), and TotalPrice matches Quantity x UnitPrice in every row.
2. Calculated descriptive statistics (mean, median, quartiles, skewness).
3. Flagged outliers with the IQR and Z-score methods.
4. Built a correlation matrix.
5. Summarised trends by month, year, product and order status.

## Key findings
- **Order value is right-skewed.** The median order is 824 against a mean of 1,054, so the median is the better "typical" value.
- **8 high-value outliers**, all Quantity 5 orders that reconcile exactly. They are genuine big orders, not errors.
- **First-half revenue is falling about 10% a year** (286,502, then 257,059, then 231,883). Each year is compared January to June only, because the data ends in June 2025.
- **41.4% of orders end Cancelled or Returned**, worth about 519,674.
- **Price drives order value** (r = 0.72), partly by construction since TotalPrice = Quantity x UnitPrice. The behavioural link is Quantity vs ItemsInCart (r = 0.65).

## Visuals
![Dashboard](images/00_dashboard.png)

## Recommendations
1. Investigate why about 2 in 5 orders are cancelled or returned, by product, referral source and payment method.
2. Treat the top-value orders as a high-value customer segment.
3. Check whether coupon discounts are applied, since TotalPrice ignores them.
4. Obtain full-year 2025 data before judging the annual trend.

## Limitations
Coupons are not reflected in TotalPrice. The 2025 data covers six months only. The currency is not stated in the dataset.

## Files
- `data/`: original dataset
- `workbook/`: full Excel analysis (Cleaned Data, Descriptive Stats, Outliers, Correlation, Trends, Charts, Insights)
- `images/`: chart and table screenshots
