# Nmap Cheatsheet

Nmap (Network Mapper) is a popular open-source tool for network exploration, management, and security auditing. This cheatsheet provides a quick reference for some of the most common Nmap commands and options.

## Basic Scan Types

- `nmap [target]`: Perform a simple scan of the target host or network.

- `nmap -sS [target]`: Perform a stealth scan.

- `nmap -sT [target]`: Perform a TCP connect scan.

- `nmap -sU [target]`: Perform a UDP scan.

- `nmap -sA [target]`: Perform an ACK scan.

- `nmap -sW [target]`: Perform a Window scan.

- `nmap -sM [target]`: Perform a Maimon scan.

## Port Specification

- `nmap -p [port list] [target]`: Specify a comma-separated list of ports to scan.

- `nmap --top-ports [number] [target]`: Scan the top `number` most common ports.

## Service and Version Detection

- `nmap -sV [target]`: Attempt to determine the version of services running on the target.

- `nmap -O [target]`: Attempt to determine the operating system of the target.

## Speed and Performance

- `nmap -T [level] [target]`: Specify the timing template for the scan. Available options are `0` (slowest) to `5` (fastest).

- `nmap -F [target]`: Scan only the 100 most common TCP ports.

- `nmap --max-rtt-timeout [time]`: Specify the maximum round-trip time (RTT) timeout value in milliseconds.

- `nmap --min-rtt-timeout [time]`: Specify the minimum round-trip time (RTT) timeout value in milliseconds.

## Output Formats

- `nmap -oN [file] [target]`: Output the results to a normal text file.

- `nmap -oX [file] [target]`: Output the results to an XML file.

- `nmap -oG [file] [target]`: Output the results to a grepable file.

## Miscellaneous Options

- `nmap -v`: Enable verbose output.

- `nmap -6`: Scan an IPv6 target.

- `nmap --open`: Only show open (or filtered) ports.

- `nmap --script [script name]`: Run the specified Nmap script.

- `nmap --datadir [directory]`: Specify the Nmap data directory.

This is by no means a comprehensive list, but it should cover most of the basic usage scenarios for Nmap. For more information and a complete list of options, consult the [Nmap documentation](https://nmap.org/book/).
