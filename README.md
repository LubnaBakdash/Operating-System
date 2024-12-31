Unix/Linux Commands and Shell Programming Project
This repository contains the solution to a series of practical exercises focused on Unix/Linux commands, shell scripting, process management, signal handling, and process synchronization. The exercises aim to demonstrate key concepts in Linux/Unix system programming.

Table of Contents
Unix/Linux Commands and Shell
Process Management
Pipe Management
Signals Handling
Process Synchronizing (Producer-Consumer Problem)
1. Unix/Linux Commands and Shell
In this section, various tasks were completed using Linux/Unix commands and shell scripting. The goal was to familiarize with file and directory management, working with environment variables, process handling, and basic shell scripting. The tasks included:

Creating directories: Two directories named one and two were created under the home directory.
Changing directory permissions: The permissions of the one directory were set to be readable, writable, and executable for the owner, and executable for the group, while no permissions were granted to others.
File creation and manipulation: A file named test was created within the two directory, and it contained basic user information (name and university ID). The file was later copied to the one directory and renamed as f2.
Displaying timestamps: The timestamps (creation/modification times) of both files were displayed using the stat command.
Environment variables: Environment variables such as PATH, HOME, and SHELL were printed to the console.
Shell variable: A shell variable named num was created and set to the value 5.
Shell script for even/odd check: A simple shell script was written to check if a given number is even or odd.
Process listing: The ps command was used to display the currently running processes in the system.
2. Process Management
This section focused on process creation and management. The task was to create a program that involved:

Defining a variable: A variable x was defined with an initial value of 100.
Creating a child process: A child process was created using fork().
Variable behavior in parent and child: The value of the variable x was printed in both the parent and child processes to observe how variables behave when processes are forked. Changes made by the child process do not affect the parent process, and vice versa.
3. Pipe Management
This task demonstrated inter-process communication (IPC) using pipes:

Creating child processes: Two child processes were created by the parent process.
Pipes for communication: The standard output of the first child was connected to the standard input of the second child using a pipe, allowing for communication between the two processes.
Reconnecting standard input/output: The standard input and output for the child processes were redirected to allow data transfer between them through the pipe.
4. Signals Handling
In this section, signal handling was implemented to simulate communication between processes using Unix signals:

Signal sending and receiving: One process sent a random signal (such as SIGUSR1, SIGUSR2, etc.) to another process.
Signal ignoring and termination: The receiving process printed the signal number but ignored it, except when a specific signal (such as SIGKILL) was received, which caused the process to terminate.
Signal acknowledgment: The parent process sent a signal back to the child process after the child received the termination signal.
5. Process Synchronizing (Producer-Consumer Problem)
The final section focused on synchronizing processes using semaphores, modeled by the Producer-Consumer problem:

Buffer and synchronization: A buffer of fixed size was used to store items produced by a producer process and consumed by a consumer process. The producer added items to the buffer, while the consumer removed them.
Semaphore usage: Semaphores were employed to synchronize the producer and consumer processes, ensuring that the producer did not produce more items than the buffer could hold, and the consumer did not consume from an empty buffer.
Process management: System calls and synchronization techniques were applied to ensure mutual exclusion and prevent race conditions between the producer and consumer.
Conclusion
This project provides a hands-on approach to learning Linux/Unix system programming, focusing on shell scripting, process management, signal handling, and inter-process synchronization. These exercises helped develop practical skills in working with the Unix/Linux environment, as well as in managing complex systems with multiple processes and communication between them.
