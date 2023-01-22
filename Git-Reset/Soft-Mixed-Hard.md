### Git Reset

- Git reset will take your branch back to certain point in the commit history, but there are 3 different levels to this. 


# git reset --soft :  uncommit changes, changes are left staged (index)

Create a directory 

```
mkdir git-reset-example
```
Go into the newly created project folder and add a local git repository to the project 

```
git init
```
Create a file named main.py either in vscode or using vim editor 


```
def sum(a,b):
    return a+b

result = sum(3,5)
print(result)
```
check the status

```
git status
```
Untracked files: main.py 

Move it to staging area

```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sum of 2 numbers"
```

Check logs

```
git log
```

Add Subrtraction function and commit 

```
def sum(a,b):
    return a+b

def sub(a,b) 
    return a-b
    
result = sum(3,5)
print(result)
```

check the status

```
git status
```
Untracked files: main.py 

Move it to staging area
```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sub of 2 numbers"
```

Check logs

```
git log --oneline 
```
You can see 2 commits. 


```
git reset --soft HEAD~1
```

```
git log --oneline 
```

```
git status
```

You can see 1 commit. sub of 2 numbers commit removed and now its in staging area.




# git reset --mixed (default) : uncommit + unstage changes, changes are left in working tree.

Create a file named main.py either in vscode or using vim editor 

```
def sum(a,b):
    return a+b

result = sum(3,5)
print(result)
```
check the status

```
git status
```
Untracked files: main.py 

Move it to staging area

```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sum of 2 numbers"
```

Check logs

```
git log
```

Add Subrtraction function and commit 

```
def sum(a,b):
    return a+b

def sub(a,b) 
    return a-b
    
result = sum(3,5)
print(result)
```

check the status

```
git status
```
Untracked files: main.py 

Move it to staging area
```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sub of 2 numbers"
```

Check logs

```
git log --oneline 
```
You can see 2 commits. 


```
git reset --mixed HEAD~1
```

```
git log --oneline 
```

```
git status
```

You can see 1 commit. sub of 2 numbers commit removed and now its in working area.







# git reset --hard : uncommit + unstage + delete changes, nothing left 

Create a file named main.py either in vscode or using vim editor 

```
def sum(a,b):
    return a+b

result = sum(3,5)
print(result)
```
check the status

```
git status
```
Untracked files: main.py 

Move it to staging area

```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sum of 2 numbers"
```

Check logs

```
git log
```

Add Subrtraction function and commit 

```
def sum(a,b):
    return a+b

def sub(a,b) 
    return a-b
    
result = sum(3,5)
print(result)
```

check the status

```
git status
```
Untracked files: main.py 

Move it to staging area
```
git add main.py 
```
check the status

```
git status
```
move it to local repository from staging area

```
git commit -m "sub of 2 numbers"
```

Check logs

```
git log --oneline 
```
You can see 2 commits. 


```
git reset --hard HEAD~1
```

```
git log --oneline 
```

```
git status
```

You can see 2nd commit sub of commit is removed including the def sub(a,b) deleted in the file.



### A -> B -> C -> D  HEAD is now at D

- git reset --soft A : Branch head is now pointing at A. Staging will contain all of the files that were committed in B,C,D
- git reset --mixed A: Branch head is now pointing at A. All of the files that were committed in B,C,D are now in working area. 
- git reset --hard A: Branch head is now pointing at A. All of the files that were committed are deleted off.












