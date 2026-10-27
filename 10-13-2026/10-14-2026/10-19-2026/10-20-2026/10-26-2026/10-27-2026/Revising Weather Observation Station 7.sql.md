# SQL Practice Task 1

**Date:** 2026-10-27  
**Question Name:** Weather Observation Station 7  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where the last character is a vowel, a, e, i, o, or u.

I use DISTINCT to eliminate duplicate city names. The RIGHT(CITY, 1) function extracts the last character of each city name, while LOWER() converts the character to lowercase to handle both uppercase and lowercase vowels.

The IN operator checks whether the final character matches any of the five vowels. This approach is shorter and easier to maintain than writing five separate LIKE conditions.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(RIGHT(CITY, 1)) IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- RIGHT(): Extracts characters from the right side of a string.
- LOWER(): Converts text to lowercase.
- IN: Checks whether a value matches any item in a list.
- WHERE: Filters rows based on specified conditions.

**Improvements:**

- Learned to use string functions to inspect the last character of a city name.
- Practiced case-insensitive vowel matching using LOWER().
- Simplified multiple conditions using the IN operator.
- Improved query readability by replacing several OR conditions with one condition.
- Reinforced the use of DISTINCT to return unique results.