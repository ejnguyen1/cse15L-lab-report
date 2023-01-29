# Lab report 2: Servers and Bugs

## Part 1: StringServer
I created a server called StringServer that prints out string messages. The first request of the server produces the following page.

![Image](https://user-images.githubusercontent.com/122569733/215231995-69a9c05c-8059-4c3c-ac9d-a43959f86e85.png)
To produce the server, several methods are called: 
- The main method is called, which takes in a number input to start the server.
- The start() method from Server.java is called. This method takes the arguments port (the number input) and handler, which helps configure a website URL. Under this start() method, a new server is created.  

To handle the requests made in the search bar when the server is live, the handleRequest() method is called.

The argument for this method is the URL in the search bar. This method breaks up the URL argument and looks at the text after `/add-message?s=`. This text is then printed out on the screen.

For the photo above, the text `/add-message?s=Hello` is at the end of the URL. This produces the following word on the screen. 

```
Hello
``` 

To print this text on the screen, the string after `/add-message?s=` is added to an output String variable in the handleRequest() method. This output string is what's returned on the page. 

To produce new words on the screen, the URL in the search bar must be changed. This change produces the following. 

![Image](https://user-images.githubusercontent.com/122569733/215233406-fdbb2a32-e033-4e72-85dd-0055ec5a2c0d.png)
The handleRequest() method is called again when the URL is edited. The edited URL is the argument. The string after `/add-message?s=` is added to the output string. In this case, the important part of the URL is the text `/add-message?s=Hi eve`. This produces the following text on the screen.

```
Hello
Hi eve
```
Although the inputted URL argument is a little bit different, the output String variable in the handleRequest() method contains past inputted text. This is why text from past URL changes are still printed out on the screen.

Although the path of the URL is edited, the domain stays the same. Only the text after `/add-message?s=` is altered.
## Part 2: Bugs 
The following method reverseInPlace() changes an input array to be in reverse order, however it contains a bug.
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
The following test case contains failure inducing input for the method.
``` 
@Test
  public void testReverseInPlace2() {
    int[] input2 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{3, 2, 1}, input2);
  }
  ```
  
