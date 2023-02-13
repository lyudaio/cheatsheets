# Neo4j cheatsheet for version 4.2.0

Neo4j is a graph database management system that provides an ACID-compliant transactional backend for your applications. It allows you to store and retrieve data as nodes and relationships, which can be queried and analyzed to reveal patterns and insights.

## Connecting to Neo4j

To connect to a Neo4j database, you can use the Neo4j Browser or the Neo4j Driver API, which is available in multiple programming languages.

## Creating a node

A node in Neo4j is a unit of data that represents an entity or an object. The following Cypher query creates a node with the label `Person` and properties `name` and `age`.

```Neo4j
CREATE (n:Person {name: "John Doe", age: 30})
```

## Creating a relationship

A relationship in Neo4j connects two nodes and has a type and direction. The following Cypher query creates a relationship of type `KNOWS` between two nodes with the `Person` label.

```Neo4j
MATCH (a:Person), (b:Person)
WHERE a.name = "John Doe" AND b.name = "Jane Doe"
CREATE (a)-[r:KNOWS]->(b)
```

## Querying data

The Cypher query language is used to retrieve data from a Neo4j database. The following query retrieves all nodes with the label `Person` and returns their `name` and `age` properties.

```Neo4j
MATCH (n:Person)
RETURN n.name, n.age
```

## Updating data

The following Cypher query updates the `age` property of a node with the label `Person` and the name `John Doe`.

```Neo4j
MATCH (n:Person)
WHERE n.name = "John Doe"
SET n.age = 31
```

## Deleting data

The following Cypher query deletes a node with the label `Person` and the name `John Doe`.

```Neo4j
MATCH (n:Person)
WHERE n.name = "John Doe"
DELETE n
```

## Additional Resources

- [Neo4j Developer Documentation](https://neo4j.com/developer/)
- [Cypher Query Language Reference](https://neo4j.com/docs/cypher-refcard/current/)
- [Neo4j Driver API for multiple programming languages](https://neo4j.com/developer/drivers-complex/)
