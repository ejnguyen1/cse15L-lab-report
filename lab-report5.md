# Lab Report 5: The "find" Command
The terminal command find traverses the given path and gives all matching files in the specified directory and subdirectories. This is how the command is used.
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
The output is the following
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
The terminal command `find -type <type>` checks if the file is of the given type. The possible types are: `b` for block special, `c` for character special, `d` for directory, `f` for regular file, `l` for symbolic link, `p` for FIFO, and `s` for socket. 

Source: find manual in VSCode terminal. 
## find -newer
The terminal command `find -newer <path>` gives all the files that are newer than the given file. 

Source: https://www.javatpoint.com/linux-find
## find 

