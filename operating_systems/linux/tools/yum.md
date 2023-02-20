# Yum Cheatsheet

This cheatsheet provides a quick reference guide for using Yum package manager.

## Basic Commands

| Command            | Description                                                   |
| ------------------ | ------------------------------------------------------------- |
| `yum update`       | Update all installed packages to their latest versions        |
| `yum install`      | Install packages from a repository                            |
| `yum remove`       | Remove installed packages                                     |
| `yum search`       | Search for a package in repositories                          |
| `yum list`         | List installed packages or packages available in repositories |
| `yum info`         | Display detailed information about a package                  |
| `yum clean`        | Remove cached data                                            |
| `yum check-update` | Check for available package updates                           |
| `yum upgrade`      | Upgrade installed packages to their latest versions           |
| `yum downgrade`    | Downgrade installed packages to a previous version            |
| `yum groupinstall` | Install all packages in a specific package group              |
| `yum groupremove`  | Remove all packages in a specific package group               |

## Display the Transaction History of Yum Commands

| Command            | Description                                               |
| ------------------ | --------------------------------------------------------- |
| `yum history`      | Display a summary of all previous transactions            |
| `yum history list` | Display a detailed list of all previous transactions      |
| `yum history info` | Display detailed information about a specific transaction |
| `yum history undo` | Undo a specific transaction                               |

## Additional Resources

- Yum command cheat sheet: https://access.redhat.com/sites/default/files/attachments/rh_yum_cheatsheet_1214_jcs_print-1.pdf
- Yum documentation: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/ch-yum
