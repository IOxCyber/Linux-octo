# Manage Local Users and Groups: ugo (user, groups, other)

### Users: superuser, system users, and regular user:
- The `superuser/root account administers the system with UID of 0`.
- The `system user accounts are used by processes` that provide supporting services without the need of running as the root.
- Systems use the `/etc/passwd` to store encrypted passwords of any user.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/a02e7bb2-1b87-4428-9dd8-75978facf5c5">
- user entry format in /etc/passwd file `username:password:UID:GID:Comments:Home_Directory:Login Shell`
- `id` command to show information about the currently logged-in user.
- `ps` command to view process information.

### Groups: 
- A collection of users which needs to share access to files and other system resources.
- Systems use the `/etc/group` file to store information about local groups.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/369857a8-2e17-42e5-920f-4b26fa5ea1e5">
- `When a regular user is created, a group is created with the same name` as the user, to be the primary group for the user.

### To check if User has Sudo privileges:
- `sudo -v` or `sudo --validate` (echo $? ->> 0 then User is sudoer)
- The `/etc/sudoers` file is the main configuration file for the sudo command.

## Gain Superuser Access:
- Switch User Accounts `su user_name`
> `sudo` is to log by default all the executed commands to `/var/log/secure`.

> ls -l /home - List out the home dir of all available users.

## Enable or disable sudo access:
<img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/6cd3c434-acf3-4f2a-818c-129c260255ae">

## Manage Local Users:
## Create a User:
- To creates a user called username `useradd username`
- To add user to suplementery/additional group while creating the user `useradd -G group_name user_name`

## Delete a User:
- `userdel username` command removes the username user from /etc/passwd, but leaves the user's home directory intact.
- `userdel -r username` command removes the user from /etc/passwd and deletes the user's home directory.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/e31d7297-d812-49b9-b43e-d350a2469131">

## Modify Existing Users from the Command Line: -g (to change primary group) & -G (to change suplementery/additional group)
- `usermod -g` command to change a user's primary group eg. `usermod -g group01 user02`
- `usermod -aG` command to add a user to a existing/suplementery group eg. `usermod -aG group01 user03`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/98ea1ecb-54c9-4eec-82f3-cfcdf9fc4b08">

## Set Passwords from the Command Line:
- To change **curent** user password: `passwd`
- To change **Other** user password: `passwd Other_Username`
> `root` user can change password of any other user with current password.

## UID ranges: `id`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/0aad5c1d-84ca-47f9-85fe-2f18296e146f">
> A user's primary group is the group that is viewed on the user's account in the /etc/passwd file & A user can belong to only one primary group at a time.

## Manage Local Group Accounts

## Manage Local Groups:
- `groupadd` command creates groups.
- groupadd command -g option specifies a GID for the group to use. eg. `groupadd -g 10000 group01`
- `/etc/login.defs` file defines the range of system GIDs,
- `groupmod` command changes the properties of an existing group
- To rename/modify the group `groupmod -n Old_name New_name`
- To assign new GID `groupmod -g 20000 groupName`
- To delete an Group `groupdel groupName`
> You cannot remove a group if it is the primary group of an existing user

## Temporarily Change Your Primary Group: `newgrp group01`
- `newgrp command` to switch your primary group, in the current shell session.

### Manage User Passwords:
- The cryptographically hashed passwords store in `/etc/shadow` file, which only the `root user` can read.
- each user has an entry with in the /etc/shadow file.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/c74bfdb9-37f5-4005-8e74-c9a3998f84d8">

### Format of an Cryptographically Hashed Password:
- Cryptographically hashed password field stores 3 pieces of information: the `hashing algorithm, the salt, and the cryptographical hash.`
- Each piece of information is `delimited by the dollar ($) character eg. $6$CSsXcYG1L/4ZfHr/$2W6evvJahUfzfHpc9X.45Jc6H30E`
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/beabff9b-4700-490a-997f-91f297fd6bc5">

### Password Verification:
- As a Users, the system -> Checks `/etc/shadow` file -> `combines the salt for the user` -> `Cryptographically hashes` the combination of the salt and plain text password with the specified hashing algorithm. If the result matches the cryptographical hash, then the user typed the right password.

### Configure Password Aging:
- `chage`, which stands for "change age".
- The command defines a minimum age (-m) of zero days, a maximum age (-M) of 90 days, a warning period (-W) of 7 days, and an inactivity period (-I) of 14 days.
- `eg. chage -m 0 -M 90 -W 7 -I 14 user`


### Restrict/Lock Access/user:
- usermod command to modify account expiration for a user eg `usermod -L user`.
- To lock at specific Date: `usermod -L -e 2022-08-14 user`
> Account will not locked for `root user`.
- Unlock the user account: `sudo usermod -U user`
- The nologin shell acts as a replacement shell for the user accounts that are not intended to log in interactively to the system.
- To add user to nologin Shell in case of the user accounts that are not intended to log in interactively to the system, `usermod -s /sbin/nologin newapp`

## Exercise:
- Run `id` to view the current user and group information.
- Print the values of the `$HOME` and `$PATH` variables to determine the home directory and user executables' path.

## Exercise:
- Set the maximum age of the user's password to 90 days: `chage -M 90 user`
- Force a password change on the first login: `chage -d 0 user`
- Set the operator1 account to expire 180 days from the current day:
- 1. Determine a date 180 days in the future: `date -d "+180 days" +%F`
- 2. Set the account to expire on the date: `chage -E "Date_from_Step1" user`
- Set the passwords to expire in 180 days for all users: `vim /etc/login.defs` > change the PASS_MAX_DAYS variable's value to 180.
> The default password and account expiry settings apply to new users but not to existing users.


## Lab - Exercise: Manage Local Users and Groups

- Configure administrative rights to enable all group members to execute any command as any user: 
- - a. create a file in `/etc/sudoers` directory.
- - b. add this to file `%GROUP_NAME  ALL=(ALL) ALL`








