1. **`/sys`**: `Information about kernel and hardware-related settings and configurations`
    - Similar to `/proc`, it's used for interacting with the kernel and configuring various system parameters.

2. `/etc/services file`: A list of `well-known and registered ports`
3. **`/etc`**: `System configuration files and settings`
- Common subdirectories:
  - `/etc/network` for network configuration,
  - `/etc/apt` for APT package manager configuration (on Debian-based systems), and `/etc/sysconfig` on Red Hat-based systems.

4. **`/var/log`**: `Log files for various system services and applications for troubleshooting and monitoring system activity`
- Common subdirectories: `/var/log/syslog`, `/var/log/auth.log`, and `/var/log/messages`, among others.

3. **`/var/www/html`**: `Default document root for the Apache web server`
   - It contains files served by the webserver to visitors.
   - Web applications, static HTML files, and other web content are often stored here.

4. **`/var/lib`**: `Contains variable data files for applications and services.`
   - It's used for storing databases, state files, and other dynamic data.
   - Common subdirectories include `/var/lib/mysql` for MySQL databases and `/var/lib/docker` for Docker container data.

5. **`/home`**: `Home directories for user accounts are located here.`
   - Each user typically has a subdirectory within `/home` that contains their personal files and settings.
   - Administrators often work with user accounts, permissions, and files stored in home directories

6. **`/opt`**: `Used for third-party applications and software not provided by the distribution's package manager`
   - Optional software packages are typically installed in this directory.
   - Each `3rd party application` may have its subdirectory within `/opt`.

7. **`/tmp`**: `Temporary files and directories are stored here`
   - These files are typically deleted upon system reboot.
   - It's important to regularly clean up the `/tmp` directory to prevent it from filling up and causing issues.

8. **`/usr`**: `Contains user-readable files and programs.`
   - It's often considered the secondary hierarchy in UNIX-like systems.
   - Common subdirectories include `/usr/bin` for executable binaries, `/usr/share` for shared data used by applications, and `/usr/local` for locally installed software.

9. **`/proc`**: `Provides information about currently running processes and system resources`
   - It's a virtual filesystem that exposes kernel data structures in a hierarchical structure.
   - Administrators can view and manipulate process information through files and directories within `/proc`.
