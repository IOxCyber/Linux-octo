# Chapter 7. Control Access to Files:

## Linux File-system Permissions:
- File permissions control access to files.
- You can set 3 permissions eg. ugo (user, group, other)
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/9bfccd73-cde6-45b8-ac44-a01b67d41f10">

## View File and Directory Permissions and Ownership:
- `ls -l file`
- The `. special directory` reflects the permissions of dir itself.
- The `.. special directory` reflects the permissions of its parent directory.

## Change File and Directory Permissions:`chmod: change mode`
1. **Symbolic method**: `chmod Who/What/Which file|directory` or who=u,g,o,a | what=+,-,= | which=r,w,x
- eg. chmod go-rw file, chmod a+x file
> By default, the permission apply to the file/dir not entire directory. To apply to entire directory tree eg. `chmod -R ug+rwx /home/user/folder`

2. **Octal Method**: `chmod ### file|directory` or ###=any single digit (0-7) (read=4,write=2,execute=1)
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/055cd6ad-2f40-4ce0-a22c-7e6d9632f1c0">

## Change File and Directory User or Group Ownership: `chown`
- user owns a file that it creates
- To recursively changes the ownership of an entire directory tree: `chown -R user Dir`
- To change group ownership of a file by preceding the group name with a colon (:) `chown :admins Dir`

## Default File Permissions:
- `umask` which stands for user file-creation mask, it works as substracting `initial permission - umask value` [^1]example
- If you create a directory, then its initial octal permissions are 0777 (drwxrwxrwx).
- If you create a regular file, then its initial octal permissions are 0666 (-rw-rw-rw-).
- The system's `default umask values` (umask) for Bash shell users are defined in the `/etc/login.defs` and in the `/etc/bashrc` file.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/3788c4d8-e338-4d0c-ae81-ce455296032b">
- To change default umask for a user: `echo "umask 007" >> ~/.bashrc`


## Summary:
- `ls -ld dir` - to check dir content & permissions
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/67e04f47-f7b6-45de-8ae7-c0fa38aadad4">









[^1]: If you create a regular file, then its initial octal permissions are 0666 (000 110 110 110, in binary representation). Then, the 0022 umask (000 000 010 010) disables the write permission bit for group and others. Thus, the owner has both read and write permission on files, and both group and other are set to read (000 110 100 100).
