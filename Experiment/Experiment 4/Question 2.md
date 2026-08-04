**Problem Link:**
https://www.codechef.com/learn/course/sql-intermediate/SQ00BS01/problems/GSQ63?tab=statement

solution
```sql
/* Write a query to do the following:
 - JOIN the tables 'student' and 'course' using 'Course_id' to match both the tables and output the joined table.
 - LEFT JOIN the tables 'student' and 'course' using 'Course_id' to match both the tables and output the joined table. */
 select * from student as s1
 inner join course as o1
 on s1.Course_id=o1.Course_id;
 
  
 select * from student as s1
 Left join course as o1
 on s1.Course_id=o1.Course_id;
