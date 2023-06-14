# Defines the function of each file in this directory

*File 0*
+ prints the path of the current directory


*File 1*
+ lists the content(files and directories) of current directory


*File 2*
+ changes the working directory to the user’s home directory


*File 3*
+ displays current directory contents in a long format


*File 4*
+ displays current directory contents in a long format including files starting with .


*File 5*
+ displays current directory contents in a long format including files starting with . with user and group IDs displayed numerically


*File 6*
+ creates a directory named `my_first_directory` in the `/tmp/` directory


*File 7*
+ moves the file betty from `/tmp/` to `/tmp/my_first_directory`


*File 8*
+ deletes file `betty` in `/tmp/my_first_directory`


*File 9*
+ deletes directory `my_first_directory` that is in the `/tmp` directory.


*File 10*
+ changes working directory to the previous one.


*File 11*
+ lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the `/boot` directory (in this order), in long format


*File 12*
+ prints the type of the file named `iamafile` in `/tmp`


*File 13*
+ creates a symbolic link to `/bin/ls`, named `__ls__`. The symbolic link is created in the current directory.


*File 14*
+ copies all HTML files from current working directory to parent of the working directory, but only files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory are copied.


*File 15*
+ moves all files beginning with an uppercase letter to the directory `/tmp/u`


*File 16*
+ deletes all files in the current working directory that end with the character `~`


*File 17*
+ creates the directories `welcome/`, `welcome/to/` and `welcome/to/school` in the current directory.


*File 18*
+ lists all the files and directories of the current directory, separated by commas (,).
+ directory names end with a slash (/)
+ files and directories starting with a dot (.) will be listed
+ listing will be alpha ordered, except for the directories . and .. which should be listed at the very beginning
+ only digits and letters will be used to sort; digits come first
+ listing end with a new line


*File 19*
+ creates a magic file `school.mgc` that can be used with the command file to detect School data files. School data files always contain the string `SCHOOL` at offset 0.


**end**
