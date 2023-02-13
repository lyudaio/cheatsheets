# Elasticsearch cheatsheet for version 7.10

Elasticsearch is a distributed, open source search and analytics engine designed for handling large amounts of data. It can be used for full-text search, structured search, analytics, and more.

## Connecting to Elasticsearch

To connect to Elasticsearch, you can use the REST API, which is available over HTTP, or a variety of client libraries that are available in multiple programming languages.

## Creating an index

The following API request creates an index named `people` with a single type named `person`.

```Elasticsearch
PUT /people
{
  "mappings": {
    "person": {
      "properties": {
        "id": { "type": "integer" },
        "name": { "type": "text" },
        "age": { "type": "integer" },
        "email": { "type": "text" }
      }
    }
  }
}
```

## Inserting data

The following API request inserts a new document into the `people` index with a type of `person`.

```Elasticsearch
POST /people/person
{
  "id": 1,
  "name": "John Doe",
  "age": 30,
  "email": "johndoe@example.com"
}
```

## Updating data

The following API request updates the `age` of a person with the `id` of 1.

```Elasticsearch
POST /people/person/1/_update
{
  "doc": { "age": 31 }
}
```

## Deleting data

The following API request deletes a person with the `id` of 1.

```Elasticsearch
DELETE /people/person/1
```

## Querying data

The following API request retrieves all documents from the `people` index with a type of `person`.

```Elasticsearch
GET /people/person/_search
```

## Additional Resources

- [Elasticsearch Documentation](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
- [Elasticsearch API Reference](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
- [Elasticsearch Client Library for multiple programming languages](https://www.elastic.co/guide/en/elasticsearch/client/index.html)
