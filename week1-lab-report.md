# Week 1 Lab Report: Remote Access in VScode

## Install VScode
  - Click [here](https://code.visualstudio.com/) to access the VScode website.
  - Follow the instructions to download and install VScode onto your computer based on your operating system. 
  - Once VScode is installed, open it. The VScode window on your screen should look like this: 
  ![Image](https://user-images.githubusercontent.com/122569733/212421120-f166bb45-027c-43ab-8d2c-0c244ffbd59b.png)
  
## Connect to your remote server through your UCSD CSE15L account
  - Open a terminal in VScode by clicking "Terminal" -> "New Terminal" in the tool bar.
  - In the terminal, copy and paste the following command: 
  ```
  ssh cs15lwi23zz@ieng6.ucsd.edu
  ```
  - Replace the "zz" with the account specific letters in your UCSD CSE15L account name (should be the last two 
      or three letters in the account name) and hit enter.
  - Your terminal should look like the following:
  ![Image](https://user-images.githubusercontent.com/122569733/214781069-3327290b-e2b5-4e06-9418-76d4fd6add12.png)
  - If you get a message that asks you to continue connecting, type yes and hit return.
  - Type in your password when prompted. The characters will not show up in the terminal. 
  - After all of this, your terminal should look like the following:
  ![Image](https://user-images.githubusercontent.com/122569733/212422206-9d8b6464-5d58-4d3e-a6c2-14975afdf68a.png)
  - This means that you have successfully connected to your remote server.

## Try out some commands
  - Test out some commands on your computer and on the remote terminal (must ssh for this). 
  - Some common commands are: pwd, which prints out the current working directory. mkdir, which creates a new directory.
      cd, which switches the current working directory to the specified directory. ls, which lists the files and folders
      of the given path. cat, which prints the contents of one or more files given by the path(s).
  - Some helpful symbols are: .. which means the directory above/outside the current directory. ~ which means a directory
      where a user's files are stored.  
  - Here are some commands you can test out in the terminal:
  ```
  pwd
  mkdir <directory> 
  cd <path>           
  ls <path>             
  ls -lat 
  cat <path1> <path2> etc
  ```
  - You can also try out a combination of the above commands and symbols. 
  - Here is an example of testing some of the above commands: 
  ![Image](https://user-images.githubusercontent.com/122569733/212422456-a48bdc8c-b269-40eb-b637-4e2f1dbe71ba.png)
  - To exit the remote server in your terminal, use the command Ctrl+D
