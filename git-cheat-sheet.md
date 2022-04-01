# Git Cheat Sheet

## 1. General Information

* [**The Three States**](#three-states)
* [**Hidden files and folders**](#git-info)

## 2. Configuration

* [**Local Configuration**](#config-local)
* [**GitHub Configuration**](#config-github)



## 3. Branch

* [**List all branches**](#git-branch)
* [**Creating a new branch**](#git-branch)
* [**Checkout Branch**](#git-checkout)
* [**Merging branch**](#git-merge)
* [**Deleting a branch**](#git-branchdel)




---
# General Information
---


### <a name = "three-states"></a> The Three States

##### Modified state
* ```git status``` shows you the status of any modified file and/or if there is any staged files
* If you get this error: ```not a git repository (or any of the parent directories): .git``` make sure you initialize git directory using ```git init```
* A file in the modified state has some changes made to it but it's not yet saved. This means that the state of the file has been altered from its previous state in the committed state.
* Any file that has not been added to the staged state will be highlighted in red


##### Staged state
* ```git add FILE``` for adding a specific file to the staged state
* ```git add .``` for all files and folders in current directory
* A file in the staged state means it is ready to be committed. In this state, all necessary changes have been made so the next step is to move the file to the commit state.
* You can verify if the file has been added to the staged state using ```git status``` the color of the file should now be green


##### Committed state
* ```git commit -m " X "```
* The message is required in order to commit, you can type anything.
* If error please check that the file was added to the staged state using ```git status```
* A file is in the committed state when all the changes made to the file have been saved in the local repo. Files in the committed stage are files ready to be pushed to the remote repo (on GitHub).


### <a name = "git-info"></a> Hidden files and folders

##### Git Directory

The .git directory is where Git stores the metadata and object database for the repository

##### Working Directory

A copy of one version of the git project, taken from compressed database in the .git directory


##### Staging Area/Index

File that stores information about what will next be committed into the git repository









---
# Configuration
---
### <a name = "config-local"></a> Local Configuration



### <a name = "config-github"></a> Github Configuration


























---
# Branch
---

### <a name = "git-branch"></a> List all branches

* ```git branch or git branch -l```
* Current branch will be highlighted with an asterisk *

### <a name = "git-branch"></a> Creating a new branch
* ```git branch BRANCH_NAME```
* Different version but a clone of main branch
* Typically for starting new work in a team and people working on different features or seperating the test to prod mentality

### <a name = "git-checkout"></a> Checkout branch
* ```git checkout BRANCH_NAME```
* This command allows you to switch branch

### <a name = "git-merge"></a> Merging branch
* Make sure you have switched to destination before using command
* ```git merge BRANCH_NAME```
* Deletes the branch using ```--force``` option

```
This command is used by git pull to incorporate changes from another repository and can be used by hand to merge changes from one                      
       branch into another.                                                                                                                                   
                                                                                                                                                              
       Assume the following history exists and the current branch is "master":                                                                                
                                                                                                                                                              
                     A---B---C topic                                                                                                                          
                    /                                                                                                                                         
               D---E---F---G master                                                                                                                           
                                                                                                                                                              
                                                                                                                                                              
       Then "git merge topic" will replay the changes made on the topic branch since it diverged from master (i.e., E) until its current
       commit (C) on top of master, and record the result in a new commit along with the names of the two parent commits and a log message 
       from the user describing the changes.                                                                                                                  
                                                                                                                                                              
                     A---B---C topic                                                                                                                          
                    /         \                                                                                                                               
               D---E---F---G---H master
               
              
              
               
from git help merge                    
```
### <a name = "git-branchdel"></a> Deleting a branch

* ```git branch -D BRANCH_NAME```
* Deletes the branch using ```--force``` option
