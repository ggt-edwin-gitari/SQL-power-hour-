# SQL Practice Task 2

**Date:** 2026-11-02  
**Question Name:** Weather Observation Station 16 
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-16/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires finding the smallest Northern Latitude (LAT_N) value greater than 38.7780 from the STATION table and rounding the result to 4 decimal places.

I use the WHERE clause to filter latitude values greater than 38.7780. The MIN() aggregate function identifies the smallest latitude among the filtered records.

Finally, I use ROUND() to format the result to 4 decimal places.

## Solution

```sql
SELECT ROUND(MIN(LAT_N), 4)
FROM STATION
WHERE LAT_N > 38.7780;
```

## Notes

**Concepts learned:**

- MIN(): Returns the smallest value in a column.
- WHERE: Filters records based on specified conditions.
- ROUND(): Rounds a numerical value to a specified number of decimal places.
- Aggregate functions: Perform calculations on multiple rows and return a single result.

**Improvements:**

- Learned how to find the minimum value using MIN().
- Practiced filtering numerical data using comparison operators.
- Learned how to round decimal values using ROUND().
- Improved my understanding of combining aggregate functions with WHERE conditions.
- Practiced retrieving a single calculated result from a database table.