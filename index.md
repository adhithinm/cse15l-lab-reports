#### Original Post - ORIGINAL POST (1):

Hello,

I'm trying to run the GradeServer.java file program by using the bash script, but I don't know what I'm doing wrong. 
The script is supposed to compile and then run the program, then grade the papers. However, it's not working, even though I can see that student-submission/ListExamples.java does exist. 
Here's the output I'm getting:

```
grade.sh: line 11: student-submission/ListExamples.java: Permission denied
Not able to access file!

Incorrect file submitted.
```

I'm not sure what the problem is. Can someone help me with it? Here's the screenshot below: 

<img width="1383" alt="Screenshot 2023-12-03 at 7 41 28 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/317bc9a8-98c1-4654-b028-63b62bb5ca92">

_____________________________________________________________________________________________________________________

#### Reply from the TA - TA RESPONSE (2):

Hello there, 

It looks like even though the file is there, the program can't see that the file exists. Have you checked to make sure that you're in the correct directory? Try checking this first. A reminder: you can use the `ls ` command along with the file you're trying to find to help the program recognize that the file exists. 

Hope this helps! 

_____________________________________________________________________________________________________________________

#### Reply from the Student - BUG DESCRIPTION (3):

Hello there, 

Thank you so much! It turns out that the program didn't recognize which directory and file I was in, so it couldn't find the `ListExamples.java` file that I was asking it to find in the `student-submission` folder. I added `ls` to the line, and it worked because the command was able to show the files in the `student-submission` folder. Since `ListExamples.java` was in the folder, it was shown in the output, and the program was able to access it. Here's a screenshot of it working. 

<img width="1440" alt="Screenshot 2023-12-03 at 7 43 23 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/ad3b8317-acb9-4b7e-8f91-f57ab2276451">

Thank you so much! 

_____________________________________________________________________________________________________________________

#### Information about Set Up - SET UP INFO (4): 
At the end, all the information needed about the setup including:
##### The file & directory structure needed
- .vscode
- grading-area
    - JUnitOutput.txt
    - Server.java
    - TestListExamples.java
- lib
  - hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar
  - junit-4.13.2.jar
- student-submission
  - ListExamples.java
- grade.sh
- GradeServer.java
- JUnitOutput.txt
- Server.java
- TestListExamples.java

##### The contents of each file before fixing the bug

GradeServer.java: 
- 
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.net.URI;
import java.net.URISyntaxException;
import java.util.Arrays;
import java.util.stream.Stream;

class ExecHelpers {

  /**
    Takes an input stream, reads the full stream, and returns the result as a
    string.

    In Java 9 and later, new String(out.readAllBytes()) would be a better
    option, but using Java 8 for compatibility with ieng6.
  */
  static String streamToString(InputStream out) throws IOException {
    String result = "";
    while(true) {
      int c = out.read();
      if(c == -1) { break; }
      result += (char)c;
    }
    return result;
  }

  /**
    Takes a command, represented as an array of strings as it would by typed at
    the command line, runs it, and returns its combined stdout and stderr as a
    string.
  */
  static String exec(String[] cmd) throws IOException {
    Process p = new ProcessBuilder()
                    .command(Arrays.asList(cmd))
                    .redirectErrorStream(true)
                    .start();
    InputStream outputOfBash = p.getInputStream();
    return String.format("%s\n", streamToString(outputOfBash));
  }

}

class Handler implements URLHandler {
    public String handleRequest(URI url) throws IOException {
       if (url.getPath().equals("/grade")) {
           String[] parameters = url.getQuery().split("=");
           if (parameters[0].equals("repo")) {
               String[] cmd = {"bash", "grade.sh", parameters[1]};
               String result = ExecHelpers.exec(cmd);
               return result;
           }
           else {
               return "Couldn't find query parameter repo";
           }
       }
       else {
           return "Don't know how to handle that path!";
       }
    }
}

class GradeServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

class ExecExamples {
  public static void main(String[] args) throws IOException {
    String[] cmd1 = {"ls", "lib"};
    System.out.println(ExecHelpers.exec(cmd1));

    String[] cmd2 = {"pwd"};
    System.out.println(ExecHelpers.exec(cmd2));

    String[] cmd3 = {"touch", "a-new-file.txt"};
    System.out.println(ExecHelpers.exec(cmd3));
  }
}

```

grade.sh
-
```
CPATH='.:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar'

rm -rf student-submission
rm -rf grading-area

mkdir grading-area

git clone $1 student-submission
echo 'Finished cloning'
 
file=` student-submission/ListExamples.java`
echo $file

if [[ -f $file ]]
then
    echo "File found."
else 
    echo "Incorrect file submitted."
    exit 1
fi

cp student-submission/* grading-area 
cd grading-area

javac -cp $CPATH ListExamples.java 2>ListExamplesErrorOutput.txt
if [[ $? -eq 0 ]]
then 
    echo "Compiled correctly."
    javac -cp $CPATH org.junit.runner.JUnitCore ../TestListExamples.java >JUnitOutput.txt 2>&1  # something here is not working
    java -cp $CPATH org.junit.runner.JUnitCore ../TestListExamples >>JUnitOutput.txt 2>&1
else 
    echo "Failed to compile."
    exit 1
fi 



# Draw a picture/take notes on the directory structure that's set up after
# getting to this point

# Then, add here code to compile and run, and do any post-processing of the
# tests
```

##### The full command line (or lines) you ran to trigger the bug

```
bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3
```

##### A description of what to edit to fix the bug

The `ls` command should be added within the `grade.sh` file in order to actually have the program look into checking the `student-submission` folder. This will help the program look at the documents inside the folder, and then realize that the `ListExamples.java` file is in the folder. 

In a couple of sentences, describe something you learned from your lab experience in the second half of this quarter that you didn’t know before. It could be a technical topic we addressed specifically, something cool you found out on your own building on labs, something you learned from a tutor or classmate, and so on. It doesn’t have to be specifically related to a lab writeup, we just want to hear about cool things you learned!
- 
Something that I learned from my lab experience in the second half of this quarter that I didn't knwo before was about Vim. I didn't know that Vim existed before, and I didn't realize that you could edit files in terminal using Vim, even though I've used terminal for various commands before with raspberry pi and other technologies previously. This was interesting, but there were a lot of commands that I needed to familiarize myself with, but it was overall really cool to see a new technology or application of something I had worked on before, and another way to use it. Typically, I'm used to having to open up my folder and having the whole set up ready before I can get started with file editing; however, Vim made it much easier to edit files in terminal alone. 
