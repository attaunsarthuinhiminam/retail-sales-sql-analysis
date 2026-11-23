## Project Overview
This project explores, cleans, and analyzes a retail sales dataset (`retail_sales`) in **PostgreSQL** using **Supabase**'s browser SQL Editor. It covers foundational data hygiene and ten business-focused SQL queries ranging from filtering and aggregations to ranking and time-of-day shift analysis.

## What This Project Covers
* **Data Exploration & Cleaning:** Inspected records (`SELECT`, `COUNT(*)`), identified and removed missing values (`IS NULL`, `DELETE`), and checked unique customers (`COUNT(DISTINCT customer_id)`) and categories (`SELECT DISTINCT category`).
* **Business Analysis (`Q.1`–`Q.10`):**
  * Filtered specific dates, categories, months, and order thresholds (`WHERE`, `AND`, `TO_CHAR`).
  * Calculated totals, averages, and order counts by category, gender, and customer (`SUM`, `AVG`, `ROUND`, `COUNT`, `GROUP BY`, `ORDER BY`, `LIMIT`).
  * Identified top-performing months per year using `EXTRACT` and `RANK() OVER (PARTITION BY ...)`.
  * Categorized orders into `Morning`, `Afternoon`, and `Evening` shifts using `EXTRACT(HOUR FROM sale_time)`, `CASE`, and a CTE (`WITH`).
