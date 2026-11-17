# SQL Practice Task 3

**Date:** 2026-11-04  
**Question Name:** Average Population  
**Link:** https://www.hackerrank.com/challenges/average-population/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

Calculate the average population of all cities in the CITY table using `AVG()`. Use `FLOOR()` to round the result down to the nearest integer.

## Solution

```sql
SELECT FLOOR(AVG(POPULATION))
FROM CITY;
```

## Notes

**Concepts learned:**

- `AVG(POPULATION)` calculates the average population across all cities.
- `FLOOR()` rounds a decimal value down to the nearest integer.
- No `WHERE` clause is needed because the question includes all cities.

**Improvements:**

- Use `FLOOR()` when a question specifically asks for rounding down.
- Use `ROUND()` for standard rounding, not rounding down.