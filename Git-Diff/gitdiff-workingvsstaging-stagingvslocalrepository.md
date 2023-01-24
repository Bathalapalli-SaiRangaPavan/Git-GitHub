# Git Diff 
- git diff command shows changes between commits, branches and more. 
- git diff command shows the differences between a file in the staging area and the edits made to that file that currently exist in the working tree. 
- git status and git diff should frequently be used as they give you information about your current working state and what git is aware of. 
- Compare changes to file in working area to that staging area 
```
git diff
```
- Compare modified files that are on the staging area that are ready to be committed 
```
git diff --staged
```
- Show the diff between two specific commits 
```
git diff <commitid> <commitid2>
```
### Practical 
Step 1 - Create a directory named git-diff-test
Step 2 - Add a git local repository to the project 
```
git init 
```
## Difference between Working area & Staging area 
Step 3 - Create a file named main.py under git-diff directory. Write some content and save it 
```
def add(a,b):
    return a+b
```
Step 4 - Move it to staging area
```
git add .
```
Step 4 - Update content in main.py 
```
def add(a,b):
    return a+b
def sub(a,b):
    return a-b
```
```
git status
```
Now u can see the file is untracked

```
git diff
```
When u execute git diff between working area and staging area u get ouput like below. You can see +def sub(a,b) n staging area newly added

```
diff --git a/main.py b/main.py
index f083797..029e03a 100644
--- a/main.py
+++ b/main.py
@@ -1,2 +1,5 @@
 def add(a,b):
     return a+b
+def sub(a,b):
+    return a-b
+    
\ No newline at end of file
```
## Difference between staging area that are ready to be committed 

Step 5 - Move it to the local repository. 
```
def add(a,b):
    return a+b
def sub(a,b):
    return a-b
```
```
git commit -a -m "sub function added"
``` 
Step 6 - Update content in main.py and move it to staging area
```
def add(a,b):
    return a+b
def sub(a,b):
    return a-b
def mul(a,b):
    return a*b
```
```
git add . 
```
```
git diff --staged
```
When u execute git diff --staged difference between staging area and local repository u get ouput like below. You can see +def mul(a,b) in staging area newly added

```
diff --git a/main.py b/main.py
index 029e03a..35efd76 100644
--- a/main.py
+++ b/main.py
@@ -2,4 +2,5 @@ def add(a,b):
     return a+b
 def sub(a,b):
     return a-b
-    
\ No newline at end of file
+def mul(a,b):
+    return a*b
\ No newline at end of file
```


