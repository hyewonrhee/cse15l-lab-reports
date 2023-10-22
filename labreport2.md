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
