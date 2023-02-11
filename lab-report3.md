# Lab Report 3: The "grep" Command
The grep terminal command searches a file or files for the given string and prints the matching lines. This is how the command is used in the terminal:
```
grep <string> <file>
```
## grep -l
When used in the terminal, the command `grep -l` searches a file or files for the given string and returns the file path of the file containing the string.

Here is an example of the command:
![Image](https://user-images.githubusercontent.com/122569733/218234666-6d2d70b6-4c38-401f-be41-69c116e10451.png)
The input in the terminal is the following.
```
grep -l "Paradox" written_2/*/*/*/*.txt
```
The output in the terminal is the following.
```
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
```
The command returns the file paths of the files containing "Paradox". This image indicates that only two text files, ch10.txt and ch2.txt, contain the string. This command is helpful for finding just the file, not the lines in the file. 

Here is another example:
![Image](https://user-images.githubusercontent.com/122569733/218234637-639f230d-9f44-46da-b82c-f9c1bc2d9245.png)
The input in the terminal is the following.
```
grep -l "Bahamas" written_2/*/*/*.txt
```
The output in the terminal is the following.
```
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```
In this example, more file paths are returned because more files contain the string "Bahamas." This command is especially helpful when the string occurs frequently because returning all lines of text as well as the file paths would be a lot of data in the terminal.

Source: https://ucsd-cse15l-w23.github.io/week/week4/
## grep -i
The terminal command `grep -i` searches a file or files for the given string, but is not case sensitive. The usual grep command is case sensitive. This command returns the lines containing the string. 

Source: the grep manual in the VSC terminal
## grep -v
The terminal command `grep -v` searches a file or files for the given string and returns all lines that don't contain the string. 

Source: https://www.ibm.com/docs/da/aix/7.1?topic=files-finding-text-strings-within-grep-command
## grep -n
The terminal command `grep -n` performs the same functions as the normal grep function but puts the line number at the beginning of each line that is returned. 

Source: https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/#:~:text=Grep%20is%20a%20useful%20command,a%20powerful%20command%20to%20use.
