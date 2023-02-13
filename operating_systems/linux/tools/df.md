# SSH Cheatsheet

## Introduction

Secure Shell (SSH) is a cryptographic network protocol used for secure data communication, remote shell services or command execution and other secure network services between two networked computers. It was designed as a replacement for Telnet and other insecure remote shell protocols.

## Key-based authentication

Key-based authentication is more secure than password-based authentication, as it eliminates the need to send a password over the network, which could be intercepted. With key-based authentication, the client machine has a public key, and the server machine has a private key.

### Generating an SSH Key-Pair

To generate a key-pair, run the following command in a terminal:

```bash
ssh-keygen -t rsa
```

### Adding your public key to the remote server

To add your public key to the remote server, use the following command:

```bash
ssh-copy-id user@remote_server
```

## Connecting to a Remote Server

To connect to a remote server, use the following command:

```bash
ssh user@remote_server
```

## Port Forwarding

Port forwarding allows you to forward traffic from a local port to a remote server. For example, to forward traffic from port 8080 on your local machine to port 80 on a remote server, run the following command:

```bash
ssh -L 8080:remote_server:80 user@remote_server
```

## SCP (Secure Copy)

SCP is a secure way to copy files between two machines over an SSH connection. To copy a file from your local machine to a remote server, run the following command:

```bash
scp file.txt user@remote_server:~/
```

To copy a file from a remote server to your local machine, run the following command:

```bash
scp user@remote_server:file.txt ~/
```

## Conclusion

This cheatsheet provides a basic understanding of how to use SSH to securely connect to remote servers and transfer files. There are many more features and options available in SSH, but these basic commands should cover most common use cases.
