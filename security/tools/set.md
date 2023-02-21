# Social Engineering Toolkit (SET) Cheatsheet

SET is a versatile social engineering toolkit that can help simulate phishing and other social engineering attacks.

## Installation

SET comes pre-installed in many security-focused Linux distributions like Kali Linux. However, you can also install it on other platforms.

To install SET, follow these steps:

1. Download the latest version of SET from the official Github repository: https://github.com/trustedsec/social-engineer-toolkit
2. Extract the contents of the downloaded archive.
3. Navigate to the extracted directory.
4. Run the following command to install SET:

   ```bash
   python setup.py install
   ```

## Usage

SET has a wide range of social engineering attack vectors, including phishing emails, credential harvesting, and more. Here are some of the most commonly used attack vectors:

### Spear-phishing Attack Vector

This attack vector allows you to create a spear-phishing email that looks legitimate to the target user. You can use this attack vector to steal credentials or deploy malware.

To use this attack vector, follow these steps:

1. Run the following command to start SET:

   ```bash
   setoolkit
   ```

2. Select the "1) Social-Engineering Attacks" option from the main menu.
3. Select the "2) Website Attack Vectors" option.
4. Select the "3) Credential Harvester Attack Method" option.
5. Select the "2) Site Cloner" option.
6. Enter the URL of the website you want to clone.
7. Wait for the website to be cloned.
8. Select the "4) Spear-Phishing Attack Vector" option.
9. Enter the email address of the target user.
10. Wait for the email to be sent.

### Infectious Media Generator

This attack vector allows you to create a USB drive that deploys malware automatically when plugged into a computer. You can use this attack vector to gain access to the target computer or steal data.

To use this attack vector, follow these steps:

1. Run the following command to start SET:

   ```bash
   setoolkit
   ```

2. Select the "1) Social-Engineering Attacks" option from the main menu.
3. Select the "4) Infectious Media Generator" option.
4. Select the type of payload you want to use.
5. Enter the IP address of the attacking machine.
6. Wait for the payload to be generated.
7. Insert the USB drive into the target computer.

### Website Attack Vector

This attack vector allows you to create a fake website that looks identical to the real one. You can use this attack vector to steal credentials or deploy malware.

To use this attack vector, follow these steps:

1. Run the following command to start SET:

   ```bash
   setoolkit
   ```

2. Select the "1) Social-Engineering Attacks" option from the main menu.
3. Select the "2) Website Attack Vectors" option.
4. Select the type of attack you want to use.
5. Enter the URL of the website you want to clone.
6. Wait for the website to be cloned.
7. Start the web server by running the following command:

   ```bash
   python -m SimpleHTTPServer
   ```

8. Send the link to the target user.

## Additional Resources

For more information on using SET, refer to the official documentation: [https://github.com/trustedsec/social-engineer-toolkit/wiki](https://github.com/trustedsec/social-engineer-toolkit/wiki)
