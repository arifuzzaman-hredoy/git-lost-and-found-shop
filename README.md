# Git Lost and Found Shop

A hands-on Git and GitHub learning project built around a lost-and-found
shop scenario. The project records six chapters of practical exercises,
from repository initialization to remote collaboration, undoing changes,
and inspecting Git history.

**Project type:** Git/GitHub practice repository\
**Focus:** Version control fundamentals and collaborative workflows\
**Documentation:** Chapter notes and terminal command history

## Learning Objectives

-   Initialize and inspect a local Git repository.
-   Understand the working directory, staging area, and repository
    history.
-   Stage, compare, commit, and unstage file changes.
-   Configure `.gitignore` and verify ignored files.
-   Create branches, switch between them, and practice merging.
-   Connect a local repository to GitHub and synchronize changes.
-   Clone a repository and work with remote branches.
-   Temporarily save unfinished work with `git stash`.
-   Rename and remove tracked files.
-   Understand the different purposes of `git reset` and `git revert`.
-   Inspect commit history with `git log` and recovery references with
    `git reflog`.
-   Create an annotated Git tag.

## Chapter Overview

  -----------------------------------------------------------------------
  Chapter                             Topics
  ----------------------------------- -----------------------------------
  1 --- Git Basics                    Initialization, status, staging,
                                      diffs, commits, and logs

  2 --- Git Ignore                    `.gitignore`, ignored files,
                                      untracking, and ignore verification

  3 --- Branching and Merging         Branch creation, switching,
                                      merging, and history inspection

  4 --- GitHub and Remote             Remote setup, cloning, pushing,
  Repositories                        pulling, and branch synchronization

  5 --- Undo and Recovery             Stash, rename/removal, reset,
                                      revert, reflog, and tags

  6 --- Repository History Review     Graph logs, branch inspection,
                                      status checks, and final push
  -----------------------------------------------------------------------

## Core Git Concepts

### Working directory

The project folder where files are created and edited.

### Staging area

The area where selected changes are prepared for the next commit. Use
`git add` to stage changes and `git status` to check their state.

### Local repository

Git's local history and metadata are stored in the hidden `.git`
directory created by `git init`.

### Commit

A snapshot of staged changes in the repository history. Use a clear,
descriptive commit message.

### Branch

An independent line of development that lets work progress separately
before changes are integrated.

### Remote repository

A shared repository hosted on a service such as GitHub, used to
synchronize work between machines or contributors.

## Essential Commands

``` bash
# Initialize and inspect
git init
git status
git log
git branch

# Stage and commit
git add .
git commit -m "Describe the change"

# Review changes
git diff
git diff --staged

# Branch workflow
git branch feature-branch
git switch feature-branch
git merge feature-branch

# Remote synchronization
git remote -v
git push -u origin main
git pull origin main

# History and recovery references
git log --oneline --graph --all --decorate
git reflog
```

## Repository Notes

-   See [`terminal-history.md`](terminal-history.md) for the
    chapter-wise command record.
-   The terminal history preserves commands from the supplied practice
    notes. Some names and commands are specific to the exercise and
    should be reviewed before reuse.
-   Replace placeholders such as `USERNAME` and `REPO` with your actual
    GitHub username and repository name.
-   Before running destructive commands such as `git reset --hard` or
    `git push --force`, confirm the current branch and understand the
    possible impact on local or remote work.
-   In collaborative projects, coordinate with teammates before
    rewriting shared history.

## Suggested Workflow

1.  Check the repository state with `git status`.
2.  Review unstaged changes with `git diff`.
3.  Stage only the intended files.
4.  Review staged changes with `git diff --staged`.
5.  Commit with a descriptive message.
6.  Inspect history when needed.
7.  Push committed changes to the correct remote branch.

## Purpose

This repository is a learning record rather than a production-ready
application. Its purpose is to build practical confidence with Git and
GitHub through repeated terminal exercises and organized documentation.
