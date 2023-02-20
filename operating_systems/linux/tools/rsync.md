# Rsync Command Cheatsheet

## Description

`rsync` is a command-line tool for efficiently copying and synchronizing files between directories or systems over a network. It is widely used for backup and mirroring purposes, as well as for transferring large amounts of data.

## Syntax

```bash
rsync [OPTION]... SRC... [DEST]
```

- `OPTION`: Optional arguments that modify the behavior of the command.
- `SRC`: The source file or directory to copy from.
- `DEST`: The destination directory to copy to.

## Options

| Option | Description                                                                    |
| ------ | ------------------------------------------------------------------------------ |
| `-a`   | Archive mode: preserve permissions, ownership, timestamps, and recursive copy. |
| `-v`   | Verbose mode: print detailed output about the transfer.                        |
| `-z`   | Compress data during the transfer to reduce network usage.                     |
| `-h`   | Human-readable output: display file sizes in a readable format.                |
| `-r`   | Recursive copy: copy directories and their contents recursively.               |
| `-u`   | Update: only copy files that are newer than the destination.                   |
| `-n`   | Dry run: simulate the transfer without actually copying any files.             |
| `-P`   | Progress: show progress during the transfer.                                   |

## Examples

### Copy Files Locally

Copy a file from one directory to another:

```bash
rsync /path/to/source/file /path/to/destination/
```

Copy a directory and its contents to another directory:

```bash
rsync -a /path/to/source/directory/ /path/to/destination/
```

### Copy Files Over Network

Copy a file from a local system to a remote system:

```bash
rsync /path/to/source/file user@remote:/path/to/destination/
```

Copy a directory and its contents from a remote system to a local system:

```bash
rsync -a user@remote:/path/to/source/directory/ /path/to/destination/
```

### Exclude Files or Directories

Exclude a specific file or directory from the transfer:

```bash
rsync --exclude 'file.txt' /path/to/source/directory/ /path/to/destination/
```

Exclude multiple files or directories using a pattern:

```bash
rsync --exclude '*.txt' /path/to/source/directory/ /path/to/destination/
```

## Additional Resources

- [Official `rsync` documentation](https://linux.die.net/man/1/rsync)
- [A Beginner's Guide to `rsync`](https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-on-a-vps)
