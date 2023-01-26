# Version Control System 

- Version Control also known as source control is the process of tracking and managing the changes to files over time. 
- It enables multiple people to simultaniously work on a single project. Each person edits his or her own copy of the files and chooses when to share those changes with the rest of time.
- These systems are critical to ensure everyone has access to the latest code. As development gets more complex, thereis a bigger need to manage multiple versions of entire products.
- Version Control gives access to historical versions of your project. If you make a mistake you can roll back to a previous version. You can reproduce and understand a bug report on a past version of your software. 
- You can also undo specific edits without losing all the work that was done in the meanwhile. 
- For any part of a file, you can determine when, why & by whom it was ever edited. 

## Why Version Control System?
1. Track history/Stored versions
2. Collaboration - Without VCS in place, you're probably working together in a shared folder on the same set of files. 
3. Track Changes - Who, What, When, Why, How
- Who created / who changes / who committed changes 
- What files they changed
- When was the last commit done to repository
- Why did they change
- How to contact who did
4. Roll backs & Reverts

### Central Version Control System vs Distributed Version Control System 

- The main difference between Centralized Version Control System vs Distributed Version Control System is the number of repositories. 

#### Central Version Control System
- In Centralized Version Control, there is just one repository.
- In Centralized Version Control System, the central server stores all the data. Each user gets his or her own working copy, but there is just one central repository. As soon as you commit, it is possible to your co workers to update and to see your changes. 
- If the central server gets crashed, there is a high chance of losing the data. SINGLE POINT OF FAILURE
- For every command, Central Version Control System connects the central server which impacts speed of operation. 
- Example: SubVersion 

#### Distributed Version Control System 
- In Distributed Version Control System, each user gets his or own local repository and a remote repository for all 
- After you commit to the local repository, others have no access to your changes to the central repository.
- If other users want to check your changes they will pull the updated central repository to their local repository and they update in their local copy. 
- Even if the main server crashes, code that is the local systems can be used to restore the data.
- Distributed Version Control System is fast compared to Central Version Control System because you don't have to connect the central server for every command. 
- Example:: Git

