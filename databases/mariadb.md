# MariaDB cheatsheet for version 10.5.9

MariaDB is an open-source relational database management system that is a fork of the MySQL database system. It provides a wide range of features, performance, and scalability.

## Basic SELECT statement

The SELECT statement is used to retrieve data from a MariaDB database.

```SQL
SELECT * FROM table_name;
```

## SELECT with a WHERE clause

The WHERE clause is used to filter the results of a SELECT statement based on specified conditions.

```SQL
SELECT * FROM table_name WHERE column_name = value;
```

## SELECT with a LIMIT clause

The LIMIT clause is used to limit the number of results returned by a SELECT statement.

```SQL
SELECT * FROM table_name LIMIT n;
```

## SELECT with a SORT clause

The ORDER BY clause is used to sort the results of a SELECT statement based on the values of one or more columns.

```SQL
SELECT * FROM table_name ORDER BY column_name ASC/DESC;
```

## SELECT with a JOIN clause

The JOIN clause is used to combine data from multiple tables based on a related column.

```SQL
SELECT * FROM table1
JOIN table2
ON table1.column_name = table2.column_name;
```

## Basic INSERT statement

The INSERT INTO statement is used to insert data into a MariaDB database.

```SQL
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

## Basic UPDATE statement

The UPDATE statement is used to modify data in a MariaDB database.

```SQL
UPDATE table_name
SET column_name = value
WHERE column_name = value;
```

## Basic DELETE statement

The DELETE statement is used to delete data from a MariaDB database.

```SQL
DELETE FROM table_name
WHERE column_name = value;
```

## Additional Resources

- [MariaDB 10.5.9 Documentation](https://mariadb.com/docs/10.5/)
