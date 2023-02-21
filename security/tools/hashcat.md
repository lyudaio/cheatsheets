# Hashcat Cheatsheet

Hashcat is a popular password cracking tool that can be used to break into password-protected systems. This cheatsheet provides a brief overview of some of the most commonly used commands and options in Hashcat.

## Getting Started

Hashcat requires a number of inputs in order to work effectively, including:

| Option             | Description                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------- |
| `-m <mode>`        | Specifies the hash mode to use. The list of modes can be found in the Hashcat documentation.   |
| `-a <attack mode>` | Specifies the attack mode to use. The list of modes can be found in the Hashcat documentation. |
| `<hashfile>`       | Specifies the file containing the hash to crack.                                               |
| `<wordlist>`       | Specifies the wordlist of possible passwords to try.                                           |

Here are some basic commands to get started with Hashcat:

| Command                                                    | Description                                                                 |
| ---------------------------------------------------------- | --------------------------------------------------------------------------- |
| `hashcat -h`                                               | Displays the help menu with all available options.                          |
| `hashcat -m <mode> -a <attack mode> <hashfile> <wordlist>` | Starts cracking the specified hash with the specified mode and attack type. |
| `hashcat -o <output file>`                                 | Specifies the file to output cracked passwords to.                          |
| `hashcat --show`                                           | Shows the cracked passwords on the screen.                                  |

## Hash Types

Hashcat supports a wide range of hash types, including:

| Hash Type | Mode Number |
| --------- | ----------- |
| MD5       | 0           |
| SHA1      | 100         |
| SHA2-256  | 1400        |
| SHA2-512  | 1700        |
| bcrypt    | 3200        |
| NTLM      | 1000        |
| MySQL     | 200         |

Here are some example commands for cracking different types of hashes:

| Command                                 | Description            |
| --------------------------------------- | ---------------------- |
| `hashcat -m 0 <hashfile> <wordlist>`    | Cracks an MD5 hash.    |
| `hashcat -m 100 <hashfile> <wordlist>`  | Cracks a SHA1 hash.    |
| `hashcat -m 1400 <hashfile> <wordlist>` | Cracks a SHA-256 hash. |
| `hashcat -m 1700 <hashfile> <wordlist>` | Cracks a SHA-512 hash. |
| `hashcat -m 3200 <hashfile> <wordlist>` | Cracks a bcrypt hash.  |
| `hashcat -m 1000 <hashfile> <wordlist>` | Cracks an NTLM hash.   |
| `hashcat -m 200 <hashfile> <wordlist>`  | Cracks a MySQL hash.   |

## Attack Modes

Hashcat provides several different attack modes for cracking passwords, including:

| Attack Mode | Description                                                            |
| ----------- | ---------------------------------------------------------------------- |
| Brute-force | Tries every possible combination of characters until it finds a match. |
| Dictionary  | Tries all the words in a dictionary file.                              |
| Hybrid      | Combines dictionary words with brute-force attempts.                   |

Here are some example commands for using different attack modes:

| Attack Mode            | Description                                                    | Example Command                                                      |
| ---------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------- |
| Straight               | Dictionary-based attack with rules applied                     | `hashcat -a 0 -m 0 hash.txt rockyou.txt -r rules/dive.rule`          |
| Combination            | Combine wordlists to generate candidate passwords              | `hashcat -a 1 -m 0 hash.txt rockyou.txt wordlist2.txt`               |
| Mask                   | Custom attack mode using a mask to specify character positions | `hashcat -a 3 -m 0 hash.txt ?d?d?d?d`                                |
| Hybrid Wordlist + Mask | Combine a wordlist and a mask attack                           | `hashcat -a 6 -m 0 hash.txt rockyou.txt -r rules/dive.rule ?d?d?d?d` |
| Hybrid Mask + Wordlist | Combine a mask attack and a wordlist                           | `hashcat -a 7 -m 0 hash.txt rockyou.txt ?d?d?d?d -r rules/dive.rule` |

Here are some additional tips and tricks:

- Use the `--show` option to display cracked passwords
- Use the `--outfile` option to save cracked passwords to a file
- Use the `--force` option to override hash type and algorithm detection
- Use the `--increment` option to perform incremental attacks
- Use the `--session` option to save the session and resume later
- Use the `--status` option to display status updates during an attack
- Use the `--benchmark` option to test hashcat performance

For more information, consult the official [Hashcat documentation](https://hashcat.net/hashcat/).
