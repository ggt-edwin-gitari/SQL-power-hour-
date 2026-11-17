# SQL Practice Task 3

**Date:** 2026-11-02  
**Question Name:** Weather Observation Station 14  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-17/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving the Western Longitude (LONG_W) of the station with the smallest Northern Latitude (LAT_N) greater than 38.7780.

I use the WHERE clause to filter stations whose LAT_N values are greater than 38.7780. I then use ORDER BY LAT_N ASC to arrange the qualifying stations from the smallest latitude to the largest.

Finally, LIMIT 1 retrieves the longitude belonging to the station with the smallest qualifying latitude. ROUND() rounds the longitude to 4 decimal places.

## Solution

```sql
SELECT ROUND(LONG_W, 4)
FROM STATION
WHERE LAT_N > 38.7780
ORDER BY LAT_N ASC
LIMIT 1;
```

## Notes

**Concepts learned:**

- WHERE: Filters records based on specified conditions.
- ORDER BY: Sorts records using a specified column.
- ASC: Sorts values in ascending order.
- LIMIT 1: Returns only the first matching record.
- ROUND(): Rounds numerical values to a specified number of decimal places.

**Improvements:**

- Learned how to retrieve one column based on the minimum value of another column.
- Practiced sorting records by latitude.
- Understood how ORDER BY and LIMIT work together.
- Improved my understanding of numerical filtering and rounding.
- Practiced retrieving related values from the same database record.