SQL Practice — Task 04
Date: 2026-10-19
Question Name: Select CITY and STATE from STATION
Link: HackerRank — https://www.hackerrank.com/challenges/weather-observation-station-1/problem?isFullScreen=true 
Difficulty: Easy
Intuition
The question asks us to retrieve the CITY and STATE columns from the STATION table.

I interpreted the task as selecting only the two specified columns. Since the question does not explicitly ask for unique records, I used DISTINCT to return unique city-and-state combinations, avoiding duplicates.

Solution

SELECT DISTINCT CITY, STATE
FROM STATION;

Notes
Concepts learned:
SELECT retrieves specific columns from a table.
DISTINCT removes duplicate combinations of selected column values.
FROM specifies the table from which to retrieve data.
Improvements:
Read the question carefully to identify whether duplicate rows should be removed.
Use DISTINCT when the task explicitly requires unique results.
Keep SQL queries simple and select only the required columns.