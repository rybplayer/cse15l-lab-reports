# Lab Report 1

## The `cd` command

Here is an example of `cd` with no argument:
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$
```
The working directory when the command was run is `/lecture1`. \
It appears a no-arg `cd` returns to the parent directory `C:\\`, 
or more specifically the most direct parent directory. \
This is not an error.

Here is an example of `cd` with a path to a directory:
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
The working directory when the command was run is `C:\\`. \
Adding a folder or path as the argument to 'cd' appears to
change the current directory into the argument path. \
This is not an error.

Here is an example of `cd` with a path to a file:
```
[user@sahara ~]$ cd Hello.java
bash: cd: Hello.java: No such file or directory
[user@sahara ~]$ 
```
The working directory when the command was run is `C:\\`. \
Adding a file to cd appears to do nothing. \
This is an error, which makes sense since `cd` changes the 
working directory, but a file is not a directory, so 
`cd` does nothing.

## The `ls` command

Here is an example of `ls` with no argument:
```
[user@sahara ~]$ cd Hello.java
bash: cd: Hello.java: No such file or directory
[user@sahara ~]$ 
```
The working directory when the command was run is `\lecture1`. \
Adding no argument to `ls` lists all the files and directories
in the working directory. \ 
This is not an error.

Here is an example of a `ls` with a directory as argument:
```
[user@sahara ~/lecture1]$ ls messages
en-us.txt  es-mx.txt  zh-cn.txt
```
The working directory when the command was run is `\lecture1`. \ 
Adding a directory to `ls` appears to list out all the files
or directories in the argument directory. \
This is not an error.

Here is an example of a `ls` with a file as argument:
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
[user@sahara ~/lecture1]$ 
```
The working directory when the command was run is `\lecture1`. \
Adding a file to `ls` appears to simply print out the name of
the argument file. This is sensible, since if we treat this single 
file as its own directory, the only file inside the directory is 
itself, so `ls` outputs it to the terminal.
This is not an error. 

## The `cat` command

Here is an example of a `cat` with no argument:
