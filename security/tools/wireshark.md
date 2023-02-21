# Wireshark Cheatsheet

Wireshark is a free and open-source packet analyzer that allows you to see what's happening on your network at a microscopic level. Here are some of the key features and commands that you need to know when working with Wireshark.

## Key Features

- **Capture and display packets**: Wireshark can capture and display packets from a wide range of network protocols, including Ethernet, Wi-Fi, Bluetooth, and many others.
- **Powerful filtering**: Wireshark provides a powerful filtering system that allows you to focus on the packets that matter most to you.
- **Live capture and offline analysis**: Wireshark can capture packets in real-time, as well as analyze packets that have been captured and saved to a file.
- **Customizable views**: Wireshark allows you to customize the way packets are displayed, including the color scheme, layout, and more.

## Basic Commands

Here are some of the basic commands that you need to know when working with Wireshark:

| Command                 | Description                                                                       |
| ----------------------- | --------------------------------------------------------------------------------- |
| `wireshark`             | Start Wireshark                                                                   |
| `wireshark -k`          | Start Wireshark and immediately start capturing packets                           |
| `wireshark -r <file>`   | Open a capture file for analysis                                                  |
| `wireshark -f <filter>` | Start Wireshark and immediately start capturing packets with the specified filter |

## Advanced Commands

Here are some of the advanced commands that you can use when working with Wireshark:

| Command                  | Description                                |
| ------------------------ | ------------------------------------------ |
| `tshark -i <interface>`  | Capture packets on the specified interface |
| `tshark -D`              | List available capture interfaces          |
| `tshark -r <file>`       | Analyze a capture file                     |
| `tshark -V`              | Display packet details in verbose mode     |
| `tshark -R <filter>`     | Apply a filter to the packets              |
| `tshark -z <statistics>` | Generate statistics on captured packets    |

## Additional Resources

For more information on Wireshark and how to use it, check out the following resources:

- [Wireshark User Guide](https://www.wireshark.org/docs/wsug_html/)
- [Wireshark Tutorials](https://www.wireshark.org/docs/tutorial/)
- [Wireshark Wiki](https://wiki.wireshark.org/)
- [Wireshark Mailing Lists](https://www.wireshark.org/lists/)
- [Wireshark Bug Tracker](https://bugs.wireshark.org/)
