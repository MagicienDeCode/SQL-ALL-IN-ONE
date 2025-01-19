# Before Start
- Make sure zoom or goole meet works.
- Create a leetcode account or login with google account.
- Just have fun.
- 恩返しです。
- Price: 648 CNY
- Contact me: xiangli1105@hotmail.com

# Class Plan
- Class 1: Introduction SQL, Relational Database vs NoSQL Database, SELECT in one table.
- Class 2 & Class 3: Basic Joins
- Class 4: Basic Aggregate Functions
- Class 5: Sorting and Grouping
- Class 6: Subqueries
- Class 7: Advanced String Functions / Regex / Clause
- Class 8: Interview Questions

# SQL (Structed Query Language)
- SQL is a standardized programming language used to manage and manipulate relational databases.

# Relational Database vs NoSQL
- [README](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/1.0.relational-db-vs-kv-db.md)

# SELECT 
- [template and basice functions](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/2.0.select.md)

- table users

|  id  |  name | email | sex | phone | age |
|:---:|:---:|:---:|:---:|:---:|:---:|
|1|xiang|magiciendecode@gmail.com|M|0123456789|32|
|2|kate|kate@gmail.com|F|9876543210|NULL|
|3|kiki|kiki@keoi.com|F|1598746320|21|
|4|lx|lx@gmail.com|F|3652987410|23|

- table jobs

|  id | company |  job_title | length_of_year | salary | user_id |
|:---:|:---:|:---:|:---:|:---:|:---:|
|1|mb|sde|0.5|1500| 1 |
|2|sp|sde|6.2|3100| 1 |
|3|bb|stage|0.2|0| 3 |

```sql
-- 1. SELECT all users name which length of email greater or equal than 14, return upper case name, example: KIKI
-- 2. SELECT all users name which has age and sex is F, return small case name: example: kiki
-- 3. calculate average age of women, if age is NULL, take default value 18
```
- homework todo, [answer](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/2.1.todo.md)

# Basic Joins

- [README](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/3.0.basic-joins.md)
- Foreign Key
- One to One (1 to 1): FK both
- One to Many (1 to n): FK in Many
- Many to Many (n to n): create a new mid table to store relation.

- IF(xx='xx',1,0)
- xx + INTERVAL 1 DAY = yy

- **JOIN filter, WHERE filter**
```sql
-- LEFT JOIN, if UnitsSold data exists, date should between start and end. if data not exists, just fill NULL
SELECT *
FROM Prices p
LEFT JOIN UnitsSold u ON p.product_id = u.product_id AND u.purchase_date BETWEEN p.start_date AND p.end_date;

-- LEFT JOIN, if data not exists, fill NULL, if data exists then apply filter, 
-- WHERE u.purchase_date BETWEEN p.start_date AND p.end_date == date should NOT be NULL, and between start and end
SELECT *
FROM Prices p
LEFT JOIN UnitsSold u ON p.product_id = u.product_id 
WHERE u.purchase_date BETWEEN p.start_date AND p.end_date;

-- INNER JOIN?
```
# Basic Aggregate Functions
- COUNT SUM AVG MIN MAX
- xx % 2 = 0 even, xx % 2 != 0 odd
- COALESCE(xx,vv) if xx is NULL, return vv
- CASE WHEN xx > 3 THEN 1 ELSE 0 END
- LEFT(xx, 7) take first 7 characters
- AVG(xx = yy)
- COUNT(xx) / (SELECT COUNT(DISTINCT xx) FROM Table)
- WHERE (xx,yy) IN (SELECT xx,yy FROM Table GROUP BY xx)
- GROUP BY xx1, xx2
- datexx BETWEEN 'date1' AND 'date2'

# Sorting and Grouping
- HAVING COUNT(xx) = (SELECT xx ..)

# Advanced Select and Joins
- UNION: Eliminates duplicate rows from the result set.
- SUM (xx) OVER (ORDER BY yy) AS cumulative_xx

# Subqueries
- IS NULL / IS NOT NULL
- xx CASE 'v1' THEN 0 WHEN 'v2' THEN 1 ELSE AS output
- CASE WHEN xx = (SELECT xx FROM table) THEN yy WHEN 'v2' THEN id + 1 ELSE
- UNION / UNION ALL
- id IN / id NOT IN

# Advanced String Functions / Regex / Clause
- CONCAT(a,b)
- SUBSTRING(xx,1,1)
- SUBSTRING(xx,2)
- GROUP_CONCAT(DISTINCT xx ORDER BY yy)

## [SQL 50](https://leetcode.com/studyplan/top-sql-50/)
- [Solutions](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/3.50.solutions.md)

# Interview
- [Interview Questions](https://github.com/MagicienDeCode/SQL-ALL-IN-ONE/blob/master/4.0.interview.md)