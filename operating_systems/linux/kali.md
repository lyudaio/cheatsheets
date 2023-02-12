# Kali Linux Cheatsheet

## Basic Terminal Commands

- ls: List the contents of the current directory
- cd [directory]: Change the current working directory to [directory]
- pwd: Print the current working directory
- cat [file]: Display the contents of [file]
- cp [source] [destination]: Copy [source] to [destination]
- mv [source] [destination]: Move [source] to [destination]
- rm [file]: Remove [file]
- rmdir [directory]: Remove [directory]
- touch [file]: Create a new empty file [file]
- echo [text]: Display [text] on the terminal

## Package Management

- apt update: Update the package list
- apt upgrade: Upgrade installed packages to their latest versions
- apt install [package]: Install [package]
- apt remove [package]: Remove [package]
- apt search [keyword]: Search for packages containing [keyword]

## Networking

- ifconfig: Display information about network interfaces
- ping [host]: Test the connectivity to [host]
- traceroute [host]: Trace the route to [host]
- nmap [host/network]: Scan [host/network] for open ports and services

## Wireless Networking

- airmon-ng: Start the wireless network interface in monitor mode
- airodump-ng [interface]: Capture wireless network traffic on [interface]
- aireplay-ng [options] [interface]: Inject wireless network traffic on [interface]

## Information Gathering

- whois [domain]: Look up information about [domain]
- nslookup [domain]: Resolve [domain] to an IP address
- dig [domain]: Look up DNS information for [domain]
- nbtscan [network]: Scan [network] for NetBIOS information

## Web Application Testing

- sqlmap: Automated SQL injection tool
- burp suite: Integrated platform for web application security testing
- w3af: Web Application Attack and Audit Framework

## Metasploit Framework

- msfconsole: Start the Metasploit Framework console
- use [module]: Load the specified Metasploit module
- show options: Display available options for the current module
- exploit: Launch the attack specified by the current module
- back: Go back to the previous context in the Metasploit console
