# Find Command Cheatsheet

## Description

`find` is a powerful command-line tool for searching files and directories in Linux. It can search for files based on various criteria such as name, size, time modified, and ownership.

## Syntax

```bash
find [path...] [expression]
```

- `path`: The directory or directories to search in. If no path is specified, the search is performed in the current directory and its subdirectories.
- `expression`: The search criteria or actions to perform.

## Examples

### Search by Name

Search for a file or directory with exact name:

```bash
find /path/to/dir -name "file.txt"
```

Search for files or directories with names that match a pattern:

```bash
find /path/to/dir -name "*.txt"
```

### Search by Type

Search for files of a specific type:

```bash
find /path/to/dir -type f
```

Search for directories:

```bash
find /path/to/dir -type d
```

### Search by Size

Search for files larger than a certain size (in kilobytes):

```bash
find /path/to/dir -type f -size +100k
```

Search for files smaller than a certain size (in kilobytes):

```bash
find /path/to/dir -type f -size -100k
```

### Search by Time

Search for files modified within the last n days:

```bash
find /path/to/dir -type f -mtime -n
```

Search for files modified exactly n days ago:

```bash
find /path/to/dir -type f -mtime n
```

### Search by Ownership

Search for files owned by a specific user:

```bash
find /path/to/dir -type f -user username
```

Search for files owned by a specific group:

```bash
find /path/to/dir -type f -group groupname
```

### Execute Actions

Execute a command on each file found:

```bash
find /path/to/dir -type f -exec command {} \;
```

Print the path of each file found:

```bash
find /path/to/dir -type f -print
```

## Additional Resources

- [Official `find` documentation](https://www.gnu.org/software/findutils/manual/html_mono/find.html)
