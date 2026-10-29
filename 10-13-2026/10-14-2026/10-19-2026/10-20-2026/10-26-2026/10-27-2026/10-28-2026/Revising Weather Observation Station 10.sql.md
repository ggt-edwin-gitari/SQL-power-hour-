# SQL Practice Task 1

**Date:** 2026-10-29  
**Question Name:** Weather Observation Station 10  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-10/problem?isFullScreen=true  
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where the last character is not a vowel, a, e, i, o, or u.

I use DISTINCT to remove duplicate city names. The RIGHT(CITY, 1) function extracts the last character of each city name, while LOWER() converts it to lowercase to handle uppercase and lowercase letters.

The NOT IN operator excludes city names ending with any of the five vowels.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(RIGHT(CITY, 1))
      NOT IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- RIGHT(): Extracts the last character of a string.
- LOWER(): Converts text to lowercase.
- NOT IN: Excludes values matching a specified list.
- WHERE: Filters records based on specified conditions.

**Improvements:**

- Learned how to filter city names based on their last character.
- Practiced excluding multiple values using NOT IN.
- Improved handling of uppercase and lowercase letters.
- Reinforced the use of DISTINCT to return unique results.
- Practiced combining string functions with filtering conditions.