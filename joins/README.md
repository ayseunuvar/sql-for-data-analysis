```text
SQL JOIN QUERIES

JOIN is used to combine rows from two or more tables based on a related column.

==================================================

SAMPLE TABLES

users
id | name
---|------
1  | Ali
2  | Ayse

orders
id | user_id | product
---|---------|---------
1  | 1       | Laptop
2  | 1       | Mouse
3  | 2       | Keyboard

==================================================

INNER JOIN
Returns only rows that have matching values in both tables.

SELECT users.name, orders.product
FROM users
INNER JOIN orders
ON users.id = orders.user_id;

Result:
- Only users who have orders

==================================================

LEFT JOIN
Returns all rows from the left table and matched rows from the right table.
If there is no match, NULL values are returned.

SELECT users.name, orders.product
FROM users
LEFT JOIN orders
ON users.id = orders.user_id;

Result:
- All users, even those without orders

==================================================

RIGHT JOIN
Returns all rows from the right table and matched rows from the left table.

SELECT users.name, orders.product
FROM users
RIGHT JOIN orders
ON users.id = orders.user_id;

Result:
- All orders, even if the user does not exist

==================================================

FULL OUTER JOIN
Returns all rows when there is a match in one of the tables.

SELECT users.name, orders.product
FROM users
FULL OUTER JOIN orders
ON users.id = orders.user_id;

Result:
- All users and all orders, NULL where no match exists

==================================================

NOTES
- INNER JOIN is the most commonly used JOIN
- LEFT JOIN keeps all records from the left table
- RIGHT JOIN keeps all records from the right table
- FULL OUTER JOIN keeps all records from both tables



