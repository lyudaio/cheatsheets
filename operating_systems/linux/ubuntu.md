# Ubuntu System Administration Cheatsheet

## General System Information

- Display system information: `lsb_release -a`
- Display kernel information: `uname -a`
- Display hostname: `hostname`
- Display system uptime: `uptime`

## User Management

- Add user: `sudo adduser [username]`
- Delete user: `sudo userdel [username]`
- Add user to group: `sudo adduser [username] [groupname]`
- Delete user from group: `sudo gpasswd -d [username] [groupname]`

## File System Management

- Display disk usage: `df -h`
- Create directory: `mkdir [directory name]`
- Change file permissions: `chmod [options] [file/directory name]`
- Change file ownership: `chown [options] [file/directory name]`

## Package Management

- Update package information: `sudo apt update`
- Upgrade packages: `sudo apt upgrade`
- Install package: `sudo apt install [package name]`
- Remove package: `sudo apt remove [package name]`
- Search for package: `sudo apt search [package name]`

## Network Configuration

- Display IP address: `ip addr show`
- Display routing information: `ip route`
- Display network interfaces: `ifconfig`
- Edit network interfaces: `sudo nano /etc/network/interfaces`

## Services

- List all services: `sudo service --status-all`
- Start service: `sudo service [service name] start`
- Stop service: `sudo service [service name] stop`
- Restart service: `sudo service [service name] restart`

## Process Management

- Display running processes: `ps aux`
- Kill process: `kill [process ID]`
- Kill process by name: `killall [process name]`
