# Pizza Sales Analysis — Professional Project

## Project overview
This project analyzes a 2015 pizza sales dataset to understand business performance, order trends, sales mix, product performance, and opportunities for operational improvement.

The project requirements are based on the three requirement screenshots supplied with the project. Those requirements specify **5 KPIs** and **7 visual-analysis areas**.

### Deliverables
- `pizza_sales_excel_file.xlsx` — source data
- `PIZZA SALES SQL QUERIES.docx` — supplied SQL query reference
- `Pizza Sales Analysis.pbix` — supplied Power BI report/dashboard
- `Pizza_Sales_Analysis_Professional_Presentation.pdf` — professional presentation
- `Pizza_Sales_Analysis_Professional_Presentation.pptx` — editable PowerPoint version
- `README.md` — project documentation

## Problem statement
The project asks for a visual analysis of pizza sales data to identify trends and understand key business performance indicators.

### Required KPIs
1. **Total Revenue** — sum of `total_price`.
2. **Average Order Value** — total revenue divided by total distinct orders.
3. **Total Pizzas Sold** — sum of `quantity`.
4. **Total Orders** — distinct count of `order_id`.
5. **Average Pizzas Per Order** — total pizzas sold divided by total orders.

### Required charts
1. Daily trend for total orders — bar chart.
2. Monthly trend for total orders — line chart.
3. Percentage of sales by pizza category — pie chart.
4. Percentage of sales by pizza size — pie chart.
5. Total pizzas sold by pizza category — funnel chart.
6. Top 5 best sellers by revenue, total quantity and total orders — bar charts.
7. Bottom 5 pizzas by revenue, total quantity and total orders — bar charts.

> **Terminology note:** the supplied SQL query for the "Daily Trend" groups by `DATENAME(DW, order_date)`, so it produces **day-of-week** results. The presentation labels this as the daily/weekday trend.

## Dataset
- **Rows:** 48,620
- **Columns:** 12
- **Date range:** 2015-01-01 to 2015-12-31
- **Distinct orders:** 21,350
- **Pizzas sold:** 49,574
- **Pizza varieties:** 32
- **Missing values:** none across the supplied fields

## KPI results
| KPI | Result |
|---|---:|
| Total Revenue | 817,860.05 |
| Average Order Value | 38.31 |
| Total Pizzas Sold | 49,574 |
| Total Orders | 21,350 |
| Average Pizzas Per Order | 2.32 |

**Currency note:** the source files do not specify a currency symbol, so the project uses the dataset's price units.

## Key findings
- **Busiest weekday:** Friday — 3,538 orders.
- **Quietest weekday:** Sunday — 2,624 orders.
- **Highest monthly order volume:** July — 1,935.
- **Lowest monthly order volume:** October — 1,646.
- **Highest monthly revenue:** July — 72,557.90.
- **Lowest monthly revenue:** October — 64,027.60.
- **Top revenue category:** Classic — 26.9% of revenue.
- **Top revenue size:** L — 45.9% of revenue.
- **Top pizza by revenue:** Thai Chicken — 43,434.25.
- **Top pizza by quantity:** Classic Deluxe — 2,453.
- **Top pizza by orders:** Classic Deluxe — 2,329.

## Category analysis
| Category | Revenue | Revenue Share | Quantity |
|---|---:|---:|---:|
| Classic | 220,053.10 | 26.9% | 14,888 |\n| Supreme | 208,197.00 | 25.5% | 11,987 |\n| Chicken | 195,919.50 | 24.0% | 11,050 |\n| Veggie | 193,690.45 | 23.7% | 11,649 |\n
## Size analysis
| Size | Revenue | Revenue Share | Quantity |
|---|---:|---:|---:|
| L | 375,318.70 | 45.9% | 18,956 |\n| M | 249,382.25 | 30.5% | 15,635 |\n| S | 178,076.50 | 21.8% | 14,403 |\n| XL | 14,076.00 | 1.7% | 552 |\n| XXL | 1,006.60 | 0.1% | 28 |\n
## Best sellers

### Top 5 by revenue
1. Thai Chicken — 43,434.25\n2. Barbecue Chicken — 42,768.00\n3. California Chicken — 41,409.50\n4. Classic Deluxe — 38,180.50\n5. Spicy Italian — 34,831.25\n
### Top 5 by quantity
1. Classic Deluxe — 2,453 pizzas\n2. Barbecue Chicken — 2,432 pizzas\n3. Hawaiian — 2,422 pizzas\n4. Pepperoni — 2,418 pizzas\n5. Thai Chicken — 2,371 pizzas\n
### Top 5 by distinct orders
1. Classic Deluxe — 2,329 orders\n2. Hawaiian — 2,280 orders\n3. Pepperoni — 2,278 orders\n4. Barbecue Chicken — 2,273 orders\n5. Thai Chicken — 2,225 orders\n
## Bottom 5 performers

### Bottom 5 by revenue
1. Brie Carre — 11,588.50\n2. Green Garden — 13,955.75\n3. Spinach Supreme — 15,277.75\n4. Mediterranean — 15,360.50\n5. Spinach Pesto — 15,596.00\n
### Bottom 5 by quantity
1. Brie Carre — 490 pizzas\n2. Mediterranean — 934 pizzas\n3. Calabrese — 937 pizzas\n4. Spinach Supreme — 950 pizzas\n5. Soppressata — 961 pizzas\n
### Bottom 5 by distinct orders
1. Brie Carre — 480 orders\n2. Mediterranean — 912 orders\n3. Spinach Supreme — 918 orders\n4. Calabrese — 918 orders\n5. Chicken Pesto — 938 orders\n
## Business insights
1. The four pizza categories are relatively balanced, with Classic leading at 26.9% of revenue.
2. Large pizzas dominate revenue at 45.9%.
3. Friday is the busiest weekday and is useful as a staffing/preparation planning signal.
4. July is the strongest month by order volume and revenue; one year is not enough to prove recurring seasonality.
5. Thai Chicken leads revenue, while Classic Deluxe leads quantity and distinct orders.
6. Low revenue does not automatically mean a product should be removed; margin and customer feedback should be considered.

## Recommendations
- Plan staffing and preparation around Friday demand, then validate with hourly trends.
- Investigate July and September–October alongside promotions, holidays and marketing activity.
- Protect availability of high-revenue products.
- Review low performers using food cost, margin and customer feedback before menu changes.
- Use the Large-size mix to support inventory and production planning.
- Extend the project with profitability, hourly, promotional and multi-year analysis.

## SQL analysis
The supplied SQL document covers the five KPIs, daily/weekday and monthly order trends, category and size revenue share, February category quantity, and top/bottom five rankings by revenue, quantity and distinct orders.

### SQL notes
- The queries use SQL Server syntax such as `TOP`, `DATENAME` and `MONTH`.
- Sort month names by numeric month when presenting chronologically.
- The category quantity query is specifically filtered to February.
- Bottom-five rankings use ascending order and `TOP 5`.
- `COUNT(DISTINCT order_id)` is the order-level metric.

## Limitations
- Only one calendar year is available.
- No cost, margin, discount, customer or marketing fields are present.
- The data supports descriptive sales analysis, not causal conclusions or profitability analysis.
- The supplied Power BI file is retained as the dashboard artifact; its internal visual configuration was not independently extracted.

## Tools
Excel • SQL Server-style SQL • Power BI • Python/pandas • Matplotlib • ReportLab • python-pptx

## Conclusion
The project shows a strong and diversified pizza sales mix with clear demand patterns by weekday, month, category, size and product. The next step is to combine sales performance with profitability and customer-level information for deeper decision-making.
