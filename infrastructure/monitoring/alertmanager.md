# AlertManager Cheatsheet (v0.22.2)

AlertManager is a tool used to manage alerts sent by client applications such as Prometheus. It groups alerts, deduplicates them, and sends them to notification channels such as email, Slack, or PagerDuty. Here's a cheatsheet for using AlertManager.

## Installation

AlertManager can be installed on Linux, macOS, and Windows. See the [official installation guide](https://prometheus.io/docs/alerting/latest/alertmanager/) for detailed instructions.

## Configuration

AlertManager is configured using a configuration file. The default configuration file is named `alertmanager.yml`.

### Routing

AlertManager defines routes to handle alerts. Routes can be based on labels and can include grouping and deduplication.

Here's an example of how to route alerts based on a label:

```yaml
route:
  group_by: ['alertname']
  group_wait: 30s
  group_interval: 5m
  repeat_interval: 4h
  routes:
  - match:
      job: 'myjob'
    receiver: 'myemail'
```

### Receivers

AlertManager defines receivers to send alerts to notification channels. Receivers can be email, Slack, PagerDuty, or other custom channels.

Here's an example of how to define an email receiver:

```yaml
receivers:
- name: 'myemail'
  email_configs:
  - to: 'me@example.com'
    from: 'alertmanager@example.com'
    smarthost: 'smtp.example.com:587'
    auth_username: 'me'
    auth_identity: 'me@example.com'
    auth_password: 'mypassword'
```

### Inhibition

AlertManager defines inhibition rules to suppress alerts. Inhibition rules can be based on labels and can include grouping and deduplication.

Here's an example of how to define an inhibition rule:

```yaml
inhibit_rules:
- source_match:
    severity: 'critical'
  target_match:
    severity: 'warning'
  equal: ['alertname']
```

## API

AlertManager provides a REST API for managing alerts. See the [official API documentation](https://prometheus.io/docs/alerting/latest/alertmanager_api/) for details.

## Links

- [AlertManager Documentation](https://prometheus.io/docs/alerting/latest/alertmanager/)
- [AlertManager Configuration Documentation](https://prometheus.io/docs/alerting/latest/configuration/)
- [AlertManager API Documentation](https://prometheus.io/docs/alerting/latest/alertmanager_api/)
- [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
