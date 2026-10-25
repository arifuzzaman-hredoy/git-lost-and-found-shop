# 💻 Git Terminal History

## The Lost-and-Found Shop — Hands-on Practice Log

This file documents the Git commands I practiced while building **The Lost-and-Found Shop**, my personal Git and GitHub learning project.

The purpose of this file is to record my command-line practice, understand each command's role, and keep a reference for future revision.

> **Important:** This is an organized practice log, not a guaranteed verbatim copy of my terminal history. Some commands are examples, and their results depend on the repository's current state.

---

## 1. Git Configuration

### Inspect Git configuration

```bash
git config --list
```

### Configure Git identity

```bash
git config --global user.name "Arifuzzaman Hredoy"
git config --global user.email "your-email@example.com"
```

**What I learned:** Git uses the configured username and email to identify the author of commits. I should replace the example email with my actual Git commit email.

---

## 2. Initialize and Inspect a Repository

### Initialize Git

```bash
git init
```

### Check repository status

```bash
git status
git status --ignored
```

### Inspect files

```bash
ls -l
ls -la
cat .gitignore
```

### Inspect commit history

```bash
git log
git log --oneline
git log --stat
git log --graph --oneline --all
git log --graph --all --oneline --decorate
```

**What I learned:** `git status` shows the state of tracked and untracked files, while `git log` helps me inspect commit history.

---

## 3. Stage and Review Changes

### Stage selected files

```bash
git add README.md my-story.md record.md
git add .gitignore terminal-history.md
```

### Stage changes in the current directory

```bash
git add .
```

### Inspect unstaged changes

```bash
git diff
```

### Inspect staged changes

```bash
git diff --staged
git diff --staged my-story.md
git diff --staged record.md
```

### Unstage changes

```bash
git restore --staged .
```

**What I learned:** Staging lets me choose which changes will be included in the next commit. Before committing, I should review staged changes with `git diff --staged`.

**Safety note:** `git restore --staged .` unstages changes but normally preserves their contents in the working directory.

---

## 4. Commit Changes

Examples of commit messages used in my practice notes:

```bash
git commit -m "Add README, learning story, and record files"
git commit -m "Resolve item data in record.md"
git commit -m "Add bazar list"
git commit -m "Document Chapter 1 in my learning story"
git commit -m "Add Git ignore rules and terminal history"
git commit -m "Update Git ignore configuration"
```

**What I learned:** A commit records the staged changes in the local repository. Good commit messages describe the changes clearly.

---

## 5. Practice `.gitignore`

### Inspect ignored files

```bash
git status --ignored
git check-ignore -v draft/private-customers.txt
```

### Stop tracking a file but keep its local copy

```bash
git rm --cached bazar-notes.txt
git rm --cached draft/private-customers.txt
```

**What I learned:**

* `.gitignore` helps prevent eligible untracked files from being added accidentally.
* Adding an already tracked file to `.gitignore` does not automatically untrack it.
* `git rm --cached` removes a file from Git's index while keeping the local copy.

**Security note:** Never commit passwords, API keys, private customer information, or other sensitive data.

---

## 6. Create and Switch Branches

### List branches

```bash
git branch
```

### Create branches

```bash
git branch book-recoard
git branch wallet-record
```

### Switch branches

```bash
git switch book-recoard
git switch master
git switch wallet-record
```

### Rename the current branch

```bash
git branch -M main
git branch -M feature-branch
```

### Create and switch to a new branch

```bash
git switch -c test-hard
git switch -c recovery-test
```

### Return to the main branch

```bash
git switch main
```

**What I learned:** Branches let me work on separate lines of development without immediately changing another branch.

**Note:** Branch names such as `master`, `main`, and `feature-branch` are not interchangeable automatically. I must verify which branches actually exist.

---

## 7. Merge Branches

Commands recorded in my practice notes:

```bash
git merge book-recoard master
git merge master wallet-record
git merge wallet-record master
```

### Inspect the commit graph

```bash
git log --graph --oneline --all --decorate
```

**What I learned:** Merging integrates changes from another line of development into the current branch.

**Important:** Before running a merge, I should check the current branch with `git branch --show-current` and review `git status`. I should also verify the intended source and target branches.

---

## 8. Connect to GitHub

### Add a remote repository

```bash
git remote add origin <repository-url>
```

### Inspect remotes

```bash
git remote -v
```

### Clone a repository

```bash
git clone <repository-url>
```

### Pull changes

```bash
git pull origin main
git pull origin feature-branch
```

### Push a branch

```bash
git push -u origin main
git push origin feature-branch:feature-branch
```

Replace `<repository-url>` with the actual repository URL.

**What I learned:**

* `git clone` creates a local copy of a remote repository.
* `git pull` downloads and integrates remote changes.
* `git push` publishes local commits to a remote repository.
* `git remote -v` displays configured remote URLs.

---

## 9. Fetch and Remote-Tracking Branches

Commands for practicing remote updates:

```bash
git fetch origin
git branch -r
git branch -vv
git log --graph --oneline --all --decorate
```

**What I learned:**

* `git fetch origin` downloads information about remote updates without integrating those updates into my current branch.
* `git branch -r` lists remote-tracking branches.
* `git branch -vv` shows local branches and their upstream tracking information.
* `git pull` fetches updates and then integrates them into the current branch.

**Practice goal:** Compare local branches and remote-tracking branches after fetching updates from GitHub.

---

## 10. Save Unfinished Work with Stash

```bash
git stash -m "Uncompleted work"
git stash pop
```

**What I learned:** Stash temporarily saves eligible working-tree changes so I can switch tasks and restore those changes later.

After using `git stash pop`, I should inspect `git status` and resolve any conflicts if they occur.

---

## 11. Rename and Remove Files

### Rename a tracked file

```bash
git mv record.md all-record.md
```

### Remove a tracked file

```bash
git rm lost-student-id.md
```

### Remove a file from Git tracking but keep it locally

```bash
git rm --cached bazar-notes.txt
```

**What I learned:** Git provides commands to manage tracked files and record file operations in repository history.

---

## 12. Undo and Recover Changes

### Create a commit that reverses a previous commit

```bash
git revert HEAD~1 --no-edit
```

### Reset to an earlier commit

```bash
git reset --hard HEAD~1
```

### Inspect recent local reference movements

```bash
git reflog
```

### Inspect a particular commit

```bash
git show <commit-hash>
```

### Create a recovery branch at a known commit

```bash
git branch recovery-branch <commit-hash>
```

**What I learned:**

* `git revert` creates a new commit that reverses an earlier commit's changes.
* `git reset` moves the current branch reference and can also change the staging area or working tree, depending on the selected mode.
* `git reflog` helps locate earlier positions of local references.
* `git show` displays information about a commit.
* A recovery branch can preserve a reference to a commit before attempting risky history changes.

### ⚠️ Recovery Safety Rules

1. Check `git status` before recovery operations.
2. Preserve important uncommitted work first.
3. Inspect the target commit before changing branch history.
4. Avoid `git reset --hard` unless I understand exactly what will be discarded.
5. Avoid force-pushing shared branches because it can overwrite remote history for other contributors.
6. Practice destructive recovery operations in a test repository or disposable branch.

---

## 13. Create and Publish a Tag

### Create an annotated tag

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
```

### List tags

```bash
git tag -n
```

### Inspect a tag

```bash
git show v1.0.0
```

### Publish a tag to GitHub

```bash
git push origin v1.0.0
```

**What I learned:** Tags provide named references to particular commits and are useful for marking releases.

A tag created locally is not automatically available on GitHub. Before publishing, I should verify that it points to the intended commit.

---

## 14. Final Repository Verification

Before finishing a practice session, inspect the repository.

```bash
git status
git branch
git branch -vv
git remote -v
git log --graph --all --oneline --decorate
git reflog
```

### Verification checklist

* [ ] Working-tree changes reviewed.
* [ ] Staged changes reviewed.
* [ ] Current branch verified.
* [ ] Commit history checked.
* [ ] Remote repository verified.
* [ ] Unfinished work preserved.
* [ ] No sensitive information accidentally staged.
* [ ] Tags checked when working on a release.

---

## 15. Important Git Lessons

| Command             | Main purpose                                                            |
| ------------------- | ----------------------------------------------------------------------- |
| `git status`        | Inspect repository state                                                |
| `git add`           | Stage changes                                                           |
| `git diff`          | Inspect unstaged changes                                                |
| `git diff --staged` | Inspect staged changes                                                  |
| `git commit`        | Record staged changes                                                   |
| `git branch`        | List or manage branches                                                 |
| `git switch`        | Switch branches                                                         |
| `git merge`         | Integrate changes from another branch                                   |
| `git fetch`         | Download remote updates                                                 |
| `git pull`          | Fetch and integrate remote changes                                      |
| `git push`          | Publish local commits                                                   |
| `git stash`         | Temporarily save changes                                                |
| `git revert`        | Reverse changes through a new commit                                    |
| `git reset`         | Move a branch reference and optionally update the index or working tree |
| `git reflog`        | Inspect recent local reference movements                                |
| `git tag`           | Create or inspect named commit references                               |

---

## 📝 Final Note

This terminal history is part of my ongoing Git learning journey. I will continue updating it as I practice more commands, solve problems, and learn safer workflows.

For a structured overview of the project and its learning chapters, see [README.md](./README.md).

For my personal learning narrative, see [my-story.md](./my-story.md).

**Author:** Arifuzzaman Hredoy
**Project:** The Lost-and-Found Shop
**Focus:** Git, GitHub, Linux Terminal, and DevOps fundamentals
