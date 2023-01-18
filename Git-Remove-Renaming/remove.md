### Git Remove


Create a directory named git-test-remove

Create a file named file1.txt 

```
git init
```
write content in file1

```
file1 line1
```
Move to staging area

```
git add . 
```

Move to local repository 

```
git commit -m "added file1"
```

Create a file named file2.xt 


```
git init
```

write content in file2

```
file2 line1
```
Move to staging area

```
git add . 
```

Move to local repository 

```
git commit -m "added file1"
```

```
git log --oneline
```

Now u can see 2 commits 

### Remove file1. txt 

```
rm file1.txt 
```

Now file1.txt got deleted

```
git ls-files
```

You can able to see file1, file2

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

when u use git rm only 2 commands involved (git rm, git commit -m "removed file2"

