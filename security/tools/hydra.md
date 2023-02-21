# Hydra Cheatsheet

Hydra is a fast and flexible network login cracker which can be used for brute-force login attacks against various types of network protocols, including HTTP, FTP, IMAP, LDAP, Telnet, and many more. In this cheatsheet, we will cover the basic usage and options for Hydra.

## Basic Usage

```bash
hydra -l <username> -P <password list> <target> <protocol> [options]
```

- `-l <username>`: Specifies the username to be used during the attack.
- `-P <password list>`: Specifies the password list to be used during the attack.
- `<target>`: Specifies the target's IP address or hostname.
- `<protocol>`: Specifies the protocol to use for the attack.

## Common Options

| Option           | Description                                                                        |
| ---------------- | ---------------------------------------------------------------------------------- |
| `-V`             | Displays version information.                                                      |
| `-t <threads>`   | Specifies the number of threads to use for the attack.                             |
| `-w <delay>`     | Specifies the delay time between requests.                                         |
| `-f`             | Stops the attack after the first valid username and password combination is found. |
| `-L <user list>` | Specifies a list of usernames to use for the attack.                               |
| `-M <host list>` | Specifies a list of hosts to use for the attack.                                   |
| `-s <port>`      | Specifies the port to use for the attack.                                          |
| `-vV`            | Displays verbose output.                                                           |

## Protocols

Here are some examples of protocols and their specific usage with Hydra:

### HTTP

```bash
hydra -l <username> -P <password list> <target> http-get [options]
```

- `http-get`: Performs a GET request with each password.

### FTP

```bash
hydra -l <username> -P <password list> <target> ftp [options]
```

- `ftp`: Specifies the FTP protocol.

### SSH

```bash
hydra -l <username> -P <password list> <target> ssh [options]
```

- `ssh`: Specifies the SSH protocol.

### Telnet

```bash
hydra -l <username> -P <password list> <target> telnet [options]
```

- `telnet`: Specifies the Telnet protocol.

### RDP

```bash
hydra -l <username> -P <password list> <target> rdp [options]
```

- `rdp`: Specifies the RDP protocol.

## Examples

Here are some example commands for using Hydra:

### HTTP (Cont.)

```bash
hydra -l admin -P passwords.txt 192.168.1.1 http-get /login.php
```

This command will use the username `admin` and the password list `passwords.txt` to perform a GET request on `http://192.168.1.1/login.php`.

### FTP (Cont.)

```bash
hydra -l john -P passwords.txt ftp://192.168.1.1
```

This command will use the username `john` and the password list `passwords.txt` to perform an FTP attack on `ftp://192.168.1.1`.

## Additional Resources

For more information on Hydra, please refer to the official documentation: [https://github.com/vanhauser-thc/thc-hydra](https://github.com/vanhauser-thc/thc-hydra)
