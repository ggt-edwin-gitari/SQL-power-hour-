# SQL Practice”
 
- **Date:** 2026-10-14
- **Question Name:Select By ID**
- **Link:https://www.hackerrank.com/challenges/select-by-id/problem?isFullScreen=true**
- **Difficulty:** Easy 
 
## Intuition
 
The question asks us to retrieve all columns for a city in the CITY table whose ID is 1661.

Since all columns are required, I use SELECT * to retrieve every column. Then, I use the WHERE clause to filter the results and return only the city whose ID matches 1661.
 
## Solution
 
``sql
SELECT *
FROM CITY
WHERE ID = 1661;
 
``
 
## Notes
 
- **Concepts learned:SELECT * retrieves all columns from a table.
FROM specifies the table to query.
WHERE filters rows based on a condition.
= checks whether the ID matches the specified value.**
- **Improvements:Use SELECT * when all columns are required.
Use specific column names when only certain fields are needed.
Apply the WHERE clause to retrieve only the required records.**