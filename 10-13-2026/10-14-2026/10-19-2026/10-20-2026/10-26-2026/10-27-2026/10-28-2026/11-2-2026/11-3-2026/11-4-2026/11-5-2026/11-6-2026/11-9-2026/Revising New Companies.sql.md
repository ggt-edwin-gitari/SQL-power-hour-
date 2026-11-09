# SQL Practice Task 1

**Date:** 2026-11-09  
**Question Name:** New Companies  
**Link:** https://www.hackerrank.com/challenges/the-company/problem?isFullScreen=true
**Difficulty:** Advanced

## Intuition

We need to retrieve each company's founder and count the unique records at every management level.

1. Start with the Company table.
2. Join the four hierarchy tables using `company_code`.
3. Count unique lead managers, senior managers, managers and employees.
4. Group the results by company code and founder.
5. Sort by company code in ascending alphabetical order.

Use `COUNT(DISTINCT column_name)` to prevent duplicate records from inflating the totals.

## Solution

```sql
SELECT
    c.company_code,
    c.founder,
    COUNT(DISTINCT lm.lead_manager_code),
    COUNT(DISTINCT sm.senior_manager_code),
    COUNT(DISTINCT m.manager_code),
    COUNT(DISTINCT e.employee_code)
FROM Company c
LEFT JOIN Lead_Manager lm
    ON c.company_code = lm.company_code
LEFT JOIN Senior_Manager sm
    ON c.company_code = sm.company_code
LEFT JOIN Manager m
    ON c.company_code = m.company_code
LEFT JOIN Employee e
    ON c.company_code = e.company_code
GROUP BY c.company_code, c.founder
ORDER BY c.company_code ASC;
```

## Notes

**Concepts learned:**

- `JOIN`: Combines records from multiple tables.
- `LEFT JOIN`: Keeps every company, even when no matching records exist in another table.
- `ON`: Specifies the condition used to match records between tables.
- `COUNT()`: Counts records or non-NULL values.
- `COUNT(DISTINCT)`: Counts unique values and prevents duplicate counting.
- `GROUP BY`: Groups results by company.
- `ORDER BY ASC`: Sorts company codes alphabetically.
- Table aliases (`c`, `lm`, `sm`, `m`, `e`): Shorten table references and make queries easier to read.

**Improvements:**

- Use `COUNT(DISTINCT)` when joining tables with one-to-many relationships.
- Use `LEFT JOIN` when you need to retain all records from the main table.
- Group by every non-aggregated column in the SELECT statement.
- Remember that company codes are strings, so ascending order is alphabetical rather than numeric.