# SQL Practice Task 07

**Date:** 2026-10-26  
**Question Name:** Weather Observation Station 6  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving city names from the STATION table where the city name starts with a vowel: A, E, I, O, or U. The results must not contain duplicates.

I use the DISTINCT keyword to return each city name only once. The LIKE operator with the % wildcard checks whether a city name starts with any of the five vowels. The % wildcard matches any sequence of characters following the first letter.

I combine the conditions using OR to include all five vowels.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE CITY LIKE 'A%'
   OR CITY LIKE 'E%'
   OR CITY LIKE 'I%'
   OR CITY LIKE 'O%'
   OR CITY LIKE 'U%';
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names from the results.
- LIKE: Matches text against a specified pattern.
- Wildcard (%): Matches zero or more characters following the specified letter.
- WHERE: Filters records based on specified conditions.
- OR: Includes records matching at least one of the conditions.

**Improvements:**

- Learned how to filter text values based on their starting characters.
- Practiced using multiple conditions with OR.
- Understood how DISTINCT prevents duplicate results.
- Improved my understanding of pattern matching in SQL.