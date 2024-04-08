1. To host the files & accessible on web browser. `sudo service apache2 start`
Certainly! Here are some additional commands commonly used by Linux system administrators for various tasks:

## Other CMDs:
1. **Managing Services**:
   - **Start a Service**: `sudo service <service-name> start`
   - **Stop a Service**: `sudo service <service-name> stop`
   - **Restart a Service**: `sudo service <service-name> restart`
   - **Enable a Service to Start on Boot**: `sudo systemctl enable <service-name>`
   - **Disable a Service from Starting on Boot**: `sudo systemctl disable <service-name>`
   - **Check Service Status**: `sudo systemctl status <service-name>`

2. **User and Group Management**:
   - **Create a New User**: `sudo adduser <username>`
   - **Change User Password**: `sudo passwd <username>`
   - **Add User to a Group**: `sudo usermod -aG <group> <username>`
   - **Create a New Group**: `sudo addgroup <groupname>`
   - **Change Group Ownership of a File or Directory**: `sudo chown :<group> <file>`
   
3. **File and Directory Operations**:
   - **Change File Permissions**: `chmod <permissions> <file>`
   - **Change Ownership of a File or Directory**: `sudo chown <user>:<group> <file>`
   - **Create a New Directory**: `mkdir <directory-name>`
   - **Copy Files or Directories**: `cp <source> <destination>`
   - **Move or Rename Files or Directories**: `mv <source> <destination>`
   - **Delete Files or Directories**: `rm <file/directory>`

4. **Package Management**:
   - **Install a Package**: `sudo apt install <package-name>`
   - **Update Package List**: `sudo apt update`
   - **Upgrade Installed Packages**: `sudo apt upgrade`
   - **Remove a Package**: `sudo apt remove <package-name>`

5. **Networking**:
   - **Show Network Interfaces**: `ip addr show`
   - **Configure Network Interface**: `sudo ifconfig <interface> <IP-address>`
   - **Show Routing Table**: `ip route show`
   - **Check Network Connectivity**: `ping <hostname or IP-address>`
   - **Open Port in Firewall**: `sudo ufw allow <port>/tcp`

6. **System Information**:
   - **View System Information**: `uname -a`
   - **Check System Load**: `top` or `htop`
   - **Check Disk Usage**: `df -h`
   - **Check Memory Usage**: `free -h`
   - **View System Logs**: `tail /var/log/syslog`
