# Chapter 8: Monitor and Manage Linux Processes

## Process States and Lifecycle:
- A **process** is a running instance of a launched, executable program.
- A process consists of `Address Space`, `ownership credentials and privileges`, `Execution Threat(s), Process State`.
- Env of process: `Local/Global var, Allocated system resources etc`
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/fd7941e6-a7a0-43c7-b2c0-dadb8f958686)
- Through the fork routine, a child process inherits security identities, previous and current file descriptors, port and resource privileges, environment variables, and program code.
> Normally, a parent process sleeps when the child process runs, and sets a wait request to be signaled when the child completes.

## Describe Process States:
- In a OS, each CPU (or CPU core) can be working on one process at a time hence, Processes are assigned a state, which changes as CPU get time.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/9a66be9f-1b90-4b01-9ae5-656aa1626603">
- ![image](https://github.com/cybersome/Linux-octo/assets/40174034/bc07b769-e61c-4f45-9f49-2f174afaa7ac)
- Process state is important to understand how the kernel communicates with processes, and how processes communicate with each other.
- To display Linux Processes state: `top`
- To see every Process in system: `ps`

> Each terminal runs in its own session, and can have a foreground process and any number of background processes. 

## Run Jobs in the Background:
- Any command or pipeline can be started in the background by appending an ampersand (&) character to the command: `sleep 1000 &`
- Use the jobs command to display the list of jobs in the shell's session: `jobs`
- Use the fg command to bring a background job to the foreground: `fg %JOB_Number` JOB_Number >> `jobs`
- To send/suspend a foreground process to the background: `ctrl+z`
- To start running the suspended process in background: `bg %JOB_Number`


## Process Control with Signals:
- A signal(an error, an external (an I/O request or an expired timer), keyboard sequence.) is a software interrupt that is delivered to a process.
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/60071ef8-87c7-4e2f-8e0f-da69df08269a">
- A keyboard control sequence `to suspend (Ctrl+z), kill (Ctrl+c), or core dump (Ctrl+\)`

## Labs:
- $@ Represents all the arguments passed to the script.
- make a file.sh with following content: 
- `#!/bin/bash
while true; do
  echo -n "$@ " >> ~/instance_outfile
  sleep 5
done`
- It'll capture the arguments to new file instance_outfile.
- Run the file.sh with some arguments as bg process.

## Kill/Resume/Terminate a Job:
- To kill a job: `kill -SIGSTOP %JOB_NUMBER` (Get JOB_NUMBER with `jobs` command)
- To Terminate a job: `kill -SIGTERM %JOB_NUMBER`
- To Resume a job: `kill -SIGCONT %JOB_NUMBER`
- To list out current running processes.: `ps -ef`


## Monitor Process Activity:
- Load average is a measurement that the Linux kernel provides, to represent the perceived system load for a period of time.
- The kernel collects the current load number every five seconds based on the number of processes in runnable and uninterruptible states.
- Real-time Process Monitoring with `top` command. 
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/eecad750-6130-4880-9b01-4814e9f5feda">
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/75c4d59d-d069-494e-b8e5-166bb40d2d7d">
- To display the current load average: `uptime`
- To determine the number of CPUs on a system: `lscpu` 


## Summary:
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/f664ef77-95a2-4739-a864-a44f5c3eae40">
