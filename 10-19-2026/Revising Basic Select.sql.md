SQL Practice — Task 
Date: 2026-10-19
Question Name: Revising the Select Query I
Link: https://www.hackerrank.com/challenges/select-all-sql/problem?isFullScreen=true 
Difficulty: Easy
Intuition
The question asks me to retrieve all columns (attributes) for every row in the CITY table. Instead of specifying each column name individually, I can use the SELECT * statement. The asterisk (*) represents all columns in the table, while FROM CITY specifies the table from which to retrieve the data.

Solution

SELECT *
FROM CITY;
Notes
Concepts learned: The SELECT statement, the * wildcard for selecting all columns, and the FROM clause for specifying a table.
Improvements: Learn when to use SELECT * for quick queries and when to specify individual columns for better readability and efficiency in production queries.