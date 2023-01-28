# Lab report 2: Servers and Bugs

## Part 1: StringServer
- I created a server called StringServer that prints out string messages. The requests of the server produce the following pages:

![Image](https://user-images.githubusercontent.com/122569733/215231995-69a9c05c-8059-4c3c-ac9d-a43959f86e85.png)
- To produce the server, several methods are called: 
  - The main method is called, which takes in a number input to start the server.
  - The start() method from Server.java is called. This method takes the arguments port (the number input) and handler, which helps configure a website URL. Under this start() method, a new server is created.  
- To handle the requests made in the search bar, another method is called:
  - To produce the words displayed on the server window, the handleRequest() method is then called. The argument for this method is the URL in the search bar. This method looks at the text after "/add-message?s=" and prints it out on the screen. To print this text on the screen, the string after "/add-message?s=" is added to an output string in the handleRequest() method. This output string is what's returned on the screen. The following is added to the end of the URL. 
```
/add-message?s=Hello
```
  - This produces the following words on the screen.
```
Hello
```
- To produce new words on the screen, the URL in the search bar must be changed. This change produces the following: 

![Image](https://user-images.githubusercontent.com/122569733/215233406-fdbb2a32-e033-4e72-85dd-0055ec5a2c0d.png)
- Again, the handleRequest() method is called. The argument is the edited URL. Again, the string after "/add-message?s=" is added to the output string. By doing this, the previous output and the new output is shown on the screen. I changed the end of the URL to: 
```
/add-message?s=Hi eve
```
  - This prints out the following:
```
Hello
Hi eve
```
- Although the inputted argument is different for the handleRequest() method 
