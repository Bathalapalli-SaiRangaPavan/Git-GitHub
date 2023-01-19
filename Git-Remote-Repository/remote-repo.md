# Remote Repository in GitHub 

- Files/Project which you have created earlier stages within your local repository. If you want to share these files with developers or team members to collaborate, you need to push the local repo to a remote repository like Github. 
-  After you have a remote repository created/set up, you upload (push) your files and revision history to it. After someone else makes changes to a remote repository, you can download (pull) their changes into your local repository. 

## Create a Remote Repository 

- Give a Repository Name, Description and make the repository public. 
- Click on Create Repository 
- Once created, github will prompt to create a new repo to add a repo we have created locally. 
- In our case, since we have already created local repository. We can push it directly. 
- Git will also show us the instructions to be followed to push our local repository. 

Execute below commands in Local Repository 

```
git remote --help
```

- Add the remote repository by running (https://github.com/your-user-name/testrepo.git)

```
git remote add origin https://github.com/Bathalapalli-SaiRangaPavan/Git-GitHub.git
```

- remote command adds a remote repository to the current repository.
- origin is an alias to the remote repository.
- We assign an alias so we won't have to write out the URL of the remote repository every time we want to work with the remote repo.
- While origin is the alias that most people prefer to use, it is not a standard and we can use own naming conventions.


Check the remote URLs and their aliases.  
```
git remote -v
```
Invoking git remote with the -v option will print the list of bookmarked repository names and additionally, the corresponding repository URL. The -v option stands for "verbose". 

  
## Push the files from Local Repository to Origin 

```
git push -u origin master
```
- git push pushes our local repo changes to the added remote repo. 
- Origin represents the remote repo and master is the branch you want to push to. 
- Git will Prompt for your credentials during push.
  
 ### As ur using [https](https://github.com/<your-user-name>/testrepo.git)
 
 There are 2 ways by using Username, Password & PAT(Personal Access Token)
  ```
  bsrp@gmail.com<Give Ur github username>
  admin12345<Give ur github Password>
  ```
  
 2nd way - Using PAT (Personal Access Token). To generate the (Personal Access Token) follow below steps. 
  
  - Go to your Github account 
  - Click on (Profile)
  - Click on (Settings) 
  - Click on (Developer Settings) 
  - Click on (Personal Access Token) 
  - Give (your Github Password)
  - Name (git-pat)  <give any name> 
  - Expiration (3 Days) <give according to ur convinience>
  - Select the following according to your need. For example i selected (repo) )
  - Click (Generate token) 
  - Copy the token once its generated. Once u close the token wont be available
 
  Execute below command in Local Repsoitory 
  
  ```
  b6eme6inskhw4fzefvpy
  ```
  Now u can see it pushed ur files from Local to Remote Repository/Origin
  
 ### If your using ssh 
  
  
```
git remote add origin git@github.com:Bathalapalli-SaiRangaPavan/Git-GitHub.git
```
- Give yours (git@github.com:your-user-name/testrepo.git)
 
 Execute below commands
  ```
  ssh-keygen
  ```
 - three times press Enter 
  ```
  ls -l /root/.ssh
  ```
  u can see id_rsa, id_rsa.pub, known_hosts, authorizedkeys
  ```
  cat /root/.ssh/id_rsa.pub
  ```
  
- copy the public key 
  
- Go to your Github account 
- Click on (Profile)
- Click on (Settings) 
- Click on (SSH AND GPG KEYS)
- Title - git-ssh <give any name>
- Key: Paste id_rsa.pub copied 
- Click (Approve)
  
```
git push -u origin master 
```
- Now u can see it pushed ur files from Local to Remote Repository/Origin

- We can omit origin and -u master parameters from the git push command with following two git configuration changes. 
  
- git config remote.pushdefault origin 
- git config push.default current

- The first setting saves you from typing origin everytime. 
- With the second setting, git assumes that the remote branch on the github side will have the same name as your local branch.
  

  
  
References: 
- Browse: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
- Browse: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/reviewing-your-ssh-keys
 
