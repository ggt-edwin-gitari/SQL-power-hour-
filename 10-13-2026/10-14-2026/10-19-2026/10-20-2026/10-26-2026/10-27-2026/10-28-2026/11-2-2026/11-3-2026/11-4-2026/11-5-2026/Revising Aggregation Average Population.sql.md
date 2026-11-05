# SQL Practice Task 24

**Date:** 2026-11-05  
**Question Name:** Average Population  
**Link:** 
**Difficulty:** Basichttps://www.hackerrank.com/challenges/average-population/problem?isFullScreen=true 

## Intuition

Calculate the average population of all cities using `AVG()`. Apply `FLOOR()` to round the result down to the nearest integer.

## Solution

```sql
SELECT FLOOR(AVG(POPULATION))
FROM CITY;
```

## Notes

**Concepts learned:**

- `AVG()` calculates the average of a column.
- `FLOOR()` rounds a decimal value down to the nearest integer.
- No `WHERE` clause is needed because the question covers all cities.

**Improvements:**

- Use `FLOOR()` for rounding down.
- Use `ROUND()` for standard mathematical rounding.