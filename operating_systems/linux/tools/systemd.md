# Systemd Cheatsheet

This cheatsheet contains the essential commands and concepts of Systemd, a system and service manager for Linux operating systems.

`Latest LTS: Systemd 249`

## Basics

### Systemctl

```bash
# Start a service
systemctl start serviceName

# Stop a service
systemctl stop serviceName

# Restart a service
systemctl restart serviceName

# Reload a service
systemctl reload serviceName

# Enable a service at boot
systemctl enable serviceName

# Disable a service at boot
systemctl disable serviceName

# Check status of a service
systemctl status serviceName
```

### Journalctl

```bash
# Show log entries for a service
journalctl -u serviceName

# Show log entries starting from a specific time
journalctl --since "2022-02-13 00:00:00"

# Show log entries for a specific process
journalctl _PID=processID

# Show log entries for a specific unit type
journalctl -t unitType
```

### Unit Files

```bash
# List all unit files
systemctl list-unit-files

# Show the status of a unit
systemctl status unitName.service

# Edit a unit file
systemctl edit unitName.service

# Check syntax of a unit file
systemctl daemon-reload
systemctl is-active unitName.service
```

## Advanced

### Targets

```bash
# Show default target
systemctl get-default

# Change default target
systemctl set-default targetName

# List available targets
systemctl list-units --type target
```

### Dependencies

```bash
# Show dependencies for a unit
systemctl list-dependencies unitName.service

# Show all units that depend on a unit
systemctl list-dependencies --reverse unitName.service
```

### Systemd-Resolved

```bash
# Show current DNS settings
systemd-resolve --status

# Show DNS server IP addresses
systemd-resolve --status | grep "DNS Servers"
```

## Official Documentation

- [Systemd Documentation](https://systemd.io/)
- [Systemd on Wikipedia](https://en.wikipedia.org/wiki/Systemd)
