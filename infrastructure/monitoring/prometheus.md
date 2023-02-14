# Prometheus Cheatsheet

Prometheus is a monitoring and alerting system. It collects metrics from configured targets, stores these metrics, and provides an HTTP API for querying the collected data. This cheatsheet covers the basics of using Prometheus.

## Installation

Prometheus can be installed on Linux, macOS, and Windows. See the [official installation guide](https://prometheus.io/docs/prometheus/latest/installation/) for detailed instructions.

## Configuration

Prometheus is configured using a YAML file. The default configuration file is named `prometheus.yml`.

### Targets

A target is a thing to be monitored by Prometheus. Targets are specified in the configuration file using the `scrape_configs` section. Here is an example configuration that scrapes metrics from a local Node.js app:

```bash
scrape_configs:
  - job_name: 'node-app'
    static_configs:
      - targets: ['localhost:3000']
```

### Exporters

An exporter is a program that exposes metrics in a format that Prometheus can understand. Exporters are specified in the configuration file using the `scrape_configs` section. Here is an example configuration that scrapes metrics from a local MySQL server using the MySQL exporter:

```bash
scrape_configs:
  - job_name: 'mysql'
    static_configs:
      - targets: ['localhost:9104']
    metrics_path: /metrics
    params:
      ds: ['mydb']
    relabel_configs:
      - source_labels: [__address__]
        regex: localhost:9104
        replacement: mysql-exporter:9104
        target_label: instance
```

### Rules

A rule is a condition that is evaluated against the collected metrics, and if the condition is true, an alert is fired. Rules are specified in the configuration file using the `rule_files` section. Here is an example configuration that fires an alert if the CPU usage is above 80% for more than 5 minutes:

```bash
rule_files:
  - alert_rules.yml
```

## Querying

Prometheus provides a powerful query language called PromQL for querying the collected data.

### Basic Queries

Here are some basic queries you can run using PromQL:

- `up`: shows whether a target is up or down.
- `node_cpu_seconds_total`: shows the total CPU time used by a node.
- `http_requests_total`: shows the total number of HTTP requests.

### Aggregation

PromQL supports a variety of aggregation functions, including `sum`, `avg`, and `count`.

```bash
sum(node_cpu_seconds_total{mode="idle"})
```

### Range Queries

PromQL also supports range queries, which allow you to query a range of data over time.

```bash
rate(http_requests_total[5m])
```

## Alerting

Prometheus supports alerting based on rules defined in the configuration file. When an alert is fired, it can be sent to various notification channels, such as email or Slack.

## Links

- [Prometheus Documentation](https://prometheus.io/docs/)
- [PromQL Documentation](https://prometheus.io/docs/prometheus/latest/querying/basics/)
- [Prometheus Exporters](https://prometheus.io/docs/instrumenting/exporters/)
