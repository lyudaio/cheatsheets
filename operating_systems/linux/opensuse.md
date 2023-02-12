# OpenSUSE Cheatsheet

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

- zypper update: Update the package list
- zypper upgrade: Upgrade installed packages to their latest versions
- zypper install [package]: Install [package]
- zypper remove [package]: Remove [package]
- zypper search [keyword]: Search for packages containing [keyword]

## Networking

- ifconfig: Display information about network interfaces
- ping [host]: Test the connectivity to [host]
- traceroute [host]: Trace the route to [host]
- nmap [host/network]: Scan [host/network] for open ports and services

## Services Management

- systemctl start [service_name]: Start the [service_name] service
- systemctl stop [service_name]: Stop the [service_name] service
- systemctl restart [service_name]: Restart the [service_name] service
- systemctl status [service_name]: Check the status of the [service_name] service

## File Permissions

- chmod [permissions] [file]: Change the permissions of [file] to [permissions]
- chown [user] [file]: Change the owner of [file] to [user]
- chgrp [group] [file]: Change the group of [file] to [group]

## Users and Groups

- useradd [user]: Add a new user [user]
- groupadd [group]: Add a new group [group]
- usermod -a -G [group] [user]: Add [user] to [group]
- passwd [user]: Change the password of [user]

## Process Management

- ps: Display information about running processes
- top: Display a dynamic real-time view of the system processes
- kill [pid]: Send a signal to terminate the process with the PID [pid]
- killall [process]: Send a signal to terminate all processes with the name [process]
