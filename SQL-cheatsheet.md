# PostgreSQL Cheatsheet

Each student will complete the Description and Example sections for the SQL clause assigned to them.

For each clause:

1. In the **Description**, explain what the clause does in plain language.main
2. In the **Example**, write a working SQL statement that shows how the clause is used (like the `SELECT and `CREATE TABLE` examples below).
3. As a reference, `SELECT` and `CREATE TABLE` are already done for you.

---

### 1. `SELECT`


2. In the **Example**, write a working SQL statement that shows how the clause is used (like the `SELECT` and `CREATE TABLE` examples below).
3. As a reference, `SELECT` and `CREATE TABLE` are already done for you. 
   

**Description:** `SELECT *` returns all columns from the provided table. You can also do `SELECT column_name_1, column_name_2` to return specific columns from the provided table.

**Example:**

```sql
SELECT *
FROM movies;
```

### 2. `CREATE TABLE`

**Description:** `CREATE TABLE` creates a new table in a database. It allows one to specify the name of the table, the name of each column, and each column's data type in the table.

**Example:**

```sql
CREATE TABLE friends (
  friend_id SERIAL PRIMARY KEY,
  name TEXT,
  birthday DATE
);
```

### 3. `INSERT INTO` — assigned to Andy

**Description:** `INSERT INTO` is used to add new rows of data to a table. Used with VALUES, which specifies the data in the rows to be added.

**Example:**

```sql
INSERT INTO mytable (col1, col2, col3, col4, col5)
VALUES (val1, val2, val3, val4, val5), (val_1, val_2, val_3, val_4, val_5);
```

### 4. `UPDATE` — assigned to Bakari

**Description:**

The update statement modefies existing dara that is recorded in a table.

**Example:**


```sql
update my_table set user_name = some_new_value;
-- or
update table1 set column_name = value where (condition)
```

### 5. `DELETE FROM` — assigned to Cassy

**Description:**
this is used to remove one or more rows from a table with givin condtions and you can also use WHERE but it will deleate all rows from table
**Example:**


```sql
 main

```sql
DELETE FROM Members
WHERE surname = 'Captain Underpants';
```

### 6. `GROUP BY` — assigned to Dharshina

**Description:**
The SQL GROUP BY clause is used to organize rows in a table that have the same values in specified columns into groups. This is particularly useful when combined with aggregate functions like COUNT(), SUM(), AVG(), MIN(), and MAX() to perform calculations on each group.
**Example:**


```sql
SELECT colors, COUNT(*) AS number_of_socks
FROM socks
GROUP BY colors;
```

### 7. `ORDER BY` — assigned to Hunter

**Description:**
`SELECT name, birth_date FROM stuudents` returns the `name` and `birth_date` columns from the `stuudents` TABLE. `ORDER BY birth_date DESC` looks at the `birth_date` column and puts it in decending order. This means the oldest will be the first on the list.

**Example:**

```sql

SELECT name, birth_date
FROM students
ORDER BY birth_date DESC;

```

### 8. `INNER JOIN` — assigned to Makeba

**The JOIN clause allows for the return of results from more than one table by joining them together with other results based on common column values specified using an ON clause. INNER JOIN is the default JOIN and it will only return results matching the condition specified by ON.:**

**Example:**

```sql
SELECT *
FROM books
JOIN authors
  ON books.author_id = authors.id;
```

### `OUTER JOIN` -

**An OUTER JOIN will combine rows from different tables even if the join condition is not met. In a `LEFT JOIN`, every row in the left table is returned in the result set, and if the join condition is not met, then NULL values are used to fill in the columns from the right table.**

**Example:**

```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2
  ON table1.column_name = table2.column_name;
```

### 9. `LIMIT`

**Description:**
The LIMIT clause is used to narrow, or limit, a result set to the specified number of rows. The given query will limit the result set to 5 rows.

**Example:**

```sql
SELECT *
FROM movies
LIMIT 5;
```

### 10. `LIKE`

**Description:**
The `LIKE` operator can be used inside of a `WHERE` clause to match a specified pattern.

**Example:**

```sql
SELECT name
FROM movies
WHERE name LIKE 'Star%';
```

The given query will match any movie that begins with Star in its title.
