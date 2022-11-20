##  inA new repo from an existing project:-
git init
git add .
git commit -m "Message"

## Connect it to github:-
git remote add origin git@github.com:sandip22sandip/GitCommands.git
git push -u origin main



## To see local branch names:-
git branch

## To see all remote branch names:-
git branch -r

## To see all local and remote branches:-
git branch -a

## To see detailed information such as the local or remote branches in use, commit ids, and commit messages:-
git branch -vv
OR
git branch -vva

## Create a New Git Branch:-
git branch <new_branch_name>

## You can then checkout the newly created branch:-
git checkout <new_branch_name>

## Create New Git Branch From Current Branch & Checkout to newly created one:-
git checkout -b <new_branch_name>

## Create New Git Branch From a Different Branch:-
git checkout -b <new_branch_name> <specific_different_branch>

Create a Branch from a Commit:-
## Find the hash key for a specific commit:-
git log

## Create a branch from an older commit::-
git branch <new_branch_name> 6009fc
Note: 
- 6009fc in the example above represents the hash. Replace this with the actual hash from your git log command.
- No need to enter the whole hash key, just the first few characters. View the git log again, and you’ll see the new branch listed.
- This method is especially helpful if you need to go back to a previous version of the software to fix a bug without removing any existing features.
- Use git checkout to switch to the newly created branch.

## Create a Branch Using Detached HEAD State:-
git checkout 6009fc

## Create a Branch from a Remote Branch:-
git branch --track <new_branch> origin/<remote_branch>
Alternatively, use the git checkout command to keep the original remote branch name:- 
git checkout --track origin/<remote_branch>

## Create a Branch in a Remote Repository:-
git push -u origin <local_branch>

## Delete a Git Branch Locally:-
git checkout master
git branch -d <branch_name>

## Delete Remote Branch Remote:-
git checkout master
git push <remote_name> --delete <branch_name>

## Fetch Remote Branch:-
git fetch

## Merge 2 Git Branch:-
git checkout master    
git merge origin/development
git push origin master
