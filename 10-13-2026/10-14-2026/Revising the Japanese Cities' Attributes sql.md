# SQL Practice” Task 2
 
- **Date:** 2026-10-14
- **Question Name:Japanese Cities' Attributes**
- **Link:https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?isFullScreen=true**
- **Difficulty:** Easy 
 
## Intuition
 
The question asks us to retrieve all attributes (columns) of every Japanese city in the CITY table.

The COUNTRYCODE column identifies the country each city belongs to. Since Japan's country code is JPN, I use SELECT * to retrieve all columns and the WHERE clause to filter the results to only cities whose COUNTRYCODE is 'JPN'.
 
## Solution
 
``sql
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'JPN';
 
``
 
## Notes
 
- **Concepts learned:SELECT * retrieves all columns from a table.
FROM specifies the table to query.
WHERE filters rows based on a condition.
String values must be enclosed in single quotes in SQL.
The equality operator (=) checks whether the country code matches 'JPN'.**

- **Improvements:Use specific column names instead of SELECT * when only certain attributes are needed.
Ensure string values are enclosed in single quotes.
Use appropriate filtering conditions to retrieve only the required records.**
 