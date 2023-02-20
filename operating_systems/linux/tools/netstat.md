# Netstat Command Cheatsheet

Netstat is a powerful command-line tool that displays network connections and their associated statistics. This cheatsheet summarizes the essential commands and options for using netstat.

## Displaying Network Connections

| Option | Description                                               |
| ------ | --------------------------------------------------------- |
| `-a`   | Display all active network connections                    |
| `-l`   | Display all listening ports                               |
| `-e`   | Display all established connections                       |
| `-n`   | Display all network connections using numerical addresses |
| `-c`   | Display all network connections in real-time              |

### Examples

Display all active network connections:

```bash
netstat -a
```

Display all listening ports:

```bash
netstat -l
```

Display all established connections:

```bash
netstat -e
```

Display all network connections using numerical addresses:

```bash
netstat -n
```

Display all network connections in real-time:

```bash
netstat -c
```

## Filtering Network Connections

| Option                     | Description                                     |
| -------------------------- | ----------------------------------------------- |
| `-t`                       | Display network connections by TCP protocol     |
| `-u`                       | Display network connections by UDP protocol     |
| `-x`                       | Display network connections by UNIX protocol    |
| `-tulpn`                   | Display network connections by port number      |
| `-an \| grep <ip_address>` | Display network connections by IP address       |
| `-p`                       | Display network connections by process ID (PID) |

### Examples

Display network connections by TCP protocol:

```bash
netstat -t
```

Display network connections by UDP protocol:

```bash
netstat -u
```

Display network connections by UNIX protocol:

```bash
netstat -x
```

Display network connections by port number:

```bash
netstat -tulpn
```

Display network connections by IP address:

```bash
netstat -an | grep <ip_address>
```

Display network connections by process ID (PID):

```bash
netstat -p
```

## Additional Resources

- [Netstat Documentation](https://man7.org/linux/man-pages/man8/netstat.8.html)

This cheatsheet provides a concise summary of essential commands and options for using netstat to display and filter network connections. For more detailed information, refer to the official documentation.
