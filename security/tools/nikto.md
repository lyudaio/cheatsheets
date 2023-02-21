# Nikto Cheatsheet

Nikto is an open-source web server scanner used to identify potential vulnerabilities and security issues in web servers. Here are some of the essential commands and options to help you use Nikto effectively:

## Basic Usage

To run a basic scan on a website, use the following command:

```bash
nikto -h [target URL or IP address]
```

For example, to scan a website at `http://example.com`, use the following command:

```bash
nikto -h http://example.com
```

## Scanning Options

Here are some of the most commonly used scanning options:

| Option                             | Description                                                        |
| ---------------------------------- | ------------------------------------------------------------------ |
| `-ssl`                             | Enables SSL scanning                                               |
| `-nossl`                           | Disables SSL scanning                                              |
| `-port [port number]`              | Specifies the port number to scan                                  |
| `-root [directory]`                | Specifies the root directory of the web server                     |
| `-plugins [plugin1],[plugin2],...` | Specifies a comma-separated list of plugins to use during the scan |
| `-mutate [0-9]`                    | Enables mutation of HTTP requests during the scan                  |
| `-list-plugins`                    | Lists all available plugins                                        |
| `-update`                          | Updates Nikto's plugins and databases                              |

## Output Options

Here are some of the most commonly used output options:

| Option                                   | Description                            |
| ---------------------------------------- | -------------------------------------- |
| `-output [file]`                         | Specifies a file to save the output to |
| `-Format [csv,json,h,jsonv,nbe,sql,txt]` | Specifies the format of the output     |
| `-noshow 404`                            | Suppresses the display of 404 errors   |
| `-Display [V]`                           | Specifies the level of output detail   |
| `-Verbosity [0-2]`                       | Specifies the level of verbosity       |

## Authentication Options

Here are some of the most commonly used authentication options:

| Option                             | Description                                                      |
| ---------------------------------- | ---------------------------------------------------------------- |
| `-id [username:password]`          | Specifies a username and password for HTTP authentication        |
| `-mutate-auth [0-9]`               | Enables mutation of HTTP authentication requests during the scan |
| `-C [cookie]`                      | Specifies a cookie for authentication                            |
| `-auth [type] [username:password]` | Specifies a type of authentication and a username and password   |

## Advanced Options

Here are some of the most commonly used advanced options:

| Option                     | Description                                    |
| -------------------------- | ---------------------------------------------- |
| `-maxtime [seconds]`       | Specifies the maximum time to spend scanning   |
| `-maxdelay [milliseconds]` | Specifies the maximum delay between requests   |
| `-E`                       | Enables Evasion techniques                     |
| `-evasion [1-9]`           | Specifies a level of evasion techniques to use |
| `-Pause [seconds]`         | Specifies a delay between requests             |

## Additional Resources

- [Official documentation](https://cirt.net/Nikto2)
- [Nikto GitHub repository](https://github.com/sullo/nikto)
- [Nikto tutorial](https://www.hackingarticles.in/comprehensive-guide-to-nikto-web-vulnerability-scanner/)
