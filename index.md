
### Lab Report 4 

For the lab report this week, reproduce the task from above on your own. For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

#### Step 4: Log into ieng6
```
ssh cs15lfa23il@ieng6.ucsd.edu Yes <password>
```


#### Step 5: Clone your fork of the repository from your Github account (using the SSH URL)
```
git clone https://github.com/adhithinm/lab7.git
```
<img width="601" alt="Screenshot 2023-11-19 at 5 46 00 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b9a07cb6-a982-4fa4-94aa-f8ec2f7dbe2f">


#### Step 6: Run the tests, demonstrating that they fail
```
bash test.sh
```
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
<img width="622" alt="Screenshot 2023-11-19 at 5 45 37 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/46dbe351-696d-4a60-bf30-1e6ce681b884">

#### Step 8: Run the tests, demonstrating that they now succeed
```
bash test.sh
```
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
