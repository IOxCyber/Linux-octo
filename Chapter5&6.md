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



