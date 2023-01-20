# Git Remove


Create a directory named git-test-remove

Create a file named file1.txt 
```
git init
```
write content in file1 and save it 
- Example: file1 line1

Move to staging area
```
git add . 
```
Move to local repository 
```
git commit -m "added file1"
```

Create a file named file2.xt and write content in file2 and save it 
- Example: file2 line1

Move to staging area
```
git add . 
```
Move to local repository 
```
git commit -m "added file1"
```
Check commit history
```
git log 
```
Now u can see 2 commits 

Remove file1. txt 
```
rm file1.txt 
```
Now file1.txt got deleted
```
git ls-files
```
You can able to see file1
```
git add file1.txt
```
```
git status
```
Now its in staging area
```
git commit -m "removed file1"
```
There are 3 commands involved to delete a file (rm file1.txt, git add file1.txt, git commit -m "removed file1")


### git rm 

Remove file2.txt 
```
git rm file2.txt
```
```
git ls-files
```
u cannot see file2
```
git commit -m "removed file2"
```
when you use git rm only 2 commands involved (git rm, git commit -m "removed file2"

# Git Renaming 

Create a new file named file3.txt. write content in file3.txt and save it

- Example - file1 line1

### Now i want to change my filename from file3.txt to file4.txt

```
mv file3.txt file4.txt
```
Move to staging area
```
git add . 
```
Move to local repository 
```
git commit -m "Renamed file3 to file4"
```
```
git ls-files
```
you can see file4.txt
```
git log 
```
There are 3 commands involved to rename a file (mv file3.txt file4.txt, git add ., git commit -m "Renamed file3 to file4")

Now i want to change my filename from file4.txt to file3.txt 
### git rm 
```
git mv file4.txt file3.txt
```
```
git commit -m "Reverted the name from file4.txt to file3.txt"
```
```
git ls-files
```
you can see file3.txt
```
git log 
```
There are 3 commands involved to rename a file (git mv file4.txt file3.txt, git commit -m "Reverted the name from file4.txt to file3.txt")


