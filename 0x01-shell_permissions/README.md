## Shell permissions

### All files in this directory are executable files. 
*what is an executable file?*
+ they are files that contain instructions to perform specific tasks
+ e.g. the /bin directory contains all sysetem-wide executable files like ls, mkdir, touch, pwd
+ inside these files are defined rules and instructions that tells the computer what to do if any of these files are executed.
+ the computer understands to list all files and directories when the `ls` file is executed.

*why are paths not specified for system defined executable files like* `ls` *and* `touch` *etc?*
+ there is a Linux variable called `PATH` which contains commonly used path names.
+ when an executable file is passed as a command without its path been specified, LINUX searches through the `PATH` variable 
+ to find where the file is located. once file is found, LINUX executes it with the instructions specified in it.


### The files in this dirctory and what they do
*File 0*
+ a script that switches the current user to a user called `betty`


*File 1*
+ script that prints the username of the current user


*File 2*
+ script that prints all the groups the current user is part of.


*File 3*
+ script that changes the owner of a file `hello` to a user `betty`


*File 4*
+ script that creates an empty file called `hello`


*File 5*
+ script that adds execute permission to the owner of the file `hello`


*File 6*
+ script that adds execute permission to the owner and the group owner, and read permission to other users, to the file `hello`


*File 7*
+ script that adds execution permission to the owner, the group owner and the other users, to the file `hello`


*File 8*
+ script that sets the permission to the file `hello` as follows - Owner no permission at all, Group: no permission at all, Other users: all the permissions


*File 9*
+ script that sets the mode of the file `hello` to this: -rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello


*File 10*
+ script that sets the mode of the file `hello` the same as `olleh`’s mode.


*File 11*
+ script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.

+ Regular files does not change.


*File 12* 
+ script that creates a directory called `my_dir` with permissions 751 in the working directory


*File 13*
+ script that changes the group owner to `school` for the file `hello`

+ The file `hello` will be in the working directory


*File 100*
+ script that changes the owner to `vincent` and the group owner to `staff` for all the files and directories in the working directory.


*File 101*
+ script that changes the owner and the group owner of `_hello` to `vincent` and staff respectively.
+ The file `_hello` is in the working directory
+ The file `_hello` is a symbolic link


*File 102*
+ script that changes the owner of the file `hello` to `betty` only if it is owned by the user guillaume.
+ The file `hello` will be in the working directory


*File 103*
+ script that will play the StarWars IV episode in the terminal.


