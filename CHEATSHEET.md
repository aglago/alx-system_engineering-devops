# My cheat sheet

### How to write a text into multiple files
+ `echo 'sample text' | tee file1 file2 file3`
+ writes `'sample text'` into `file1`, `file2` and `file3` at the same time.

### How to check the first line statement of each file in a directory
+ `head -n 1 *`
+ prints the first line in every file in the directory

### How to check the number of characters in your file
+ `wc -l ....`
+ 
