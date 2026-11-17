SQL Practice — Task 3
Date: 2026-10-19
Question Name: Weather Observation Station 3
Link: https://www.hackerrank.com/challenges/weather-observation-station-3/problem?isFullScreen=true 
Difficulty: Easy
Intuition
The question asks me to retrieve city names from the STATION table where the ID is an even number. It also requires that duplicate city names be excluded and that the results can be returned in any order.

To solve this, I use WHERE to filter rows with even IDs, MOD() to check divisibility by 2, and DISTINCT to eliminate duplicate city names.

Solution
SELECT DISTINCT CITY
FROM STATION
WHERE ID % 2 = 0;

Notes
Concepts learned:
SELECT DISTINCT returns unique city names.
WHERE filters rows based on a condition.
MOD(ID, 2) = 0 checks whether an ID is even.
FROM specifies the table to query.
Improvements:
Identify filtering conditions before writing the query.
Use DISTINCT when duplicate results must be excluded.
Practice using MOD() to check even and odd numbers.
Keep SQL queries readable by placing each clause on a separate line.