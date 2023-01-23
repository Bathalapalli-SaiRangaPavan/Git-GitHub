# Git Clone
- git clone is used to clone an existing repository into your local machine.
- When we clone a repository, all the files are downloaded to the local machine but the remote git repository remains unchanged.
- Making changes to this cloned repository and committing them on your local repository will not affect the remote repository in anyway. 
- These changes made on the local machine can be pushed to the repository anytime the user wants.
- Whenever working on a team, weather if it's in an open source project or a corporate setting, its always a good practice to create a new branch and start the changes from there.
- You cannot directly push your changes to the cloned repository unless you are added as the collaborator to that project by the project.
- It is always advised to create a separate branch, work on the changes in that branch and create Pull Request or Merge Request for merging feature branch changes to the master branch. 
- The Master branch holds the working copy of the work product and no changes are to be pushed to that branch unless properly reviewed & approved.
- For some open source projects, you canot directly clone and push your changes (contribute) in such cases we fork the project make changes and submit a PR to the original project.
- If its a public repository you can clone into local machine.
- If its a private repository you cannot clone it.

### Practical - Cloning an Existing Repository 

```
git clone https://github.com/Bathalapalli-SaiRangaPavan/Software-Installation.git
```
```
ls -la
```
You can see Software-Installation and go inside it. 
Create a new branch & Switch 
```
git checkout -b feature-01
```
Edit an existing file and add it to staging.
```
git add <edited file>
```
Commit the changes to Local Repository 
```
git commit -m "modified file"
```
Push the changes to Remote Repository 
```
git push origin feature-01
```
Check remote & Local Branches 
```
git branch -a
```
