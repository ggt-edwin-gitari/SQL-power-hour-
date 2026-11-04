# SQL Practice Task 2

**Date:** 2026-11-04  
**Question Name:** Average Population  
**Link:** https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires calculating the average population of all cities in the CITY table where the District is California.

I use the AVG() aggregate function to calculate the average population. The WHERE clause filters the records and selects only cities whose District value matches 'California'.

The AVG() function adds the population values and divides the total by the number of non-NULL population values.

## Solution

```sql
SELECT AVG(Population)
FROM CITY
WHERE District = 'California';
```

## Notes

**Concepts learned:**

- AVG(): Calculates the average of numerical values in a column.
- WHERE: Filters records based on specified conditions.
- Equality operator (=): Matches records with a specific value.
- Aggregate functions: Perform calculations across multiple records.
- NULL handling: AVG() ignores NULL values when calculating the average.

**Improvements:**

- Learned how to calculate averages using AVG().
- Practiced filtering records using a text-based condition.
- Understood the difference between SUM(), COUNT(), and AVG().
- Improved my understanding of aggregate functions.
- Practiced retrieving summarized data from a database table.