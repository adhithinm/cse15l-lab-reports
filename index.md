
### Lab Report 4 

For the lab report this week, reproduce the task from above on your own. For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

#### Step 4: Log into ieng6
```
ssh cs15lfa23il@ieng6.ucsd.edu
Yes
<password>
```
This was simply typed. My password was also typed. 

#### Step 5: Clone your fork of the repository from your Github account (using the SSH URL)
```
git clone https://github.com/adhithinm/lab7.git
```
<img width="601" alt="Screenshot 2023-11-19 at 5 46 00 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b9a07cb6-a982-4fa4-94aa-f8ec2f7dbe2f">
This was typed; I typed in git clone, and pasted the cloning url into my terminal. 

#### Step 6: Run the tests, demonstrating that they fail
```
bash test.sh
```
I used the up arrow to bring back the command and use it again. 

This command runs the test.sh script file, and turns all of the commands in the file. This makes it easier so that I don't have to type in the same string of commands each time I want to do them. 
<img width="600" alt="Screenshot 2023-11-19 at 5 45 50 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/0fbdbd51-7f7e-42f3-be88-1bae20051073">


#### Step 7: Edit the code file to fix the failing test
```
j
l
x
i
2
<escape>
:wq!
<enter> 
```
I used these keys to edit the failing test, and to navigate, I used the j arrow and l arrow which is possible in Vim. 
I clicked `j` to navigate down to the area I wanted to fix, and I used `l` to navigate to the right of the file. 
Then I used `x` to delete the character, just once. 
I clicked `i` to insert the character `2`. 
Then I clicked `<escape>` to escape from editing the text file.
To save and quit the file editing in one command, I clicked `:wq!`. 
Then I clicked `<enter>` to exit out of the command. 

<img width="622" alt="Screenshot 2023-11-19 at 5 45 37 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/46dbe351-696d-4a60-bf30-1e6ce681b884">

#### Step 8: Run the tests, demonstrating that they now succeed

I used the up arrow to bring back the command and use it again. 
```
bash test.sh
```
This command runs the test.sh script file, and turns all of the commands in the file. This makes it easier so that I don't have to type in the same string of commands each time I want to do them. 
<img width="626" alt="Screenshot 2023-11-19 at 5 45 21 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/ac057354-322d-4ed9-a76e-c0542ccc28fe">


#### Step 9: Commit and push the resulting change to your Github account (you can pick any commit message!)

```
git commit -a
i
Error fixed!
<escape>
:wq!
<enter>
``` 
The `git commit -a ` helps me commit the file with a message. 
`i` allows me to insert my own text, which I did when I typed `Error fixed!`. 
I then used the `<escape>` button to exit out of typing and editing the file. 
Then I pressed `:wq!` to save and exit the file in one command. 
Then I hit `<enter>` to return to editing and navigating using Vim. 
