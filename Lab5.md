# Week 10 Lab Report 
## Exploring more Grep commands 

This lab report will showcase the usage of different types of grep commands with some of my own example files. All of the commands were executed on a Unix-based operating system. 

## Sources
- [ChatGPT](https://chat.openai.com/chat)
- [GeeksForGeeks](https://www.geeksforgeeks.org/)

## grep -E - Using Extended Regular Expressions
The grep -E command allows the usage of extended regular expressions. Here's an example usage:
```
$ grep -E '\b[A-Z][a-z]+\b' sample.txt
John Doe
Jane Smith
```
This command will look for lines in the file sample.txt that have words with an uppercase letter and one or more lowercase letters as part of their word beginnings. By indicating word boundaries with the b metacharacter, only complete words are matched. These words are printed to the console on two lines in this example.

## grep -v - Inverting the Search
The grep -v command inverts the search, i.e., it will print all lines that do not match the given pattern. Here's an example usage:

```
$ grep -v 'error' logfile.txt
2023-03-12 15:43:23 INFO Connection established
2023-03-12 15:43:24 DEBUG Processing request
2023-03-12 15:43:25 INFO Request completed successfully
```

This command will print all lines in the file logfile.txt that do not contain the word "error". In this example, three lines are printed, which do not have the word "error" in them.

## grep -i - Case-Insensitive Search

The grep -i command performs a case-insensitive search, i.e., it will match patterns regardless of their case. Here's an example usage:

```
$ grep -i 'chicago' cities.txt
Chicago
chicago
CHICAGO
```
This command will print all lines in the file cities.txt that contain the word "chicago", regardless of the case. In this example, three lines are printed, which have the word "chicago" in different cases.

## grep -m - Limiting the Number of Matches
The grep -m command limits the number of matches to a specified number. Here's an example usage:
```
$ grep -m 2 'password' users.txt
john:x:1000:1000:John Doe:/home/john:/bin/bash
jane:x:1001:1001:Jane Smith:/home/jane:/bin/sh
```
This command will print the first two lines in the file users.txt that contain the word "password". In this example, only two lines are printed, even though the file contains more lines that match the pattern.

## Conclusion
Testing these grep commands using ChatGPT and my own terminal made me understand the concept far better.
