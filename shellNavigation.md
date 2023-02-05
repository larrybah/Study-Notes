# Linux And Shell Navigation Notes

Like windows all unix-like Operating Systems are structured in a hirachical order.

One of the most important differences between windows and unix-like Operating systems such as Linux is that linux does not employ the concept of drive letters. while windows drive letters split the file systems into a series of different trees (one letter for each drive/device), linux always has a single tree. Different storage devices may be different branches of the tree, but there is always just a single tree.

- pwd - present working directory.
- cd - current working directory.
- ls - list directories

## ls 

The `ls` Command is used to list the contents of a directory, It is probably the most used linux commmand.

It can be used in different ways.

| list type | meaning |
| --------- | ---------- |
| ls | list the files in the working directory  |
| ls /bin | list the files in the /bin directory |
| ls -l | lists the files in the working directory in a long format |
| ls -l /etc /bin | lists the files in the /bin directly and /etc directory in long format |
| less | less is a program that lets us view the content of a file. This is very handy since many of the files used to control and configure linux are human readable |

As we wander around the linux file system, it is helpful to determine what kind of data a file contains before we try to view it. This is where the **`file`** command comes in. file will examine a file content and tell us what kind of file it is.

## Manipulating Files 

> cp - copies files and directories from one location to the other.
> 
> mv - moves or rename files adn directoriesl.
> 
> rm - removes or deletes files or directories.
> 
> rmkdir - remove only directories.
> 
> mkdir - creates new directories.

<hr />

## Wildcards 

Wildcards allow you to sellect filenames based on patterns of characters.

| Wildcards   | Meaning  |
| ------------ | ------------- |
| * | matches any character |
| ? | matches any single character|
| [character] | matches any single character that is a member of the set characters. The set of characters may also be expressed as a posix character class such as one of the following 
| posix Characters | Meaning |
| [:alnum:] | Alphanumeric character|
| [:alpha:] | Alphabetic character |
| [:digit:] | Numerals |
| [upper ] | uppercase alphabets |
| [lower ] | lowercase alphabets |
| [:characters] | matches any character that is not a member of the characters |
| [!:lower:]] | Any file name that does not end with a lower letter.|
| cp file file | Copies the content of file1 into file2. if file2 does not exist, it is created. Otherwise, file2 is silently overwritten with the contents of file1.|
| type | Displays Information about a command type.|
| which | locates a command|
| help | Displays reference page.|
| man | Displays an online command reference.|

<hr />

## What are Commands?
An executable program like all those files we saw in /usr/bin, within this category programs can be compiled to binaries, such as programs written in C and C++ or programs written in scripting languages such as the shell, perl, python and ruby etc.

A command built into the shell itself, bash provides a number of commands internally called shell builtins. The `cd` command for example is a shell built in.

A Shell function: These are miniature shell scripts incorporated into the environment.

An alias - Commands that we can define ourselves, builtin from other commands.

# I/O Redirection (Input/Output Redirection)

Standard output - Most command line programs that display their results do so by sending their results to a facility called standard output. To redirect standard output to a file the `>` greater than character is used like this: `ls > file.txt`. This copies the `ls` command output to a file.

`ls >> file.txt`  This appends or add the output of `ls` to the file.

**Many Commands can accept input from a facility called standard input. To redirect standard input from a file instead of the keyboard, the `<` less than character is used.**

| Commands | Meaning |
| ------ | --------- |
| sort < file.txt | This command sorts the elements inside of a file.|
| sort < file.txt > sorted_file.txt | This is used to sort the the elements in a file and transfer them to a new file.|

## Pipelines `|`

The most useful and powerful thing we can do with I/O redirection is to connect multiple commands together to form what is called pipelines. With pipelines the standard output of one command is fed into the standard input to another.

| Commands | Meaning |
| ------ | ---------- |
| ls -l `|` less |  This takes output of the command `ls` and displays it in the `less` pager. You can press `q` to exit the pager.|
| ls lt `|` head | Displays the 10 newest files in the current directory. |
| du `|` sort -nr | Displays a list of directories and how much space they consume, Sorted from the largest to the smallest. |
| Find . -type f -print `|` wc -l | Displays the total number of files in the current working directory and all of its subdirectories.|

## Filters 


