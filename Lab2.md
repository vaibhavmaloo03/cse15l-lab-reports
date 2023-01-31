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
