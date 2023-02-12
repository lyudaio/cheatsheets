# Debian Cheatsheet

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

## Services Management

- service [service_name] start: Start the [service_name] service
- service [service_name] stop: Stop the [service_name] service
- service [service_name] restart: Restart the [service_name] service
- service [service_name] status: Check the status of the [service_name] service

## File Permissions

- chmod [permissions] [file]: Change the permissions of [file] to [permissions]
- chown [user] [file]: Change the owner of [file] to [user]
- chgrp [group] [file]: Change the group of [file] to [group]

## Users and Groups

- adduser [user]: Add a new user [user]
- addgroup [group]: Add a new group [group]
- usermod -a -G [group] [user]: Add [user] to [group]
- passwd [user]: Change the password of [user]

## Process Management

- ps: Display information about running processes
- top: Display a dynamic real-time view of the system processes
- kill [pid]: Send a signal to terminate the process with the PID [pid]
- killall [process]: Send a signal to terminate all processes with the name [process]
