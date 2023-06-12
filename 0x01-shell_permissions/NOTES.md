# Notes on shell basics

## *who is a user on Linux*
In Linux, a user refers to an individual who interacts with the system by logging in and performing various tasks. Each user is assigned a unique username and is associated with specific permissions and privileges that determine what actions they can perform on the system.

Linux supports different types of users with varying levels of privileges. Here are some common types of users:

+ Superuser (root): The superuser, also known as the root user, has unrestricted administrative access to the entire system. They have full control and can perform any action, including system configuration, installing software, modifying system files, and managing other users. The root user should be used with caution, as any mistakes or misuse of privileges can have severe consequences.

+ Regular Users: Regular users are standard user accounts created on the system. They have limited privileges and can perform most tasks required for their own user environment. Regular users can create, modify, and delete their files and directories, run applications, and customize their user settings. However, they typically do not have the ability to modify system files or perform administrative tasks.

+ System Users: System users are created to run specific system services or processes. These users are often associated with system daemons or background processes that require dedicated user accounts. System users typically do not have login access and are restricted to performing specific system-related tasks.

It's important to note that user privileges can be further customized through user groups and permissions. User groups allow multiple users to be assigned common access privileges, while permissions dictate what actions can be performed on files and directories by different users or user groups.

By default, regular users can access their home directories, run applications, and perform tasks within their user environment. However, they may not have access to system-wide configuration files or perform administrative actions. This segregation of user types and privileges helps maintain security, prevent unauthorized access, and limit the potential impact of user mistakes or malicious actions.

The superuser (root) has the highest level of privileges and can perform any action on the system. It's important to exercise caution and use the root user only when necessary to avoid unintended consequences or system vulnerabilities. Regular users should be used for day-to-day tasks to maintain a secure and well-managed system.


### How to switch users on a `LINUX` system
the command `su`: switch user. 
*syntax*: `su <user-name>`
*function*: changes current user to `user-name`

## What are groups in `Linux`?
Groups provides a way to organize and manage users with similar permissions and requirements.

### what is the command to view all groups that a certain user belongs to?
+ the command: groups
*syntax*: `groups`
*function*: prints all groups the user belongs to.

###
