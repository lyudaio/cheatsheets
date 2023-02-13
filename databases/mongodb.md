# MongoDB cheatsheet for version 4.4.7

MongoDB is a NoSQL database management system that provides high scalability and performance for handling large amounts of unstructured or semi-structured data.

## Key concepts

- Collection: A collection is a group of MongoDB documents.
- Document: A document is a set of key-value pairs that represent data in MongoDB.
- Key: A key is the name of a field in a MongoDB document.
- Value: A value is the data stored in a field of a MongoDB document.
- BSON: BSON is a binary format for representing MongoDB documents.

## Basic SELECT statement

The find() method is used to retrieve data from a MongoDB collection.

```JavaScript
db.collection_name.find({});
```

## SELECT with a WHERE clause

The find() method with a filter parameter is used to filter the results of a MongoDB query based on specified conditions.

```JavaScript
db.collection_name.find({ key: value });
```

## SELECT with a LIMIT clause

The limit() method is used to limit the number of results returned by a MongoDB query.

```JavaScript
db.collection_name.find({}).limit(n);
```

## SELECT with a SORT clause

The sort() method is used to sort the results of a MongoDB query based on the values of one or more fields.

```JavaScript
db.collection_name.find({}).sort({ key: 1 });
```

## SELECT with a JOIN clause

Joining is not supported in MongoDB, instead you need to use embedded documents or manual referencing to store related data in the same document.

## Basic INSERT statement

The insertOne() method is used to insert a single document into a MongoDB collection.

```JavaScript
db.collection_name.insertOne({ key: value, ... });
```

## Basic UPDATE statement

The updateOne() method is used to modify a single document in a MongoDB collection.

```JavaScript
db.collection_name.updateOne({ key: value }, { $set: { newKey: newValue } });
```

## Basic DELETE statement

The deleteOne() method is used to delete a single document from a MongoDB collection.

```JavaScript
db.collection_name.deleteOne({ key: value });
```

## Additional Resources

- [MongoDB 4.4.7 Documentation](https://docs.mongodb.com/manual/release-notes/4.4/#4.4.7)
