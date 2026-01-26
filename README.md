## Table of Contents
- Data Source
- Dataset
- Database Tables
- Data Cleaning & Standardization
- Analytical Insights
- Key Insights
- Recommendations

## Data Source
This toy store database is sourced from Maven Analytics.
- **Dataset:** Toy Store Database 
- **Provider:** [Maven Analytics](https://mavenanalytics.io/data-playground/toy-store-e-commerce-database)
- **Tool:** PostgreSQL
- **Project Overview:** This repo analyzes a synthetic toy store database from Maven Analytics to uncover sales patterns, assess product profitability, and identify refund drivers.
- **Skills Demonstrated:** SQL querying, data cleaning, exploratory analysis
- **Setup Instructions:** Load data into PostgreSQL via pgAdmin: `CREATE DATABASE toystore_db;` then import CSVs from Maven Analytics.

## Data Tables 

### Products Table
We have a total of 4 products:
1. The Original Mr. Fuzzy
2. The Forever Love Bear
3. The Birthday Sugar Panda
4. The Hudson River Mini Bear
```sql
SELECT * FROM products;
```

### Orders Table
```sql
SELECT * FROM orders LIMIT 10;
```
We have a total of 32,313 orders.
```sql
SELECT COUNT(orders.order_id) AS Total_Orders FROM orders;
```

### Order Items
```sql
SELECT count(*) FROM order_items;
```
We have a total of 40025 items orderd.

```sql
SELECT COUNT(*) FROM order_items;
```

### Order Item Refunds
```sql
SELECT * FROM order_item_refunds LIMIT 10;
```
We have a total of 1,731 refunds since the store launched.
```sql
SELECT COUNT(order_item_refund_id) FROM order_item_refunds;
```

### Website Pageviews
```sql
SELECT * FROM website_pageviews LIMIT 10;
```
WE have a total of 1188124 page views;
```sql
SELECT COUNT(website_session_id) FROM website_pageviews;
```
### Website Sessions
```sql
SELECT * FROM website_sessions LIMIT 10;
```
We have 472871 website sesstions.
```sql
SELECT COUNT(*) FROM website_sessions;
```

