# Tree Cheatsheet

This cheatsheet contains the essential commands and options of the `tree` command, a utility for displaying directory trees in Unix-like operating systems.

`Latest LTS: Ubuntu 20.04`

## Basics

### Displaying Directory Trees

```bash
# Display directory tree with depth of 1
tree -L 1

# Display directory tree with specified depth
tree -L 2 path/to/directory

# Display directory tree with full path
tree -f path/to/directory

# Display directory tree with hidden files
tree -a path/to/directory

# Display directory tree in long format
tree -l path/to/directory

# Display directory tree with file sizes
tree -s path/to/directory

# Display directory tree with file sizes and human-readable units
tree -h path/to/directory
```

### Filtering Output

```bash
# Display directory tree with specific file extensions
tree -P "*.txt" path/to/directory

# Display directory tree without specified file extensions
tree -I "*.txt" path/to/directory
```

### Output Control

```bash
# Save directory tree to file
tree path/to/directory > output.txt

# Display directory tree in color
tree -C path/to/directory

# Display directory tree with file permissions
tree -p path/to/directory

# Display directory tree with file modification times
tree -D path/to/directory

# Display directory tree in XML format
tree -X path/to/directory

# Display directory tree in JSON format
tree -J path/to/directory
```

### Display Options

```bash
# Display directory tree without indentation lines
tree -i path/to/directory

# Display directory tree without showing the root directory
tree -O path/to/directory

# Display directory tree with only directories
tree -d path/to/directory
```

## Advanced

### Compare Directories

```bash
# Compare two directories
tree --du --inodes path/to/directory1 > directory1.txt
tree --du --inodes path/to/directory2 > directory2.txt
diff directory1.txt directory2.txt
```

### Filter Based on Size

```bash
# Display directory tree with files larger than a specified size
tree -L 2 path/to/directory --filelimit size

# Display directory tree with files smaller than a specified size
tree -L 2 path/to/directory --filelimit -size
```

### Official Documentation

- [tree man page](https://manned.org/tree)
