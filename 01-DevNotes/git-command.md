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
> # create a new brea
> 
> # push to remote
> 
> ```
