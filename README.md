# Elevate_Labs_Task_7
# 📊 Task 7: Basic Sales Summary using Python and SQLite

## 🎯 Objective
This task demonstrates how to use **SQL inside Python** to extract and visualize basic sales data from an SQLite database using `sqlite3`, `pandas`, and `matplotlib`.

---

## 🧰 Tools & Libraries Used
- Python 3
- SQLite (via `sqlite3`)
- Pandas
- Matplotlib
- Jupyter Notebook (`.ipynb`)

---

## 📂 Files Included
| Filename | Description |
|----------|-------------|
| `Task_7_Basic_Sales_Summary_using_Python_and_SQLite.ipynb` | Main notebook containing the code and SQL query execution |
| `sales_data.db` | SQLite database with sample sales data |
| `sales_chart.png` | Bar chart showing revenue per product |
| `Task_7_output_screenshort.PNG` | Screenshot of console output and generated chart |

---

## 🛠️ Steps Performed

1. **Connected Python to SQLite database** using `sqlite3`.
2. **Created and populated** a `sales` table with product, quantity, and price data.
3. **Ran SQL Query** to calculate:
   - Total quantity sold per product
   - Total revenue per product
4. **Loaded results into Pandas** DataFrame for easy manipulation and display.
5. **Plotted revenue** using a basic bar chart via `matplotlib`.
6. **Saved the chart** as `sales_chart.png`.

---

📸 Output Summary
The notebook prints a sales summary table and generates a bar chart comparing revenue by product.

---

📌 Concepts Practiced
-SQL GROUP BY, SUM operations
-Python-SQLite connection
-Using Pandas to fetch and format SQL data
-Basic matplotlib plotting

---

## 🔍 SQL Query Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product

---
