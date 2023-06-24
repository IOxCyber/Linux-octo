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

## Introduction to Red Hat Insights:
- Red Hat Insights is a predictive analytics tool to help you to identify and remediate threats.
- Red Hat delivers Red Hat Insights as a Software-as-a-Service (SaaS) product.
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/bb5ab80e-b388-4ec1-b694-34f5b65c85ef)
- Just register a system with Red Hat Insights Clients & the system will show in the `Red Hat Insights platform`.
- Install Red Hat Insights Clients: `dnf install insights-client`
- To refresh: `insights-client`
- To register: `insights-client --register`
- System will visible in `https://console.redhat.com/insights` web UI.

