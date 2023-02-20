# Sed Cheatsheet

## Description

Sed is a powerful command-line tool for stream editing. It is used to transform text by applying a series of commands to it. Sed works by reading the input file line by line and performing the specified operations on each line.

## Command Options

| Command | Description |
| --- | --- |
| `sed [options] [script] [inputfile]` | Execute the sed script on the input file |
| `-n` | Suppress automatic printing of pattern space |
| `-e script` | Add the script to the commands to be executed |
| `-f script-file` | Add the commands contained in the file to the commands to be executed |
| `-r` | Use extended regular expressions in the script |
| `-i [suffix]` | Edit files in place |
| `-s` | Treat input as a single line |
| `-u` | Use unbuffered output |

## Examples

### 1. Print specific line of a file

To print a specific line of a file, use the following command:

```bash
sed -n '5p' file.txt
```

### 2. Replace text in a file

To replace text in a file, use the following command:

```bash
sed -i 's/old-text/new-text/g' file.txt
```

### 3. Delete lines from a file

To delete lines from a file, use the following command:

```bash
sed -i '2,5d' file.txt
```

## Common Uses

- Search and replace text in a file
- Delete lines from a file
- Extract specific lines from a file
- Transform data in a file into a new format

## Additional Resources

Official sed documentation: https://www.gnu.org/software/sed/manual/sed.html
