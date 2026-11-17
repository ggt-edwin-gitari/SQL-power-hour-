# SQL Practice Task 13

**Date:** 2026-10-29  
**Question Name:** Weather Observation Station 11  
**Link:** https://www.hackerrank.com/challenges/weather-observation-station-11/problem?isFullScreen=true  
**Difficulty:** Basic

## Intuition

The question requires retrieving unique city names from the STATION table where either the first character is not a vowel or the last character is not a vowel.

I use DISTINCT to remove duplicate city names. The LEFT(CITY, 1) function extracts the first character, while RIGHT(CITY, 1) extracts the last character. LOWER() converts the characters to lowercase to handle uppercase and lowercase letters consistently.

The OR operator returns a city if at least one condition is true. Therefore, a city is excluded only when both its first and last characters are vowels.

## Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE LOWER(LEFT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u')
   OR LOWER(RIGHT(CITY, 1)) NOT IN ('a', 'e', 'i', 'o', 'u');
```

## Notes

**Concepts learned:**

- DISTINCT: Removes duplicate city names.
- LEFT(): Extracts the first character of a string.
- RIGHT(): Extracts the last character of a string.
- LOWER(): Converts characters to lowercase.
- NOT IN: Checks whether a value does not match any item in a list.
- OR: Returns rows when at least one condition is true.
- WHERE: Filters rows based on specified conditions.

**Improvements:**

- Learned how to combine conditions involving the first and last characters of a string.
- Practiced using OR to evaluate alternative conditions.
- Understood the difference between OR and AND when combining filters.
- Improved my understanding of SQL string functions and duplicate removal.
- Practiced translating a question with multiple conditions into a SQL query.