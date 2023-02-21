# Burp Suite Cheatsheet

Burp Suite is a powerful web application security testing tool used by security professionals and software engineers to perform various security testing techniques such as scanning, intercepting, and modifying network traffic.

This cheatsheet covers some of the most commonly used features in Burp Suite.

## Versions

| Latest LTS Version               | Latest Community Version              |
| -------------------------------- | ------------------------------------- |
| Burp Suite Professional 2021.2.1 | Burp Suite Community Edition 2021.2.1 |

## Getting Started

1. Download and install Burp Suite from the [official website](https://portswigger.net/burp/communitydownload).
2. Launch Burp Suite.
3. Configure your browser to use Burp Suite as a proxy.
4. Start browsing the target website through Burp Suite.

## Commonly Used Features

### Proxy

Burp Suite intercepts and modifies network traffic, allowing you to view and modify requests and responses.

- **Intercept Requests:** Proxy > Intercept > Intercept Client Requests
- **Intercept Responses:** Proxy > Intercept > Intercept Server Responses
- **Forward Intercepted Requests:** Press the Forward button in the Proxy tab
- **Drop Intercepted Requests:** Press the Drop button in the Proxy tab

### Scanner

Burp Suite scans for vulnerabilities in web applications.

- **Start a New Scan:** Scanner > New Scan
- **Choose Scan Type:** Select from Active, Passive, or Spider scanning
- **Configure Scan Settings:** Set the scope, URLs to exclude, and scan issues to report

### Repeater

Burp Suite allows you to manually send requests and view responses.

- **Send a Request:** Select a request in the Proxy tab and click Send to Repeater
- **Modify a Request:** Edit the request in the Repeater tab

### Intruder

Burp Suite allows you to automate requests with payloads and perform brute-force attacks.

- **Start an Intruder Attack:** Intruder > Start Attack
- **Choose Attack Type:** Select from Sniper, Battering Ram, Pitchfork, or Cluster Bomb attacks
- **Configure Payload:** Add or remove payloads to use in the attack

### Decoder

Burp Suite allows you to decode or encode data in various formats.

- **Decode Data:** Decoder > Base64 Decode, URL Decode, HTML Decode, etc.
- **Encode Data:** Decoder > Base64 Encode, URL Encode, HTML Encode, etc.

### Extender

Burp Suite allows you to extend its functionality by writing custom plugins.

- **Create a New Extension:** Extender > Extensions > Add
- **Choose Extension Type:** Choose from API-based, Scanner-based, or UI-based extensions
- **Write Extension Code:** Use Java or Python to write your extension code

## Tips and Tricks

- Use the **Project Options** tab to configure project settings, such as the project scope and URL rewrite rules.
- Use the **Target** tab to view details about the target website, such as its IP address and server version.
- Use the **History** tab to view all requests and responses captured by Burp Suite.
- Use the **Search** function to search for specific keywords in requests and responses.

## Additional Resources

- [Official Burp Suite Documentation](https://portswigger.net/burp/documentation/)
- [Burp Suite Tutorials and Webinars](https://portswigger.net/web-security/learning-path/burp-suite)
