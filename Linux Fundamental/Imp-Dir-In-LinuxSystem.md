1. To `host a file on Apache Web Server`, it uses files inside `/var/www/html` dir.
2. A list of `well-known and registered ports` is in the `/etc/services file`
3. **`/etc`**: `System configuration files and settings`
## Common subdirectories:
 - `/etc/network` for network configuration,
 - `/etc/apt` for APT package manager configuration (on Debian-based systems), and `/etc/sysconfig` on Red Hat-based systems.

4. **`/var/log`**: `Log files for various system services and applications`
   -  are stored here. Monitoring log files is essential for troubleshooting and monitoring system activity.
   - Subdirectories include `/var/log/syslog`, `/var/log/auth.log`, and `/var/log/messages`, among others.

3. **`/var/www/html`**:
   - This directory is the default document root for the Apache web server. It contains files served by the web server to visitors.
   - Web applications, static HTML files, and other web content are often stored here.

4. **`/home`**:
   - Home directories for user accounts are located here. Each user typically has a subdirectory within `/home` that contains their personal files and settings.
   - Administrators often work with user accounts, permissions, and files stored in home directories.

5. **`/var/lib`**:
   - This directory contains variable data files for applications and services. It's used for storing databases, state files, and other dynamic data.
   - Common subdirectories include `/var/lib/mysql` for MySQL databases and `/var/lib/docker` for Docker container data.

6. **`/opt`**:
   - Optional software packages are typically installed in this directory. It's commonly used for third-party applications and software not provided by the distribution's package manager.
   - Each application may have its own subdirectory within `/opt`.

7. **`/tmp`**:
   - Temporary files and directories are stored here. These files are typically deleted upon system reboot.
   - It's important to regularly clean up the `/tmp` directory to prevent it from filling up and causing issues.

8. **`/usr`**:
   - This directory contains user-readable files and programs. It's often considered the secondary hierarchy in UNIX-like systems.
   - Common subdirectories include `/usr/bin` for executable binaries, `/usr/share` for shared data used by applications, and `/usr/local` for locally installed software.

9. **`/proc`**:
   - This directory provides information about currently running processes and system resources. It's a virtual filesystem that exposes kernel data structures in a hierarchical structure.
   - Administrators can view and manipulate process information through files and directories within `/proc`.

10. **`/sys`**:
    - Similar to `/proc`, this directory provides information about kernel and hardware-related settings and configurations.
    - It's used for interacting with the kernel and configuring various system parameters.
