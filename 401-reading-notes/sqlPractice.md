# SQL Practice

## SELECT DATA

| Operator           | Condition                                            | SQL Example                   |
| ------------------ | ---------------------------------------------------- | ----------------------------- |
| =, !=, < <=, >, >= | Standard numerical operators                         | col_name != 4                 |
|=                   | Case sensitive exact string comparison (notice the single equals) | col_name = "abc" |
|!= or <>            | Case sensitive exact string inequality comparison | col_name != "abcd"|
| BETWEEN … AND …    | Number is within range of two values (inclusive)     | col_name BETWEEN 1.5 AND 10.5 |
| NOT BETWEEN … AND …| Number is not within range of two values (inclusive) | col_name NOT BETWEEN 1 AND 10 |
| IN (…)             | Number exists in a list                              | col_name IN (2, 4, 6)         |
| NOT IN (…)         | Number does not exist in a list                      | col_name NOT IN (1, 3, 5)     |
|LIKECase            | insensitive exact string comparison | col_name LIKE "ABC"|
|NOT LIKE            | Case insensitive exact string inequality comparison | col_name NOT LIKE "ABCD" |
|%                   | Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) | col_name LIKE "%AT%" (matches "AT", "ATTIC", "CAT" or even "BATS") |
|_                   | Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) | col_name LIKE "AN_"(matches "AND", but not "AN") |

### SELECT: select column from the table

### SELECT DISTINCT: blindly remove duplicate rows

### FROM: select which table to retreive data from

### WHERE: condition for the selected data

### ORDER BY: way to sort your results by a given column in ascending or descending order

### LIMIT: will reduce the number of rows to return

### OFFSET: the optional OFFSET will specify where to begin counting the number rows from

### INNER JOIN or JOIN: combine row data across two separate tables using this unique key

FORM:

```sql
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
```

---

## MODIFY DATA

---

### INSERT INTO:  inserting data into a database

FORM:

```SQL
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
```

OR:

```SQL
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
```

### UPDATE: update existing data

FORM:

```SQL
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;
```

### DELETE: delete data from a table in the database

FORM:

```SQL
DELETE FROM mytable
WHERE condition;
```

---

## TABLES

---

### CREATE TABLE

```SQL
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);
```

### ALTER TABLE: add, remove, or modify columns and table constraints

- Adding columns

```sql
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;
```

- Removing columns

```sql
ALTER TABLE mytable
DROP column_to_be_deleted;
```

- Renaming the table

```sql
ALTER TABLE mytable
RENAME TO new_table_name;
```

### DROP TABLE IF EXISTS mytable: Drop a table

```sql
DROP TABLE IF EXISTS mytable;
```

---

## EXAMPLES

---

```sql
SELECT column, another_column, …
FROM mytable;
```

```sql
SELECT * 
FROM mytable;
```

```sql
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```

```sql
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);
```

```sql
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;
```

```sql
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;
```

```sql
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;
```

```SQL
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
```

```SQL
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
```

```SQL
UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;
```

```SQL
DELETE FROM mytable
WHERE condition;
```

```SQL
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);
```

```sql
ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;
```

```sql
ALTER TABLE mytable
DROP column_to_be_deleted;
```

```sql
ALTER TABLE mytable
RENAME TO new_table_name;
```

```sql
DROP TABLE IF EXISTS mytable;
```

| Keyword | functionality | example |
| ------- | ------------- | ------- |
| SELECT  | select column from the table | SELECT column, another_column, …|
| SELECT DISTINCT | blindly remove duplicate rows | SELECT DISTINCT column, another_column, … |
| FROM | select which table to retreive data from | FROM mytable |
| WHERE | condition for the selected data | WHERE condition(s) |
| ORDER BY | way to sort your results by a given column in ascending or descending order | ORDER BY column, … ASC/DESC |
| LIMIT | will reduce the number of rows to return | LIMIT num_limit OFFSET num_offset |
| OFFSET | the optional OFFSET will specify where to begin counting the number rows from | LIMIT num_limit OFFSET num_offset |
| INNER JOIN or JOIN | combine row data across two separate tables using this unique key | INNER JOIN another_table --> ON mytable.id = another_table.id |
| INSERT INTO | inserting data into a database | INSERT INTO mytable --> (column, another_column, …) --> VALUES (value_or_expr, another_value_or_expr, …), --> (value_or_expr_2, another_value_or_expr_2, …),…; |
| UPDATE | update existing data | UPDATE mytable --> SET column = value_or_expr, other_column = another_value_or_expr,… --> WHERE condition; |
| DELETE | delete data from a table in the database | DELETE FROM mytable --> WHERE condition; |

<div class="datatable">
    <table class="table table-striped table-condensed">
        <tbody><tr>
            <td style="width: 30%">Data type</td>
            <td class="unhighlight">Description</td>
        </tr>
        <tr>
            <td><code>INTEGER</code>, <code>BOOLEAN</code></td>
            <td>The integer datatypes can store whole integer values like the count of a number or an
                age.  In some implementations, the boolean value is just represented as an integer value
                of just 0 or 1.</td>
        </tr>
        <tr>
            <td><code>FLOAT</code>, <code>DOUBLE</code>, <code>REAL</code></td>
            <td>The floating point datatypes can store more precise numerical data like measurements
                or fractional values.  Different types can be used depending on the floating point
                precision required for that value.</td>
        </tr>
        <tr>
            <td><code>CHARACTER(num_chars)</code>, <code>VARCHAR(num_chars)</code>, <code>TEXT</code></td>
            <td><p>The text based datatypes can store strings and text in all sorts of locales.  The distinction
                between the various types generally amount to underlaying efficiency of the database when working
                with these columns.</p>
                <p>Both the CHARACTER and VARCHAR (variable character) types are specified with
                the max number of characters that they can store (longer values may be truncated), so can be more
                efficient to store and query with big tables.</p></td>
        </tr>
        <tr>
            <td><code>DATE</code>, <code>DATETIME</code></td>
            <td>SQL can also store date and time stamps to keep track of time series and event data.  They can be
                tricky to work with especially when manipulating data across timezones.</td>
        </tr>
        <tr>
            <td><code>BLOB</code></td>
            <td>Finally, SQL can store binary data in blobs right in the database.  These values are often opaque
                to the database, so you usually have to store them with the right metadata to requery them.</td>
        </tr>
        <tr>
            <td colspan="2">Docs:
                <a href="http://dev.mysql.com/doc/refman/5.6/en/data-types.html" title="MySQL Data Types">MySQL</a>,
                <a href="http://www.postgresql.org/docs/9.4/static/datatype.html" title="Postgres Data Types">Postgres</a>,
                <a href="https://www.sqlite.org/datatype3.html" title="SQLite Data Types">SQLite</a>,
                <a href="https://msdn.microsoft.com/en-us/library/ms187752.aspx" title="Microsoft SQL Server Data Types">Microsoft SQL Server</a>
            </td>
        </tr>
    </tbody></table>
</div>
