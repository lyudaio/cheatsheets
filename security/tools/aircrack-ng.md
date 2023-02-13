# Aircrack-ng (1.7)

Aircrack-ng is a suite of tools to assess Wi-Fi network security. It works by capturing and analyzing packets of data sent and received over a wireless network.

## Scanning for Networks

To scan for available Wi-Fi networks, use the following command:

```bash
airodump-ng wlan0
```

Replace `wlan0` with the name of your wireless interface.

## Capturing Packets

To capture packets from a specific network, use the following command:

```bash
airodump-ng -c <channel> --bssid <bssid> -w <filename> wlan0
```

Replace `<channel>` with the channel number of the network, `<bssid>` with the BSSID (MAC address) of the access point, `<filename>` with a desired name for the output file, and `wlan0` with the name of your wireless interface.

## Cracking Passwords

To crack the password of a WPA/WPA2 network, use the following command:

```bash
aircrack-ng <filename>.cap -w <wordlist>
```

Replace `<filename>` with the name of the captured packets file and `<wordlist>` with the path to a wordlist file containing possible passwords.

END_OF_MESSAGE
