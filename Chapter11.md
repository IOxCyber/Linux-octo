# Describe Networking Concepts

## TCP/IP Network Model:
- Describes how data communications are **packetized, addressed, transmitted, routed, and received** between computers over a network.
- 4 Layers:
- 1. Application: For Representaion of data. Protocols: SSH, HTTPS (secure web), FTP (file sharing), and SMTP (electronic mail delivery).
- 2. Transport: For virtual-circuit connection between applications (Ports & Protocols) Protocols: TCP/UDP
> A list of well-known and registered ports is in the `/etc/services file`
- 3. Internet: carries data from the source host to the destination host. Protocols: IPv4 and IPv6
- 4. Link: provides the connection to physical media. Protocols: wired Ethernet (802.3) and wireless Wi-Fi (802.11).
- **Summary**:
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/7a7794f7-9908-4a8b-9d7f-b7494f322696)

## Network Interface: 
- eth0, eth1, and eth2 (interface name was the first network port that the operating system detected)
- Ethernet interfaces begin with **en**
- WLAN interfaces begin with **wl**
- WWAN interfaces begin with **ww**
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/bf72f3c3-6122-45b7-9bf2-18707707ebfb)
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/d8201d18-a54e-4bf7-8474-ad1db62ef9bc)

## Example Network Calculations:
- <img width="448" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/ff6e80c1-80ac-40a9-ba72-9f5a1baac52d">
- <img width="451" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/9ed73510-df68-4b5b-9cba-806959948fc2">
- <img width="453" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/db661a13-e393-43c9-b54f-94e29c5a1832">
- <img width="885" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/1b66efc1-de60-4ba5-8af1-56f5078b182b">
> To create static entries for each hostname in each system's `/etc/hosts` file
> A nameserver configuration is typically obtained through DHCP or by creating static address settings in the `/etc/resolv.conf`






