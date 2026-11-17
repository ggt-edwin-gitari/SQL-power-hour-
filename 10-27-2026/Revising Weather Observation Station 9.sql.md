# SQL Practice Task 3

**Date:** 2026-10-27  
**Question Name:** Weather Observation Station 9  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-9/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where the first character is not a vowel, a, e, i, o, or u.

I use DISTINCT to eliminate duplicate city names. The LEFT(CITY, 1) function extracts the first character of each city name, while LOWER() converts it to lowercase to handle uppercase and lowercase letters consistently.

The NOT IN operator excludes city names whose first character matches any of the five vowels.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1))
      NOT IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- LEFT(): Extracts the first character of a string.
- LOWER(): Converts text to lowercase.
- NOT IN: Excludes values matching a specified list.
- WHERE: Filters records based on specified conditions.

**Improvements:**

- Learned how to filter strings based on their first character.
- Practiced excluding multiple values using NOT IN.
- Improved handling of uppercase and lowercase letters.
- Reinforced the use of DISTINCT to return unique results.
- Improved my understanding of SQL string functions and filtering conditions.