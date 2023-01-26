- Git sees every file in your working copy as one of three things.
1. Tracked - A file which has been previously staged or committed.
2. Untracked - A file which has not been staged or committed.
3. Ignored - A file which git has been explicitly told to ignore. 
- Git is meant to store only source files and never the generated files or the personal config files with confidential information.
Any generated code/binaries should not be committed due to following reasons.
- The generated files can be reacted at any time on the client side and may need to be created in a different form. So it is a waste of time and space to store them in git. 
- The generated files are often larger than the original source files themselves. Putting them in the repo means that everyone needs to download and store those generated files, even if they are not using them. This increased the clone times.
- Git usually stores only changes made to the file in the subsequent commits by using diff algorithm. Binary files don't really have good diff tools. So git will frequently just need to store the entire file each time it is committed. 

### Practical

- Step 1 - Create a folder named git-gitignore-test (mkdir git-gitignore-test)
- Step 2 - Initialize the local repository (git init)
- Step 3 - Example - Create a file called testing.txt
- Step 4 - Add some contents to the file (This is my personal file)
- Step 5 - Create few more files (touch .project, touch .classpath) 
Git shows the file as untracked. But these are personal preferences and should not be committed.
### .gitignore 
- Step 6 - Create a file named .gitignore 
We can add this file to .gitignore file to instruct git to ignore the changes done to testing.txt, .project, .classpath and not to track. 
Check the status 
```
git status
```
when u do git status u can see testing.txt, .project, .classpath, .gitignore
```
vi .gitignore
```
```
new.txt
.classpath
testing.txt
```
```
git status
```
you can see .gitignore file. We should commit .gitignore file so others can use it and update it with their own to be ignored content like files generated code, log files and IDE specific. 

```
git add .gitignore
```
```
git commit -m "updated ignore files"
```
```
git push origin master
```
you can see .gitignore file in the remote repository. 

