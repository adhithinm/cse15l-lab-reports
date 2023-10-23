### Lab Report 2 

Part 1 
- 

## Code for StringServer: 


`import java.io.IOException;`
`import java.net.URI;`
`import java.util.ArrayList;`
`import java.util.List;`

`class Handler implements URLHandler {`
  `  // The one bit of state on the server: a number that will be manipulated by
    List<String> list = new ArrayList<>();`

    // a method that returns the string of the website. If not found, we return a 404 error.
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "Word List: " + list;
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    list.add(parameters[1]);
                    StringBuilder output = new StringBuilder();
                    for (int i = 0; i < list.size(); i++) {
                        output.append(i + 1).append(". ").append(list.get(i)).append("\n");
                    }
                    return output.toString();
                }
            }
            return "404 Not Found!";
        }
    }
}

`class StringServer {
    public static void main(String[] args) throws IOException {`

        //Checks for port number 
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        // If we have a port number, then we parse through the number 
        int port = Integer.parseInt(args[0]);

        // We start the server on the port number 
        Server.start(port, new Handler());
    }
`}`

## Screenshot 1 <img width="1440" alt="Screenshot 2023-10-22 at 9 33 22 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/42eac82e-6300-470e-9e23-fc546acd3604">

#### Which methods in your code are called?
URL Handler and String Server

#### What are the relevant arguments to those methods, and the values of any relevant fields of the class?
parameters[1] 

#### How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
parameters[1] gets changed when there is a new string in the add message url routing. 

## Screen 2 <img width="1440" alt="Screenshot 2023-10-22 at 9 36 35 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/87863d2f-2b5c-48f5-b91c-ecbc9dac4197">

#### Which methods in your code are called?
URL Handler and String Server

#### What are the relevant arguments to those methods, and the values of any relevant fields of the class?
parameters[1] 

#### How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
parameters[1] gets changed when there is a new string in the add message url routing. 

Part 2
- 

Using the command line, show with ls and take screenshots of:

The path to the private key for your SSH key for logging into ieng6 (on your computer or on the home directory of the lab computer)
The path to the public key for your SSH key for logging into ieng6 (within your account on ieng6)
A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password.

<img width="1440" alt="Screenshot 2023-10-22 at 11 00 48 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/1d9a91fa-2898-46e3-813e-17a12694b6e9">

Part 3
-
#### In a couple of sentences, describe something you learned from lab in week 2 or 3 that you didn’t know before.
I didn't know about how web servers worked, and how the routing system worked for them. I didn't realize that there was code based on what the link was on, and I didn't know what the question marks and random symbols in the url path stood for. Now, I know that they stood for the query and input, and it told the program what to do with them. 
