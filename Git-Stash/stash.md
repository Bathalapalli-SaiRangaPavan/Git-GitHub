# Git Stash

### Consider a scenario 
- You are working on a feature branch to implement a new feature.You have made lot of changes to the code in that branch but they are not yet ready to be committed. Now, you recieved a request to fix a bug in the master branch and you are to switch to master branch to fix the issue. But, you don't want to lose your work in the feature branch. 

### Solution 
- In this case, git stash command will allow you to save your local modifications and revert back to the working directory that is in line with the most recent HEAD commit. 
- Git stash takes the present state of the working file and puts in on the stack and gives you back a clean working file. Now you are free to switch to other branch. So, git stash lets us preserving the changes and restore them whatever needed. 
- Git stash apply will restore all the saved changes to the working area again. 
- when you are done with the stashed element or want to delete it from the directory, run the git stash drop command. It will delete the last added stash item by default. 

### Practical - Lab

- Step 1 - Create a directory named git-statsh-test. (mkdir git-stash-test)
- Step 2 - Once u created do git init to initialize the repository. (git init)
- Step 3 - Create a file named file1.txt inside the directory. write content in file1.txt Example: file1 line1 

when u do git status its in working area. Move to staging area
```
git add .
```
Move from staging area to Local repository. 
```
git commit -m "file1 in master branch"
```

- Step 4 - Create a branch named feature and switch to feature branch  
```
git checkout -b feature
```
```
ls
```
you can see file1.txt in feature branch.

Modify file1.txt in feature branch 
```
file1 line1
file2 line2 
file1 line3
```
Now its in working area. I have got a requirement to fix bug in master branch. You execute below command and switch to master branch
## Git stash 

```
git stash save "added few lines" --include-untracked
```
```
git stash list
```
output - stash@{0}: On feature: added few lines

switch to master branch
```
git checkout master
```
- Step 5 - Create file3.txt move to local repository 
- Step 6 - Now i want to bring back al; the changes i saved in feature branch. switch to feature branch 
```
git checkout feature
```
Below commad shows the difference 
```
git stash show stash@{0} --patch
```
To start working on the file where u stopped. 
```
git stash apply
```
To delete the stash 
```
git stash clear
```
It disappears 
```
git stash list 
```

Note: If you are commited files in feature branch, if you want to go and start working in master branch execute below command.

```
git stash save "you give your stash message"
```
```
git stash push -m "stash message"
```
To apply and delete stash 
```
git stash pop 
```

