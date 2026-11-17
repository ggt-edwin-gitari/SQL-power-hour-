SQL Practice Task 1

Date: 2026-11-17

Question Name: The Blunder

Link: https://www.hackerrank.com/challenges/the-blunder/problem?isFullScreen=true 

Difficulty: Basic

Database: MySQL

Intuition

Samantha calculated the average salary after accidentally removing every zero from each employee's salary.

We need to calculate two averages:

Actual average salary using the original Salary values.

Incorrect average salary after removing zeros using REPLACE().

Next, subtract the incorrect average from the actual average and use CEIL() to round the result up to the next integer.

Solution

SELECT
    CEIL(
        AVG(Salary) - AVG(REPLACE(Salary, '0', ''))
    )
FROM EMPLOYEES;



