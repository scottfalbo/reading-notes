# 301 Read-08: SQL Structured Query Language
[SQL lesson](https://sqlbolt.com/)<br>

*1-4*
## SQL

> SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database.

> A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

### Select Queries
+ To retrieve from a SQL database we use `SELECT` statements, or *queries*.
  + A query declares what data we are looking for, where to find it in the database, and optionally, how to transform it.
  + ```
    SELECT column, column_two, ...
    FROM tableName;
    ```
  + `SELECT *` would retrieve all columns

### Queries with constraints

+ The `WHERE` clause is used to filter return results. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
  + ```
    SELECT column01, column02, ...
    FROM tableName
    WHERE //condition
      AND/OR //another condition
      AND/OR //another..;
    ```
  + Get data from a specific row, `WHERE id = #;`
  + `WHERE id BETWEEN 1 AND 5` will select rows based on id number.
  + Standard numerical operators, `=, !=, <, <=, >, >=`
  + Within a range of two values, `col_name BETWEEN x AND y`
  + Not within range, `col_name NOT BETWEEN x AND y`
  + Exists within a list, `col_name IN(x, y, z)`
  + Does not exist, `col_name NOT IN(x, y, z)`
    + *What is existence?*
+ **More comparison operators**
  + `LIKE ""` case insensitive exact string comparison
    + `NOT LIKE ""`
  + `%` Used anywhere in a string to match a sequence of zero or more characters.
    + `column LIKE "%AB%"` matches anything with 'AB' in it.
  + `_` Used anywhere in a string to match a single character.
    + `column LIKE "AN_"` would return 'AND' but not 'AN'.
  + `IN(str)` String exists in a list. `column IN("A", "Z")`
    + `NOT IN`

### Filtering and Sorting

+ `DISTINCT` is a convenient way to discard rows that have duplicate column values.
+ `ORDER BY` sorts results by a given column in ascending or descending order.
  + `ORDER BY columnName <ASC/DESC>`
  + Each row is sorted alpha-numerically based on the specified columns value.
  + `LIMIT` will reduce the number of rows returned
  + `OFFSET` will specify where to begin counting the rows from
  + `LIMIT <x> OFFSET <y>`
+ ```
  SELECT column, columnTwo
  FROM tableName
  WHERE condition(s)
  ORDER BY column <ASC/DESC>
  LIMIT <x> OFFSET <y>;
  ```

## Schema
*13-18*

> The database schema is what describes the structure of each table, and the datatypes that each column of the table can contain.

+ `INSERT` allows us to insert new data into the database
  + ```
    INSERT INTO tableName
    (column01, column02)
    VALUES (value1, value2);
    ```

+ `UPDATE` can update existing data in a table
  + ```
    UPDATE tableName
    SET column = value,
        column2 = value2
    WHERE <condition>;
    ```  
  + > One helpful tip is to always write the constraint first and test it in a SELECT query to make sure you are updating the right rows, and only then writing the column/value pairs to update.


+ `DELETE` delete row(s)
  + ```
    DELETE FROM tableName
    WHERE condition;
    ```

+ `CREATE TABLE`

[Back to the main page](../README.md) 