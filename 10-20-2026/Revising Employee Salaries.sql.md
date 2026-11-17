SQL Practice — Task 01
Date: 2026-10-20
Question Name: Employee Salaries
Link: https://www.hackerrank.com/challenges/salary-of-employees/problem?isFullScreen=false
Difficulty: Easy
Intuition
The question asks us to display the names of employees who earn more than $2,000 per month and have worked for the company for less than 10 months.

I approached the problem by selecting the name column from the Employee table and using a WHERE clause to filter employees based on both conditions. Finally, I used ORDER BY employee_id to arrange the results in ascending order of employee ID.

Solution

SELECT name
FROM Employee
WHERE salary > 2000
  AND months < 10
ORDER BY employee_id ASC;
Notes
Concepts learned:
SELECT — retrieves specific columns from a table.
WHERE — filters rows based on conditions.
AND — ensures that both conditions must be true.
ORDER BY ASC — sorts the results in ascending order.
Improvements:
Practice combining multiple conditions in SQL queries.
Improve understanding of filtering and sorting data.
Write cleaner queries by using SQL defaults, such as omitting ASC when ascending order is implied.