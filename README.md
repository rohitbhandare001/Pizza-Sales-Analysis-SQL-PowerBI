# Pizza Sales Analysis | SQL Server & Power BI

An end-to-end sales analysis project using SQL Server for querying pizza sales data and Power BI for interactive reporting.

## Project overview

This project explores pizza sales performance through business KPIs, time-based order trends, category and size contribution, and best-/worst-selling pizzas.

## Tools used

- Microsoft SQL Server / SQL Server Management Studio (SSMS)
- Power BI Desktop
- SQL (aggregations, `GROUP BY`, `ORDER BY`, `WHERE`, `TOP`, `DATENAME`, `COUNT(DISTINCT)`, subqueries and `CAST`)

## Repository structure

```text
Pizza-Sales-Analysis-SQL-PowerBI/
├── SQL/
│   └── Pizza_Sales_Analysis.sql
├── PowerBI/
│   └── Pizza_Sales_Dashboard.pbix
├── Documentation/
│   ├── SQL_Analysis_Documentation.pdf
│   └── Best_Worst_Sellers_Screenshot.png
└── README.md
```

## Business questions covered

- What are the total revenue, total orders and total pizzas sold?
- What is the average order value and average number of pizzas per order?
- How do orders vary by weekday and month?
- What percentage of revenue comes from each pizza category and size?
- Which five pizzas perform best and worst by revenue, quantity and number of orders?

## Key figures shown in the supplied SQL documentation

| KPI | Value |
|---|---:|
| Total Revenue | $817,860.05 |
| Average Order Value | $38.31 |
| Total Pizzas Sold | 49,574 |
| Total Orders | 21,350 |
| Average Pizzas per Order | 2.32 |

These are the figures recorded in the project documentation; they have not been independently recalculated here.

## Power BI report pages

1. **Home Dashboard** – KPI cards and sales/order trend and distribution visuals.
2. **Best & Worst Sellers** – top five and bottom five pizzas by revenue, quantity and total orders.

A screenshot of the Best & Worst Sellers page is available in `Documentation/`.

## How to use

1. Open `SQL/Pizza_Sales_Analysis.sql` in SQL Server Management Studio.
2. Load the pizza sales dataset into a SQL Server table named `pizza_sales` with the columns referenced in the script.
3. Execute the queries to reproduce the analysis.
4. Open `PowerBI/Pizza_Sales_Dashboard.pbix` in Power BI Desktop. If the source data connection is not available on your machine, update it to point to your local dataset.

## Notes and future improvements

- The weekday query groups orders by weekday name, rather than by each calendar date.
- The monthly query groups by month name; for multi-year datasets, consider grouping by year and month and sorting chronologically.
- The category quantity query in the supplied analysis is filtered to February (`MONTH(order_date) = 2`).
- Future improvements can include validating the measures against the source data, documenting the data model and adding business recommendations.

## Author

Rohit Bhandare

