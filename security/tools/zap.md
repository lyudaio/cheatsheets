# ZAP

## Introduction

OWASP ZAP (Zed Attack Proxy) is a free, open-source web application security scanner. It helps you automatically find security vulnerabilities in your web applications while you are developing and testing your applications.

## Main Features

### Intercepting Proxy

Allows you to intercept and modify HTTP/HTTPS requests and responses.

```bash
# To enable, navigate to Tools -> Options -> Local Proxies
```

### Automated Scanner

Automatically scans applications to find vulnerabilities.

```bash
# To run, right-click on your site from the Sites tab, then choose Attack -> Active Scan
```

### Passive Scanner

Passively analyzes web applications to detect potential vulnerabilities.

```bash
# To enable, navigate to Analyze -> Passive Scan
```

## Other Features

### Brute Force Scanner

Allows you to conduct a brute force attack on various web application elements.

```bash
# To run, right-click on your site from the Sites tab, then choose Attack -> Forced Browse
```

### Fuzzer

Allows you to send a series of inputs to various web application elements to detect anomalies.

```bash
# To use, select a request in the History or Sites tab, then right-click and choose Attack -> Fuzz
```

### Web Sockets

Allows you to intercept, modify, and replay WebSocket messages.

```bash
# To enable, navigate to Tools -> Options -> WebSocket
```

## Resources

For more information, check the official documentation at:

```bash
https://www.zaproxy.org/docs/
```

Please ensure to use this tool responsibly and ethically.
