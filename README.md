# Task 7 - Basic Sales Summary from SQLite with Python

## Steps I followed:
1. Created a small SQLite database with a `sales` table.
2. Inserted sample sales data (product, quantity, price).
3. Wrote SQL inside Python to calculate total quantity and revenue per product.
4. Loaded results into Pandas and displayed them.
5. Created a bar chart of revenue by product using Matplotlib.

## How to Run:
1. Install Python and libraries:
   pip install pandas matplotlib
2. Run the script:
   python task7.py

## Output:
- Printed sales summary
- Bar chart saved as `sales_chart.png`



INTERVIEW QUESTIONS:

1.How did you connect Python to a database?
→ I used Python’s built-in sqlite3 module and sqlite3.connect("sales_data.db") to connect.

2.What SQL query did you run?
→

SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product


3.What does GROUP BY do?
→ It groups rows with the same value in a column so aggregate functions (SUM, AVG, etc.) work per group.

4.How did you calculate revenue?
→ By multiplying quantity * price for each row and then summing it per product.

5.How did you visualize the result?
→ I used Pandas’ .plot(kind='bar') with Matplotlib to create a bar chart showing revenue by product.

6.What does Pandas do in your code?
→ Pandas loads SQL query results into a DataFrame for easy manipulation, printing, and plotting.

7.What’s the benefit of using SQL inside Python?
→ It lets you combine the power of SQL for data retrieval with Python’s libraries for analysis and visualization in one workflow.

8.Could you run the same SQL query directly in DB Browser for SQLite?
→ Yes, the same query works in DB Browser or any SQLite client — Python is just automating the process.
