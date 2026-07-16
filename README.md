# Mobile-Sales-Dashboard---Power-BI
📌 Project Overview

This project is an interactive Mobile Sales Dashboard developed using Power BI to analyze sales performance across different cities, mobile brands, payment methods, and time periods. The dashboard helps stakeholders monitor KPIs, identify trends, and make data-driven business decisions.

🎯 Business Objective

The objective of this dashboard is to provide a centralized solution for:

Monitoring overall sales performance.
Tracking Month-to-Date (MTD) sales.
Comparing current sales with the previous year's performance.
Identifying top-performing cities, brands, and mobile models.
Understanding customer purchasing behavior and payment preferences.

📊 Key Performance Indicators (KPIs)
| KPI                   | Value  |
| --------------------- | ------ |
| Total Sales           | 769M   |
| Total Quantity Sold   | 19K    |
| Total Transactions    | 3.835K |
| Average Selling Price | 40.11K |

📄 Dashboard Pages
1️⃣ Dashboard Overview

Provides a high-level summary of business performance including:

Total Sales, Quantity, Transactions, and Average Price.
Sales distribution across cities.
Monthly sales trend analysis.
Customer ratings distribution.
Sales by mobile model.
Payment method analysis.
Sales by weekday analysis.

2️⃣ MTD Report
Focuses on short-term performance monitoring:

Month-to-Date sales trends.
Daily sales analysis.
Drill-down capability using Year → Quarter → Month → Day hierarchy.
3️⃣ Same Period Last Year Analysis

Enables historical comparison using Power BI Time Intelligence functions:

Year-over-Year sales comparison.
Quarterly sales comparison.
Monthly sales comparison.
Growth trend analysis.
🛠 Tools & Technologies Used
Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Data Modeling
Time Intelligence Functions


📂 Data Model
The project follows a Star Schema design:

Fact Table
Sales_data
Dimension Table
Custom_Calendar

Relationship:

Custom_Calendar[Date] → Sales_data[Date]

📈 DAX Measures Used
Total Sales = SUM(Sales_data[Total Sales])

Total Quantity = SUM(Sales_data[Quantity])

Transactions = COUNT(Sales_data[Transaction ID])

Average Price = AVERAGE(Sales_data[Price Per Unit])

MTD Sales =
TOTALMTD(
    [Total Sales],
    Custom_Calendar[Date]
)

Sales SPLY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(Custom_Calendar[Date])
)

🔍 Key Insights
The business generated 769M revenue from approximately 19K mobile units sold.
Sales are distributed across multiple cities, highlighting strong geographical coverage.
Mobile brands such as Apple, Samsung, OnePlus, Vivo, and Xiaomi contribute significantly to total revenue.
Payment methods are evenly distributed among UPI, Credit Card, Debit Card, and Cash, indicating diverse customer preferences.
Customer ratings show that most customers reported a Good experience.
Monthly sales trends reveal seasonal fluctuations that can support forecasting and inventory planning.

💡 Business Impact
This dashboard helps businesses to:

Monitor sales performance in real time.
Identify top-performing products and locations.
Improve inventory management.
Analyze customer buying patterns.
Support strategic business decisions using historical comparisons.
