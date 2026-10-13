# SQL Practice” Task 02
 
- **Date:** 2026-10-13
- **Question Name:Revising the Select Query I**
- **Link:https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=false**
- **Difficulty:** Easy 
 
## Intuition
 
The question asks us to retrieve all cities from the CITY table that meet two conditions:

The city must be in the United States, identified by COUNTRYCODE = 'USA'.

The city's population must be greater than 100000.

Since we need all the columns from the matching cities, we use SELECT *. The WHERE clause filters the records, while AND ensures that both conditions must be true for a city to be included in the result.
 
## Solution
 
``sql
-- SELECT *
FROM CITY
WHERE COUNTRYCODE = 'USA' 
AND POPULATION > 100000 ;

 
``
 
## Notes
 
- **Concepts learned:I learned how to use SELECT, WHERE, and AND to retrieve records that satisfy multiple conditions in SQL.**
- **Improvements: do more practices on the same type of queries**
 