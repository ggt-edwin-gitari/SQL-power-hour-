# SQL Practice Task 27

**Date:** 2026-11-09  
**Question Name:** Type of Triangle  
**Link:** https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

Use a `CASE` statement to classify each record based on the three side lengths: A, B and C.

First, check whether the sides form a valid triangle. The sum of any two sides must be greater than the third side.

Then classify valid triangles:

- Equilateral: All three sides are equal.
- Isosceles: Exactly two sides are equal.
- Scalene: All three sides are different.

## Solution

```sql
SELECT
    CASE
        WHEN A + B <= C OR A + C <= B OR B + C <= A
            THEN 'Not A Triangle'
        WHEN A = B AND B = C
            THEN 'Equilateral'
        WHEN A = B OR A = C OR B = C
            THEN 'Isosceles'
        ELSE 'Scalene'
    END
FROM TRIANGLES;
```

## Notes

**Concepts learned:**

- `CASE WHEN`: Evaluates conditions and returns a result based on the first matching condition.
- `AND`: Requires all conditions to be true.
- `OR`: Requires at least one condition to be true.
- `<=`: Checks whether a value is less than or equal to another value.
- `ELSE`: Handles records which do not match the earlier conditions.

**Improvements:**

- Always check triangle validity before classifying its type.
- Remember the triangle inequality rule: the sum of any two sides must exceed the third side.
- Order `CASE` conditions carefully because SQL returns the first matching result.