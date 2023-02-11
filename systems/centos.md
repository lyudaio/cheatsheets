# CentOS System Administration Cheatsheet

## General System Information

- Display system information: `cat /etc/centos-release`
- Display kernel information: `uname -a`
- Display hostname: `hostname`
- Display system uptime: `uptime`

## User Management

- Add user: `sudo useradd [username]`
- Delete user: `sudo userdel [username]`
- Add user to group: `sudo usermod -a -G [groupname] [username]`
- Delete user from group: `sudo gpasswd -d [username] [groupname]`

## File System Management

- Display disk usage: `df -h`
- Create directory: `mkdir [directory name]`
- Change file permissions: `chmod [options] [file/directory name]`
- Change file ownership: `chown [options] [file/directory name]`

## Package Management

- Update package information: `sudo yum update`
- Upgrade packages: `sudo yum upgrade`
- Install package: `sudo yum install [package name]`
- Remove package: `sudo yum remove [package name]`
- Search for package: `sudo yum search [package name]`

## Network Configuration

- Display IP address: `ip addr show`
- Display routing information: `ip route`
- Display network interfaces: `ifconfig`
- Edit network interfaces: `sudo nano /etc/sysconfig/network-scripts/ifcfg-[interface]`

## Services

- List all services: `sudo systemctl list-units --type=service`
- Start service: `sudo systemctl start [service name]`
- Stop service: `sudo systemctl stop [service name]`
- Restart service: `sudo systemctl restart [service name]`

## Process Management

- Display running processes: `ps aux`
- Kill process: `kill [process ID]`
- Kill process by name: `killall [process name]`
