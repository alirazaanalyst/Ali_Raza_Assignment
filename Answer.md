# Part 1 — Concepts & Theory

## Q1. Terminal basics 
## Q1.1 What is a terminal? How is it different from clicking through folders in a file explorer?
### ANS:  A terminal is a place where we type commands to tell the computer what to do. Unlike File Explorer, where we click on folders and files, a terminal lets us perform tasks by typing commands. It can make our work faster and easier, especially when using Git.


## Q1.2 Write the terminal command to: 

### (a) list all files including hidden ones     : ls -a
### (b) create a folder called project           : mkdir
### (c) move into that folder                    : cd "path"




## Q1.3 What does the cd .. command do? What about cd ~ ?
### ANS: cd ..  takes you back to your back directory , cd ~   takes you to home directory.







## Q2. Version control concepts 
## Q2.4 Explain what version control is in your own words. Give one real-world analogy (not Google Docs — pick your own).
## What is Version Control?

### Version control is a system that tracks changes made to files over time. It helps us see what has changed and restore an earlier version if needed.
### Real-world analogy: It is like saving different versions of a video game. If an update introduces a bug, you can return to an earlier version that worked correctly.

## Q2.5 What is the difference between Git and GitHub? Can you use Git without GitHub?
## ANS: Git is a tool that tracks changes in files on our computer, while GitHub is an online platform used to store and share Git repositories.
## Yes, we can use Git without GitHub because Git works locally on our computer.



## Q2.6 Name three features GitHub provides that Git alone does not
## ANS: 1. Online Repository Hosting: Store and share code online.
## 2. Pull Requests:Review and discuss code changes before merging.
## 3. Issue Tracking: Report bugs and manage project tasks.



## Q2.7 What is a repository? What is the difference between a local repository and a remote repository?

## A repository is a place where project files and their change history are stored.
## Local Repository: Stored on our computer.
## Remote Repository:Stored on an online platform like GitHub, where we can share our code with others.








## Q3.1 Git internals

## ANS: HEAD is a pointer that shows which commit we are currently working on.
## When we switch branches, HEAD moves to the latest commit of the selected branch.




## Q3.2 What is a .gitignore file? Write a .gitignore that ignores: all .log files, a folder called node_modules/ , and any file ending in .env .

## ANS: .gitignore file tells Git which files and folders it should ignore and not track.





## 2.2.6 Why did we commit A+B separately from C? When would you want to split commits this way?

## ANS: we commit A+B separately from C and we similar do this to keep similar modules togather make the commit history easier to understand.



## 2.3.6  In answers.md , answer: What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
## ANS: If we commit locally without pulling first, our branch may be behind the remote branch, causing conflicts when pushing.






## 3.1.9 In answers.md : Did this merge create a merge commit or was it a fast-forward? How can you tell?

## ANS: We can see in the terminal that it was a fast-forward merge. This means Git moved the branch pointer forward without creating a new merge commit.


## 3.2.15 

### 1. Why did this conflict happen?
## The conflict happened because both branches edited the same line in the same file (`team.txt`).

### 2. Would there have been a conflict if the branches edited different lines of `team.txt`?
## Usually, no. Git can merge changes made to different lines automatically.

### 3. Would there have been a conflict if one branch edited `team.txt` and the other edited `about.md`?
## No, because the branches edited different files, so Git can merge the changes automatically.








## 4.13 
## 1. Purpose of a pull request:It allows others to check and review our code before merging it into the main branch.

## 2. Two things a reviewer should check:
##   - If the code is working correctly.
##   - If there are any mistakes or bugs.

## 3. Merge commit vs. fast-forward merge: A merge commit creates a new commit to combine branches, while a fast-forward merge simply moves the branch forward without creating a new commit.







# Q.5
## 5.1 Scenario A. Ahmed creates a branch and changes line 10 of index.html . Sara creates different branch and changes line 1 of the same index.html . Both merge into there be a conflict? Why or why not?

## ANS:No, there will be no conflict because Ahmed and Sara changed different lines in the same file. Git can merge both changes automatically.


## 5.2 Scenario B. Ali edits style.css on his branch. Fatima edits main . Willapp.js on her branch. Both merge into main . Will there be a conflict? Why or why not?

## ANS:No, there will be no conflict because Ali and Fatima edited different files (style.css and app.js). Git can merge both changes automatically.



## 5.3 Scenario C. Dev A changes line 5 of config.py to DEBUG = True . Dev B changes line 5 of config.py to DEBUG = False . Both merge into main . Will there be a conflict? If yes, show exactly what the conflict markers would look like in the file

## ANS: Yes, there will be a conflict because both developers changed the same line to different values.The conflict markers will look like this:

## ```
## <<<<<<< HEADDEBUG = True=======DEBUG = False>>>>>>> dev-b
## ```

## - `<<<<<<< HEAD`: Shows the change currently in the main branch.
## - `=======`: Separates the two changes.
## - `>>>>>>> dev-b`: Shows the change from Dev B’s branch.

## The conflict must be resolved manually before merging.




## 5.4  Scenario D. 

## ANS:1. Open `index.html` and find the conflict markers.
## 2. Edit the file and keep the correct changes, removing the conflict markers.
## 3. Save the file.
## 4. Run these commands:

## ```
## git add index.html
## git commit -m "Resolve merge conflict"
## git status
## ```

## The conflict is resolved, and the merge is completed.







## 5.5  Scenario E.

## ANS:Yes, it is a good practice because `git pull` brings the latest changes from the remote repository to your local branch. If they skip it, they may work on outdated code and face merge conflicts later.





