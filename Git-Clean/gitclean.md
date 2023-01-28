# Git Clean 
- Git Clean command is used to clean the untracked files in the repository.

### Practical 

Create a file named new.txt add content
```
hello
```
Create one more file named file.txt add content
```
hi
```
Check the status
```
git status
```
when u check the status its untracked.
- To remove files  we use git clean 
```
git clean -n
```
git clean -n command asks preview.
```
git clean -f
```
git clean -f command will directly remove files
