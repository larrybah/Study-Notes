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

## Wildcards 

Wildcards allow you to sellect filenames based on patterns of characters.

| Wildcards | Meaning |
| ---------- | ----------- |
| * | matches any character |
