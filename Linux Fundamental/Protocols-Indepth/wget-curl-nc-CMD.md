### Command Format: command [options…][arguments…]

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
- It can operate in both client and server modes, allowing for various network-related tasks such as file transfer, port scanning, and network troubleshooting.
- For example, to transfer a file from one computer to another using nc - `Syntex: nc -l -p <port>`
1. On the receiving end (server), you use `nc -l -p <port> > file.txt` to listen for incoming connections on a specified port (<port>) and redirect the received data to a file (file.txt).
2. On the sending end (client), you use nc <receiver_ip> <port> < file.txt to connect to the server at the specified IP address (<receiver_ip>) and port, and then send the contents of the file (file.txt) to the server.

> The client initiates communication by making requests to the server & The server listens for incoming connections and responds to client requests.

- ncat is an enhanced version of nc that is part of the Nmap suite of network tools.
- `Syntex: ncat -l -p <port>`
