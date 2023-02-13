# InfluxDB 2.0.4

InfluxDB is an open-source time-series database designed to handle high write and query loads.

## Basic Operations

1. Connect to the InfluxDB server: `influx`
2. Show databases: `SHOW DATABASES`
3. Create a database: `CREATE DATABASE <database_name>`
4. Use a database: `USE <database_name>`
5. Insert data: `INSERT <measurement_name>,<tag_key>=<tag_value> <field_key>=<field_value> <timestamp>`
6. Query data: `SELECT <field_key> FROM <measurement_name> WHERE <condition>`
7. Drop a database: `DROP DATABASE <database_name>`

## Additional Resources

- [InfluxDB Documentation](https://v2.docs.influxdata.com/influxdb/)
- [InfluxDB GitHub Repository](https://github.com/influxdata/influxdb)
