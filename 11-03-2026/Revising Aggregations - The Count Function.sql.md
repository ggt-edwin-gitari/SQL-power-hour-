# SQL Practice Task 21

**Date:** 2026-11-03  
**Question Name:** Revising the Select Query II  
**Link:** https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

The question requires counting the number of cities in the CITY table whose population is greater than 100,000.

I use the COUNT() aggregate function to count the number of city records. The WHERE clause filters the records and selects only cities whose Population exceeds 100,000.

Since the question asks for a count rather than individual city names, I only need one SELECT statement with COUNT(*) and a WHERE condition.

## Solution

```sql
SELECT COUNT(*)
FROM CITY
WHERE Population > 100000;
```

## Notes

**Concepts learned:**

- COUNT(): Counts the number of records returned by a query.
- COUNT(*): Counts all rows, including rows containing NULL values.
- WHERE: Filters records based on specified conditions.
- Greater than (>): Selects values exceeding a specified number.
- Aggregate functions: Perform calculations across multiple records and return a single result.

**Improvements:**

- Practiced counting records based on a numerical condition.
- Improved my understanding of COUNT(*) and aggregate functions.
- Learned how to combine WHERE with COUNT().
- Practiced filtering database records using comparison operators.
- Strengthened my ability to retrieve summarized information from a database.