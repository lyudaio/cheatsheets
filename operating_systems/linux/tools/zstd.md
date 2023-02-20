# Zstandard (zstd) Command Cheatsheet

## Description

`zstd` is a fast lossless compression algorithm and command-line tool developed by Facebook. It can compress and decompress files and streams, and supports multi-threading for improved performance.

## Syntax

Compression: `zstd [OPTIONS]... [FILE]...`

Decompression: `zstd -d [OPTIONS]... [FILE]...`

## Options

| Option | Description                                         |
| ------ | --------------------------------------------------- |
| `-#`   | Set compression level (1-22, default: 3).           |
| `-d`   | Decompress input file(s).                           |
| `-k`   | Keep input file(s) after compression/decompression. |
| `-f`   | Force compression, even if output file exists.      |
| `-t`   | Test compressed file(s) integrity.                  |
| `-C`   | Change directory before operation.                  |

## Examples

Compress file `file.txt` with maximum compression level:

```bash
zstd -19 file.txt
```

Decompress file `file.txt.zst`:

```bash
zstd -d file.txt.zst
```

Compress all files in current directory with default compression level and keep original files:

```bash
zstd -k *
```

Compress all files in current directory and subdirectories with maximum compression level:

```bash
find . -type f -print0 | xargs -0 zstd -19
```

Test integrity of compressed file:

```bash
zstd -t file.txt.zst
```

## Additional Resources

- [Official zstd documentation](https://github.com/facebook/zstd/blob/dev/README.md)
- [Zstandard website](https://facebook.github.io/zstd/)
