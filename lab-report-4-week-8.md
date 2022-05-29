## Week 8 Lab Report 4

For this lab report, we will run tests on some test files. Here are the 3 test files and their expected output from VScode preview. 

1. Snippet 1
![image](snippet1.png)

2. Snippet 2
![image](snippet2.png)

3. Snippet 3
![image](snippet3.png)

We will run tests on [our implementation of markdown-parse](https://github.com/mrreganwang/markdown-parser) and [implementation from other group](https://github.com/Luke-Sheltraw/markdown-parser/)

Here are the tests we'll be running on both implementations:
![image](testsForSnippets.png)

And here are the results    

our implementation:
![image](ourResult.png)

other group's implementation:
![image](theirResult.png)

For Snippet 1, I believe there is a way of resolving the issue by making small code changes within 10 lines. One way we can do this is to keep track of the index of the backticks and compare them to the index of open or closed bracket to determine whether we want to keep the link or not. 

For Snippet 2, I believe there is also a way of resolving the issue by making small code changes. One way of doing so it to keep updating the the index of the closed parenthesis until we get to the last closed parenthesis. 

For Snippet 3, It's a bit more difficult but I think it can also be done within 10 lines. To fix the spaces we can just write an if-statement to check if the character is space. As for the closing parenthesis issue we can do a check so that if we reach an opening bracket without finding a closed parenthesis it'll just not get added to the returned arrayList. 


