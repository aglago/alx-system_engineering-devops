# Notes on shell permissions

## who is a user on Linux
+ a user refers to an individual who interacts with the system by logging in and performing various tasks. 
+ each user has a unique username and specific permissions and privileges that determine what actions they can perform on the system.
+ there are different types of users and each user has its own privileges.
+ the superuser (root) has full control and unrestricted access and can perform any action at all to the system.
+ the regular users have limited privileges and can perform tasks required for their own user environment. 
+ Regular users can create, modify and delete files and directories, run application, cutomize their user settings but do not have the ability to modify system files or perform administrative tasks.
+ system users are created to run specific system services or processes.
+ **NB**  privileges can be further customized through user groups and permissions.


## Terminologies and commands
 + `whoami` : used to check the current user of the system.
 + `groups` : used to print all the groups that the current user is a part of.
 + `su` : switch user; used to switch current user to a new user on the system.
 + `chown` : changes the owner of a file or directory.
 + `chmod` : changes basic informations of the user and file and directories permissions.
 + `chgrp` : changes the group of the user specified
 +  



## Permissions
 + 777 - rwx


### Add execution rights to all.
+ chmod +x

### Add execution rights to users
+ chmod u+x

### Remove execution rights to all
+ chmod -x

