**Problem Link:**
https://www.codechef.com/learn/course/sql-intermediate/SQ00BS08/problems/GSQ82

*Solution*

```sql
SELECT Department, 
COUNT(CASE WHEN Marks > 80 THEN 1 ELSE NULL END) AS Dept_HighScore_Count
FROM student
GROUP BY Department;
