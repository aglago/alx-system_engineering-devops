### Engineering Devops Directories

*what is an executable file (program)?*
+ they are files that contain instructions to perform specific tasks
+ they are written in programming languages such as C++, C, Python and others
+ they can directly be executed by the operating system.
+ e.g. the /bin directory contains all system-wide executable files like `ls`, `mkdir`, `touch`, `pwd`
+ inside these files are defined rules and instructions that tells the computer what to do if any of these files are executed.
+ the computer understands to list all files and directories when the `ls` file is executed.


*what are the types of executable programs?*
**compiles executable programs**
+ Compiled executable files are created from programming languages like C, C++, Rust, among others and compiled into machine code, which is specific to the processor architecture, and stored in an executable binary file. The compiled binary file contains the instructions that the computer's processor can directly execute.

**interpreted executable programs**
+ they contain human readable instructions which are then interpreted and by an interpreted program like shell, zsh among others. they are written in interpreter languages like Python, scripting languages, Perl, Ruby and they need an interpreter program to run their codes. 


*are all executable programs files?*
YES


*is it possible to create executable programs myself?*
YES


#### This repository contains interpreted executable programs, written by me to perform specific functions.
+ These executable files are organized into directories per their functions.






#### Extra notes

*why are paths not specified for system defined executable files like* `ls` *and* `touch` *etc?*
+ there is a Linux variable called `PATH` which contains commonly used path names.
+ when an executable file is passed as a command without its path been specified, `LINUX` searches through the `PATH` variable
+ to find where the file is located. once file is found, LINUX executes it with the instructions specified in it.


*what is the* `LINUX` `$PATH` *variable and what does the* `PATH` *variable contain and what is it used for?*
is a LINUX environment variable that contains list of directories where the system look for executable files when a command is run in the terminal.
+ it helps the system locate and execute commands without requiring you to provide full path of the executable file.
+ e.g.s `/bin`, `/usr/bin`, `/usr/local/bin` and `/sbin` among others.


*how do i view what is inside the* `$PATH` *variable?*
`echo $PATH`


*can I edit the* `$PATH` *variable and how?*
yes, the `$PATH` variable can be edited. but not advisable to now (for me)

