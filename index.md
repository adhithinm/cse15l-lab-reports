# Lab Report 3

Part 1 
- 

Comment: The link is not clickable. 
Edit: It's not supposed to be; it comes up with the website link and format. This is not part of the actual lab report. 

### Provide:
#### Name of method: 
Reverse in Place 

#### A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
```
int[] input1 = { 3 , 5};
```


#### An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
```
int[] input1 = { 3 };
```

#### The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)

Comment: Image not visible. 
Edit: Here's the image. 
<img width="630" alt="Screenshot 2023-11-19 at 5 04 55 PM" src="https://github.com/adhithinm/cse15l-lab-reports/assets/146797389/f34ac3bb-373d-4560-ba59-c56feb88910e">


#### The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
##### Before: 

Comment: Code markdown format incorrect. 
Edit: Fixed. 

```
static void reverseInPlace(int[] arr) { 
    for(int i = 0; i < arr.length; i += 1) { 
        arr[i] = arr[arr.length - i - 1];
  } 
 } 
 ```

Comment: Incorrect formatting. 
Edit: Fixed. 

##### After: 

```
static void reverseInPlace(int[] arr) {
 for(int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i]; 
    arr[i] = arr[arr.length - i - 1]; 
    arr[arr.length - i - 1] = temp;
 } 
} 
```

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

Output: 
```
1. DNA, or deoxyribonucleic acid, is the hereditary material in humans and almost all other organisms.
4. Nearly every cell in a person's body has the same DNA.
7. Most DNA is located in the cell nucleus (where it is called nuclear DNA), but a small amount of DNA can also be found in the mitochondria.
12. The sequence of the DNA is responsible for genetic inheritance.
15. DNA replication is a complex process of duplicating the DNA before cell division.
18. Alterations in DNA sequences can lead to genetic disorders and diseases.
21. DNA analysis has become crucial in forensic science, helping to solve crimes.
24. The study of DNA involves various branches of science including biology, genetics, and biochemistry.
27. Environmental factors can also affect DNA expression and function.
30. Recent advances in DNA technology have paved the way for breakthroughs in medical research.
```

**Example 2:**

`grep -i "dna" ./biomed/`

This example searches for the word "dna" in the entire biomed directory. DNA or dna will be counted, since this search is not case sensitive due to the `-i` command. 

Output: 

```
./biomed/article1.txt: DNA is the main component of chromosomes in the nucleus of biological cells.
./biomed/article1.txt: The structure of DNA is dynamic along its length.
./biomed/article2.txt: Methods for DNA sequencing have evolved rapidly.
./biomed/article2.txt: DNA mutations can lead to diseases.
./biomed/research_paper3.txt: Understanding DNA replication is essential for genetic research.
./biomed/research_paper3.txt: DNA repair mechanisms are crucial for cell survival.
./biomed/notes.txt: Seminar on DNA polymerase function next week.
```

#### Command line option 2: `-r` 

**What it does:** 

The search begins a recursive search for a string in all subdirectories of the given directory. 
**Example 1:**

`grep -r "players" ./football/`

This example searches for the word "players" in all of the subdirectories of the directory "football" by performing a recursive search. 

Output: 

```
./football/team_stats.txt: The team has a roster of 25 players.
./football/match_reports/match1.txt: Several players received accolades for their performance.
./football/match_reports/match2.txt: Two players were given red cards.
./football/training/schedule.txt: Training sessions are mandatory for all players.
./football/player_profiles/player1.txt: This player has been in top form this season.
./football/player_profiles/player2.txt: Among the youngest players, he stands out for his skill.
./football/news/announcement.txt: The club is looking to recruit new players during the transfer window.
```

**Example 2:**

`grep -r "leaves" ./journal/october/`

This example searches for the word "leaves" in the subdirectories of the october directory, which is part of the journal directory. A recursive search is performed to find the word. 

Output: 

```
./journal/october/week1.txt: The way the leaves fall in October is mesmerizing.
./journal/october/week1.txt: He leaves for his trip to Spain next week.
./journal/october/week2.txt: The garden needs raking; too many leaves have fallen.
./journal/october/week3.txt: The recipe calls for bay leaves.
./journal/october/week4.txt: She leaves for her new job in New York.
./journal/october/week4.txt: The leaves turning red and gold is a highlight of the season.
./journal/october/special_events.txt: Remember to collect leaves for the art project.
```

#### Command line option 3: `-v` 

**What it does:** 

This search returns all of the lines in a text file which does not have the string specified. 

**Example 1:**

`grep -v "honda" ./cars/2013cars.txt`

This example outputs all of the lines that do not have the word "honda" in them from the 2013cars.txt file. It removes any lines with the string "honda" when placing them in the output. 

Ouput: 

```
Toyota Camry: Midsize sedan, great fuel efficiency.
Ford F-150: Popular full-size pickup truck with robust capabilities.
BMW 3 Series: Luxury compact sedan with excellent driving dynamics.
Chevrolet Impala: Full-size car known for its spacious interior.
Nissan Altima: Well-rounded midsize sedan, strong performance.
Volkswagen Golf: Compact hatchback with a comfortable ride.
Mazda CX-5: Compact crossover SUV, known for its agile handling.
Subaru Outback: Versatile wagon with all-wheel drive as standard.
```

**Example 2:**

`grep -v "cat" ./pets-owned`

This example searches for the string "cat" in the all of the text files of the pets-owned directory. It outputs all of the lines that do not have the string "cat" in them. 

Output: 
```
Dog - Golden Retriever
Fish - Goldfish
Dog - Beagle
Rabbit - Angora
Bird - Parakeet
Dog - Labrador
Fish - Betta
Hamster - Syrian
Bird - Canary
```

#### Command line option 4: `-c` 

**What it does:** 

This search returns the number of lines that have the string specified. 

**Example 1:**

`grep -c "starbucks" ./coffee-shops-ca/san-diego.txt`

Output: 

```
12
```

This example displays the number of the lines in the san-diego.txt files where the string "starbucks" appears. 

**Example 2:**

`grep -c "coffee bean" ./coffee-shops-ca/`

This example displays the number of lines in the coffee-shops-ca directory which has the string "coffee bean". 

Output: 

```
./coffee-shops-ca/san-diego.txt:5
./coffee-shops-ca/los-angeles.txt:8
./coffee-shops-ca/san-francisco.txt:3
./coffee-shops-ca/sacramento.txt:2
./coffee-shops-ca/san-jose.txt:4
```

Citing Sources: 
Chatgpt was the only source used. It is cited below. 

OpenAI. "ChatGPT response." OpenAI, 11/19/2023. Accessed 11/19/2023. https://openai.com/chatgpt
