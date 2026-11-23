# Retail Sales Analysis (SQL)

I built this as my first SQL project using a retail sales dataset (`retail_sales`) in **PostgreSQL** via **Supabase**. Everything was written and run right in the browser, so there was no local setup to wrestle with.

## What's Inside
- `retail_sales_analysis.sql` — My full SQL script, starting with basic data checks and cleanup and moving through ten business questions (`Q.1`–`Q.10`).
- `README.md` — Notes on what I practiced and how the queries are put together.

## What I Did & Learned
- **Checking and cleaning the data:** Started by peeking at sample rows (`LIMIT 10`), counting records (`COUNT(*)`), checking unique customers (`COUNT(DISTINCT customer_id)`) and categories (`SELECT DISTINCT category`), and finding/deleting rows with `NULL` values (`IS NULL`, `DELETE`).
- **Answering business questions (`Q.1`–`Q.10`):**
  - Pulled sales for a specific date (`'2022-11-05'`), filtered `'Clothing'` orders in November 2022 with `quantity >= 4`, and found orders over `1000` (`WHERE`, `AND`, `TO_CHAR`).
  - Added up sales and counted orders by category, checked average customer age in `'Beauty'` (`ROUND(AVG(age), 2)`), counted transactions by gender and category, and pulled the top 5 spending customers (`SUM`, `COUNT`, `GROUP BY`, `ORDER BY`, `LIMIT`).
  - Found the highest-averaging sales month each year using `EXTRACT`, `AVG`, and `RANK() OVER (PARTITION BY ...)`.
  - Split orders into `Morning`, `Afternoon`, and `Evening` shifts based on `sale_time` using `CASE`, `EXTRACT(HOUR FROM ...)`, and a CTE (`WITH`).

## Running It Yourself
1. Open a project in **Supabase** and go to the **SQL Editor**.
2. Load the `retail_sales` CSV data into a table with `transactions_id` as the primary key.
3. Paste queries from `retail_sales_analysis.sql` and run them (picking **No limit** when you want full results).
