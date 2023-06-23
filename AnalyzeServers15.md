# Chapter 14:
## Analyze and Manage Remote Servers:
- Web console: RHEL web-based management interface (monitor,performance)
- To install: `dnf install cockpit`
- To enable: `systemctl enable --now cockpit.socket`
- To Verify the status: `systemctl status cockpit.socket`
- Add cockpit service to firewalld on 9090: `firewall-cmd --add-service=cockpit --permanent`
- Log in to the Web Console: `https://servername:9090`
- We can add user, manage services, access terminal etc.

- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/dfc4a25f-0af6-4543-b311-d7a95e8ee1d7">
