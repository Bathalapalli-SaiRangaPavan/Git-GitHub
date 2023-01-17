## Create a Local Git Repository

- Create a new project folder in your local file system name. My folder name is my-repo. 

```
 mkdir my-repo 
```
- Go into this newly created project folder and add a local git repoitory to the project

```
cd my-repo
```

```
git init
```

- Now this project can be managed using Git. 
- Git creates a hidden folder .git in the project whenever you do git init.

```
ls -l
```

- The .git folder contains all the information that is necessary for your project in version control and all the information about commits, branches, remote repository, address etc. All of them are present in this folder. It also contains a log that stores your commit history so that you can roll back to history. 
- Without .git the project will not be managed by git, that means you cannot perform any git operations. 

### Create a sample file 

```
vi file1.txt
```
- It will open the vi editor. Once it opens Press i and give whatever u want to.  I am taking example of Hello Git & GitHub 

```
Hello Git & GitHub
```

- save the file using Press Esc then :wq  (if ur using vi editor)

To check the status of the file

```
git status
```
untracked file - It is in working area. 

### Add Files to stagiing area using git add

- The staging area is there to keep track all the files which are to be committed. Any file which is not added to the staging area will not be committed. This gives the developer control over which files need to be committed at once. 
- git add lets you add files to staging area

```
git add file.txt
```
check the status of the file

```
git status
```
- This status shows that file1.txt is ready to be committed to the local repository. 
- In case you want to add multiple files you can use git add file1 file2 git add file3 (or) git add . (or) git add -A (or) git add *

### Git Config 

- git config command configures your Git installation. 
- Using this command you can describe the repository behavior, preferences, and user information. 
- The global config resides at ~/.git config in the user's home directory. While the repository specific config at .git/config inside the project. For more info use below command.

```
git config --help 
```
- Before we commit any changes to the repo, we need to set the user name and email address for the git user to as to make git aware of who has made the commits. 
- Run below commands to set the configuration.

give your name and email
```
git config --global user.name "Sai Ranga Pavan"  
```
```
git config --global user.email "Bathalapalli.sairangapavan@gmail.com" 
```

To edit 

```
git config --global --edit
```

to check weather the user name and email are matching 

```
git config --global --list
```

### Move the file from staging to Local repository. Committing the code

- Committing is the process in which the code is added to the local repository. 
- Each commit has an associated commit message explaining why a particular change was made. Commit messages capture the history of your changes. So other contributors can understand what you have done and why.
- To give commit message use -m flag 
```
git commit -m "my first commit"
```
- If you do not use -m, git will bring up an editor for you to write the commit message.
- Each time you commit changes to the repository, Git creates a new SHA (20 byte number) that describes that state. 

To see commit history 
```
git log --stat 
```
