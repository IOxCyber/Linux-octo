# Chapter 10: Access the Remote Command Line with SSH:

- Secure Shell Examples: `ssh user_name@IP_Host`
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

## Configure SSH Key-based Authentication:
- To create a key pair `ssh-keygen`
- Private and public keys are saved in the ~/.ssh/id_rsa and ~/.ssh/id_rsa.pub files.
> Always create backups of your keys, if they are overwritten or lost.
- To add private keys from the default ~/.ssh/id_rsa file eg. `ssh-add`
- and then from a ~/.ssh/key-with-pass eg. `ssh-add ~/.ssh/key-with-pass`

## Basic SSH Connection Troubleshooting:
- `ssh -v user@remotehost`
- The ssh command provides three verbosity levels with the -v, -vv, and -vvv options.

## Lab 1: Configure SSH Key-based Authentication
- Generate a set of SSH keys: `ssh-keygen`
- Send/Export/Copy the Public Key of the SSH key pair to the other user on different machine. `ssh-copy-id Public_Key user@hostNameOrIP`
- Execute the hostname command on the servera machine remotely by using the ssh command without accessing the remote interactive shell `ssh user@hostNameOrIP hostname` 

## Configure the OpenSSH Server:
- The `sshd` daemon provides the OpenSSH service, can configure the service by editing the `/etc/ssh/sshd_config` file.
- To prohibit direct login to the root user account from remote systems `PermitRootLogin no` > To apply changes `systemctl reload sshd`
> Whenever you change the /etc/ssh/sshd_config file, you must reload the sshd service to apply the changes.

## Summary:
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/d8220fb9-3d13-4ada-9455-887b21a7914d">





