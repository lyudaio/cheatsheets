
# Hydra

## Introduction

Hydra is a powerful, flexible, and fast network login attack tool. It supports numerous network protocols, including HTTP, FTP, IMAP, LDAP, Telnet, and many others, making it an invaluable tool for penetration testing and security auditing.

## Basic Syntax

The basic command structure for Hydra is:

```bash
hydra -l <username> -P <password list> <target> <protocol> [options]
```

- `-l <username>`: This flag specifies the username to be used during the attack.
- `-P <password list>`: This flag specifies the path to the file containing a list of potential passwords.
- `<target>`: This is the IP address or domain name of the target system.
- `<protocol>`: This specifies the protocol to be used for the attack.

## Common Options

- `-V`: Displays the version of Hydra.
- `-t <threads>`: Specifies the number of concurrent connections to attempt during the attack.
- `-w <delay>`: Sets a delay (in seconds) between connection attempts.
- `-f`: Instructs Hydra to stop the attack after finding the first valid username and password combination.
- `-L <user list>`: Specifies a file containing a list of usernames to attempt.
- `-M <host list>`: Specifies a file containing a list of target hosts.
- `-s <port>`: Specifies the port to be used for the attack.
- `-vV`: Verbose mode. Displays information about every attempted username and password combination.

## Protocol Specific Usage

### HTTP

```bash
hydra -l <username> -P <password list> <target> http-get /path
```

- `http-get /path`: Specifies that Hydra should use the HTTP protocol, with a GET request to the specified path.

### FTP

```bash
hydra -l <username> -P <password list> <target> ftp
```

- `ftp`: Specifies that Hydra should use the FTP protocol.

### SSH

```bash
hydra -l <username> -P <password list> <target> ssh
```

- `ssh`: Specifies that Hydra should use the SSH protocol.

### Telnet

```bash
hydra -l <username> -P <password list> <target> telnet
```

- `telnet`: Specifies that Hydra should use the Telnet protocol.

### RDP

```bash
hydra -l <username> -P <password list> <target> rdp
```

- `rdp`: Specifies that Hydra should use the RDP protocol.

## Examples

Here are some example commands for using Hydra:

### HTTP

```bash
hydra -l admin -P passwords.txt 192.168.1.1 http-get /login.php
```

This command will use the username `admin` and the password list `passwords.txt` to perform a GET request on `http://192.168.1.1/login.php`.

### FTP

```bash
hydra -l john -P passwords.txt ftp://192.168.1.1
```

This command will use the username `john` and the password list `passwords.txt` to perform an FTP attack on `ftp://192.168.1.1`.

## Further Resources

For more information on Hydra and its capabilities, you can refer to the [official documentation](https://github.com/vanhauser-thc/thc-hydra).

Please ensure to use this tool responsibly and ethically.
