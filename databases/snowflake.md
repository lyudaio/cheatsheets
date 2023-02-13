# Snowflake Database Cheatsheet (Latest LTS Version: Unknown)

Snowflake is a cloud-based data warehousing platform that provides high performance, secure, and scalable data storage, querying and management capabilities. It is a fully managed service that operates on top of the Amazon Web Services (AWS) cloud infrastructure.

## Creating a Database

```sql
CREATE DATABASE <database_name>;
```

## Creating a Schema

```sql
CREATE SCHEMA <schema_name>;
```

## Creating a Table

```sql
CREATE TABLE <table_name> (
   <column_name_1> <data_type_1>,
   <column_name_2> <data_type_2>,
   ...
);
```

## Inserting Data into a Table

```sql
INSERT INTO <table_name> (column_1, column_2, ...)
VALUES (value_1, value_2, ...);
```

## Selecting Data from a Table

```sql
SELECT <column_1>, <column_2>, ...
FROM <table_name>;
```

## Updating Data in a Table

```sql
UPDATE <table_name>
SET <column_1> = <new_value_1>, <column_2> = <new_value_2>, ...
WHERE <condition>;
```

## Deleting Data from a Table

```sql
DELETE FROM <table_name>
WHERE <condition>;
```

## Joining Tables

```sql
SELECT <columns>
FROM <table_1>
JOIN <table_2>
ON <join_condition>;
```

## Grouping Data

```sql
SELECT <grouping_columns>, SUM(<aggregate_column>)
FROM <table_name>
GROUP BY <grouping_columns>;
```

For more information and a comprehensive guide on Snowflake, visit the [Official Documentation](https://docs.snowflake.com/en/index.html)
