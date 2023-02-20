# Linux Cat Command Cheatsheet

## Description

The `cat` command is a Unix utility used for concatenating and displaying files on the terminal.

## Syntax

`cat [OPTION]... [FILE]...`

## Options

- `-b`: Number non-blank output lines.
- `-e`: Display end-of-line characters as `$`.
- `-n`: Number all output lines.
- `-s`: Squeeze multiple blank lines into one.
- `-T`: Display tab characters as `^I`.
- `-u`: Disable output buffering.
- `-v`: Display non-printable characters as `^` notation.

## Examples

- Display contents of a file:
  `cat filename`

- Display contents of multiple files:
  `cat file1 file2 file3`

- Display contents of all files in a directory:
  `cat *`

- Create a new file and enter text:
  `cat > filename`

- Append text to an existing file:
  `cat >> filename`

## Additional Resources

- Official documentation: <https://www.gnu.org/software/coreutils/cat>
- Linux man page: <http://man7.org/linux/man-pages/man1/cat.1.html>
