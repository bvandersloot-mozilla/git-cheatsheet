# How I git Firefox

A quick collection of some useful commands

## The Basics

- `git status`
- `git add ./file/to/add.cpp`
- `git commit [-a]`
- `git log`
- `git branch`


## Undoing

- `git commit -a -m WIP`
- `git checkout main`

  or

- `git stash`

  or

- `git reset HEAD --hard`


## Managing Phabricator Changes

- `git checkout -b feature-description`
- `git branch --set-upstream-to=origin/main feature-description`
- `moz-phab submit`
- `git commit -a --fixup commit-to-update`
- `git rebase -i --autosquash`
- `git rebase main feature-description`
- `git rebase --onto main last-commit-merged feature-description`
- `git branch -D feature-description`

## A Bit Deeper

- `git checkout source-commit -- file/to/take`
- `git log --all --decorate --oneline --graph`
- [git absorb](https://github.com/tummychow/git-absorb)
- Want just part of a file's changes? Use the VSCode GUI

## The Safety Net

- `git reflog`
- `git checkout HEAD@{4}`
- `git switch -c feature-SAVED`
