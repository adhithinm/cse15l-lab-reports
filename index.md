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
