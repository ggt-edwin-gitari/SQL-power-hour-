# SQL Practice Task 09

**Date:** 2026-10-27  
**Question Name:** Weather Observation Station 8  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-8/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where both the first and last characters are vowels, a, e, i, o, or u.

I use DISTINCT to remove duplicate city names. The LOWER() function converts city names to lowercase to handle uppercase and lowercase letters consistently. LEFT(CITY, 1) extracts the first character, while RIGHT(CITY, 1) extracts the last character.

The IN operator checks whether both characters belong to the list of vowels. I combine the two conditions using AND because both the first and last characters must be vowels.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1)) IN ('a', 'e', 'i', 'o', 'u')
  AND LOWER(RIGHT(CITY, 1)) IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- LEFT(): Extracts the first character of a string.
- RIGHT(): Extracts the last character of a string.
- LOWER(): Converts text to lowercase.
- IN: Checks whether a value matches an item in a list.
- AND: Requires both conditions to be true.
- WHERE: Filters records based on specified conditions.

**Improvements:**

- Learned to check the first and last characters of a string.
- Practiced combining multiple conditions using AND.
- Simplified vowel checks using the IN operator.
- Improved handling of uppercase and lowercase characters.
- Reinforced the use of DISTINCT to return unique results.