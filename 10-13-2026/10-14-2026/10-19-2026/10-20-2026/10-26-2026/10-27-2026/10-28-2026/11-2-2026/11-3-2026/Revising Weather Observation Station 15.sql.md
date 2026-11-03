# SQL Practice Task 1

**Date:** 2026-11-03  
**Question Name:** Weather Observation Station 15  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-15/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving the Western Longitude (LONG_W) corresponding to the largest Northern Latitude (LAT_N) that is less than 137.2345.

I use the WHERE clause to filter stations whose LAT_N values are less than 137.2345.

I then use ORDER BY LAT_N DESC to arrange the qualifying latitude values from largest to smallest. LIMIT 1 retrieves the longitude belonging to the station with the largest qualifying latitude.

Finally, ROUND() rounds the longitude to 4 decimal places.

## Solution

```sql
SELECT ROUND(LONG_W, 4)
FROM STATION
WHERE LAT_N < 137.2345
ORDER BY LAT_N DESC
LIMIT 1;
```

## Notes

**Concepts learned:**

- WHERE: Filters records based on specified conditions.
- ORDER BY: Sorts records using a specified column.
- DESC: Sorts values in descending order.
- LIMIT 1: Returns only the first matching record.
- ROUND(): Rounds numerical values to a specified number of decimal places.

**Improvements:**

- Learned how to retrieve a value from one column based on the maximum value of another column.
- Practiced filtering numerical data using the less-than operator.
- Improved my understanding of descending order.
- Practiced combining ORDER BY and LIMIT to retrieve a specific record.
- Strengthened my understanding of SQL sorting, filtering, and rounding.