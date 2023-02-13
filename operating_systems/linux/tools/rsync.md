# rsync Cheatsheet

## Introduction

rsync is a fast and versatile utility for synchronizing files and directories between two locations over a network. It is commonly used for backing up data, copying files from one place to another, and transferring data from a remote server to a local machine.

## Basic Usage

The basic syntax for rsync is as follows:

```
rsync [OPTION]... SRC [SRC]... DEST
```

where `SRC` is the source location and `DEST` is the destination.

## Options

Here are some common options used with rsync:

- `-a, --archive`: Archive mode; equals to -rlptgoD.
- `-v, --verbose`: Verbose output.
- `-r, --recursive`: Recurse into directories.
- `-z, --compress`: Compress file data during the transfer.
- `-h, --human-readable`: Output file sizes in a human-readable format.
- `-n, --dry-run`: Do a trial run with no changes made.
- `--delete`: Delete files in the destination that are not present in the source.

## Examples

Here are some common use cases for rsync:

- Backup a directory:

```bash
rsync -av /path/to/source /path/to/destination
```

- Copy files from a remote server to a local machine:

```bash
rsync -av username@remote:/path/to/source /path/to/destination
```

- Synchronize a directory with a remote server:

```bash
rsync -av --delete /path/to/source username@remote:/path/to/destination
```

## Conclusion

rsync is a powerful tool for synchronizing files and directories, and it offers many options to customize the behavior of the transfer. Whether you are using it to backup data, copy files, or transfer data from a remote server, rsync is a versatile and essential tool to have in your toolbox.
