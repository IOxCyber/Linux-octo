### Chapter 5. Create, View, and Edit Text Files:
- File Descriptors: A running program, or process, reads input and writes output.
- All processes start with at least three file descriptors. 
1. Standard input (channel 0) reads input from the keyboard. 
2. Standard output (channel 1) sends normal output to the terminal. 
3. Standard error (channel 2) sends error messages to the terminal.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/abb92fd0-069e-4293-a937-efeaa289c45d">
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/07abe697-05f7-4b6a-9cf4-88bb3df73a7f">


## Redirect Output to a File: 
- Command_Output > newFile
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/f4ac0be4-746a-4e72-b2d7-a44cd759f3bf">

## Construct Pipelines (|):
- A pipeline connects the standard output of the first command to the standard input of the next command.

> To discard the output of a process, you can redirect to the empty `/dev/null` special file.

## Edit Text Files from the Shell Prompt:
- [Vimtutor](http://www2.geog.ucl.ac.uk/~plewis/teaching/unix/vimtutor)
- Edit: `vim file_name`
- Exit without saved changes: `Esc + :!q` or `Shift+ZZ`
- Save & Exit: `:wq`
- `shift+v` (block mode of Vim/to select) & `press x` to delete
- `Uppercase V` (visual line mode of Vim/select a line)

### Change the Shell Environment

## Shell Variable Usage: `$VAR=value`
- Shell variables can help you to run commands, and are unique to a shell session.

Set the Default Text Editor: `export EDITOR=nano`
- The EDITOR environment variable specifies your default text editor for command-line programs. 

## Bash Aliases: 
### Set Alias: `alias 'Text=command'`
- Bash aliases are shortcuts to other Bash commands. 
- eg. alias hello='echo "Hello, this is a long string."'

### unset Alias:
- `unset VAR`
- `unalias 'Text'`

> ls -R Directory_path
> ls -l File_Name

## Back up and append the date:
- cp $file_var fileWithDate_$(date +%s).txt



