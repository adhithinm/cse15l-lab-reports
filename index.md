# Lab Report 3

Part 1 
- 

Comment: The link is not clickable. 
Edit: It's not supposed to be; it comes up with the website link and format. This is not part of the actual lab report. 

### Provide:
#### Name of method: 
Reverse in Place 

#### A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
int[] input1 = { 3 , 5};


#### An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
int[] input1 = { 3 };

#### The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)

Comment: Image not visible. 
Edit: Here's the image. 
<img width="630" alt="Screenshot 2023-11-19 at 5 04 55 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/f34ac3bb-373d-4560-ba59-c56feb88910e">


#### The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
##### Before: 

Comment: Code markdown format incorrect. 
Edit: Fixed. 

`
static void reverseInPlace(int[] arr) { `
  
  `  for(int i = 0; i < arr.length; i += 1) {`
   
   `     arr[i] = arr[arr.length - i - 1];`
 
 ` }`

`}`
`


##### After: 
`static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
`

##### Briefly describe why the fix addresses the issue.
The fix addressess the issue because the method before tried to change the indexes of the elements. However, it gave the same elements the same indexes, so it did not change anything. WHile this worked when the list only had 1 element, it did not work when the list had multiple elements. 

Part 2
- 

#### Consider the commands less, find, and grep. Choose one of them. 
I chose the `grep` command. 

#### Command line option 1: `-i` 
**What it does:** 

The search is made to be case insensitive, meaning that the uppercase and lower case do not matter when typing your input file and pattern. 

**Example 1:**

`grep -i "dna" ./biomed/article1.txt`

This example searches for the word "dna" in the article1.txt file. DNA or dna will be counted, since this search is not case sensitive. 

**Example 2:**

`grep -i "dna" ./biomed/`

This example searches for the word "dna" in the entire biomed directory. DNA or dna will be counted, since this search is not case sensitive due to the `-i` command. 

#### Command line option 2: `-r` 

**What it does:** 

The search begins a recursive search for a string in all subdirectories of the given directory. 
**Example 1:**

`grep -r "players" ./football/`

This example searches for the word "players" in all of the subdirectories of the directory "football" by performing a recursive search. 

**Example 2:**

`grep -r "leaves" ./journal/october/`

This example searches for the word "leaves" in the subdirectories of the october directory, which is part of the journal directory. A recursive search is performed to find the word. 

#### Command line option 3: `-v` 

**What it does:** 

This search returns all of the lines in a text file which does not have the string specified. 

**Example 1:**

`grep -v "honda" ./cars/2013cars.txt`

This example outputs all of the lines that do not have the word "honda" in them from the 2013cars.txt file. It removes any lines with the string "honda" when placing them in the output. 

**Example 2:**

`grep -v "cat" ./pets-owned`

This example searches for the string "cat" in the all of the text files of the pets-owned directory. It outputs all of the lines that do not have the string "cat" in them. 

#### Command line option 4: `-c` 

**What it does:** 

This search returns the number of lines that have the string specified. 

**Example 1:**

`grep -c "starbucks" ./coffee-shops-ca/san-diego.txt`

This example displays the number of the lines in the san-diego.txt files where the string "starbucks" appears. 

**Example 2:**

`grep -c "coffee bean" ./coffee-shops-ca/`

This example displays the number of lines in the coffee-shops-ca directory which has the string "coffee bean". 

