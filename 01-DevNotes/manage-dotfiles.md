---
title: Manage Dotfiles with STOW & GIT
createDate: 2024-08-10
draft: true
---

## Why I need to Manage dotfiles
- As a developer, I usually install more tools that I use it for development. I have taken time to config after I install a fresh OS. I also like to keep things consistent across my different machines. So I make sure to store all my dotfiles and configuration on Github.
- But in the past, to keep things in sync, I always had to do something like this:

```bash
cp dotfiles/.zshrc ~/.zshrc
```

## Introducing GNU Stow
GNU Stow is a symlink farm manager, which means it helps you store all your configuration files in one common location.
So when you "stow" a file, it will create a symlink between your files and and identical in our home directory

You can use command like this to create a symlink:

```bash
ln -s [source_path] [target_path]
```

But on some folders you do not want to create symlink. 
Ex: 