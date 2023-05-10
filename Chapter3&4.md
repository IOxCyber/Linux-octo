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
> 
> 


