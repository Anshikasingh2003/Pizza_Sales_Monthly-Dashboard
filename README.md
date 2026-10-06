# Pizza Sales Monthly Dashboard

**Tools:** SQL (MySQL), Excel (pivot tables, dashboard)

## Business questions

A pizza store wanted to know how it performed in 2020:

- How much revenue came in, how many orders, and how many pizzas were sold?
- On which days and at which hours do orders peak?
- Which categories and sizes bring in the most sales?
- Which pizzas sell best and worst?

## Data

48,620 order lines from 1 Jan to 31 Dec 2020.
Columns: order_id, order_date, order_time, pizza_name, pizza_size, pizza_category, quantity, unit_price, total_price, pizza_ingredients.

## Approach

1. Wrote SQL queries for each KPI and chart (see `Pizza Sales SQL Queries.docx`):
   - `SUM`, `COUNT(DISTINCT)` and `ROUND` for the KPIs
   - `DAYOFWEEK` and `HOUR` with `GROUP BY` for order trends
   - subqueries for percentage of sales by category and size
   - `ORDER BY ... LIMIT 5` for top and bottom sellers
2. Built pivot tables and a one-page dashboard in Excel to match the SQL results.

## Key results

| KPI | Value |
| --- | --- |
| Total revenue | 817,860 |
| Total orders | 21,350 |
| Pizzas sold | 49,574 |
| Average order value | 38.31 |

## Insights

- Orders peak at lunch (12–1 pm) and again around 6 pm.
- Sales are spread evenly across categories: Classic 26.9%, Supreme 25.5%, Chicken 24.0%, Veggie 23.7%.
- Large pizzas bring in 45.9% of sales; XL and XXL together are under 2%.
- Best sellers by quantity: Classic Deluxe, Barbecue Chicken and Hawaiian.
- The Brie Carre pizza sells least (490 units), about a fifth of the best seller.

## Files

- `Pizza Sales SQL Queries.docx` – all SQL queries
- `Pizza_sales Dashboard.xlsx` – data, pivot tables and dashboard
