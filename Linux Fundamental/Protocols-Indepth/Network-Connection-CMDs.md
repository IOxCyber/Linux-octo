> Command Format: command [options…][arguments…]
> 
## Network Configuration:
- `ifconfig [OPTIONS]`
> The iwconfig command is similar to the ifconfig command, but it is dedicated to wireless network interfaces.
> The lo device is the loopback device, a special network device used by the system when sending network-based data to itself.
- `ping ipaddress/hostname`
- The ping command is used to verify connectivity between two computers.

## Utility Commands:
1. wget: 
- stands for web get. The wget is a free non-interactive file downloader command. 
- Non-interactive means it can work in background when user is not logged in. This allows user to get disconnected with the system while wget finish its work.
- eg. wget http://website.com/files/file.zip

2. curl:
- Use to transfer data to or from a server, using any of the supported protocols (HTTP, FTP, IMAP, POP3, SCP, SFTP, SMTP, TFTP, TELNET, LDAP, or FILE).
- This tool is preferred for automation since it is designed to work without user interaction. curl can transfer multiple files at once.
- Wget is a simple transfer utility, while curl offers so much more.
- eg. curl [options] [URL...]

3. nc or ncat:
- nc (netcat) used for reading from and writing to network connections.
- For example, to transfer a file from one computer to another using nc, you can run `nc -l -p <port> > file.txt` on the receiving end
- and `nc <receiver_ip> <port> < file.txt` on the sending end.
- `Syntex: nc -l -p <port>`
- ncat is an enhanced version of nc that is part of the Nmap suite of network tools.
- `Syntex: ncat -l -p <port>`

4. 

