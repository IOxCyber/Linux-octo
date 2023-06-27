# Chapter9: Control Services and Daemons:

## Identify Automatically Started System Processes:
- `Daemons` are processes that either wait or run in the background, to perform various tasks.
- Daemons `start automatically at boot time and continue to run until shutdown or until you manually stop` them.
- `daemon names end with d.`
- A service in the systemd sense often refers to one or more daemons.
- systemd unit is an abstract concept to define objects that the system knows how to manage.
- `Units` are represented by `configuration files` called unit files, which encapsulate `information about system services, listening sockets, and other relevant objects` for the systemd init system.Units are represented by configuration files called unit files, which encapsulate information about system services, listening sockets, and other relevant objects for the systemd init system.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/892d0e0f-57ff-46c3-a9a7-a9ec968f0a50">

## List Service Units: `systemctl` used to control and manage systemd and services.
- `systemctl` to lists units that are both loaded and active. `systemctl list-units --type=service`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/82e26047-69ed-4d26-9f60-1071492655d5">
> By default, the systemctl list-units --type=service command lists only the service units with active activation states.
- `systemctl status name.type` To verify the status of a service eg. systemctl status sshd.service
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/803337d7-862b-4112-bc22-007bbdd3dc7e">
- `systemctl is-active sshd.service` To Verify the Status of a Service
- Systemctl Output: <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/92a94467-284b-46f1-b4d4-4f5dac777f6d">
- 
- To start/stop/restart/reload service: `systemctl start/stop/restart/reload Service_name`
- Mask and Unmask Services: To prevent starting a service that conflicts with other services: `systemctl mask service_name` & `systemctl unmask service_name`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/84f9479a-4b2d-4cd3-aeef-bd8fd50d6b23">
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/d2238cfa-4551-45c8-ad7b-ce1b980eab54">

