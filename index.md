#### Original Post:

Hello,

I'm trying to run the GradeServer.java file program by using the bash script, but I don't know what I'm doing wrong. 
The script is supposed to compile and then run the program, then grade the papers. However, it's not working, even though I can see that student-submission/ListExamples.java does exist. 
Here's the output I'm getting:

```
grade.sh: line 11: student-submission/ListExamples.java: No such file or directory

Incorrect file submitted.
```

I'm not sure what the problem is. Can someone help me with it? 

_____________________________________________________________________________________________________________________

#### Reply from the TA:

Hello there, 

It looks like even though the file is there, the program can't see that the file exists. Have you checked to make sure that you're in the correct directory? Try checking this first. A reminder: you can use the `ls ` command along with the file you're trying to find to help the program recognize that the file exists. 

Hope this helps! 

_____________________________________________________________________________________________________________________
