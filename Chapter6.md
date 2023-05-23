# Manage Local Users and Groups: ugo (user, groups, other)

### Users: superuser, system users, and regular user:
- The superuser/root account administers the system with UID of 0.
- The system user accounts are used by processes that provide supporting services without the need of running the as the root.
- Systems use the `/etc/passwd` file to store information about local user.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/a02e7bb2-1b87-4428-9dd8-75978facf5c5">
- `id` command to show information about the currently logged-in user.
- `ps` command to view process information.

### Groups: 
- A collection of users that need to share access to files and other system resources.
- Systems use the `/etc/group` file to store information about local groups.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/369857a8-2e17-42e5-920f-4b26fa5ea1e5">
- `When a regular user is created, a group is created with the same name` as the user, to be the primary group for the user.
- 
### To check if USer is has Sudo privileges:
- `sudo -v` or `sudo --validate` (echo $? ->> 0 then User is sudoer)
- The `/etc/sudoers` file is the main configuration file for the sudo command.

## Gain Superuser Access:
- Switch User Accounts `su user_name`
- `sudo` is to log by default all the executed commands to `/var/log/secure`.

> ls -l /home - List out the home dir of all available users.

## Enable or disable sudo access:
<img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/6cd3c434-acf3-4f2a-818c-129c260255ae">

## Manage Local Users:
## Create a User:
- `useradd username` command creates a user called username.

## Delete a User:
- `userdel username` command removes the username user from /etc/passwd, but leaves the user's home directory intact.
- `userdel -r username` command removes the user from /etc/passwd and deletes the user's home directory.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/e31d7297-d812-49b9-b43e-d350a2469131">

## Modify Existing Users from the Command Line:
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/98ea1ecb-54c9-4eec-82f3-cfcdf9fc4b08">

## Set Passwords from the Command Line:
- `root` user can change password of any other user with current password.

## UID ranges: `id`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/0aad5c1d-84ca-47f9-85fe-2f18296e146f">






















## Exercise:
- Run `id` to view the current user and group information.
- Print the values of the `$HOME` and `$PATH` variables to determine the home directory and user executables' path.
- 












