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

##### The full command line (or lines) you ran to trigger the bug

##### A description of what to edit to fix the bug
