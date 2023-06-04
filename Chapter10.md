# Access the Remote Command Line with SSH:

- Secure Shell Examples: `ssh user_name`
- Identifying Remote Users: `w`
- SSH secures communication through public-key encryption.
- The key might be preconfigured in the /etc/ssh/ssh_known_hosts file, or in the user home directory ~/.ssh/known_hosts file.

## Strict Host Key Checking:
- The StrictHostKeyChecking parameter is set by:
- - the user-specific `~/.ssh/config`
- - system-wide `/etc/ssh/ssh_config`
- - StrictHostKeyChecking= option
- If the StrictHostKeyChecking parameter is set to yes, then the ssh command always aborts the SSH connection if the public keys do not match.
- If the StrictHostKeyChecking parameter is set to no, then the ssh command enables the connection and adds the key of the target host to the ~/.ssh/known_hosts file.


## SSH Known Hosts Key Management:
- The system-wide `/etc/ssh/ssh_known_hosts` file.
- The `~/.ssh/known_hosts` file in each user's home directory.

## :
- 





