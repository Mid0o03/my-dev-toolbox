# SQL Basics

## Basic Queries
- `SELECT * FROM table;`
- `INSERT INTO table (col1, col2) VALUES (val1, val2);`
- `UPDATE table SET col1 = val1 WHERE id = 1;`
- `DELETE FROM table WHERE id = 1;`

## Joins
- `INNER JOIN`: Matches in both tables.
- `LEFT JOIN`: All from left + matches from right.
- `RIGHT JOIN`: All from right + matches from left.
- `FULL OUTER JOIN`: All rows when there is a match in one of the tables.

## Constraints
- `PRIMARY KEY`: Unique identifier.
- `FOREIGN KEY`: Link between two tables.
- `UNIQUE`: Ensure all values in a column are different.
- `NOT NULL`: Ensure a column cannot have a NULL value.

## Aggregations
- `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`
- `GROUP BY`: Group rows that have the same values.
- `HAVING`: Filter groups.
