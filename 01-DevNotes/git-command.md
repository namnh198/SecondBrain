---
title: Git Command
createDate: 2024-11-16
published: 
tags:
  - Git
  - Tools
  - Skills
---
> [!example]+ Clone a repo
> 
> ```shell
> git clone repo-link
> # or using gh
> ```

> [!example]+ Check status (What are in stage or unstage)
> ```shell
> git status
> ```

> [!example]+ Show list of commit
> ```shell
> # local, current branch
> git log --graph --decorate --oneline
> # press "q" to quit
> 
> # remote branch b1 (local may have different commits)
> git fetch origin 
> git log origin/b1 --graph --decorate --oneline
> ```

> [!example]+ Working with branches
> ```shell
> # create a new branch from a commit
> git checkout -b new_branch_name commit_hash
> 
> # create a new branch based on another branch
> git checkout -b new_branch_name existing_branch_name
> 
> # push to remote
> git push -u origin branch_name
> 
> # force to push
> git push -u origin branch_name --force
> 
> # rename currently local branch
> git branch -m old_branch new_branch
> 
> # verify branch
> git branch
> 
> # remote
> git branch -r
> 
> push renamed branch to remote and delete the one on remote
> git push origin -u new_branch
> git push origin --delete old_branch
> 
> # remove a local branch
> git branch -d branch_name
> 
> # force
> git branch -D branch_name
> 
> # remove a remote branch
> git push origin --delete branch_name
> ```

> [!example]+ Stage and Unstage
> ```shell
> # stage file
> git add file
> 
> # stage 
> ```