# Week 2 Lab report
---
## Part 1: Creating a Server
The servers objective is to keep track of single string that gets added to by incoming requests.
The code for the server is as follows:
```
import java.io.IOException;
import java.net.URI;
import org.xml.sax.ErrorHandler;
import org.xml.sax.ErrorHandler;

class Handler implements URLHandler {

StringBuilder str = new StringBuilder();

    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            
            str.append(url.getQuery().substring(2)+"\n");
            return str.toString();
        }
         else {
            System.out.println("Path: " + url.getPath());
            return "404 Not Found!";
        }
    }
}
class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
When run, this code generates a web server like this:

![image](1.png)

First, the main method in `StringServer` class is called. Which makes a `Handler` object. For this, the `Handler` class implements the `handleRequest` method which processes the path and query to give results on the screen of a website. If the url doenst have a `/add-message?s=` in it, it is an unfound web page and the server returns a 404 not found error.
When another "message" is added after the first message, the server puts the message in the next line and keeps track of messages.
For example:

![image](2.png)

## Part 2: Bugs from lab 3
One of the bugs I found in Lab 3 was while testing the `testReverseInPlace()` method of the class `ArrayExamples`.

![image]

## Part 3: Learnings from Lab 2 and Lab 3
In the last two lab classes, I learnt how to create a web server and connect it to my website. I learnt how to handle and process urls especially using different queries. I also learnt how to use Junit effectively and find bugs.
