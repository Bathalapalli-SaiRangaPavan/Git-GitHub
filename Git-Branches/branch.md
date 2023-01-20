# Branches 

- Git Branch is about maintaining the separate line of development. The default branch is master/main.
- Git lets you branch out from the original code base. This lets you more easily work with other developers and gives you a lot of flexibility in  your workflow. 
- Lets say you need to work on a new feature for a website. You create a new branch and start working. You haven't finished your new feature, but you get a request to make a rush change that needs to go live on the site today. You switch back to the master branch, make the change, and push it live. Then you can switch back to your new feature branch into the master branch, and both the new feature and rush change are kept. 
- Basically, a branch is the isolkated and independent line of developing the feature. 
- Assume the middle line as the master branch where the code is stable, working & updated. Then assume a developer-1 is cutting a branch from the master branch. Similarly developer-2 is assigned to develop feature-2 and he is cutting a branch from the master branch. When both of them are done with their changes they merge their changes to the master and these feature branches can be safely deleted. 
- Lets assume the code base is set of four files called file-1, file-2, file-3, file-4. So, when developer-1 is taking the branch from master to develop feature-1. Assume file1 and file3 are going to be changed for the development. So, the developer can safely commit the changes on both files into the master branch. Viceversa, whendeveloper-2 is taking the branch from maser to develop feature-2. Assume file-2 and file-4 are going to be changed for the development. 

### Branch

Check what branch your in 
```
git status
```
List all of the branches in your local repository. The current local branch will be marked with an alterisk.
```
git branch --list
```
To see remote branches

```
git branch -r
```
To see all local and remote branches 

```
git branch -a
```


create a new branch 
```
git branch dev
```
Switch to dev branch 
```
git checkout -b dev
```
Check HEAD (HEAD points out the last commit in the current checkout branch
```
git show head
```
For making commits in dev branch, you should be in dev branch already.
