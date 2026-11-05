# SQL Practice Task 3

**Date:** 2026-11-05  
**Question Name:** Population Difference  
**Link:** https://www.hackerrank.com/challenges/population-density-difference/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

Find the highest and lowest population values in the CITY table using `MAX()` and `MIN()`. Subtract the minimum population from the maximum population.

## Solution

```sql
SELECT MAX(POPULATION) - MIN(POPULATION)
FROM CITY;
```

## Notes

**Concepts learned:**

- `MAX()` returns the highest value in a column.
- `MIN()` returns the lowest value in a column.
- Subtraction calculates the difference between the two values.

**Improvements:**

- Use aggregate functions to calculate values across an entire table.
- Combine aggregate functions in one query when calculating a difference.