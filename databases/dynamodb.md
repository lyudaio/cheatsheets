# DynamoDB cheatsheet for version 2022-08-06

Amazon DynamoDB is a fully managed NoSQL database service provided by Amazon Web Services (AWS). It is designed to provide fast and predictable performance with seamless scalability.

## Connecting to DynamoDB

To connect to DynamoDB, you will need an AWS account and access to the AWS Management Console. Once you have access, you can use the AWS CLI or the AWS SDK to interact with your DynamoDB tables.

## Creating a table

A table in DynamoDB is a collection of items, where each item represents a set of attributes. The `CREATE TABLE` command is used to create a new table in DynamoDB.

```DynamoDB
aws dynamodb create-table \
  --table-name table_name \
  --attribute-definitions AttributeName=attribute_name,AttributeType=S \
  --key-schema AttributeName=attribute_name,KeyType=HASH \
  --provisioned-throughput ReadCapacityUnits=5,WriteCapacityUnits=5
```

## Adding an item

An item in DynamoDB is a collection of attributes, where each attribute has a name and a value. The `PUT ITEM` command is used to add an item to a DynamoDB table.

```DynamoDB
aws dynamodb put-item \
  --table-name table_name \
  --item '{"attribute_name": {"S": "attribute_value"}}'
```

## Updating an item

The `UPDATE ITEM` command is used to modify an existing item in a DynamoDB table.

```DynamoDB
aws dynamodb update-item \
  --table-name table_name \
  --key '{"attribute_name": {"S": "attribute_value"}}' \
  --update-expression "SET attribute_name= :val" \
  --expression-attribute-values '{":val": {"S": "new_attribute_value"}}'
```

## Deleting an item

The `DELETE ITEM` command is used to remove an item from a DynamoDB table.

```DynamoDB
aws dynamodb delete-item \
  --table-name table_name \
  --key '{"attribute_name": {"S": "attribute_value"}}'
```

## Retrieving an item

The `GET ITEM` command is used to retrieve an item from a DynamoDB table.

```DynamoDB
aws dynamodb get-item \
  --table-name table_name \
  --key '{"attribute_name": {"S": "attribute_value"}}'
```

## Additional Resources

- [Amazon DynamoDB Developer Guide](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Welcome.html)
- [AWS CLI Command Reference for Amazon DynamoDB](https://docs.aws.amazon.com/cli/latest/reference/dynamodb/)
