# CLDQ - CSE LABS "DONE QUICK"
This lab report is all about speeding up our work on the command line. To do so, we'll be using a bunch of keyboard shortcuts and some built-in command
line functions to optimize our work flow on the command line. For the purpose of hands on learning, we'll be executing the commands on a sample repository `lab7`.\
For setup, we'll be forking the `lab7` repository to our GitHub account.\
Get the stopwatches out!
## 3... 2... 1... GO!
### 1. Logging into `ieng6` server
We start off by logging into our course specific server. Command to be run to log into the server is as follows:-
```bash
  $ ssh cs15lwi23ajk@ieng6.ucsd.edu
```
SSH is a remote administration protocol which allows users to access, control and modify remote servers over the internet. The command mentioned above allows us to securely log into the `ieng6` server.\
![Image](S1.jpg)
```bash
  Keys Pressed: <Control + R> "ssh" <enter>
```
For this, I used the history function. Typing out ssh brought the login command right up and since I have the ssh passkey set, all I had to do was press `<enter>` and I was in. Pretty simple!
### 2. Cloning the repository
We then move on to cloning the repository onto the `ieng6` server. Command to be run to clone the `lab7` repository onto the server are as follows:-
```bash
  $ git clone git@github.com:ArnavTalreja/lab7.git
```
The command mentioned above allows us to clone the forked repository onto the server. Since I have the ssh passkey set, I had to specifically use the ssh link to clone the repository in question. \
![Image](S2.jpg)
```bash
  Keys Pressed: "git clo" <tab> <command + V>
```
For this, I simply typed out `"git clo"` before hitting the `<tab>` key and allowing bash to auto-complete the command for me. I then pressed `<command + V>` to paste the link to the `lab7` repository I had copied to the clipboard earlier.
### 3. Compiling and running the code
Then, its onto running the tester to test the code given to us. The commands to be run to compile and run the code are as follows:-
```bash
  $ javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-2.2.jar *.java
  $ java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-2.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
The first command compiles all the java files in the current working directory while the second command runs the junit tests in the `ListExamplesTests.java` file. \
![Image](S3.jpg)
```bash
  1. Compiling the code:-
    Keys Pressed: <Control + R> "jav" <enter>
  
  2. Running the code:-
    Keys Pressed: <Control + R> "java -c" <right arrow> "Li" <tab> "Te" <tab> <enter>
```
For this, I used the history function again. Typing `"jav"` brought up the command to compile all the java files in the repository at once. All I had to do was hit `<enter>`.
I did the exact same thing for pulling up the command to run the code. All I did was type `"java -c"` and once again, all I had to do was hit `<enter>`.
### 4. Fixing the errors
Compiling and running the tester displayed error messages which looked like the following:-
![Image](S4.jpg)


So, the next step was to open up and edit the `ListExamples.java` file and fix the bugs. For doing so, I used the `nano` command. I then used the `Where is` function on the `nano` screen to navigate to the required lines. The command to open `ListExamples.java` using nano is as follows:-
```bash
  $ nano ListExample.java
  $ <Control + W> "index1"
  $ <Control + W> "add"
```
The first command opens the file `ListExample.java` in the nano text editor. The second and the third commands use the built-in `Where is` function in nano to find the strings you type. \
![Image](S5.jpg)
```bash
  Keys Pressed: "nan" <tab> "Li" <tab> ".java" <enter> <Control + W> "index1" <enter> <left> <left> <left> 
                <left> <left> <fn + delete> "2" 
```
To fix the first bug, I used the `Where is` function on the `nano` screen to navigate to line 42 where I switched `index1` with `index2`.
![Image](S9.jpg)
```bash
  Keys Pressed: <Control + W> "add" <left> <left> <left> <left> <fn + delete> <fn + delete> <fn + delete>
```
To fix the second bug, I used the `Where is` function on the `nano` screen to navigate to line 15 where I changed `result.add(0,s);` to `result.add(s);`.
I then saved the file and exited nano.
```bash
  Keys Pressed: <Control + x> "Y"
```
### 5. Compiling and running the code (AGAIN!)
Basically repeated step 3. here and everything was running smoothly! The commands to be run to compile and run the code are as follows:-
```bash
  $ javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-2.2.jar *.java
  $ java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-2.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
The first command compiles all the java files in the current working directory while the second command runs the junit tests in the `ListExamplesTests.java` file. \
![Image](S3.jpg)
```bash
  1. Compiling the code:-
    Keys Pressed: <Control + R> "jav" <enter>
    
  2. Running the code:-
    Keys Pressed: <Control + R> "java -c" <right arrow> "Li" <tab> "Te" <tab> ".java" <enter>
```
### 6. Pushing the updated file to GitHub
We use the `git add` and `git commit -m` commands to push the updated file onto GitHub. The commands are as follows:-
```bash
  $ git add ListExamples.java
  $ git commit -m 'Updated ListExamples.java'
```
The first command adds the file `ListExamples.java` to the list of files to be posted to the repository when the commit is made, while the second command makes the commit. The `-m` modifier in for `git commit` allows us to add a description of the commit for future reference! \
![Image](S7.jpg)
```bash
  1. Adding ListExamples.java to the files that are to be commited:-
    Keys Pressed: "git add" "Li" <tab> ".java" <enter>
  
  2. Commit:-
    Keys Pressed: "git commit -m 'Updated ListExamples.java' <enter>
```

