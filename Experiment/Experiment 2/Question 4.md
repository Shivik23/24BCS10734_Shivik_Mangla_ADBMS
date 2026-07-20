**Problem Link:**
https://www.codechef.com/learn/course/sql-intermediate/SQ00BS07/problems/GSQ78A

Solution
```sql
select emp_name
from employee
union all 
select emp_name
from pt_employee
