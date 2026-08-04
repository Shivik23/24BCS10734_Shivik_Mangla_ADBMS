**Problem Link:**
https://www.codechef.com/learn/course/sql-intermediate/SQ00BS01/problems/ASQL01D?tab=statement

solution
```sql
-- 1. Customers and Orders: List the customer_name and order_date for all customers who have placed orders.
SELECT C1.customer_name, O1.order_date
FROM customers AS C1
INNER JOIN orders AS O1
ON C1.customer_id = O1.customer_id;

-- 2. All Customers and Their Orders: List all customer names and their corresponding product_name from orders, if they have any. Include customers even if they haven't placed any orders.
SELECT c.customer_name, o.product_name
FROM customers c
LEFT JOIN orders o
ON c.customer_id = o.customer_id;

-- 3. Find Products and Their Orders: Display Product Name and the order_date from all the products that are ordered.
SELECT p.product_name, o.order_date
FROM products p
INNER JOIN orders o
ON p.product_name = o.product_name;
