# df - Display the Amount of Disk Space Used and Available

## Introduction

`df` is a Unix command that shows the amount of disk space used and available on a Linux file system. The `df` command is used to check the disk space available on the file system that a file resides on.

## Syntax

```bash
df [OPTION]... [FILE]...
```

## Options

- `-a, --all`: include pseudo, duplicate, inaccessible file systems
- `-B, --block-size=SIZE`: use SIZE-byte blocks
- `-h, --human-readable`: print sizes in human readable format (e.g., 1K 234M 2G)
- `-H, --si`: equivalent to `--block-size=1000`
- `-i, --inodes`: list inode information instead of block usage
- `-k, --kilobytes`: default, use 1024-byte blocks
- `-l, --local`: limit listing to local file systems
- `-t, --type=TYPE`: limit listing to file systems of type TYPE
- `-T, --print-type`: print file system type
- `-x, --exclude-type=TYPE`: limit listing to file systems not of type TYPE

## Examples

To display the disk space usage of all mounted file systems:

```bash
df -h
```

To display disk space usage of a specific file system:

```bash
df -h /dev/sda1
```

To display disk space usage in kilobytes:

```bash
df -k
```

To display disk space usage of all file systems excluding NFS:

```bash
df -x nfs
```

## Conclusion

In conclusion, the `df` command is a useful tool for checking disk space usage in Linux. It provides information on the amount of disk space used and available on a file system, and also provides options for displaying disk space usage in different formats, such as human-readable format or kilobytes. By using the `df` command regularly, you can monitor disk space usage and ensure that you have enough disk space for your needs. END_OF_MESSAGE
