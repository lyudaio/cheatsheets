# SQL Server cheatsheet for version 2022

SQL Server is a relational database management system (RDBMS) developed by Microsoft. It is commonly used for data warehousing, business intelligence, and web-based application development.

## Connecting to the database

The `sqlcmd` command-line tool is used to connect to a SQL Server database.

```SQL
sqlcmd -S server_name -U username -P password
```

## Creating a table

The `CREATE TABLE` statement is used to create a new table in a SQL Server database.

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

- [SQL Server 2022 Documentation](https://docs.microsoft.com/en-us/sql/sql-server/sql-server-technical-documentation?view=sql-server-ver15)
