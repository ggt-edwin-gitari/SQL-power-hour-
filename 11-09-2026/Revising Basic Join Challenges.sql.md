# SQL Practice Task 2

**Date:** 2026-11-09  
**Question Name:** Challenges  
**Link:** https://www.hackerrank.com/challenges/challenges/problem?isFullScreen=true 
**Difficulty:** Basic

## Intuition

We need to display each student's ID, name and total number of challenges created.

1. Join `Hackers` and `Challenges` using `hacker_id`.
2. Count the challenges created by each student.
3. Identify the maximum challenge count.
4. Identify challenge counts shared by multiple students.
5. Keep students with unique counts or the maximum count.
6. Sort by challenge count descending, then hacker ID ascending.

## Solution

```sql
SELECT
    h.hacker_id,
    h.name,
    COUNT(c.challenge_id) AS total_challenges
FROM Hackers h
JOIN Challenges c
    ON h.hacker_id = c.hacker_id
GROUP BY h.hacker_id, h.name
HAVING
    total_challenges = (
        SELECT MAX(challenge_count)
        FROM (
            SELECT COUNT(*) AS challenge_count
            FROM Challenges
            GROUP BY hacker_id
        ) AS counts
    )
    OR total_challenges NOT IN (
        SELECT challenge_count
        FROM (
            SELECT COUNT(*) AS challenge_count
            FROM Challenges
            GROUP BY hacker_id
        ) AS student_counts
        GROUP BY challenge_count
        HAVING COUNT(*) > 1
    )
ORDER BY total_challenges DESC, h.hacker_id ASC;
```

## Notes

**Concepts learned:**

- `JOIN`: Combines student details with their created challenges.
- `COUNT()`: Counts the challenges created by each student.
- `GROUP BY`: Groups challenges by each hacker.
- `HAVING`: Filters grouped results based on aggregate conditions.
- Subquery: Runs a query inside another query.
- `MAX()`: Finds the highest challenge count.
- `NOT IN`: Excludes challenge counts appearing in a specified list.
- `ORDER BY DESC`: Sorts challenge counts from highest to lowest.
- `ASC`: Sorts tied results by hacker ID in ascending order.
- Derived tables: Use the results of an inner query as a temporary table.

**Improvements:**

- Learn to distinguish unique counts from duplicated counts.
- Use `HAVING` when filtering results involving aggregate functions.
- Understand how nested subqueries work.
- Read exclusion conditions carefully, especially when the question makes exceptions for the maximum value.