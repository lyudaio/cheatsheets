# Solr cheatsheet for version 8.7.0

Solr is an open-source, highly scalable, and powerful enterprise search platform that can be used for full-text search, hit highlighting, faceted search, and more.

## Connecting to Solr

To connect to Solr, you can use the SolrJ Java client library or the Solr REST API, which is available over HTTP.

## Creating a core

A core in Solr is an index and set of configuration files. To create a new core, you can use the Solr administration UI or the `bin/solr` script.

```bash
./bin/solr create -c <core_name>
```

## Indexing data

Data can be indexed into Solr in several ways, including using the SolrJ client library, the Solr REST API, or the `bin/post` script. The following example uses the `bin/post` script to index a set of documents in XML format.

```bash
./bin/post -c <core_name> example/exampledocs/*.xml
```

## Querying data

Data can be queried from Solr using the SolrJ client library, the Solr REST API, or the `bin/post` script. The following example uses the Solr REST API to retrieve documents matching the query `*:*`.

```bash
curl "http://localhost:8983/solr/<core_name>/select?q=*:*"
```

## Updating data

Data can be updated in Solr using the SolrJ client library, the Solr REST API, or the `bin/post` script. The following example uses the Solr REST API to add a field to all documents in the index.

```bash
curl "http://localhost:8983/solr/<core_name>/update?stream.body=<add><doc><field name="new_field">new_value</field></doc></add>"
```

## Deleting data

Data can be deleted from Solr using the SolrJ client library, the Solr REST API, or the `bin/post` script. The following example uses the Solr REST API to delete all documents in the index.

```bash
curl "http://localhost:8983/solr/<core_name>/update?stream.body=<delete><query>*:*</query></delete>"
```

## Additional Resources

- [Solr Documentation](https://lucene.apache.org/solr/guide/)
- [SolrJ Client Library](https://lucene.apache.org/solr/guide/7_7/solrj.html)
- [Solr REST API Reference](https://lucene.apache.org/solr/guide/7_7/solr-rest-api.html)
