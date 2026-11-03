# SQL Practice Task 2

**Date:** 2026-11-03  
**Question Name:** Weather Observation Station 16  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-18/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires calculating the Manhattan Distance between two points on a 2D plane using the minimum and maximum values of Northern Latitude (LAT_N) and Western Longitude (LONG_W) from the STATION table.

Manhattan Distance is calculated by adding the absolute differences between the corresponding coordinates of the two points.

I use MIN() to retrieve the minimum latitude and longitude values, and MAX() to retrieve the maximum latitude and longitude values.

The ABS() function returns the absolute differences, while ROUND() rounds the final result to 4 decimal places.

## Solution

```sql
SELECT ROUND(
    ABS(MAX(LAT_N) - MIN(LAT_N)) +
    ABS(MAX(LONG_W) - MIN(LONG_W)),
    4
)
FROM STATION;
```

## Notes

**Concepts learned:**

- MIN(): Retrieves the smallest value in a column.
- MAX(): Retrieves the largest value in a column.
- ABS(): Returns the absolute value of a numerical expression.
- ROUND(): Rounds a numerical result to a specified number of decimal places.
- Manhattan Distance: Calculates distance by adding the absolute differences between two coordinates.
- Aggregate functions: Calculate values across multiple rows.

**Improvements:**

- Learned how to calculate Manhattan Distance using SQL.
- Practiced combining multiple aggregate functions in one query.
- Understood how ABS() handles negative differences.
- Improved my understanding of mathematical operations in SQL.
- Practiced rounding calculated results to a specified decimal scale.