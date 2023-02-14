# PS Cheatsheet

This cheatsheet contains the essential commands and options of the `ps` command, a utility for displaying information about active processes in Unix-like operating systems.

`Latest LTS: Ubuntu 20.04`

## Basics

### Displaying Process Information

```bash
# Display information for all processes
ps -e

# Display information for a specific process by name
ps -C processName

# Display process information with additional fields
ps -eo pid,ppid,cmd,%mem,%cpu
```

### Sorting Output

```bash
# Sort by process ID (ascending)
ps -e --sort pid

# Sort by process ID (descending)
ps -e --sort -pid

# Sort by process name (ascending)
ps -e --sort cmd

# Sort by process name (descending)
ps -e --sort -cmd

# Sort by process start time (oldest first)
ps -e --sort start_time

# Sort by process start time (newest first)
ps -e --sort -start_time
```

### Filtering Output

```bash
# Display process information with a specific PID
ps -p PID

# Display processes by user name
ps -U userName

# Display processes by TTY
ps -t TTY
```

## Advanced

### Process Tree

```bash
# Display process tree of all processes
ps -e --forest

# Display process tree for a specific process
ps -f --ppid PARENT_PID
```

### Continuous Output

```bash
# Display process information continuously (like top)
ps -e --forest --sort start_time --no-headers -o pid,ppid,cmd,%mem,%cpu | awk '{print $1,$2,$3,$4,$5; fflush()}'
```

### Official Documentation

- [ps man page](https://man7.org/linux/man-pages/man1/ps.1.html)
