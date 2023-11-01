# Lab Report 2

## Part 1

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    
    int num = 0;
    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Number: %d", num);
        } else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    num += 1;
                    str += (String.format(num + ". " + parameters[1]+ "\n"));
                    // num += Integer.parseInt(parameters[1]);
                    // return String.format("Number increased by %s! It's now %d", parameters[1], num);
                    return str;
                }
            }
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

![Screenshot1](/cse15l-lab-reports/LR2-1.png)

- Which methods in your code are called?

    The method `handleRequest` is called.

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?

    The `handleRequest` method in the `Handler` class takes in a `URI` object, which was the URL requested. Relevant values within are `int num`, which keeps track of the number and is initially set to zero, and `String str`, which keeps track of the message the user wants to input, and is initially set as an empty String. When the path contains "/add-message", another relevant field is the `String[]` called `parameters`, which splits the query of the URL to access the appropriate part/message.

- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

  Since "/add-message" was used in this request, and the first of the `parameters` array was equal to "s", the `num` value was incremented by 1, and the `str` value was concatenated with a String version of `num` and the requested message "Hello", as well as a new line, through the split query by `.getQuery().split("=")`.

![Screenshot2](/cse15l-lab-reports/LR2-2.png)

- Which methods in your code are called?

    The method `handleRequest` is called.

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?

    The `handleRequest` method in the `Handler` class takes in a `URI` object again, which was the (updated) URL that was requested. Relevant values are `int num`, which now has a value of 1 after the first request, and `String str`, which now has a value containing the previous message (numbered) and a new line.
  
- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

    Since "/add-message" was used in this request as well, the `num` value was incremented to 2, and the `str` value was concatenated with the newly updated value of `num` and the requested message "How are you", as well as another new line, created a two-item numbered list of the previous request, as well as the new message.

## Part 2

![Screenshot3](/cse15l-lab-reports/LR2-5.png)

Path to public key for my SSH key (within account on ieng6)


![Screenshot3](/cse15l-lab-reports/LR2-6.png)

Path to private key for my SSH key (on personal computer)


![Screenshot4](/cse15l-lab-reports/LR2-3.png)
Terminal interaction logging into `ieng6` without being asked for a password.

## Part 3

**In a couple sentences, describe something you learned from lab in week 2 or week 3 that you didn't know before.**

I didn't know that you could copy files and/or directories between two systems, specifically the local system on my laptop and the remote system on the lab computers. Using the `scp` command during our most recent lab, it made sense to be able to have both our private and public keys available on both our VSCode and our remote accounts. I can see how this command can come to be very useful in settings outside of this course, in terms of being able to share code, either across systems or with other programmers. 
