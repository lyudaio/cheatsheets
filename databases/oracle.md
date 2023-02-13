# Oracle Database cheatsheet for version 21c

Oracle Database is a widely-used relational database management system (RDBMS) that offers a high level of reliability, security, and scalability. It provides powerful features for data warehousing, OLAP, and business intelligence, as well as web-based application development.

## Connecting to the database

The `sqlplus` command-line tool is used to connect to an Oracle database.

```SQL
sqlplus username/password@connection_identifier
```

## Creating a table

The `CREATE TABLE` statement is used to create a new table in an Oracle database.

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

- [Oracle Database 21c Documentation](https://docs.oracle.com/en/database/oracle/oracle-database/21/index.html)
