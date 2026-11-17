# SQL Practice Task 2

**Date:** 2026-11-05  
**Question Name:** Japan Population  
**Link:** https://www.hackerrank.com/challenges/japan-population/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

Calculate the total population of Japanese cities using `SUM()`. Filter the CITY table using `WHERE` to include only rows where `COUNTRYCODE` is `'JPN'`.

## Solution

```sql
SELECT SUM(POPULATION)
FROM CITY
WHERE COUNTRYCODE = 'JPN';
```

## Notes

**Concepts learned:**

- `SUM()` calculates the total of numeric values in a column.
- `WHERE` filters rows based on a condition.
- `'JPN'` identifies Japan in the COUNTRYCODE column.

**Improvements:**

- Apply filters before calculating aggregates.
- Use `SUM()` for totals, `AVG()` for averages, and `COUNT()` for record counts.
