# Shell Redirections & 

## Redirections
+ allows to change default input or output location of a command.
+ uses the `>` or `<` symbols to specify the source of destination of the input or output.
+ E.g. `ls > file1` will send the out output of the `ls` command as text in `file1`.
+ E.g. `cd < echo $HOME` will navigate to the directory specified by the `$HOME` variable, as the cd command will be taking input not from the keyboard, but from the variable content.

## Pipelines
+ Allows to add multiple commands together where the output of one command becomes the input for another.
+ uses the `|` symbol to pass the output of one command as the input to the next command.
+ E.g. `ls -l | less`
+

## Filters
+ programs that read input from a source (such as a file or the output of another command) and write the modified or filtered output to the standard output (terminal)

### commonly used filters
+ `sort` : sorts inputed data based on specified criteria. *e.g* alphabetical order.
+ `grep` : examines each line of data it receives from standard input and outputs every line that contains a specified pattern of characters.
+ `head` : outputs the first few lines of inputed data.
+ `tail` : outputs the last few line of inputed data.
+ `uniq` : makes sure that every line is unique by removing duplicate lines from inputed data.
+ `fmt` : outputs formatted text of the inputed text.
+ `pr` : (for printing) takes data from standard input and splits data into pages with page breaks, headers and footers for printing.
+ `tr` : (translates characters) takes data and converts them like to upper/lower case or delete characters in a given input.
+ `sed` : (stream editor) performs text transformation based on patterns and rules.
+ `awk` : processes files line by line to manipulate and extract data from inputed text, it is also a programming language designed for constructing filters.
+ `wc` : (word count) counts the number of lines, words or characters of inputed data.
+ `cut` : used to extract specific information from structured data.
+ `rev` : reverses the order of characters on each line of the input and produces the reversed output.


### usage examples of filers
+
+
+


## other commands
+ `echo` : 
+ `find` : used to search for files in a directory hierarchy.
