# Chapter 14:
## Analyze and Manage Remote Servers:
- Web console: RHEL web-based management interface (monitor,performance)
- To install: `dnf install cockpit`
- To enable: `systemctl enable --now cockpit.socket`
- Add cockpit service to firewalld on 9090: `firewall-cmd --add-service=cockpit --permanent`
- Log in to the Web Console: `https://servername:9090`


