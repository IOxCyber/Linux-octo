## Chapter 1:
### Linux: Open source, CLI based OS.
- In 1991, graduate student Linus Torvalds developed a UNIX-like kernel that he named Linux, and licensed it as open source software under the GPL
- Open source software is `software with source code that anyone can use, study, modify, and share.`
- Open source has many benefits for the user such as `Control, Implement real world Security, Stability & Stability`
- 2 types of copyrights for OSS are `1. Copyleft licenses[^1] 2. Permissive licenses[^2]`
- Developers of Open Source Software `By professional & Volunteers and the academic community`
- `A Linux distribution provides an easy method` to install and manage a working Linux system eg. Ubuntu, debian, RedHat RHEL, Kali Linux, Fedora, Parrot OS etc.

### Red Hat Enterprise Linux:
- `Red Hat Enterprise Linux (RHEL)` is Red Hat's production-ready, commercially supported Linux distribution. 
- `RHEL CoreOS (RHCOS)` is not a stand-alone operating system, but it is built from RHEL components, and is then released, upgraded, and managed as part of the Red Hat OpenShift Container Platform (RHOCP) for cloud-native applications.
- `Red Hat Universal Base Image (UBI)` is essentially a freely redistributable derivative of RHEL
- `RHEL for Edge` is an image-based variant of RHEL, with a different deployment mechanism. RHEL provides the ability to create purpose-built operating system images through a tool called Image Builder.

## Chapter 2:
- CLI: A command line is a text-based interface that is used to input instructions to a computer system.
- If `regular user` starts a shell, the prompt includes an ending `dollar ($) character eg. [user@host ~]$`
- If `superuser/root user` starts a shell, the prompt includes an ending `hash (#) character eg. [user@host ~]#`
- `CMds Options Args`

### Points to Note: `Login to Remote VM with SSH`
> The bash shell is conceptually similar to the Microsoft Windows cmd.exe command-line interpreter.

> In Linux, the most common way to get a shell prompt on a remote system is to use Secure Shell (SSH) (ssh command encrypts the connection)

> An alternative way to authenticate to a remote machine without entering a password is through public key authentication, users have a special identity file with a private key, which is equivalent to a password. 

> when we try to connect to a new remote host with ssh, the remote host sends its host key to authenticate itself and to help to set up encrypted communication[^3], this `host key` will be saved for future reference & connection gets established.

> To log out `ctrl+c` or `exit`

### Quiz 2:
- Term describes the interpreter - shell
- Term describes the visual cue that indicates that an interactive shell is waiting for the user to type - prompt
- Term describes an interface that provides a display for output and a keyboard for input to a shell session - Terminal
- term describes one of multiple logical consoles that can each support an independent login session - virtual console

- `GNOME 40` is the default desktop environment in Red Hat Enterprise Linux 9
<img width="756" alt="image" src="https://user-images.githubusercontent.com/40174034/236505951-184a384f-75bd-41de-a6e3-912289c61496.png">
- 1. Top bar, 2. Activities Overview, 3. System Menu, 4. Dash, 5. Windows Overview, 6. Workspace selector, 7. Meessage try
> `Alt+F2` key combination to open the Enter a Command.
> 




































[^1]: Copyleft, or "share-alike" licenses, require that anyone who distributes the source code, with or without changes, must pass along the freedom for others to also copy, change, and distribute the code. Common copyleft licenses include the GNU General Public License (GPL) and the Lesser GNU Public License (LGPL).

[^2]: Permissive licenses maximize the reusability of source code. You can use the source for any purpose if the copyright and license statements are preserved, including reusing code under more restrictive or proprietary licenses. Examples of permissive licenses include the MIT/X11 license, the Simplified BSD license, and the Apache Software License 2.0

[^3]: The ssh command compares the host key against a list of saved host keys to ensure that it is not changed. If the host key changed, then it might indicate that someone is trying to pretend to be that host to hijack the connection, which is also known as an interceptor attack.
