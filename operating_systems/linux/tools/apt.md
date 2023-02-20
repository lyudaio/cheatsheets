# APT Cheatsheet

APT (Advanced Package Tool) is a powerful command-line tool for managing packages on Debian-based Linux systems. This cheatsheet summarizes the essential commands and options for using APT.

## Updating Package Information

| Command            | Description                                                                                                                |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| `apt update`       | Update package information from configured repositories                                                                    |
| `apt upgrade`      | Upgrade all installed packages to their latest versions                                                                    |
| `apt dist-upgrade` | Upgrade all installed packages to their latest versions, including dependencies with new package installations or removals |
| `apt full-upgrade` | A more aggressive version of `dist-upgrade` that may remove more packages or install new dependencies                      |
|                    |

## Examples

Update package information from configured repositories:

```bash
apt update
```

Upgrade all installed packages to their latest versions:

```bash
apt upgrade
```

Upgrade all installed packages to their latest versions, including dependencies with new package installations or removals:

```bash
apt dist-upgrade
```

A more aggressive version of `dist-upgrade` that may remove more packages or install new dependencies:

```bash
apt full-upgrade
```

## Managing Packages

| Command                 | Description                                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| `apt install <package>` | Install a package                                                                              |
| `apt remove <package>`  | Remove a package, but leave configuration files                                                |
| `apt purge <package>`   | Remove a package and all of its configuration files                                            |
| `apt autoremove`        | Remove all packages that were automatically installed as dependencies and are no longer needed |

## Examples (Cont)

Install a package:

```bash
apt install <package>
```

Remove a package, but leave configuration files:

```bash
apt remove <package>
```

Remove a package and all of its configuration files:

```bash
apt purge <package>
```

Remove all packages that were automatically installed as dependencies and are no longer needed:

```bash
apt autoremove
```

## Searching for Packages

| Command                | Description                                  |
| ---------------------- | -------------------------------------------- |
| `apt search <package>` | Search for packages matching a keyword       |
| `apt show <package>`   | Display detailed information about a package |

### Examples

Search for packages matching a keyword:

```bash
apt search <package>
```

Display detailed information about a package:

```bash
apt show <package>
```

## Additional Resources

- [APT Documentation](https://manpages.debian.org/buster/apt/apt.8.en.html)

This cheatsheet provides a concise summary of essential commands and options for using APT to manage packages on Debian-based Linux systems. For more detailed information, refer to the official documentation.
