# SQL Practice Task 2

**Date:** 2026-11-09  
**Question Name:** Occupations  
**Link:** https://www.hackerrank.com/challenges/occupations/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

We need to transform rows into four columns: Doctor, Professor, Singer and Actor.

1. Use `ROW_NUMBER()` to assign a number to each name within its occupation, sorted alphabetically.
2. Use `CASE WHEN` to place each name into its corresponding occupation column.
3. Use `MAX()` to combine the names sharing the same row number.
4. Group by the row number to produce the final output.

## Solution

```sql
SELECT
    MAX(CASE WHEN Occupation = 'Doctor' THEN Name END) AS Doctor,
    MAX(CASE WHEN Occupation = 'Professor' THEN Name END) AS Professor,
    MAX(CASE WHEN Occupation = 'Singer' THEN Name END) AS Singer,
    MAX(CASE WHEN Occupation = 'Actor' THEN Name END) AS Actor
FROM (
    SELECT
        Name,
        Occupation,
        ROW_NUMBER() OVER (
            PARTITION BY Occupation
            ORDER BY Name
        ) AS row_num
    FROM OCCUPATIONS
) AS ranked
GROUP BY row_num
ORDER BY row_num;
```

## Notes

**Concepts learned:**

- `ROW_NUMBER()`: Assigns a sequential number to each row.
- `OVER()`: Defines the window used by a window function.
- `PARTITION BY`: Restarts row numbering for each occupation.
- `ORDER BY`: Sorts names alphabetically within each occupation.
- `CASE WHEN`: Places names into the correct occupation column.
- `MAX()`: Retrieves the non-NULL name for each occupation and row number.
- `GROUP BY`: Combines records sharing the same row number.
- `NULL`: Appears when an occupation has fewer names than another occupation.

**Improvements:**

- Learn conditional aggregation using `CASE WHEN` with aggregate functions.
- Understand the difference between `ROW_NUMBER()` and `RANK()`.
- Practise converting rows into columns using SQL pivot techniques.