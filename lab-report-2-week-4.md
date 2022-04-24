# Lab Report 2:

The symptom we found was a infinte loop. When we tried to run the test-file.md there is nothing in the output becasue the program would not break the while loop and print out the result.

## Here are three changes we made:

### 1st Change:

At the first time running the code, we did not know there was an infinte loop. However, the program was able to run and could be compiled. The first change was adding a print statement at the end of the while loop and seeing what did the program print out. Please see below screen shot. 

<img width="500" alt="Screen Shot 2022-04-24 at 11 09 32 AM" src="https://user-images.githubusercontent.com/97696773/164990354-947e6e63-e84a-42f0-aaf2-05b5a4d92134.png">


And here is the commit change screen shot:

<img width="1246" alt="Screen Shot 2022-04-24 at 11 45 13 AM" src="https://user-images.githubusercontent.com/97696773/164991610-b23ca5c5-ff6c-4a37-831f-ff299eaff3c4.png">


As we can see, at line 28, I wrote a print statement to print out "currentIndex" and see what the loop will give us. Please refer link for code chanegd and screen shot of the output by command line. 

<img width="1246" alt="Screen Shot 2022-04-24 at 11 24 33 AM" src="https://user-images.githubusercontent.com/97696773/164990897-4ae21cc1-dd43-4e99-81a5-7c7409c3fc5e.png">

The command we typed here were `javac MarkdownParse.java` for compiling and `java MarkdownParse test-file.md` for running the program. On the terminnal side, there were two numbers that were lept printing out, which were 64, and 39. 

Below is the link to test-file. 

[test-file.md](https://raw.githubusercontent.com/AstroWang0306/markdown-parser/main/test-file.md)

or 

[test-file.md](https://github.com/AstroWang0306/markdown-parser/blob/main/test-file.md)


Relationship between bug, symptom and 
The symptom here was the infinte loop as we can see the screen shot with the terminal. By the output, we can see 64 and 39. However, if we count the length of test-file.md, we can get the length of 65, which means the while loop will never reach the end of tje file and hence can escape from the loop. The inducing input are the test-file.md or the content in the file.

### 2nd Change:

Out team knew what caused the symptom or the infinte loop and we thought we could set condition and break the while loop. For this change, we set a if condition when `openBracket` is equal to -1, then break at the end of the program. Below are the screen shots of code chamged and the commit changed. 

Code changed: 
<img width="784" alt="Screen Shot 2022-04-24 at 12 11 12 PM" src="https://user-images.githubusercontent.com/97696773/164992618-0be78ed0-eb21-49dc-9688-5ab534b7944f.png">

Commit history:
<img width="1239" alt="Screen Shot 2022-04-24 at 12 09 31 PM" src="https://user-images.githubusercontent.com/97696773/164992632-76c81c14-1c2e-4f26-8119-3b690c7570c1.png">

Let's run the program for the same test file and see what happen now. 
Please see below for the output in the terminal. 
<img width="1286" alt="Screen Shot 2022-04-24 at 12 14 59 PM" src="https://user-images.githubusercontent.com/97696773/164992735-26c40604-3094-4516-bade-4ee721b02994.png">

The output seems to be correct. However, if we look at the test file. We knew there is something wrong with this output. Please use below link referring to the test file. 

[test-file.md](https://raw.githubusercontent.com/AstroWang0306/markdown-parser/main/test-file.md)

or 

[test-file.md](https://github.com/AstroWang0306/markdown-parser/blob/main/test-file.md)

In the test-file.md, we can only see two link in the file. The output in the terminal are three links, which is obviously not correct and is another symptom. But we solve the previous bug which was no conditions to have the loop break. The new bug and symptom will be solved by the third code change. The failure-inducing input is test-file.md or the content in the file. 

### 3rd Change:

As we found the new bug and symptom after making the second change. Because the third link we printed out were the same as the first link. We thought that the program would loop again before going to the if statement. So, we moved the if statement to after line 17 which was after the variable openBracket. Please see below screen shots for code changed and commit history. 

Code changed:
<img width="741" alt="Screen Shot 2022-04-24 at 1 10 52 PM" src="https://user-images.githubusercontent.com/97696773/164994740-dafca1cc-b8e8-491a-9f48-3259159e31ee.png">

Commit history:
<img width="741" alt="Screen Shot 2022-04-24 at 1 13 07 PM" src="https://user-images.githubusercontent.com/97696773/164994814-e1e62687-13e4-4c6c-a117-629f8fb0f535.png">

After moving the if statement after line 17, let's see what happen now. Please see the below screen for the output. 

<img width="1291" alt="Screen Shot 2022-04-24 at 1 16 56 PM" src="https://user-images.githubusercontent.com/97696773/164994897-745356f8-84df-4878-b7e6-b57c2f7421a6.png">

The outputs are coorect right now. Pleae use below links to access test file. 

[test-file.md](https://raw.githubusercontent.com/AstroWang0306/markdown-parser/main/test-file.md)

or 

[test-file.md](https://github.com/AstroWang0306/markdown-parser/blob/main/test-file.md)

The symptom here for the third change were the three links in the output, which the correct one were only two links. The bug here was we put the if statement at the end of the while loop and caused the program to loop again hence printed out one more time the first link. In order to fix the bug, we moved the if statement to line 18 which the program will break immediately if the variable - `openBracket` was equal to -1. The failure-inducing input was the test-file.md or the content in the file. 












