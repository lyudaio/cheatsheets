# SQL cheatsheet for MySQL 8.0

SQL (Structured Query Language) is a standard language used to manage relational databases and perform various operations on data stored in these databases. MySQL is an open-source relational database management system that implements the SQL language.

## Basic SELECT statement

The SELECT statement is used to retrieve data from a table in a database.

```SQL
SELECT column1, column2, ...
FROM table_name;
```

## SELECT with a WHERE clause

The WHERE clause is used to filter the results of a SELECT statement based on certain conditions.

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

## SELECT with an ORDER BY clause

The ORDER BY clause is used to sort the results of a SELECT statement.

```SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC];
```

## SELECT with a GROUP BY clause

The GROUP BY clause is used to group the results of a SELECT statement based on the values of one or more columns.

```SQL
SELECT column1, SUM(column2), ...
FROM table_name
GROUP BY column1;
```

## SELECT with a JOIN clause

The JOIN clause is used to combine rows from two or more tables based on a related column between them.

```SQL
SELECT column1, column2, ...
FROM table1
JOIN table2
ON table1.column = table2.column;
```

## Basic INSERT statement

The INSERT statement is used to insert data into a table.

```SQL
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

## Basic UPDATE statement

The UPDATE statement is used to modify data in a table.

```SQL
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

## Basic DELETE statement

The DELETE statement is used to delete data from a table.

```SQL
DELETE FROM table_name
WHERE condition;
```

## Additional Resources

- [MySQL 8.0 Documentation](https://dev.mysql.com/doc/refman/8.0/)
