# OpenSSL Cheatsheet (Latest LTS Version: 1.1.1g)

OpenSSL is a full-featured open-source toolkit implementing the Secure Sockets Layer (SSL) and Transport Layer Security (TLS) protocols. It is widely used to secure network communications, secure web-based applications, and encrypt files.

## Installing OpenSSL

You can install OpenSSL on various platforms, including Windows, Mac, and Linux.

### Linux

Use the package manager for your Linux distribution to install OpenSSL.

#### Debian / Ubuntu

```bash
sudo apt-get install openssl
```

#### Fedora / CentOS

```bash
sudo yum install openssl
```

### Mac

Use Homebrew to install OpenSSL:

```bash
brew install openssl
```

### Windows

You can download a pre-compiled version of [OpenSSL for Windows from the official website](https://slproweb.com/products/Win32OpenSSL.html):

## Basic Usage

Here are some common tasks you can perform with OpenSSL:

### Generating a Self-Signed Certificate

The following command generates a self-signed certificate:

```bash
openssl req -new -newkey rsa:2048 -nodes -keyout example.key -out example.csr
```

This will create two files: `example.key` and `example.csr`. The `.key` file is the private key and should be kept secret. The `.csr` file is the certificate signing request and can be used to request a certificate from a certificate authority.

### Generating a Certificate Signing Request (CSR)

The following command generates a certificate signing request:

```bash
openssl req -new -newkey rsa:2048 -nodes -keyout example.key -out example.csr
```

### Generating a Private Key

The following command generates a private key:

```bash
openssl genpkey -algorithm RSA -out private.key -aes256
```

### Encrypting a File

The following command encrypts a file using AES-256 encryption:

```bash
openssl enc -aes-256-cbc -in plaintext.txt -out encrypted.txt
```

### Decrypting a File

The following command decrypts an encrypted file:

```bash
openssl enc -d -aes-256-cbc -in encrypted.txt -out plaintext.txt
```

### Verify SSL/TLS Connection

The following command verifies an SSL/TLS connection to a remote server:

```bash
openssl s_client -connect example.com:443
```

## Conclusion

This cheatsheet provides a basic overview of OpenSSL and its capabilities. For more information, you can refer to the [Official Documentation.](https://www.openssl.org/docs/manmaster/man1/openssl.html)
