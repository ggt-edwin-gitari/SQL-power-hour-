# SQL Practice” Task 03
 
- **Date:** 2026-10-13
- **Question Name:The PADS**
- **Link:https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=false**
- **Difficulty:** / Medium /
 
## Intuition
 
The problem requires us to generate two result sets from the OCCUPATIONS table.

First result set: Display all names in alphabetical order, followed by the first letter of their occupation in parentheses. We can use CONCAT() to combine the name with the first letter of the occupation, and ORDER BY Name to sort the results alphabetically.

Second result set: Count how many people belong to each occupation. We use COUNT(*) to count the records, GROUP BY Occupation to group people by their professions, and ORDER BY to sort by the count in ascending order and then alphabetically by occupation when counts are equal. We also use LOWER() to display occupation names in lowercase.
 
## Solution
 
``sql
SELECT CONCAT(Name, '(', LEFT(Occupation, 1), ')')
FROM OCCUPATIONS
ORDER BY Name;

SELECT CONCAT(
    'There are a total of ',
    COUNT(*), ' ',
    LOWER(Occupation), 's.'
)
FROM OCCUPATIONS
GROUP BY Occupation
ORDER BY COUNT(*) ASC, Occupation ASC;
 
``
 
## Notes
 
- **Concepts learned:Concepts Learnt
CONCAT() — combines strings into a single output.

LEFT(Occupation, 1) — extracts the first letter of an occupation.

ORDER BY — sorts results alphabetically or numerically.

COUNT(*) — counts the number of records.

GROUP BY — groups rows with the same occupation for aggregation.

LOWER() — converts occupation names to lowercase.

Multiple-column sorting — ORDER BY COUNT(*) ASC, Occupation ASC sorts by count first, then alphabetically to break ties.**
- **Improvements: I learned how to format query output using string functions, aggregate records using COUNT() and GROUP BY, and sort grouped results using multiple criteria. I need to do more research on the same **
 