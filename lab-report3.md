# Lab Report 3: The "grep" Command
The grep terminal command searches a file or files for the given string and prints the matching lines and file paths containing the string. This is how the command is used in the terminal:
```
grep <string> <file>
```
There are many different variations of the grep command. 
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
The command returns the file paths of the files containing "Paradox." This image indicates that only two text files, ch10.txt and ch2.txt, contain the string. This command is helpful for finding just the file, not the lines in the file. 

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
The terminal command `grep -i` searches a file or files for the given string, but is not case sensitive. The usual grep command is case sensitive. This command returns the lines containing the string and the file paths. For both examples, I also included `-l` so that only the file paths would be printed, not all the lines of text. 

Here is an example of the command:
![Image](https://user-images.githubusercontent.com/122569733/218236023-595a3dbb-5ace-4969-90b9-2650e58cc29c.png)
The input in the terminal is the following.
```
grep -i -l "Paradox" written_2/*/*/*/*.txt
```
The output in the terminal is the following.
```
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
```
This command is similar to the example two photos above, but there are more file paths shown. This is because the given string "Paradox" isn't case sensitive, so files containing "paradox" and "Paradox" are returned. 

Here's another example:
![Image](https://user-images.githubusercontent.com/122569733/218236330-39acb0f5-9d7a-43b1-8794-46c3d1e79cbf.png)
The input in the terminal is the following.
```
grep -i -l "Nominally" written_2/*/*/*.txt
```
The output in the terminal is the following.
```
written_2/travel_guides/berlitz1/HistoryDublin.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
```
This output means that all of these files contain either "Nominally" or "nominally." 

Source: the grep manual in the VSC terminal
## grep -v
The terminal command `grep -v` searches a file or files for the given string and returns all lines that don't contain the string. 

Here's an example of the command in the terminal:
![Image](https://user-images.githubusercontent.com/122569733/218238057-560195b0-cce4-45f4-abbe-2f4b895a77c1.png)
The input in the terminal is the following.
```
grep -v "the" written_2/travel_guides/berlitz1/HandRLosAngeles.txt
```
The output is the following.
```
Recommended Hotels
The following hotels are listed alphabetically in three
area and Orange County. All hotels are of a high standard, with private
bath, air-conditioning, television, and telephone; most have king- or
queen-sized beds. Breakfast is not usually included at US hotels,
except on executive floors and at some budget motels that offer morning
coffee, orange juice, and doughnuts or muffins.
To make direct reservations with a hotel, we have included
addresses (all in California, abbreviated CA) and telephone/fax
numbers. Check-out time is generally noon or 1pm, with check-in usually
available from 2pm to 3pm. All hotels accept major credit cards.
Rates vary greatly according to season and availability;
many hotels offer special weekend packages, business rates, and
following symbols to indicate room prices (two persons in a double
room, per night):
❁❁❁$200 and up
❁❁$100–$200
❁under $100
```
In this example, the file HandRLosAngeles.txt is searched, and the lines not containing "the" are returned. Lines containing capitalized "The" are included because the command isn't case sensitive.

Here's another example:
![Image](https://user-images.githubusercontent.com/122569733/218238272-4eb2a75b-53b0-400b-a11d-5b724f55c814.png)
The input in the terminal is the following.
```
grep -v "a" written_2/travel_guides/berlitz2/Cancun-History.txt
```
The output is the following.
```
A Brief History
The Henequen Boom
```
These are the only two lines in the file Cancun-History.txt not containing the character "a."

Source: https://www.ibm.com/docs/da/aix/7.1?topic=files-finding-text-strings-within-grep-command
## grep -n
The terminal command `grep -n` performs the same functions as the normal grep function but puts the line number at the beginning of each line that is returned. 

Here's an example of the command:
![Image](https://user-images.githubusercontent.com/122569733/218239646-ae40345d-b712-4eb9-889f-f98194397f0e.png)
The input in the terminal is the following.
```
grep -n "Myceneans" written_2/*/*/*.txt
```
The output is the following.
```
written_2/travel_guides/berlitz1/HistoryGreek.txt:36:        The Minoans and the Myceneans
written_2/travel_guides/berlitz2/Athens-History.txt:9:The Achaeans’ chief rivals and mentors were the dazzling Minoans of Crete — until about 1450 b.c., when the Minoan empire was devastated, possibly by tidal waves caused by the eruption of the volcanic island of Thera (Santorini). From the seafaring Minoans, the Myceneans learned to make bronze by combining copper and tin and, with no written language of their own, they adpated the linear script used by Minoan scribes. For several centuries, the Mycenaeans dominated the eastern Mediterranean and Aegean. A long series of conflicts, however, including the legendary siege of Troy, weakened these mighty mainland warriors.
```
There are multiple files containing "Myceneans," so there are multiple file paths listed. After the file path, the line number is given, followed by the lines containing the string.

Here's another example:
![Image](https://user-images.githubusercontent.com/122569733/218239797-8a09adc8-ec90-4fa1-8118-bdb122198a43.png)
The input in the terminal is the following.
```
grep -n "Pacific" written_2/travel_guides/berlitz1/HistoryHawaii.txt
```
The output is the following.
```
9:        arrived from the Marquesas in the South Pacific perhaps as early as
35:        Northwest Passage linking the Atlantic and Pacific oceans. He, too, had
191:        war on Japan. Hawaii, as America’s western outpost and major Pacific
208:        Pacific frontier was still expanding. Hilton built a resort village
218:        advanced Pacific Rim studies.
```
This time, only the specific file HistoryHawaii.txt is searched. The lines containing "Pacific" are returned, including their line number.

Source: https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/#:~:text=Grep%20is%20a%20useful%20command,a%20powerful%20command%20to%20use.
