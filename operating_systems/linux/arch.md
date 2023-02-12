# Arch Linux System Administration Cheatsheet

## General System Information

- Display system information: `cat /etc/arch-release`
- Display kernel information: `uname -a`
- Display hostname: `hostname`
- Display system uptime: `uptime`

## User Management

- Add user: `sudo useradd -m [username]`
- Delete user: `sudo userdel [username]`
- Add user to group: `sudo gpasswd -a [username] [groupname]`
- Remove user from group: `sudo gpasswd -d [username] [groupname]`

## File System Management

- Display disk usage: `df -h`
- Create directory: `mkdir [directory name]`
- Change file/directory permissions: `chmod [options] [file/directory name]`
- Change file/directory ownership: `chown [options] [file/directory name]`

## Package Management

- Update package information: `sudo pacman -Sy`
- Upgrade packages: `sudo pacman -Su`
- Install package: `sudo pacman -S [package name]`
- Remove package: `sudo pacman -R [package name]`
- Search for package: `sudo pacman -Ss [package name]`

## Network Configuration

- Display IP address: `ip addr show`
- Display routing information: `ip route`
- Display network interfaces: `ip link show`
- Edit network interfaces: `sudo nano /etc/systemd/network/[interface].network`

## Services

- List all services: `sudo systemctl list-units --type=service`
- Start service: `sudo systemctl start [service name]`
- Stop service: `sudo systemctl stop [service name]`
- Restart service: `sudo systemctl restart [service name]`
- Enable service: `sudo systemctl enable [service name]`
- Disable service: `sudo systemctl disable [service name]`

## Process Management

- Display running processes: `ps aux`
- Kill process: `kill [process ID]`
- Kill process by name: `pkill [process name]`
