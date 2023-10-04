### Lab Report 1 - Remote Access and FileSystem (Week 1)


<!-- Lab Report 1 Directions---> 

<details>
<summary>Lab Report 1 Directions</summary>
<br>
You’ll submit a lab report by writing a blog post about the basic filesystem commands we learned today. You should create the post, like we just described using Github Pages. The lab report is due Monday, October 9 by 10pm. See the FAQ below for common questions, including how to add images and what to submit to Gradescope.

#### For each of the commands cd, ls, and cat, and using the workspace you created in this lab:

*• Share an example of using the command with no arguments.*

*•  Share an exmaple of using the command with a path to a directory as an argument.*

*• Share an example of using the command with a path to a file as an argument.*

#### So that’s 9 total examples (3 for each command). For each, include:
   
   *• A screenshot or Markdown code block showing the command and its output*
  
   *• What the working directory was when the command was run*
   
   *• A sentence or two explaining why you got that output (e.g. what was in the filesystem, what it meant to have no arguments).*
    
   *• Indicate whether the output is an error or not, and if it’s an error, explain why it’s an error.*

*You will upload your submission by publishing the page on Github Pages, then printing the page to PDF and uploading to the Lab Report 1 assignment on Gradescope.*

</details>

### `cd` command 

#### What is the `cd` command and what does it do? 

The `cd` command allows the user to move between directories. 

`no arguments` 

<details>
<summary> Image </summary>
<br>

<img width="1440" alt="Screenshot 2023-10-04 at 9 30 50 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/fe9d483c-fb66-48ab-b1b0-13686d14b723">


</details>

`path to a directory` 

<details>
<summary> Image </summary>
<br>

<img width="1440" alt="Screenshot 2023-10-04 at 9 33 01 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/18944df2-e325-4286-9ab5-6abc62a2df0e">

</details>

`path to a file` 

This is actually invalid. The `cd` command does not allow a user to go to a file. 

<details>
<summary> Image </summary>
<br>

<img width="1440" alt="Screenshot 2023-10-04 at 9 34 30 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b9aa751f-6d9a-4ad5-97ca-f6a484839d52">


</details>




### `ls` command 

#### What is the ls command and what does it do? 

The `ls` command lists files in a certain directory. 

`no arguments` 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 9 44 55 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/b029df37-1ad0-4449-93d6-aadb4790ebae">
</details>

`path to a directory` 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 9 45 40 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/dfc74449-70b8-4691-bfd3-81d5c15419ec">
</details>

`path to a file` 

Not possible. It will just list the file. 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 9 48 10 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/66ea019f-50cc-4380-93c4-a642a828c4ea">

</details>


### `cat` command 

#### What is the cat command and what does it do? 

The `cat` command reads in data from the file argument and displays that data as an output in terminal. It prints out the contents of a file. 

`no arguments` 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 11 03 39 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/2691ffb3-bc33-4ea4-a625-8d7baddcbe54">
</details>

`path to a directory` 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 11 05 10 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/2c01efdf-1cd1-479f-811d-32774c1a8241">
</details>


`path to a file` 

<details>
<summary> Image </summary>
<br>
<img width="1440" alt="Screenshot 2023-10-04 at 11 07 07 AM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/3fc19508-5f4a-4f9f-bc86-30fe21dcb030">

</details>

