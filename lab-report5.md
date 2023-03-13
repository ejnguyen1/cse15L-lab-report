# Lab Report 5: The "find" Command
The terminal command `find` traverses the given path and gives all matching files in the specified directory and subdirectories. This is how the command is used.
```
find <path>
```
It can do more specific searches with certain modifiers. I talk about a few of these different uses below using examples from the `docsearch` repository.
## find -name *pattern*
The terminal command `find -name <pattern>` searches the files in the given directory for file names that contain the matching pattern.

The input in the terminal is the following. For context, the current working directory is `docsearch/written_2/travel_guides/berlitz2/`.
```
find -name "*Budapest*"
```
The output is the following.
```
./Budapest-History.txt
./Budapest-WhatToDo.txt
./Budapest-WhereoGo.txt
```
These file names are returned in the terminal because they contain the string "Budapest." This indicates that these are the only files in the current directory that contain the given pattern.  

Here is another example. The input in the terminal is the following. The working directory is `docsearch/written_2/travel_guides`.
```
find -name "*sta*"
```
The output is the following.
```
./berlitz1/HandRIstanbul.txt
./berlitz1/HistoryIstanbul.txt
./berlitz1/IntroIstanbul.txt
./berlitz1/WhatToIstanbul.txt
./berlitz1/WhereToIstanbul.txt
./berlitz2/Costa-History.txt
./berlitz2/Costa-WhatToDo.txt
./berlitz2/Costa-WhereToGo.txt
./berlitz2/CostaBlanca-History.txt
./berlitz2/CostaBlanca-WhatToDo.txt
./berlitz2/CstaBlanca-WhereToGo.txt
```
All of these files are returned because they contain "sta" somewhere in their file name. Since the working directory contains the directories `berlitz1` and `berlitz2`, the files returned are from both directories. This command is helpful for searching for directories for file names containing a specific string pattern. 

Source: find manual in VSCode terminal. 
## find -type *type*
The terminal command `find -type <type>` searches the current working directory for files of the specified type. The possible types are: `b` for block special, `c` for character special, `d` for directory, `f` for regular file, `l` for symbolic link, `p` for FIFO, and `s` for socket. 

Here is an example of the command. The input in the terminal is the following. The working directory is `docsearch/written_2/non-fiction/OUP/Rybczynski`.
```
find -type f
```
The output is the following.
```
./ch1.txt
./ch2.txt
./ch3.txt
```
These three files are returned because they're all of the specified type `f` (regular file). This means that all of these are regular files contained in the working directory. 

Here's another example of the command when the working directory is `docsearch/written_2/non-fiction/OUP`. The input in the terminal is the following.
```
find -type d
```
The output is the following.
```
.
./Abernathy
./Berk
./Castro
./Fletcher
./Kauffman
./Rybczynski
```
Since the specified type was `d` (directory), all the directories in the current working directory are returned. This command is helpful when searching for a specific type within a repository. 

Source: find manual in VSCode terminal. 
## find -newer
The terminal command `find -newer <path>` gives all the files that are newer than the given file. 

Here is an example of the command. The input in the terminal is the following. The current working directory is `docsearch/written_2/non-fiction/OUP/Castro`.
```
find -newer chN.txt
```
The output in the terminal is the following.
```
.
./chO.txt
./chP.txt
./chQ.txt
./chR.txt
./chV.txt
./chW.txt
./chY.txt
./chZ.txt
```
This means that all of these outputted files are newer than the file `chN.txt`.

Here's another example of the command. The working directory stays the same, but the specified file changes.
```
find -newer chW.txt
```
The output is the following.
```
.
./chY.txt
./chZ.txt
```
This time, fewer files are returned because there are fewer files in the current directory that are newer than `chW.txt`. This command is helpful for searching for something you know you made after a specific file. 

Source: https://www.javatpoint.com/linux-find
## find -size *size*
The terminal command `find -size <size>` looks through the working directory for files of the specified size. The possible sizes are `b` for 512-byte blocks (default size), `c` for bytes, `w` for two-byte words, `k` for Kilobytes, `M` for Megabytes, `G` for Gigabytes. Each size variable must have a number before it indicating the amount of units. You can also include a `+` of `-` to search for files greater than or less than the specified size.

Here's an example of the command. The current working directory is `docsearch/written_2/non-fiction/OUP/Fletcher`. The input in the terminal is the following.
```
find -size +1b 
```
The output is the following.
```
.
./ch1.txt
./ch10.txt
./ch2.txt
./ch5.txt
./ch6.txt
./ch9.txt
```
This indicates that all of these given files are greater than 1 byte-block. 

Here is another example of the command when in the same working directory. The input is the following.
```
find -size +50k
```
The output is the following.
```
./ch2.txt
./ch6.txt
./ch9.txt
```
This means that these files are greater than 50 Kilobytes. Since not all the files in the directory are shown, it means that the files not shown are less than 50 Kilobytes. This command is useful for searching for and sorting files based on size.

The find command is very helpful for searching directories and files. Though these are only a few applications of the command, there are many other uses.
