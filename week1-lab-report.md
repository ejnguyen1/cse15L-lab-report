Week 1 Lab Report: How to get Remote Access in VScode

First, install VScode
  - Go to https://code.visualstudio.com/ to access the VScode website.
  - Follow the instructions to install VScode onto your computer based on your operating system. 
  - Once VScode is installed, open it. Your screen should look like the following: 
  
  
 Second, connect to your remote server through your UCSD CSE15L account.
  - Open a terminal in VScode by clicking "Terminal" -> "New Terminal".
  - In the terminal, type the following command: 
    ```
    ssh cs15lwi23zz@ieng6.ucsd.edu
    ```
  - Replace the "zz" with the account specific letters in your UCSD CSE15L account name (should be the last two 
      or three letters in the account name) and hit enter.
  - If you get a message that asks you to continue connecting, type yes and hit return.
  - Type in your password when prompted. The characters will not show up in the terminal. 
  - After all of this, your terminal should look like the following:
  

Third, try out some commands.
  - Test out some commands on your computer and on the remote terminal (must ssh). 
  - Here are some commands to test out:
      - pwd, mkdir, cd, cd ~, ls, ls -lat, cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/, 
        cat /home/linux/ieng6/cs15lwi23/public/hello.txt
  - Here is an example of testing some of the above commands: 
  
  
  - To exit the remote server in your terminal, use the command Ctrl D
