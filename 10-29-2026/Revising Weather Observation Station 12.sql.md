# SQL Practice Task 14

**Date:** 2026-10-29  
**Question Name:** Weather Observation Station 12  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-12/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where the first character is not a vowel and the last character is not a vowel.

I use DISTINCT to remove duplicate city names. LEFT(CITY, 1) extracts the first character, while RIGHT(CITY, 1) extracts the last character. LOWER() converts both characters to lowercase to handle uppercase and lowercase letters consistently.

I combine the two conditions using AND because both conditions must be true for a city to appear in the results.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u')
  AND LOWER(RIGHT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- LEFT(): Extracts the first character of a string.
- RIGHT(): Extracts the last character of a string.
- LOWER(): Converts characters to lowercase.
- NOT IN: Excludes values matching a specified list.
- AND: Requires both conditions to be true.
- WHERE: Filters records based on specified conditions.

**Improvements:**

- Learned how to filter strings using both their first and last characters.
- Practiced combining conditions using AND.
- Understood the difference between AND and OR in SQL filtering.
- Improved handling of uppercase and lowercase vowels.
- Reinforced the use of DISTINCT to return unique results.
