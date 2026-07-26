**Problem Link:**
https://leetcode.com/problems/customers-who-never-order/submissions/2082260820/

**Solution**
```sql
SELECT Name AS Customers
FROM Customers
WHERE Id NOT IN (SELECT CustomerId FROM Orders);
