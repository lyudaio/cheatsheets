# Pacman Package Manager Cheatsheet

Pacman is the package manager for Arch Linux and its derivatives. It is a powerful and easy-to-use tool for installing, upgrading, and managing packages on your system.

## Basic Commands

| Command                   | Description                                  |
| ------------------------- | -------------------------------------------- |
| `pacman -S package_name`  | Install a package                            |
| `pacman -Syu`             | Synchronize and upgrade all packages         |
| `pacman -Ss search_term`  | Search for a package                         |
| `pacman -R package_name`  | Remove a package                             |
| `pacman -Q`               | List all installed packages                  |
| `pacman -Qi package_name` | Display detailed information about a package |
| `pacman -Qu`              | List all packages that can be upgraded       |

## Advanced Commands

| Command                   | Description                                               |
| ------------------------- | --------------------------------------------------------- |
| `pacman -Sw package_name` | Download a package without installing it                  |
| `pacman -Scc`             | Clear package cache                                       |
| `pacman -U package_name`  | Install a local package                                   |
| `pacman -Rs package_name` | Remove a package and its dependencies                     |
| `pacman -Qdt`             | List packages that are no longer required as dependencies |

## Configuration Files

| File                       | Description                                        |
| -------------------------- | -------------------------------------------------- |
| `/etc/pacman.conf`         | Main configuration file for pacman                 |
| `/etc/pacman.d/mirrorlist` | List of mirrors to use for package synchronization |

## Additional Resources

- [Pacman Documentation](https://wiki.archlinux.org/title/pacman)
- [Pacman Tips and Tricks](https://wiki.archlinux.org/title/Pacman/Tips_and_tricks)
