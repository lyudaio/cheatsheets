# OpenVAS Cheatsheet

OpenVAS (Open Vulnerability Assessment System) is a free and open-source vulnerability scanner used for testing the security of a network. This cheatsheet covers the basic concepts of OpenVAS and its key features.

## Installation

OpenVAS can be installed on various operating systems, including Linux, Windows, and macOS. Here are the steps to install OpenVAS on Ubuntu:

1. Install the OpenVAS package: `sudo apt install openvas`.
2. Initialize the OpenVAS system: `sudo openvas-setup`.
3. Start the OpenVAS manager: `sudo systemctl start openvas-manager`.
4. Start the OpenVAS scanner: `sudo systemctl start openvas-scanner`.
5. Access the OpenVAS web interface at `https://localhost:9392`.

## Basic Usage

1. Launch a web browser and access the OpenVAS web interface.
2. Login with the default credentials (username: `admin`, password: `admin`).
3. Create a new target by entering the IP address or hostname of the target system.
4. Create a new task by selecting the target and choosing a scan type (e.g. full scan, fast scan, etc.).
5. Start the scan and wait for the results.

## Scan Types

OpenVAS supports several scan types, including:

| Scan Type          | Description                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------- |
| Full and fast      | A comprehensive scan that checks for all known vulnerabilities.                                |
| Full and very deep | A comprehensive scan that checks for all known vulnerabilities and performs additional checks. |
| Fast and very deep | A faster scan that checks for all known vulnerabilities and performs additional checks.        |

## Configuring Scans

OpenVAS provides many options for configuring scans. Here are some important settings:

| Setting       | Description                                                     |
| ------------- | --------------------------------------------------------------- |
| NVT selection | Choose which vulnerability tests (NVTs) to include in the scan. |
| Schedule      | Set the time and frequency of scans.                            |
| Scan options  | Configure scan timing, reporting, and other advanced settings.  |
| Credentials   | Specify login credentials for the target system.                |

## NVTs

NVTs (Network Vulnerability Tests) are the individual tests that OpenVAS uses to detect vulnerabilities. OpenVAS has over 50,000 NVTs available. Here are some important categories of NVTs:

| Category         | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| General          | Basic tests that check for common vulnerabilities.           |
| Web applications | Tests for vulnerabilities in web applications.               |
| Services         | Tests for vulnerabilities in network services.               |
| Compliance       | Tests for compliance with security standards (e.g. PCI DSS). |

## Results

OpenVAS provides detailed reports on the results of each scan. Here are some important sections of the report:

| Section  | Description                                 |
| -------- | ------------------------------------------- |
| Hosts    | Information on each target host.            |
| Alerts   | Details of each vulnerability found.        |
| Services | Information on each target service.         |
| Notes    | Additional information and recommendations. |

## Additional Resources

- [Official documentation:](https://docs.greenbone.net/GSM-Manual/)
- [OpenVAS forums](https://community.greenbone.net/)
- [OpenVAS source code](https://github.com/greenbone/)
- [OpenVAS feeds](https://www.greenbone.net/en/feed-data/)
