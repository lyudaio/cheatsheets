# Grafana Cheatsheet

Grafana is an open-source data visualization and monitoring tool. It supports a wide range of data sources, including Prometheus, Graphite, Elasticsearch, and more. This cheatsheet covers the basics of using Grafana.

## Installation

Grafana can be installed on Linux, macOS, and Windows. See the [official installation guide](https://grafana.com/docs/grafana/latest/installation/) for detailed instructions.

## Configuration

Grafana is configured using a configuration file. The default configuration file is named `grafana.ini`.

### Data Sources

A data source is a database or API that Grafana uses to fetch data. Data sources are added in the Grafana UI. Here is an example configuration for adding a Prometheus data source:

1. In the Grafana UI, click on the "Configuration" gear icon in the sidebar, then click on "Data Sources".
2. Click on "Add data source".
3. Select "Prometheus" as the data source type.
4. Enter the URL of your Prometheus server, and click "Save & Test".

### Dashboards

A dashboard is a collection of panels that display data from one or more data sources. Dashboards are created and edited in the Grafana UI. Here is an example configuration for creating a dashboard:

1. In the Grafana UI, click on the "Create" button in the sidebar, then click on "Dashboard".
2. Click on "Add panel".
3. Select a data source for the panel.
4. Choose a visualization type for the panel, such as "Graph" or "Singlestat".
5. Configure the panel by selecting metrics and setting options.

## Panels

A panel is a visualization of data from a data source. Grafana supports a wide range of panel types, including graphs, tables, and gauges.

### Graphs

A graph is a visualization of time-series data. Grafana supports a variety of graph types, including line graphs, bar graphs, and stacked area graphs.

### Tables

A table is a visualization of tabular data. Grafana supports a variety of table types, including singlestat, table, and heatmap.

### Gauges

A gauge is a visualization of a single value. Grafana supports a variety of gauge types, including gauge, bar gauge, and gauge panel.

## Alerts

Grafana supports alerting based on rules defined in the configuration file. When an alert is fired, it can be sent to various notification channels, such as email or Slack.

## Resources

- [Grafana Documentation](https://grafana.com/docs/)
- [Grafana Panels Documentation](https://grafana.com/docs/grafana/latest/panels/)
- [Grafana Data Sources Documentation](https://grafana.com/docs/grafana/latest/datasources/)
