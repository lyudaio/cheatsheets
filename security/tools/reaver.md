# Reaver Cheatsheet

Reaver is a tool used to crack Wi-Fi network WPS (Wi-Fi Protected Setup) passwords. It exploits a flaw in the WPS standard to find the WPA/WPA2 keys used to secure wireless networks.

## Installation

Reaver can be installed on Linux systems using the package manager:

```bash
sudo apt-get install reaver
```

## Usage

To use Reaver, you will need to have a wireless adapter that supports monitor mode and packet injection. You can check if your wireless adapter supports these modes using the `iwconfig` command.

To start the Reaver attack, use the following command:

```bash
reaver -i [interface] -b [BSSID] -c [channel] -vv
```

Here is what each of the options mean:

- `-i [interface]`: specifies the wireless interface to use.
- `-b [BSSID]`: specifies the BSSID of the target AP (Access Point).
- `-c [channel]`: specifies the channel the target AP is on.
- `-vv`: sets the verbosity level to high, which will output more detailed information during the attack.

Once the attack starts, Reaver will begin trying out different PIN combinations to crack the WPS PIN. The attack can take anywhere from a few hours to a few days depending on the complexity of the password.

## Tips

- Make sure your wireless adapter supports monitor mode and packet injection before attempting to use Reaver.
- Reaver is not always successful in cracking WPS passwords, particularly if the router has WPS lockout after a certain number of failed attempts.
- To increase the likelihood of a successful attack, try using the `-S` (small) or `-L` (large) options to limit the range of PINs tested by Reaver.

## Additional Resources

- Reaver User Guide: [https://github.com/t6x/reaver-wps-fork-t6x/blob/master/doc/reaver.txt](https://github.com/t6x/reaver-wps-fork-t6x/blob/master/doc/reaver.txt)
- Reaver GitHub repository: [https://github.com/t6x/reaver-wps-fork-t6x](https://github.com/t6x/reaver-wps-fork-t6x)
- Compatible wireless adapters list: [https://github.com/t6x/reaver-wps-fork-t6x/wiki/Supported-Adapters](https://github.com/t6x/reaver-wps-fork-t6x/wiki/Supported-Adapters)
