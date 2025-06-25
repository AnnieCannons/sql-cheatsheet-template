# PostgreSQL Cheatsheet

---

## 💠 PostgreSQL Terminology 

**1. SQL is...**
a programming language designed to manipulate and manage data stored in relational databases

**2. A relational database is...**
a database that organizes information into one or more tables.

**3. A clause is ...**
a built-in function in SQL that performs a specific task. `SELECT`, `CREATE TABLE`, `FROM`, and `WHERE` are all examples of claues. By convention, clauses are written in capital letters. Clauses are also often called commands.

**4. A constraint is...**
a rule that limits the data type that can be stored in a column. This ensures the accuracy and reliability of the data in the table.

---

## 💠 PostgreSQL Constraints 

### 1. `PRIMARY KEY`

Description: Specifies that this column uniquely identifies each row/record in a database table.	

### 2. `NOT NULL`

Description: Ensures that a column cannot have a NULL value.	

### 3. `UNIQUE`

Description: Ensures that all values in a column are different.	

---

## 💠 PostgreSQL Clauses

### 1. `SELECT` 

Description: `SELECT *` returns all columns from the provided table. You can also do `SELECT column_name_1, column_name_2` to return specific columns from the provided table. 

Example:
```sql
SELECT *
FROM movies;
```

### 2. `CREATE TABLE` 

Description: `CREATE TABLE` creates a new table in a database. It allows one to specify the name of the table, the name of each column, and each column's data type in the table.

Example:
```sql
CREATE TABLE friends (
  friend_id SERIAL PRIMARY KEY,
  name TEXT,
  birthday DATE
);
```

### 3. `INSERT INTO` — assigned to Andy 

Description:

Example:
```sql

```

### 4. `UPDATE` — assigned to Bakari

Description:

Example:
```sql

```
### 5. `DELETE FROM` — assigned to Cassy

Description:

Example:
```sql

```
### 6. `GROUP BY` — assigned to Dharshina

Description:

Example:
```sql

```
### 7. `ORDER BY` — assigned to Hunter

Description:

Example:
```sql

```

### 8. `INNER JOIN` — assigned to Makeba

Description:

Example:
```sql

```
