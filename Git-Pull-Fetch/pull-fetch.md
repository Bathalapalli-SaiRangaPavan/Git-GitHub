- Let's say once the feature branch is merged to master, master has a new modified file. Our local repository is unaware of this change as the merging happend directly in the remote repo. In order to get the latest changes from the remote repository we can use git pull or git fetch. 

# Git Fetch 
- git fetch pulls all new commits from the desired branch and saves it in your local repository. 
- So, your local repository is in sync with your remote repository is in sync with your remote by one or few commits. 
- If you need to reflect these changes in your target branch, git fetch should be followed with a git merge. 

# Git Pull
- git pull does both fetch and merge.

```
git pull = git fetch + git merge
```
