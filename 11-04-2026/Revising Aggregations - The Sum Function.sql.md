# SQL Practice Task 1

**Date:** 2026-11-04  
**Question Name:** Revising the Select Query III  
**Link:** https://www.hackerrank.com/challenges/revising-aggregations-sum/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires calculating the total population of all cities in the CITY table where the District is California.

I use the SUM() aggregate function to calculate the total population. The WHERE clause filters the records and selects only cities whose District value matches 'California'.

Since the question asks for the total population, I use SUM(Population) instead of COUNT(), which counts records.

## Solution

```sql
SELECT SUM(Population)
FROM CITY
WHERE District = 'California';
```

## Notes

**Concepts learned:**

- SUM(): Calculates the total of numerical values in a column.
- WHERE: Filters records based on specified conditions.
- Equality operator (=): Matches records with a specific value.
- Aggregate functions: Perform calculations across multiple records.
- String comparison: Filters records using text values such as district names.

**Improvements:**

- Learned how to calculate the total population using SUM().
- Practiced filtering records using a text-based condition.
- Understood the difference between COUNT() and SUM().
- Improved my ability to combine aggregate functions with WHERE.
- Practiced retrieving summarized data from a database table.