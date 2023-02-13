# Redis cheatsheet for version 6.0.9

Redis (Remote Dictionary Server) is an in-memory data structure store that is used as a database, cache, and message broker. It supports various data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs, and geospatial indexes with radius queries.

## Basic SET and GET commands

The SET command is used to set a value in Redis, while the GET command is used to retrieve a value.

```Redis
SET key value
GET key
```

## Hashing values

The HMSET command is used to hash multiple key-value pairs, while the HGET command is used to retrieve a value from a hash.

```Redis
HMSET key field1 value1 field2 value2 ...
HGET key field
```

## Storing lists

The LPUSH command is used to add elements to a list from the left, while the RPUSH command is used to add elements to a list from the right. The LRANGE command is used to retrieve a range of elements from a list.

```Redis
LPUSH key value1 value2 ...
RPUSH key value1 value2 ...
LRANGE key start stop
```

## Storing sets

The SADD command is used to add elements to a set, while the SMEMBERS command is used to retrieve all elements in a set.

```Redis
SADD key value1 value2 ...
SMEMBERS key
```

## Storing sorted sets

The ZADD command is used to add elements to a sorted set, while the ZRANGE command is used to retrieve a range of elements from a sorted set based on their scores.

```Redis
ZADD key score1 value1 score2 value2 ...
ZRANGE key start stop [WITHSCORES]
```

## Transactions

The MULTI command is used to start a transaction, while the EXEC command is used to execute a transaction.

```Redis
MULTI
command1
command2
...
EXEC
```

## Additional Resources

- [Redis 6.0.9 Documentation](https://redis.io/documentation)
