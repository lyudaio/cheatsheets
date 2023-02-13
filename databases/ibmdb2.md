# IBM DB2 cheatsheet for version 11.5

IBM DB2 is a relational database management system (RDBMS) developed by IBM. It is commonly used for enterprise data management and supports multiple operating systems, including Windows, Linux, and Unix.

## Connecting to the database

The `db2` command-line tool is used to connect to a DB2 database.

```SQL
db2 connect to database_name user username using password
```

## Creating a table

The `CREATE TABLE` statement is used to create a new table in a DB2 database.

```SQL
CREATE TABLE table_name (
  column1_name column1_datatype,
  column2_name column2_datatype,
  ...
);
```

## Inserting data

The `INSERT INTO` statement is used to insert data into a table.

```SQL
INSERT INTO table_name (column1_name, column2_name, ...)
VALUES (value1, value2, ...);
```

## Updating data

The `UPDATE` statement is used to modify data in a table.

```SQL
UPDATE table_name
SET column1_name = value1,
    column2_name = value2,
    ...
WHERE some_column = some_value;
```

## Deleting data

The `DELETE` statement is used to remove data from a table.

```SQL
DELETE FROM table_name WHERE some_column = some_value;
```

## Querying data

The `SELECT` statement is used to retrieve data from a table.

```SQL
SELECT column1_name, column2_name, ...
FROM table_name
WHERE some_column = some_value;
```

## Joining tables

The `JOIN` clause is used to combine rows from two or more tables based on a related column between them.

```SQL
SELECT column1_name, column2_name, ...
FROM table1_name
JOIN table2_name
ON table1_name.related_column = table2_name.related_column;
```

## Additional Resources

- [IBM DB2 11.5 Documentation](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.5.0/com.ibm.db2.luw.sql.ref.doc/doc/r0001975.html)
