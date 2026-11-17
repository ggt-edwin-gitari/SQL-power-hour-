# SQL Practice Task 1

**Date:** 2026-11-02  
**Question Name:** Employee Names  
**Link:** https://www.hackerrank.com/challenges/name-of-employees/problem?isFullScreen=true  
**Difficulty:** Basic

## Intuition

The question requires retrieving the names of all employees from the Employee table and displaying them in alphabetical order.

I use SELECT to retrieve the name column from the Employee table. I then use ORDER BY Name ASC to sort the employee names alphabetically, from A to Z.

Since the question only requires employee names, there is no need for filtering or grouping.

## Solution

```sql
SELECT name
FROM Employee
ORDER BY name ASC;
```

## Notes

**Concepts learned:**

- SELECT: Retrieves specific columns from a table.
- FROM: Specifies the table from which to retrieve data.
- ORDER BY: Sorts the query results.
- ASC: Sorts values in ascending order, alphabetically from A to Z.

**Improvements:**

- Practiced retrieving specific columns from a database table.
- Learned how to sort text values alphabetically.
- Improved my understanding of ascending order in SQL.
- Practiced writing simple queries without unnecessary filtering or grouping.