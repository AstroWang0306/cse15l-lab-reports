# Lab Report5:

I found the results by using vimdiff and other commands that can write the result into a text file.
 1. `bash script.sh > result.txt` , I used this command in two different directories, which gave me two different results.
 2. `vimdiff my-markdown-parser/result.txt markdown-parser/result.txt`, use vimdiff to check if there were some diferent results. 

 To verify the correct results, I used the website [CommonMark](https://spec.commonmark.org/dingus/), which was provided by previous labs. 

## Bug 1:
The bug happened at test-493:
Here's the link to the test-493: [test-493](https://github.com/AstroWang0306/markdown-parser/blob/main/test-files/493.md)

Use `vimdiff` to show different results:
<img width="665" alt="Screen Shot 2022-06-10 at 2 19 47 PM" src="https://user-images.githubusercontent.com/97696773/173152781-0f99de1d-bf88-4c8f-88de-a37a527cbe97.png">

The correct result displayed by CommonMark:
<img width="1193" alt="Screen Shot 2022-06-10 at 3 03 10 PM" src="https://user-images.githubusercontent.com/97696773/173156672-f20535c7-f4a0-4986-8669-2a0cf36084a6.png">

I think mine and the other one are both incorrect. 
In my result, there is no bracket and there is no expected output. It might because my program ignore the structure if there are many brackets and paraentheses. To fix this issue, I think it might be useful if I add one more if statement to ensure print out something that the program store the last index of bracket and parantheses. 

## Bug 2:
The bug happened at test-578
Here's the link to the test-578: [test-578](https://github.com/AstroWang0306/markdown-parser/blob/main/578.md)

Use `vimidff` to shoe different results:
<img width="897" alt="Screen Shot 2022-06-10 at 3 19 34 PM" src="https://user-images.githubusercontent.com/97696773/173157931-ec403b4c-f44a-41a7-a3d5-9e553ab672d4.png">

The correct result displayed by CommonMark: 
<img width="991" alt="Screen Shot 2022-06-10 at 3 20 22 PM" src="https://user-images.githubusercontent.com/97696773/173157993-b1fa492d-ef66-4431-b52a-81f1f5aa69b0.png">

I think mine result is not correct. But the other one is correct. In the 578.md, there is a space after "title". In my output, there is no space. The reason is because my program cannot recognize space and hence ignore it. To fix this issue, I think I can also add another if statement when there is a space, skip to the next index until there is a bracket or paraentheses. 
