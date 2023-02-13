# OrientDB cheatsheet for version 4.1

OrientDB is a multi-model NoSQL database management system that supports graph, document, key-value, and object models. It is known for its high performance and scalability.

## Connecting to the database

The `orientdb` command-line tool is used to connect to an OrientDB database.

```SQL
orientdb> CONNECT remote:host/database_name root root
```

## Creating a class

A class in OrientDB represents a collection of records (documents or vertices) and can be thought of as a table in a relational database. The `CREATE CLASS` statement is used to create a new class in an OrientDB database.

```SQL
orientdb> CREATE CLASS class_name
```

## Creating a property

A property in OrientDB represents a field within a class. The `CREATE PROPERTY` statement is used to create a new property within a class.

```SQL
orientdb> CREATE PROPERTY class_name.property_name data_type
```

## Inserting data

The `INSERT INTO` statement is used to insert data into a class.

```SQL
orientdb> INSERT INTO class_name (property1, property2, ...) VALUES (value1, value2, ...)
```

## Updating data

The `UPDATE` statement is used to modify data within a class.

```SQL
orientdb> UPDATE class_name SET property1 = value1, property2 = value2 WHERE some_property = some_value
```

## Deleting data

The `DELETE` statement is used to remove data from a class.

```SQL
orientdb> DELETE FROM class_name WHERE some_property = some_value
```

## Querying data

The `SELECT` statement is used to retrieve data from a class.

```SQL
orientdb> SELECT property1, property2, ... FROM class_name WHERE some_property = some_value
```

## Traversing graph data

In OrientDB, graph data is stored as vertices and edges and can be queried using the `TRAVERSE` statement.

```SQL
orientdb> TRAVERSE * FROM (SELECT FROM class_name WHERE some_property = some_value)
```

## Additional Resources

- [OrientDB 4.1 Documentation](https://orientdb.com/docs/4.1.x/index.html)
