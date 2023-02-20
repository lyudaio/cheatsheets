# Traceroute Cheatsheet

## Description

`traceroute` is a command-line tool used to trace the path that an Internet Protocol (IP) packet takes from a source to its destination. It provides information about the IP addresses and routers (or "hops") that the packet passes through on its way to the destination.

## Syntax

```bash
traceroute [-FIldnrv] [-f first_ttl] [-m max_ttl] [-p port] [-q nqueries]
           [-s src_addr] [-t tos] [-w waittime] [-z pausemsecs] host [packetlen]
```

## Options

| Option | Description                                                                          |
| ------ | ------------------------------------------------------------------------------------ |
| `-F`   | Use `IPPROTO_ICMP` type `ECHO` instead of the default UDP probes.                    |
| `-I`   | Use ICMP `ECHOREQ` instead of the default UDP probes.                                |
| `-d`   | Enable socket-level debugging.                                                       |
| `-l`   | Set the initial Time To Live (TTL) value of outgoing packets.                        |
| `-n`   | Do not perform DNS lookups on IP addresses.                                          |
| `-r`   | Bypass the normal routing tables and send directly to a host on an attached network. |
| `-v`   | Verbose output, showing ICMP error messages received in response to packets.         |
| `-f`   | Set the initial TTL value for the first packet sent.                                 |
| `-m`   | Set the maximum number of hops to allow.                                             |
| `-p`   | Set the destination port number for the probes.                                      |
| `-q`   | Set the number of probes to send per hop.                                            |
| `-s`   | Set the source IP address to use.                                                    |
| `-t`   | Set the Type of Service (TOS) value for outgoing packets.                            |
| `-w`   | Set the time (in seconds) to wait for a response.                                    |
| `-z`   | Set the time (in milliseconds) to wait between probes.                               |

## Examples

- To trace the route to the host `google.com`, with a maximum of 30 hops:

  ```bash
  traceroute google.com -m 30
  ```

- To use ICMP `ECHOREQ` probes instead of UDP probes:

  ```bash
  traceroute -I google.com
  ```

- To set the initial TTL value for the first packet to 2:

  ```bash
  traceroute -f 2 google.com
  ```

## Additional Resources

- [traceroute man page](https://linux.die.net/man/8/traceroute)
- [How traceroute works](https://www.lifewire.com/definition-of-traceroute-817952)
