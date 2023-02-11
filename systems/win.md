# Windows Server System Administration Cheatsheet

## General System Information

- Display system information: `systeminfo`
- Display kernel information: `winver`
- Display hostname: `hostname`
- Display system uptime: `net statistics server`

## User Management

- Add user: `net user [username] [password] /add`
- Delete user: `net user [username] /delete`
- Add user to group: `net localgroup [groupname] [username] /add`
- Remove user from group: `net localgroup [groupname] [username] /delete`

## File System Management

- Display disk usage: `fsutil volume diskfree [drive letter]`
- Create directory: `md [directory name]`
- Change file/directory permissions: `icacls [file/directory name] [options] [permission specifications]`

## Package Management

- Install package: `Server Manager` > `Manage` > `Add Roles and Features`
- Remove package: `Server Manager` > `Manage` > `Remove Roles and Features`
- Search for package: `Get-WindowsFeature`

## Network Configuration

- Display IP address: `ipconfig`
- Display routing information: `route print`
- Display network interfaces: `Get-NetAdapter`
- Edit network interfaces: `ncpa.cpl`

## Services

- List all services: `Get-Service`
- Start service: `Start-Service [service name]`
- Stop service: `Stop-Service [service name]`
- Restart service: `Restart-Service [service name]`

## Process Management

- Display running processes: `Get-Process`
- Kill process: `Stop-Process -Id [process ID]`
- Kill process by name: `Get-Process | Where-Object { $_.ProcessName -eq "[process name]" } | Stop-Process`
