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

NOTES
- INNER JOIN is the most commonly used JOIN
- LEFT JOIN is safer when you want to keep all records from the main table

### ✅ What this gives you
- ONE **Copy** button
- Click once → **everything is copied**
- Works exactly the way you want on GitHub

---

## Common mistake (why “update joins” didn’t copy)

If you had something like this:

```md
# SQL JOIN
Some explanation

```sql
SELECT ...

Then:
- Copy on SQL block ❌ → only SQL
- Explanation ❌ not included

That’s why.

---

## Recommended commit message

Use one of these:


or


---

## One-line summary

> If you want **one copy button → one code block → everything inside it**.

If you want, next we can:
- Apply this **same single-block style** to `basics`
- Do `GROUP BY / HAVING`
- Design a **consistent SQL learning repo structure**

Just tell me.

