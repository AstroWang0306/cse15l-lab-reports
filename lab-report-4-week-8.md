# Lab Report4:

Here's the link to week7 markdown-parser: [week7-markdown-parser](https://github.com/AstroWang0306/CSE15L-week7-markdown-parser )

Here're three test cases in MarkdownParseTest.java:
<img width="1000" alt="Screen Shot 2022-05-21 at 10 26 04 PM" src="https://user-images.githubusercontent.com/97696773/169680209-d2862f94-b516-4c7a-b980-bd91923baba3.png">

## Snippet1:
The expected output:
<img width="1000" alt="Screen Shot 2022-05-21 at 5 51 18 PM" src="https://user-images.githubusercontent.com/97696773/169673775-097a8a14-2bec-4cb5-913a-29ed3b0f3dcd.png">

or

[url.com, `google.com, google.com, ucsd.edu]


snippet1 in MarkdownParseTest.java:


### From my implementation:

Output from my implementation, I use `make test` to run the test case:
<img width="1000" alt="Screen Shot 2022-05-21 at 7 02 05 PM" src="https://user-images.githubusercontent.com/97696773/169675141-dec8af07-0f50-4de8-9880-5c84b00740e1.png">
As the screenshot shown, the test case pass.


### From week7 code review:

Output from the week7 code review:
<img width="1000" alt="Screen Shot 2022-05-21 at 7 21 57 PM" src="https://user-images.githubusercontent.com/97696773/169675542-f921f2b0-ce63-463b-812d-5c7cf1dceebc.png">

As the screenshot shown, the test case did not pass.

## Snippet2:
Expected output:
<img width="993" alt="Screen Shot 2022-05-21 at 8 55 26 PM" src="https://user-images.githubusercontent.com/97696773/169677777-0c5b80d9-eb12-49d4-8971-5efda0c8a196.png">

or 

a.com, a.com(()), example.com

### From my implementation:

<img width="1000" alt="Screen Shot 2022-05-21 at 9 13 02 PM" src="https://user-images.githubusercontent.com/97696773/169678264-9039e24f-c966-4dbc-a0f1-381039c807eb.png">

As the screenshot shown, the snippet2 test case failed. I think the reason is the code the reecognize the index of the first `(` and use the index to get the first index of `)`. Hence, if there are more `)` after the first index of `)`, those will not be added as the link. 

### From week7 code review:

<img width="1000" alt="Screen Shot 2022-05-21 at 9 44 18 PM" src="https://user-images.githubusercontent.com/97696773/169679106-46406037-20b1-4e27-8a96-9bbcca7c0ad8.png">

As the sceenshot shown, the test case did not pass. 

## Snippet3:
Expected output:
<img width="1000" alt="Screen Shot 2022-05-21 at 10 23 51 PM" src="https://user-images.githubusercontent.com/97696773/169680164-ef15ca07-2bf3-4ff0-a6ab-cf18b83d21e5.png">

or

https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/

### From my implementation:

<img width="1058" alt="Screen Shot 2022-05-21 at 10 11 37 PM" src="https://user-images.githubusercontent.com/97696773/169679836-bc848836-156d-4ab0-bdf1-3c7a9f327095.png">

As the screenshot shown, the test case fail. The reason I think is I did not notice the space. With recognizing the index of `[`,`]`,`(`, and `)`. My code will include every contents inside the paraenthesis. Hence, the output contained so much space compare to the correct result. 

### From week7 review code:


<img width="994" alt="Screen Shot 2022-05-21 at 10 19 40 PM" src="https://user-images.githubusercontent.com/97696773/169680072-485c38bf-6478-4e18-8c79-e94781fafb8e.png">

As the screenshot shown, the test case failed. 

## Conclusion:

### Q1:
For the first test case, it passed. I did not change anything. 

### Q2: 
For the second test case, I think I can write a while loop that will rocgnize the last index of `)` and print out the link content befor that index. IN this way, I believe this will be less than 10 line codes. 

### Q3:
For the third case, I think I can use a if statment to avoid collect the space and print them out. If there is only a if statement, it will definitely be less than 10 line codes. 


