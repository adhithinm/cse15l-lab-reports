### Lab Report 1 - Remote Access and FileSystem (Week 1)

`cd` command 
-

#### What is the `cd` command and what does it do? 

The `cd` command allows the user to move between directories. 

### `no arguments` 

I was not in a directory and I tried to follow the commands. Having no arguments didn't do anything to the terminal; it had no output. There is no output, and this is not an error. 

##### Resubmission Comments and Fixes

Need to explicitly mentioned where cd takes you back to if there is no argument: Without an argument, using cd takes you back to the home directory, instead of taking you to another directory. 

Missing the discussion of the working directory for this: As already discussed in the first submission, I was in the home directory, and not in an explicit directory that I had created in my folders. Trying to follow the commands and using cd with no argument did not do anything to the terminal, and there was no output. This was not an error, and the working directory did not change. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 30 50 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/fe9d483c-fb66-48ab-b1b0-13686d14b723">


### `path to a directory` 

I was not in any directory when initially starting, so I used `cd` to move into a directory. I got this output because that was the goal of using `cd` followed by the name of the directory. As a result, this is not an error. 

Missing a discussion of the working directory for this: As already discussed in the first submission, I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used cd to move into the directory, I was able to move into another directory when I used cd following by the name of the directory. Since this did what I wanted it to do and gave me the right output, this was not an error. An error is defined as being a mistake, which in this case, there was no mistake since this was expected behavior of the computer. The working directory changed when I used the cd command. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 33 01 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/18944df2-e325-4286-9ab5-6abc62a2df0e">

### `path to a file` 

This is actually invalid. The `cd` command does not allow a user to go to a file, which makes this an error. I began in no directory, and then moved into a directory, but could not use the `cd` command followed by the name of a file because that was not what this command was meant to do. 

Missing a discussion of the working directory for this: As already discussed in the first submission, I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used cd to move into the directory with the file name after the command, I made an error, since this is not what is supposed to happen. This command is only meant to move in and out of directories, and not access files. The working directory did not change, and I got an error message instead, which told me that using cd followed by a file name was not possible. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 34 30 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b9aa751f-6d9a-4ad5-97ca-f6a484839d52">

`ls` command 
-

#### What is the ls command and what does it do? 

The `ls` command lists files in a certain directory. 

`no arguments` 
Typing in `ls` gives us the name of the directory. When I move into another directory and use the `ls` command, the files, classes, and directories. There is no error here, since that is what the command is supposed to do. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used ls in the home directory, it listed the directories available. I moved into the next directory using cd, and then used ls with no arguments again, and the files and directories in the directory I was in were listed. After I moved into the next directory using cd again, I used ls with no arguments, and the computer listed the available files in the current working directory. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 44 55 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b029df37-1ad0-4449-93d6-aadb4790ebae">

`path to a directory` 
When I use the `ls` command with a directory, it lists the directories in the direcotyr and other text files. There is no error here, since that is what the `ls` command is supposed to do. There is not error. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used ls followed by the name of the directory in the home directory, the terminal listed the classes and directories in the directory I typed in. When I moved into that directory using cd, and did the same thing, the computer listed the files that were in that directory. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 45 40 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/dfc74449-70b8-4691-bfd3-81d5c15419ec">

`path to a file` 
Not possible. It will just list the file. Even though this command runs with a file name, it just returns the file name, and doesn't do anything, which is an error. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used ls followed by the file name, I was not able to access it from the current working directory. I used cd to move into the directory, and then I tried using ls followed by the file name. This made the computer print out the file name. However, all this was doing was listing the file name, so this is an error even though the command still runs and gives an output. 

<img width="1440" alt="Screenshot 2023-10-04 at 9 48 10 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/66ea019f-50cc-4380-93c4-a642a828c4ea">

`cat` command 
-

#### What is the cat command and what does it do? 

The `cat` command reads in data from the file argument and displays that data as an output in terminal. It prints out the contents of a file. 

`no arguments` 

This is invalid. When using the `cat` command with no arguments, the terminal waits for another input. If I stop the page, then the command does not do anything. This is not an error;  `cat` can handle no arguments, but all it will do is just read the data from the standard input, and write them to its standard output. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used cat followed by no arguments, I was not met with any response. This happened regardless of the directory I was in. However, this isn't an error. The terminal will wait for an input, and then it will read the data from that standard input, and sent this to the standard output. 

Notes: 

It is not actually an error! What happens if the user were to type something and hit enter after running "cat" with no args? Actually, the cat command will read data from its standard input and write them to its standard output! Try it out! 

<img width="1440" alt="Screenshot 2023-10-04 at 11 03 39 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/2691ffb3-bc33-4ea4-a625-8d7baddcbe54">


`path to a directory` 
This is not valid and is an error because the `cat` command is not designed to read directories; it is designed for reading files. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used cat followed by the name of the working directory, the computer verified that the directory that I used was indeed a directory. That's all it did, and that's because the command is not designed to read directories, and is designed for reading files instead. 

<img width="1440" alt="Screenshot 2023-10-04 at 11 05 10 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/2c01efdf-1cd1-479f-811d-32774c1a8241">

`path to a file` 
This is not an error. `cat` followed by the file name results in the ouput of the contents of that file, after we enter the directory that the file is directly in. 

Missing a discussion of the working directory for this: I was in the initial home directory, which the computer created for me. I was in a directory that I did not physically create. When I used cat followed by the name of the file, nothing happened. I used cd to change my working directory, and then used cat followed by the file name. As a result, the computer printed out the content of the file. This same thing happened when I changed my working directory again to another directory, and then used the cat command followed by a file name. 

<img width="1440" alt="Screenshot 2023-10-04 at 11 07 07 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/3fc19508-5f4a-4f9f-bc86-30fe21dcb030">


