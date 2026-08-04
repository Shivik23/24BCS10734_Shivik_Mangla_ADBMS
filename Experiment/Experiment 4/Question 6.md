**Problem Link:**
https://www.codechef.com/learn/course/sql-intermediate/SQ00BS01/problems/ASQL01C?tab=statement

Solution
```sql
-- Part 1: Find pairs of students in the same department
SELECT 
    s1.St_id,
    s1.St_Name,
    s1.Department,
    s2.St_id,
    s2.St_Name,
    s2.Department
FROM student AS s1
INNER JOIN student AS s2
ON s1.Department = s2.Department
AND s1.St_id != s2.St_id;

-- Part 2: Identify students with the same favorite Course_id
SELECT DISTINCT
    s1.St_id,
    s1.St_Name,
    s1.Course_id
FROM student AS s1
INNER JOIN student AS s2
ON s1.Course_id = s2.Course_id
AND s1.St_id != s2.St_id
ORDER BY s1.Course_id;
