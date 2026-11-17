# SQL Practice Task 3

**Date:** 2026-11-09  
**Question Name:** Binary Tree Nodes  
**Link:** https://www.hackerrank.com/challenges/binary-search-tree-1/problem?isFullScreen=true 
**Difficulty:** Advanced

## Intuition

Each node has a value `N` and a parent value `P`.

We classify the nodes using three conditions:

1. Root: The parent value `P` is NULL.
2. Leaf: The node value `N` does not appear in the parent column `P`.
3. Inner: The node is neither a root nor a leaf.

Use `CASE WHEN` to check these conditions and `ORDER BY N` to sort the output.

## Solution

```sql
SELECT
    N,
    CASE
        WHEN P IS NULL THEN 'Root'
        WHEN N NOT IN (SELECT P FROM BST WHERE P IS NOT NULL)
            THEN 'Leaf'
        ELSE 'Inner'
    END AS Node_Type
FROM BST
ORDER BY N;
```

## Notes

**Concepts learned:**

- `CASE WHEN`: Evaluates multiple conditions and returns the matching result.
- `IS NULL`: Checks whether a column has no value.
- `NOT IN`: Checks whether a value does not appear in a specified list.
- Subquery: Runs a query inside another query.
- `SELECT P FROM BST`: Retrieves parent values to identify nodes with children.
- `ORDER BY`: Sorts the output by node value.
- `ELSE`: Handles nodes which do not match the root or leaf conditions.

**Improvements:**

- Check for NULL values using `IS NULL`, not `= NULL`.
- Exclude NULL values from the `NOT IN` subquery.
- Always check the Root condition first.
- Understand the relationship between a node and its parent when working with tree structures.