# Lab Report 3

Part 1 
- 

### Provide:
#### Name of method: 
Reverse in Place 

#### A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
int[] input1 = { 3 , 5};


#### An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
int[] input1 = { 3 };

#### The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
{image} 

#### The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
##### Before: 

`
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
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

