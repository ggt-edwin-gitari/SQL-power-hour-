# SQL Practice Task 04

**Date:** 2026-10-20  
**Question Name:** Top Competitors  
**Link:** https://www.hackerrank.com/challenges/full-score/problem?isFullScreen=false  
**Difficulty:** Basic

## Intuition

The question requires identifying hackers who achieved full scores in more than one challenge and ranking them according to the number of challenges completed with full scores.

My approach was to join four tables: Hackers, Submissions, Challenges, and Difficulty. These tables provide the hacker's details, submitted scores, challenge information, and maximum possible scores.

I used the WHERE clause to compare each submission's score against the maximum score for its challenge. I then grouped the results by hacker and used HAVING to filter hackers with full scores in more than one distinct challenge.

Finally, I sorted the results by the number of fully scored challenges in descending order and hacker_id in ascending order to resolve ties.

## Solution

```sql
SELECT
    h.hacker_id,
    h.name
FROM Hackers h
JOIN Submissions s
    ON h.hacker_id = s.hacker_id
JOIN Challenges c
    ON s.challenge_id = c.challenge_id
JOIN Difficulty d
    ON c.difficulty_level = d.difficulty_level
WHERE s.score = d.score
GROUP BY h.hacker_id, h.name
HAVING COUNT(DISTINCT s.challenge_id) > 1
ORDER BY
    COUNT(DISTINCT s.challenge_id) DESC,
    h.hacker_id ASC;
```

## Notes

**Concepts learned:**

- INNER JOIN: Combining related records from multiple tables using common columns.
- WHERE: Filtering submissions to identify scores equal to the maximum possible score.
- GROUP BY: Grouping records by hacker to calculate their performance.
- HAVING: Filtering grouped results based on aggregate conditions.
- COUNT(DISTINCT): Counting unique challenges without including duplicate full-score submissions.
- ORDER BY: Sorting results using multiple conditions, including descending and ascending order.
- Table aliases: Using shorter names to improve SQL readability.

**Improvements:**

- Improved my understanding of joining four related tables to retrieve information.
- Learned the difference between WHERE and HAVING when filtering individual records versus grouped results.
- Used COUNT(DISTINCT) to prevent multiple submissions for the same challenge from affecting the leaderboard.
- Practiced combining aggregation, filtering, and sorting in a single SQL query.
- Strengthened my ability to translate problem requirements into SQL conditions.