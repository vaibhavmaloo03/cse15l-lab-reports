# Week 7 Lab Report
## Using the command-line more effectively
---
## Step 4
To log into the ieng6 account, I simply used the keys
```
<up><up><enter>
```
<img width="626" alt="Screenshot 2023-03-13 at 5 39 39 AM" src="https://user-images.githubusercontent.com/122576282/224704510-66d40460-b290-4f3f-b3fa-55a81dcd007a.png">

This has the command `ssh cs15lwi23auc@ieng6.ucsd.edu`. This command was used before and since my device was already added as a key, I logged in instantly.
## Step 5

To clone the repository and store it in the file `grader-review-vaibhavmaloo03`, I had my git repositories link on my clipboard and I used
```
git clone <ctrl-V><enter>
```
<img width="567" alt="Screenshot 2023-03-13 at 5 52 03 AM" src="https://user-images.githubusercontent.com/122576282/224707127-8bae62c5-4fac-4912-a175-888bb02f3e8b.png">

My clipboard had this link stored: `git@github.com:vaibhavmaloo03/grader-review-vaibhavmaloo03.git`. This helped me speed my process by not going to my GitHub account and actually looking for the link.

## Step 6

To run the JUnit tests, I used the up arror to search my log for the code.
```
cd grader-review-vaibhavmaloo03
<up><up><up><up><up><up><up><up><up><up><enter>
```
<img width="1440" alt="Screenshot 2023-03-13 at 6 12 18 AM" src="https://user-images.githubusercontent.com/122576282/224711727-81dcf53f-391a-4c77-986c-c0dee197967a.png">

This had the code `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java && java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`

This resulted in failure

<img width="593" alt="Screenshot 2023-03-13 at 6 13 27 AM" src="https://user-images.githubusercontent.com/122576282/224712057-a2a06cd8-e1a9-428e-893d-ea13437fa7dc.png">

## Step 7
After discussing with some of my friends, I figured that a fast way to do this step would be to copy an already edited(correct) file from the parent directory. 
To do this I typed
```
cp ../ListExamples.java
```
This copied the "correct" code and pasted it in the directory 
`/home/linux/ieng6/cs15lwi23/cs15lwi23auc/grader-review-vaibhavmaloo03`


## Step 8
Since I had just run the JUnit tests one step back. All I had to do is 
```
<up><up><enter>
```
This ran the same JUnit compilation and run code.
This time however, it passed both tests

<img width="566" alt="Screenshot 2023-03-13 at 6 26 26 AM" src="https://user-images.githubusercontent.com/122576282/224715228-f9485621-0b18-4917-a16b-314a19478658.png">

## Step 9
This step took the shortest time since these commands were shorter
```
git add
git commit -m "hello"
git push
```
The commit -m command helped skipping the vim editor step that requires an additional message on the command line

<img width="947" alt="Screenshot 2023-03-13 at 6 29 42 AM" src="https://user-images.githubusercontent.com/122576282/224716063-78f770ba-2386-4086-9079-4bcca6364412.png">


### Conclusion
I did decrease the time for the whole process by a factor of 2. This was a good learnign experience and truly taught me how efficiently I can write commands on the terminal.



