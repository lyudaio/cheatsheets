# FirebirdSQL cheatsheet for version 4.0

FirebirdSQL is a relational database management system that supports SQL and is known for its high performance and stability. It can run on multiple operating systems, including Windows, Linux, and macOS.

## Connecting to FirebirdSQL

To connect to a FirebirdSQL database, you can use the `isql` command-line tool or a variety of client libraries that are available in multiple programming languages.

## Creating a table

The following SQL statement creates a table named `people` with columns for `id`, `name`, `age`, and `email`.

```FirebirdSQL
CREATE TABLE people (
  id INTEGER NOT NULL PRIMARY KEY,
  name VARCHAR(100),
  age INTEGER,
  email VARCHAR(100)
);
```

## Inserting data

The following SQL statement inserts a new row into the `people` table.

```FirebirdSQL
INSERT INTO people (id, name, age, email)
VALUES (1, 'John Doe', 30, 'johndoe@example.com');
```

## Updating data

The following SQL statement updates the `age` of a person with the `id` of 1.

```FirebirdSQL
UPDATE people
SET age = 31
WHERE id = 1;
```

## Deleting data

The following SQL statement deletes a person with the `id` of 1.

```FirebirdSQL
DELETE FROM people
WHERE id = 1;
```

## Querying data

The following SQL statement retrieves all rows from the `people` table.

```FirebirdSQL
SELECT * FROM people;
```

## Additional Resources

- [FirebirdSQL Documentation](https://firebirdsql.org/en/reference-manuals/)
- [FirebirdSQL Client Library for multiple programming languages](https://firebirdsql.org/en/development-libraries/)
- [FirebirdSQL User Guide](https://firebirdsql.org/en/user-guide/)
