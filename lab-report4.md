# Lab Report 4: "Done Quick" Lab
## Step 1: Setup
To delete the forked repository from my ieng6 account, I typed `rm -rf lab7` in the terminal, then hit `<enter>`. I did so in the VSCode terminal after ssh-ing in. The following screenshot shows the command in the terminal, as well as the contents of my ieng6 directory before and after deleting the forked lab7 repository. 

![Image](https://user-images.githubusercontent.com/122569733/221288036-7719b81e-25ad-499e-a80a-4242a286e97b.png)

I also deleted the forked repository from my Github account. I went into the forked repository, went to settings, scrolled to the bottom, and clicked "Delete this repository," as shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221288455-adb41395-8c74-45d7-b660-cd04760d7227.png)
## Step 2: Forking
To fork the repository, I clicked on the "Fork" button once in the repository. 

![Image](https://user-images.githubusercontent.com/122569733/221288921-74d32d9b-1f08-41c4-9e92-c6c0ec585f63.png)

At the next page, click "Create Fork." 

![Image](https://user-images.githubusercontent.com/122569733/221291464-5765501a-39f8-442e-a406-396cbf83aed7.png)
## Step 3: Start the Timer
Start the timer on your phone to time the next steps. 
## Step 4: ssh
Log into your ieng6 account using ssh. To do this, I typed `ssh cs15lwi23asa@ieng6.ucsd.edu` into my terminal and hit `<enter>`. 

![Image](https://user-images.githubusercontent.com/122569733/221290614-cb4ddd5d-797b-4dc0-9814-850b364169e1.png)

I was never prompted for my password because I saved my public ssh key in my ieng6 account. 
## Step 5: Cloning
To clone the forked repository from my Github account, I first clicked on the "Code" button under the repository. Next, I copied the HTTPS link, as shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221291872-0c246e29-eb5b-4342-b0c8-9d6f4d12f78f.png)

Once I had the link copied, I went back to the VSCode terminal. I typed `git clone` then hit the buttons `<command>+<v>` to paste the link after. Next, I hit `<enter>`. The terminal command and output should look like the following. 

![Image](https://user-images.githubusercontent.com/122569733/221292584-ed01542d-2fbe-425d-8f7d-4cefab2d7162.png)
## Step 6: Run the Tests
To run the tests on the files, I first typed `ls lab7` into the terminal and hit `<enter>` to look at the files in the lab7 directory. The terminal should look like the following.

![Image](https://user-images.githubusercontent.com/122569733/221293547-76c1d770-433d-4c9d-ac78-c448c77c2756.png)

Now that I knew the files to use to run the tests, I moved into the lab7 directory so I could run the tests on the files in it. I typed `cd lab7` into the terminal and hit `<enter>`, as shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221294164-ef1383e8-09e5-47cf-af02-65635ab54d9e.png)

To run the tests, I copied the JUnit commands at the bottom of the CSE15L Week 7 page and pasted them into the terminal. I first used `<command>+<c>` to copy the JUnit compile command. I used `<command>+<v>` to paste it into the terminal and hit `<enter>`. Once the code compiled successfully, I used `<command>+<c>` to copy the JUnit run command. I used `<command>+<v>` to paste it into the terminal and typed `ListExamplesTests` after, since that's the testing file. After hitting `<enter>`, my terminal looked like the following. 

![Image](https://user-images.githubusercontent.com/122569733/221295159-67340b62-e9f0-4ea2-92ad-2361416cc6d6.png)

The failure message indicates that there is a bug in the ListExamples.java file. 
## Step 7: Edit the Code
The error in the file ListExamples.java is in line 43. The variable that should be incrementing is index2, not index1. To edit the code, I typed `nano ListExamples.java` and hit `<enter>`, as shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221467625-6e37be16-a193-4fd3-91b6-f5e482958940.png)
  
This is the resulting nano editor.
  
![Image](https://user-images.githubusercontent.com/122569733/221467686-782adf5c-78f7-433a-9b43-4c5d623a7257.png) 

Next I scrolled to the bottom. My cursor started out at the bottom of the java code, so I pressed `<up><up><up><up><up><up><up>` and `<right><right><right><right><right><right><right>` to get to the part in line 43 I had to edit. I clicked `<delete>` to delete the `<1>` and typed `<2>` to change the variable `index1` to `index2`. The terminal before then after editing are pictured below. 
  
![Image](https://user-images.githubusercontent.com/122569733/221470599-ece358fb-876c-445c-aa54-b67576cf3544.png)
![Image](https://user-images.githubusercontent.com/122569733/221470634-7c466fb7-40d7-4aa1-ac76-0f5138627b3a.png)
  
To save the changes, I typed `<control>+<o>`. The screen asked what I wanted to save the file as and showed the name `ListExamples.java1`, as shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221474097-52a6725a-65ad-4947-a53d-ddfef5139a5e.png)

Since I wanted to keep this as the name, I hit `<enter>`. To exit, I typed `<control>+<x>`. 
  
## Step 8: Run the Tests (Again)
To run the tests, I accessed the JUnit compile and run commands using bash history. To access this history, I typed `<control>+<r>`. This pulled up a section where I could search for past commands I had already used, so I typed in `javac` to get the JUnit compile command. The command autofilled at the end of the line. The terminal looked like the photo below. 

![Image](https://user-images.githubusercontent.com/122569733/221475922-f1342b41-a848-43fa-8262-68a3b54ca5b0.png)

I hit `<enter>` to compile both .java files in the lab7 directory. To run the JUnit tests, I accessed my bash search history again by typing `<control>+<r>`. In the search area I typed `ListExamplesTests`. My terminal looked like the following. 

![Image](https://user-images.githubusercontent.com/122569733/221476403-58764ca8-ad3d-4d7f-885d-f5eba478aea6.png)

After I hit `<enter>`, the JUnit tests ran. My terminal indicated that all tests passed, as shown below. This means that the code in ListExamples.java is no longer buggy. 

![Image](https://user-images.githubusercontent.com/122569733/221476794-2c24b0a8-8f5c-428a-9700-fe3bdc8f7fb8.png)
## Step 9: Commit and Push
To commit the changes made in ListExamples.java to the main Github repository, I first typed in `git add ListExamples.java` and hit `<enter>`. This command saves the modified version of the .java file so that it can be committed. Next, I typed `git commit -m "ListExamples.java edited"`. This command commits the file and prints out a message to indicate this. I hit `<enter>`. The commands and their output are shown below. 

![Image](https://user-images.githubusercontent.com/122569733/221744489-2aed5044-e124-420f-93a9-8ebe993c8377.png)

To push the file, I typed `git push`. I was then prompted for my Github username and password. Once entered, my terminal indicated that the push was successful. 

![Image](https://user-images.githubusercontent.com/122569733/221744788-953479c6-03d1-4433-90ed-e189b558f896.png)

Just to be sure this step was successful, I went to my Github account online to look at recent pushes. My Github indicated that the file commit and push were successful. 

![Image](https://user-images.githubusercontent.com/122569733/221744928-d83fcdf5-6697-4330-b470-4615b273ab4e.png)
