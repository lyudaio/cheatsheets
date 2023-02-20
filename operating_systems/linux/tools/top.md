# TOP COMMAND CHEATSHEET

## Introduction

The `top` command is a utility that provides real-time information about the system's running processes, memory usage, and CPU utilization. By default, it displays a dynamic view of the system that updates periodically.

## Basic Usage

To run the `top` command, simply open a terminal and type:

```bash
top
```

This will launch the `top` utility and display a real-time view of the system's processes.

## Command-Line Options

Here are some of the most commonly used command-line options for the `top` command:

| Option          | Description                                  |
| --------------- | -------------------------------------------- |
| `-d <seconds>`  | Set the delay between updates (in seconds)   |
| `-p <pid>`      | Monitor a specific process ID (PID)          |
| `-u <username>` | Monitor a specific user's processes          |
| `-b`            | Run `top` in batch mode (useful for scripts) |
| `-c`            | Show the command-line arguments of processes |

## Interactive Commands

While `top` is running, you can use a number of interactive commands to control its behavior. Here are some of the most useful ones:

| Command | Description                            |
| ------- | -------------------------------------- |
| `q`     | Quit `top`                             |
| `k`     | Kill a process                         |
| `r`     | Renice a process (change its priority) |
| `f`     | Show or hide fields                    |
| `o`     | Change the sort order of the processes |
| `s`     | Change the update interval             |
| `l`     | Toggle display of load average         |

## Sorting Options

By default, `top` displays processes sorted by CPU usage. However, you can change the sorting order by using the following keys:

| Key | Description                 |
| --- | --------------------------- |
| `P` | Sort by CPU usage (default) |
| `M` | Sort by memory usage        |
| `T` | Sort by process time        |
| `N` | Sort by process name        |
| `<` | Sort by PID (ascending)     |
| `>` | Sort by PID (descending)    |

## Conclusion

The `top` command is an essential tool for monitoring system performance and troubleshooting issues related to CPU and memory usage. By using the options and commands outlined in this cheatsheet, you can customize its behavior and get the most out of it.
