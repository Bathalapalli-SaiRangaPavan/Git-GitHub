# Git Revert 

-  Revert some existing commits
-  git revert is used to record some new commits to reverse the effect of some earlier commits

### Scenario 
You've committed twice to master and it’s bad. You've pushed and other people have your bad changes.You want to undo it. You just want to put it all back how it was.

#### Practical 

Step 1 - Cretae a file named testing.txt and add content and save it.
```
hello this is to test
```
Step 2 - When u check git status it is untracked move it to staging area, local repository and push it to remote repository
```
git status
```
```
git add .
```
```
git commit -m "testingt"
```
```
git push origin master
```
When u go to remote repository, you can see testing.txt. Now i want to revert back from the remote repository. Execute below commands in local repository.
```
git log 
```
Take the latest commit id

```
git revert <commit id>
```
it opens (i -> reverted... )at start u give the content let it be

```
git push origin master
```
you can see its deleted in the remote repository.
