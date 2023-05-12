# Chapter 3: Copy, move, create, delete, and organize files from the Bash shell.

### Execute Commands with the Bash Shell:
- Basics covered in other Repo.

> autocomplete cmds: cmdTab
> To re-execute cmd from History: !number
> To copy the last argument of previous commands: Esc + (.) dot

### The File-system Hierarchy:
- `The / directory is the root directory` at the top of the file-system hierarchy
- <img width="450" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/e3e00123-a664-46b0-8a6f-3ab764def18f">
- <img width="454" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/47137330-38d2-4e04-ae09-9e51f44cc856">
- <img width="452" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/7059bcd3-d2f1-4fa2-b48c-272e93e48c5b">
- Persistent: content remains after a reboot. eg. config settings.
- Runtime: content from a process or from the system is deleted on reboot.
- Dynamic or variable content might be modified or appended by active processes.
- Static content remains unchanged until explicitly edited or reconfigured.

> Directory contains regular commands and utilities: /usr/bin
> 
> Directory contains non-persistent process runtime data: /run
> 
> Directory contains installed software programs and libraries: /usr
>
> Absolute path is a fully qualified name that specifies the exact location of the file in the file system hierarchy.
> 
> When a user logs in and opens a command window, the initial location is typically the user's home directory.
> 
> One dot (.) refers to the current directory, and two dots (..) refer to the parent directory, tilde (~) refers to home directory of current user, (-) to toggle between previous & current directory.
> 
> cd (used to return to the current user's home directory)

### Make Links Between Files:
- `ln existingfile.txt /dir/newfile-hardlink.txt` To make a hardlink to file.
- Two types of links: a hard link, or a symbolic link (sometimes called a soft link).
> To determine whether two files are hard linked, use the ls command -i option to list each file's inode number.
> You can use hard links only with regular files. You cannot use the ln command to create a hard link to a directory or special file or on different file system (check `df` for file system).
- 
- `ln -s existingfile.txt /dir/newfile-hardlink.txt` To make a symbolic/softlink to file.
- Symbolic links can link two files on different file systems, can point to a directory or special file.
- A hard link points a name to data on a storage device.
- A symbolic link points a name to another name, which points to data on a storage device.

### Command-line Expansions:
<img width="448" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/796cb226-613e-4d66-97ca-24d33594c5e9">

## Brace Expansion:
- Brace expansion is used to generate discretionary strings of characters.
<img width="457" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/6f15d833-b520-482a-868c-87a70159d994">
> A practical use of brace expansion is to quickly create multiple files or directories.

## Tilde Expansion:
- The tilde character (~), matches the current user's home directory.
<img width="193" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/e9781855-db1d-40d7-8554-10a0e0b89b24">

## Variable Expansion:
- A variable acts like a named container that stores a value in memory.
<img width="185" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/64d14501-7a34-454a-9403-a75dca24ebf0">
> Variable names can contain only letters (uppercase and lowercase), numbers, and underscores. Variable names are case-sensitive and cannot start with a number.

## Command Expansion: `${cmd}`
- Command substitution allows the output of a command to replace the command itself on the command line.


### Pathname Expansion and Pattern Matching:
<img width="661" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/76f5663e-bf8b-457a-bdf3-c58c4f92f79d">
























