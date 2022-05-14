---
author: Alexandre Lamberty
title: Git
description: | Software for tracking changes in any set of files, usually used
for coordinating work among programmers collaboratively developing source code
during software development
category: Software
tags: [content,versioning]
created: 2021-10-23T20:38:58+02:00
updated: 2021-10-23T20:38:58+02:00
---
# Git

## Lexical

> Need more explainations and more lexic

- Working dir
- Cache, Stage and Index are synonyms. Some command still use `--cache` but most
  use `--index`
- HEAD

--patch See that important [kaar] from IRC

```bash
git reset -p
```

## Configuration

```bash
git config --global user.email "yourEmail" #your email at Bitbucket
git config --global user.name "yourName" #your name at Bitbucket
```

### Cloning

### Fetching

Fetch from remote to HEAD.

### Pulling

Fetch and merge from remote repository

### Pushing

> Need information!

## Stagging

> ! Stagging is global. Not branch specific.

Add all unstaged files

```bash
git add .
```

Add specific file

```bash
git add file [file]
```

## Committing

A good question to ask before naming a commit "If I applied, this commit
will ..."

Commit all staged files

```bash
git commit -a[m]
```

### Fixing commit
    
See Stashing

### Change last commit

```bash
git commit --amend
```

> ! Don’t amend your last commit if you’ve already pushed it.

### Reorder commits

Rebase interactively and change or remove commits.

## Branching

### Creating a new branch

```bash
git checkout -b [branch-name]
```

### Listing all branch

```bash
git branch
```

### Change branch

```bash
git switch branch-name
```

### Rename branch

If you want to rename a branch while pointed to any branch, do:

```bash
git branch -m <oldname> <newname>
```

If you want to rename the current branch, you can do:

```bash
git branch -m <newname>
```

### Pushing a branch

Push -u create upstream

```bash
git push -u <remote> <branch>
```

### Delete branch

> Need formating and complement of informations

```bash
git branch -d <local-branch>
```
```bash
git branch -D <local-branch>
```
```bash
git push origin --delete <remote-branch-name>
```

#### Rebase

git rebase master

### Merging

```bash
git merge --squash
```

## Reset

Squash the last 3 commits

```bash
git reset --soft HEAD~3 && git commit
```

```bash
git reset -p
```

### Squashing

Squashing commit from HEAD to the desired commit.

```bash
git rebase -i HEAD~5
```

Edit choose an operation pick, squash, fixup

### Rebasing

### Versioning

### Stashing

## Show

git show `commit-id`

```bash
git show is HEAD~
```

## Diff

Use diff to see changes between branches

```bash
git diff [--cached]
```

## Log
    
## Remote

```bash
git remote add [name] [remote_name]
```

```bash
git push -u origin master
```

## Stashing

Stash is global not branch specific. Stash is a stack.

git stash list git stash show -p 1

## Submodules

```bash
git submodule add ssh://uri
```

Track HEAD

```bash
git submodule add -b <branch> <repository> [<path>]
```

```bash
git submodule init
```

```bash
git submodule update
```

```bash
git submodule update --init
```

```bash
git submodule update --init --recursive`
```

Git 1.8.2 features a new option, --remote, that will enable exactly this behavior. Running

```bash
git submodule update --remote --merge
```

[doc](https://git-scm.com/docs/git-submodule)

### Remove a submodule

Delete the relevant section from the `.gitmodules` file.

Stage the .gitmodules changes:

```bash
git add .gitmodules
```

Delete the relevant section from `.git/config.`

Remove the submodule files from the working tree and index:

```bash
git rm --cached path_to_submodule (no trailing slash).
```

Remove the submodule's .git directory:

```bash
rm -rf .git/modules/path_to_submodule
```

Commit the changes:

```bash
git commit -m "Removed submodule <name>"
```

Delete the now untracked submodule files:

```bash
rm -rf path_to_submodule
```

## References

- [Git - Rewriting History](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)
- [Tech Talk: Linus Torvalds on git](https://www.youtube.com/watch?v=4XpnKHJAok8&ab_channel=Google)
