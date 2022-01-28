# Lab Report 2: Debugging

A fundamental aspect of developing software is making sure that the behavior of our code is consistent with what we defined it to be as "normal" In the following report, I will talk about some changes we made in the provided MarkdownParse.java file we recieved in order to ensure proper behavior

# First Issue
## First code change:

![image](Lab2change1.PNG)

## Failure-inducing Input
[test1.md](test1.md)


## Symptom of bug
![image](Lab2symptom1.PNG)

## Bug-Symtpm-Failure-inducing input relationship

The bug that was shown in the picture above was an infinite loop. We Initially ofund this because we noticed that we were recieving no output when running `java MarkdownParse test1.md`. We decided to add a print statement to find out what was going on, and we noticed an infinite loop which made us realize we needed to add a break statement in case the next open bracket wasn't found in order to avoid the infinite repeating loop.