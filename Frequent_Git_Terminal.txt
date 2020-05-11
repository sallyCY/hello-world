## Terminal keywords
pwd         # print working directory
ls          # list files in directory
cd          # change directory
~           # home directory
..          # up one directory
-           # previous working directory
mkdir       # create new directory


## Get Start
git clone <url>                     # Fetch remote depository
git checkout -b <new-branch>        # Create new local branch
git push -u origin <new-branch>     # Sync local branch with remote

## Working with branches
git branch                  # Get available branches (* is the active/current branch)
git checkout <branch>       # Switch to existing local branch

git checkout master         # go back to master branch
git merge <branch>          # merge changes from branch
git pull . <branch>         # merge changes from branch (all git version)


git checkout -b <new-branch>     # Create new branch off current branch and switch
--- same as ---
git branch <new_branch>              # Create new branch
git checkout <new_branch>            # Swithch to new created branch
--- additional case ---
git checkout -b <new-branch> <existing-branch>  # Create new branch off specific branch

git fetch --all       # fetch the contents of the branch before checkout a remote branch 
git checkout <remote-branch>


git push origin <branch>        # Push branch to remote
git branch -d <branch>          # delete local branch
git push origin :<branch>       # delete remote branch

git branch -m <newname>         # rename branch



## Create Project
git init                            # initializes the repository, convert an existing, unversioned project to a Git repository or initialize a new, empty repository
git add <filename>                  # add file 
git add .                           # add all files
git commit -m 'message'            # Commit all changes with message


## Special Examples
//have 11 files but want to commit 10 files
git checkout filename
git add .
git commit -m " "
git push



## Excercise - 11 May 2020
1. `ssh key setup -- done`
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"       # create new ssh key using email address
eval "$(ssh-agent -s)"                  # Start the ssh-agent in the background
open ~/.ssh                             # check existence of file
pbcopy < ~/.ssh/id_rsa.pub              # copy ssh key into keyboard and ready to paste

2. `Init a repo in GitHub`
mkdir repo
cd repo
git init

###
(base) sallycy@Whats-up-Air repo1 % git commit -m 'add md file'

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'sallycy@Whats-up-Air.(none)')
###

3. `Clone a repo`
git clone <url>

4. `Add a readme.med & edit the file`
git add readme.md

5. `Submit the file`
git status
git commit -m 'add readme.md file'
git push

6. `Create a branch called dev`
git branch dev

7. `Checkout the branch`
git checkout dev

--> `Create a branch and checkout`
git checkout -b dev


8. `Make changes`
git add .

9. `Submit changes`
git status
git commit -m 'message'
git push