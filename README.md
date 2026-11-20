# SQL Practice

SQL exercises on the Brazilian E-commerce (Olist) dataset, run from a Jupyter notebook against SQLite. Exercises were generated with ChatGPT's help; the queries are my own solutions.

## Data
[Olist Brazilian E-commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) from Kaggle: customers, orders, order items, payments, reviews, products, sellers, geolocation and category translations. Each CSV is loaded with pandas and written to its own SQLite database, then attached together for joins.

## Topics practised
- `JOIN`s across orders, customers, items, products and sellers
- Aggregation and `GROUP BY` (average payment per state, orders per status)
- `CASE` expressions (classifying payments as LOW / MEDIUM / HIGH)
- Window functions (`LAG()` for days between purchases, top customers per state)
- Top-N queries

## Sample findings
- Highest average payment value by state: PB (about 248); lowest: SP (about 138).
- Orders by status: 96,478 delivered, 1,107 shipped, 625 canceled, 609 unavailable.

## Run it
```bash
pip install pandas ipython-sql kagglehub jupyter
jupyter notebook "sql-practice (1).ipynb"
```
