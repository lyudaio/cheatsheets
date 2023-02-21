# John the Ripper Cheatsheet

John the Ripper is a popular password cracking tool used by security professionals to test the strength of passwords. It can perform both dictionary-based and brute-force attacks on password hashes.

## Basic Usage

The basic syntax of John the Ripper is:

```bash
john [OPTIONS] [PASSWORD_FILE]
```

### Options

Here are some common options used with John the Ripper:

| Option            | Description                                       |
| ----------------- | ------------------------------------------------- |
| `-w`              | Use wordlist mode                                 |
| `--wordlist=FILE` | Specify a wordlist file to use with wordlist mode |
| `-mask`           | Use mask mode                                     |
| `--mask=MASK`     | Specify a mask to use with mask mode              |
| `--session=NAME`  | Specify a session name for the cracking process   |
| `--show`          | Show cracked passwords                            |
| `--rules`         | Enable word mangling rules                        |
| `--format=FORMAT` | Specify the hash format to be cracked             |

### Hash Formats

Here are some common hash formats supported by John the Ripper:

| Format   | Description        |
| -------- | ------------------ |
| `md5`    | MD5 hash format    |
| `sha1`   | SHA1 hash format   |
| `sha256` | SHA256 hash format |
| `sha512` | SHA512 hash format |

## Examples

### Wordlist Mode

To use John the Ripper in wordlist mode, specify the wordlist file to use with the `--wordlist` option. For example:

```bash
john --wordlist=rockyou.txt passwords.txt
```

### Mask Mode

To use John the Ripper in mask mode, specify the mask to use with the `--mask` option. For example:

```bash
john --mask=?d?d?d?d passwords.txt
```

### Session Name

To specify a session name for the cracking process, use the `--session` option. For example:

```bash
john --session=my_session passwords.txt
```

### Show Cracked Passwords

To show cracked passwords, use the `--show` option. For example:

```bash
john --show passwords.txt
```

### Rules

To enable word mangling rules, use the `--rules` option. For example:

```bash
john --wordlist=rockyou.txt --rules passwords.txt
```

### Format

To specify the hash format to be cracked, use the `--format` option. For example:

```bash
john --format=md5 passwords.txt
```

## Additional Resources

For more information and documentation on John the Ripper, visit the [official website](https://www.openwall.com/john/).
