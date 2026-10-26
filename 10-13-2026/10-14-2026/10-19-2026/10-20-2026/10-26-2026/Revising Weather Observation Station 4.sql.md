# SQL Practice Task 05

**Date:** 2026-10-26  
**Question Name:** Weather Observation Station 4  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-4/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires finding the difference between the total number of CITY entries and the number of distinct CITY entries in the STATION table.

I used COUNT(CITY) to count all non-NULL city entries, including duplicates. I then used COUNT(DISTINCT CITY) to count unique city names, excluding duplicates and NULL values.

Subtracting the distinct count from the total count gives the number of duplicate city entries.

## Solution

```sql
SELECT COUNT(CITY) - COUNT(DISTINCT CITY)
FROM STATION;
```

## Notes

**Concepts learned:**

- COUNT(): Counts non-NULL values in a column.
- DISTINCT: Returns unique values by removing duplicates.
- Arithmetic operations: Subtracting one aggregate result from another.
- Duplicate identification: Comparing total entries against unique entries.
- NULL handling: Both COUNT(CITY) and COUNT(DISTINCT CITY) exclude NULL values.

**Improvements:**

- Improved my understanding of aggregate functions in SQL.
- Learned how to calculate duplicate entries without using GROUP BY.
- Practiced combining aggregate functions in a single query.
- Understood how COUNT() handles NULL values when applied to a specific column.