# **Lab Report 2**

## Part 1: 

```
import java.net.URI;
import java.io.IOException;

class Handler implements URLHandler {

    String runningString = new String();
    
    public String handleRequest(URI url) {
        
        if(url.getPath().contains("/add-message")){
            String[] parameter = url.getQuery().split("=");
            if (parameter[0].equals("s")) {
                runningString = runningString + "\n" + parameter[1];
            }
        }
        return runningString;
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
