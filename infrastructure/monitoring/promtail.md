# Promtail Cheatsheet (v2.5.0)

Promtail is an agent which ships the contents of local logs to a private Prometheus instance. It can be used in conjunction with Loki to aggregate logs. Here's a cheatsheet for using Promtail.

## Installation

Promtail can be installed on Linux, macOS, and Windows. See the [official installation guide](https://grafana.com/docs/loki/latest/installation/) for detailed instructions.

## Configuration

Promtail is configured using a configuration file. The default configuration file is named `promtail-local-config.yaml`.

### Targets

Promtail defines targets to scrape logs from. Targets can be files, directories, or `systemd` journal files.

Here's an example of how to scrape logs from a file:

```yaml
scrape_configs:
- job_name: myjob
  static_configs:
  - targets:
      - localhost
    labels:
      job: myjob
      __path__: /var/log/mylog.log
```

### Labels

Promtail adds labels to logs before sending them to Prometheus. Labels can be static or dynamic.

Here's an example of how to add a static label to logs:

```yaml
scrape_configs:
- job_name: myjob
  static_configs:
  - targets:
      - localhost
    labels:
      job: myjob
```

Here's an example of how to add a dynamic label to logs:

```yaml
scrape_configs:
- job_name: myjob
  pipeline_stages:
  - match:
      selector: '{job="myjob"}'
    stages:
    - regex:
        expression: '(?P<my_label>my_regex)'
  static_configs:
  - targets:
      - localhost
    labels:
      job: myjob
      my_label: '{{.my_label}}'
```

### Pipeline Stages

Promtail defines pipeline stages to process logs before sending them to Prometheus. Pipeline stages can include matching, parsing, and labelling stages.

Here's an example of how to add a parsing stage to logs:

```yaml
scrape_configs:
- job_name: myjob
  pipeline_stages:
  - match:
      selector: '{job="myjob"}'
    stages:
    - json:
        expressions:
          message: '$.log'
  static_configs:
  - targets:
      - localhost
    labels:
      job: myjob
```

### Integrations

Promtail integrates with various logging libraries to support logging in different languages. See the [official integration documentation](https://grafana.com/docs/loki/latest/clients/) for details.

## Resources

- [Promtail Documentation](https://grafana.com/docs/loki/latest/clients/promtail/)
- [Promtail Configuration Documentation](https://grafana.com/docs/loki/latest/clients/promtail/configuration/)
- [Promtail Integration Documentation](https://grafana.com/docs/loki/latest/clients/)
- [Loki Documentation](https://grafana.com/docs/loki/)
