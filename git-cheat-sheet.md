# Git Cheat Sheet

## 1. General Information

* [**Git Directory Information**](#git-info)
* [**The Three States**](#three-states)


## 2. Git Config

* [**Local Configuration**](#config-local)
* [**GitHub Configuration**](#config-github)



## 3. Branch

* [**Branch**](#git-branch)
* [**Checkout Branch**](#git-checkout)
* [**Merging Branch**](#git-merge)



---
# <a name = "git-info"></a> Git Directory Information
---

## Git Directory

The .git directory is where Git stores the metadata and object database for the repository

## Working Directory

A copy of one version of the git project, taken from compressed database in the .git directory


## Staging Area/Index

File that stores information about what will next be committed into the git repository



---
# <a name = "three-states"></a> The Three States
---

## Modified state - git status

A file in the modified state has some changes made to it but it's not yet saved. This means that the state of the file has been altered from its previous state in the committed state.


## Staged state - git add X

A file in the staged state means it is ready to be committed. In this state, all necessary changes have been made so the next step is to move the file to the commit state.


## Committed state - git commit -m "X"

A file is in the committed state when all the changes made to the file have been saved in the local repo. Files in the committed stage are files ready to be pushed to the remote repo (on GitHub).


---
# <a name = "config-github"></a> GitHub Configuration
---

---
# <a name = "git-branch"></a> Branch
---

### List all branches

* ```git branch or git branch -l```
* Current branch will be highlighted with an asterisk *

### Creating a new branch

* ```git branch BRANCH_NAME```
* Different version but a clone of main branch
* Typically for starting new work in a team and people working on different features or seperating the test to prod mentality

### Deleting a branch

* ```git branch -D BRANCH_NAME```



---
# <a name = "git-checkout"></a> Checkout Branch
---

---
# <a name = "git-merge"></a> git-branch
---
