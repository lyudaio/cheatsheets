# iptables Cheatsheet

This cheatsheet covers the basic commands and syntax for the `iptables` command in Linux. `iptables` is a powerful firewall tool that allows you to control incoming and outgoing traffic to your server.

## Basic Syntax

```bash
iptables [-t table] command chain rule-specification [options]
```

- `-t table` - Specifies the table to work with (default is `filter`).
- `command` - Specifies the action to take (`-A` to append a rule, `-D` to delete a rule, `-I` to insert a rule, `-L` to list rules, etc.).
- `chain` - Specifies the chain to work with (`INPUT`, `OUTPUT`, `FORWARD`, etc.).
- `rule-specification` - Specifies the criteria that must be met for the rule to apply (e.g., `-s` to specify a source IP address, `-p` to specify a protocol, etc.).
- `options` - Additional options for the rule (e.g., `-j` to specify the target of the rule, `-i` to specify the input interface, `-o` to specify the output interface, etc.).

## Common Commands

| Command                                           | Description                                          |
| ------------------------------------------------- | ---------------------------------------------------- |
| `iptables -A INPUT -p tcp --dport 22 -j ACCEPT`   | Allow incoming SSH traffic on port 22.               |
| `iptables -A INPUT -p tcp --dport 80 -j ACCEPT`   | Allow incoming HTTP traffic on port 80.              |
| `iptables -A INPUT -p tcp --dport 443 -j ACCEPT`  | Allow incoming HTTPS traffic on port 443.            |
| `iptables -A INPUT -p icmp -j ACCEPT`             | Allow incoming ICMP (ping) traffic.                  |
| `iptables -A INPUT -j DROP`                       | Drop all incoming traffic that doesn't match a rule. |
| `iptables -A OUTPUT -p tcp --dport 80 -j ACCEPT`  | Allow outgoing HTTP traffic on port 80.              |
| `iptables -A OUTPUT -p tcp --dport 443 -j ACCEPT` | Allow outgoing HTTPS traffic on port 443.            |
| `iptables -A OUTPUT -p icmp -j ACCEPT`            | Allow outgoing ICMP (ping) traffic.                  |
| `iptables -A OUTPUT -j DROP`                      | Drop all outgoing traffic that doesn't match a rule. |
| `iptables -L`                                     | List all current rules.                              |
| `iptables -F`                                     | Flush all current rules.                             |
| `iptables-save > /etc/iptables/rules.v4`          | Save current rules to a file (iptables v4).          |
| `iptables-restore < /etc/iptables/rules.v4`       | Restore saved rules from a file (iptables v4).       |
| `ip6tables-save > /etc/iptables/rules.v6`         | Save current rules to a file (iptables v6).          |
| `ip6tables-restore < /etc/iptables/rules.v6`      | Restore saved rules from a file (iptables v6).       |

## Additional Resources

For more information about using `iptables`, consult the official `iptables` documentation:

- [Netfilter/Iptables Official Documentation](https://www.netfilter.org/documentation/)
