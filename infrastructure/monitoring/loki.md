# Loki Cheatsheet (v2.5.0)

Loki is a horizontally scalable, highly available, multi-tenant log aggregation system. It can be used as a backend for Grafana's Explore feature. Here's a cheatsheet for using Loki.

## Installation

Loki can be installed on Linux, macOS, and Windows. See the [official installation guide](https://grafana.com/docs/loki/latest/installation/) for detailed instructions.

## Configuration

Loki is configured using a configuration file. The default configuration file is named `loki-local-config.yaml`.

### Log Labels

Loki uses log labels to extract and index key-value pairs from logs. Log labels can be added to logs in various ways, including using a logging library that supports log labels or by adding them directly to log lines.

Here's an example of how to add a log label to a log line using Java:

```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.slf4j.MDC;

public class MyLogger {
  private static final Logger logger = LoggerFactory.getLogger(MyLogger.class);

  public void logMessage(String message, String key, String value) {
    MDC.put(key, value);
    logger.info(message);
    MDC.remove(key);
  }
}
```

### Queries

Loki supports queries using the LogQL query language. Here are some examples of LogQL queries:

- To get all logs for a specific label value:

  ```bash
  {label_name="label_value"}
  ```

- To filter logs by a regular expression:

  ```bash
  {label_name=~"regular_expression"}
  ```

- To aggregate logs by a label:

  ```bash
  sum by (label_name) ({label_name="label_value"} |= "metric_name")
  ```

- To group logs by a label and show the top 10 values:

  ```bash
  topk(10, {label_name})
  ```

### API

Loki provides a REST API for querying logs and managing the system. See the [official API documentation](https://grafana.com/docs/loki/latest/api/) for details.

## Resources

- [Loki Documentation](https://grafana.com/docs/loki/)
- [LogQL Query Language](https://grafana.com/docs/loki/latest/logql/)
- [Loki API Documentation](https://grafana.com/docs/loki/latest/api/)
