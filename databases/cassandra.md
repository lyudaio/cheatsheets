# Cassandra cheatsheet for version 3.11.7

Apache Cassandra is a NoSQL database management system that provides high availability and scalability for handling large amounts of structured data. It is designed to handle big data workloads across multiple nodes without a single point of failure.

## Key concepts

- Cluster: A cluster is a set of nodes that work together to store and manage data.
- Node: A node is a single server that runs a Cassandra instance.
- Keyspace: A keyspace is a container for data in Cassandra, similar to a database in a relational database management system.
- Table: A table is a collection of columns and rows that represent data in Cassandra.
- Column: A column is a field in a Cassandra table.
- Partition Key: The partition key determines the node that stores the data in a Cassandra table.

## Basic SELECT statement

The SELECT statement is used to retrieve data from a Cassandra table.

```SQL
SELECT column1, column2, ...
FROM keyspace_name.table_name;
```

## SELECT with a WHERE clause

The WHERE clause is used to filter the results of a SELECT statement based on specified conditions.

```SQL
SELECT column1, column2, ...
FROM keyspace_name.table_name
WHERE condition;
```

## SELECT with an ORDER BY clause

The ORDER BY clause is used to sort the results of a SELECT statement.

```SQL
SELECT column1, column2, ...
FROM keyspace_name.table_name
ORDER BY column1 [ASC|DESC];
```

## SELECT with a GROUP BY clause

The GROUP BY clause is used to group the results of a SELECT statement based on the values of one or more columns.

```SQL
SELECT column1, SUM(column2), ...
FROM keyspace_name.table_name
GROUP BY column1;
```

## SELECT with a JOIN clause

Joining is not supported in Cassandra, instead you need to use denormalization techniques to store related data in the same table.

## Basic INSERT statement

The INSERT statement is used to insert data into a Cassandra table.

```SQL
INSERT INTO keyspace_name.table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

## Basic UPDATE statement

The UPDATE statement is used to modify data in a Cassandra table.

```SQL
UPDATE keyspace_name.table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

## Basic DELETE statement

The DELETE statement is used to delete data from a Cassandra table.

```SQL
DELETE FROM keyspace_name.table_name
WHERE condition;
```

## Additional Resources

- [Cassandra 3.11.7 Documentation](https://cassandra.apache.org/doc/latest/index.html)
