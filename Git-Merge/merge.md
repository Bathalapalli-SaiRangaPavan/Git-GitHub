# Git Merge


### Practical - Lab

- Step 1 - Create a directory named git-statsh-merge
- Step 2 - Once u created do git init to initialize the repository
- Step 3 - Create a file named file1.txt inside the directory. write content in main.py
Example 
```
print(Hello Git-GitHub)
```
when u do git status its in working area. Move to staging area
```
git add .
```
Move from staging area to Local repository. 
```
git commit -m "commit in master branch"
```

- Step 4 - Create a branch named dev and switch to dev branch  
```
git checkout -b dev
```
```
ls
```
you can see main.py in dev branch.

Modify main.py in feature branch. Add Hello DevOps World
```
print("Hello Git-GitHub")
print("Hello DevOps world")
```
Now move from working area to local repository 
```
git commit -a -m "changed in dev branch"
```
Step 5 - Checkout to master 
```
git checkout master 
```
when you are in master branch whatever you did changes in the dev branch is not seen in master branch. To see u need to merge. 

### Git Merge 
```
git merge dev
```
Now whatever is changed in dev branch is appeared in the master branch.


