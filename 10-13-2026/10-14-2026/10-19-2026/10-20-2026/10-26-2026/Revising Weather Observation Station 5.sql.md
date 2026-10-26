# SQL Practice Task 06

**Date:** 2026-10-26  
**Question Name:** Weather Observation Station 5  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires finding the city with the shortest name and the city with the longest name in the STATION table, along with the number of characters in each city name.

If multiple cities share the shortest or longest name length, I use alphabetical order to select the city appearing first.

I use LENGTH(CITY) to calculate the number of characters in each city name. I then run two separate queries. The first sorts cities by name length in ascending order, followed by city name alphabetically. The second sorts by name length in descending order, followed by city name alphabetically. LIMIT 1 returns the first matching city from each query.

## Solution

```sql
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) ASC, CITY ASC
LIMIT 1;

SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) DESC, CITY ASC
LIMIT 1;
```

## Notes

**Concepts learned:**

- LENGTH(): Calculates the number of characters in a city name.
- ORDER BY: Sorts results by city name length and alphabetically.
- ASC: Sorts values in ascending order.
- DESC: Sorts values in descending order.
- LIMIT 1: Returns only the first row after sorting.
- Tie-breaking: Uses CITY ASC to select the alphabetically first city when multiple cities have the same name length.

**Improvements:**

- Learned how to identify minimum and maximum string lengths using SQL.
- Practiced sorting by multiple columns to resolve ties.
- Used LIMIT to retrieve a single record for each condition.
- Improved my understanding of string functions and result ordering.