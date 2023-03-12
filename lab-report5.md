# Lab Report 5: The "find" Command
The terminal command find traverses the given path and gives all matching files in the specified directory and subdirectories. This is how the command is used.
```
find <path>
```
It can do more specific searches with certain modifiers. I talk about a few of these different uses below. 

## find -name *pattern*
The terminal command `find -name <pattern>` checks if the last component of the pathname in question matches the given pattern.

Source: find manual in VSCode terminal. 
## find -name *type*
The terminal command `find -type <type>` checks if the file is of the given type. The possible types are: `b` for block special, `c` for character special, `d` for directory, `f` for regular file, `l` for symbolic link, `p` for FIFO, and `s` for socket. 

Source: find manual in VSCode terminal. 
## find -newer
The terminal command `find -newer <path>` gives all the files that are newer than the given file. 

Source: https://www.javatpoint.com/linux-find
## find 

