# My Git Practice Journey

## Project: The Lost-and-Found Shop

**Author:** Arifuzzaman Hredoy
**Repository:** `git-lost-and-found-shop`
**Purpose:** Personal Git and GitHub practice
**Learning Level:** Beginner
**Environment:** WSL Ubuntu, Git, GitHub, and VS Code

---

## Chapter 1: Understanding Git Fundamentals

### My Learning Experience

I started this project to understand how Git manages files, tracks changes, and maintains project history.

The first concept I learned was the difference between the working directory, staging area, and local repository.

The **working directory** is the folder where I create and modify project files.

My working directory was:

```text
/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop
```

The **staging area** is where I prepare selected changes before committing them. Git does not automatically include every modification in the next commit. I must stage the changes that I want to record.

The **local repository** stores Git's history and metadata. I initialized the repository using `git init`, which created the hidden `.git` directory.

I used `git status` to inspect the current repository state and `git diff` to review changes before committing them.

### Commands I Practiced

```bash
git config --list
git config --global user.name "Arifuzzaman Hredoy"
git config --global user.email "arifuzzamanhredoy@gmail.com"

git init
ls -l
ls -la
git status

git add README.md my-story.md record.md
git diff
git diff --staged
git diff --staged my-story.md

git log
git commit -m "Add README, learning story, and record files"
```

I also practiced staging and committing additional changes to `record.md` and `bazar-notes.txt`.

```bash
git diff --staged record.md
git commit -m "Resolve item data in record.md"

git add bazar-notes.txt
git commit -m "Add bazar list"
```

I then experimented with removing a file from the Git index while keeping the local copy:

```bash
git rm --cached bazar-notes.txt
```

I also practiced unstaging changes:

```bash
git restore --staged .
```

### What I Learned

* `git init` initializes a Git repository.
* `git add` stages changes for the next commit.
* `git status` displays the current state of the working tree and staging area.
* `git diff` displays unstaged changes to tracked files.
* `git diff --staged` displays staged changes compared with the current commit.
* `git commit` records staged changes in repository history.
* `git log` displays commit history.
* `git rm --cached <file>` removes a file from the index without deleting the working copy.

I also learned that `git restore --staged .` unstages staged changes throughout the current directory. I should inspect `git status` before running it so that I understand which changes will be affected.

---

## Chapter 2: Working with `.gitignore`

### My Learning Experience

In this chapter, I practiced preventing selected files from being added to the repository.

The `.gitignore` file contains patterns that tell Git which untracked files or directories to ignore.

I learned that adding a filename to `.gitignore` does not automatically remove a file that Git already tracks. Previously tracked files must be removed from the index if I want Git to stop tracking them.

### Commands I Practiced

I updated my learning report and added the ignore configuration and terminal history.

```bash
git status
git add my-story.md
git commit -m "Document Chapter 1 in my learning story"

git add .gitignore terminal-history.md
git commit -m "Add Git ignore rules and terminal history"

cat .gitignore
```

I then experimented with a file named `draft/private-customers.txt`.

```bash
git add draft/private-customers.txt
git commit -m "Add practice file before configuring ignore rules"

git rm --cached draft/private-customers.txt

git status --ignored
git check-ignore -v draft/private-customers.txt
```

The commands above document the intended workflow I practiced. The exact result of each command depends on the repository state and the ignore rules present at the time.

### What I Learned

* `.gitignore` applies primarily to untracked files.
* `git rm --cached <file>` removes a tracked file from the index but leaves the working copy.
* `git check-ignore -v <file>` helps identify which ignore rule matches a path.
* `git status --ignored` helps inspect ignored files.
* Ignoring a file does not remove it from previous commits.

I also learned an important security lesson: if a real password, API key, or other secret is committed, adding the file to `.gitignore` is not enough. Exposed credentials should be revoked or rotated, and repository history may need to be cleaned.

---

## Chapter 3: Branching and Merge Conflicts

### My Learning Experience

I learned that a Git branch is a movable reference to a commit. Branches allow me to develop different changes independently before integrating them.

In a team environment, developers can work on separate feature branches and then merge their changes into a shared branch after review.

I created branches for the book and wallet records and switched between branches during the exercises.

### Commands I Practiced

```bash
git branch
git branch book-recoard
git branch wallet-record

git switch book-recoard
git switch master
git switch wallet-record
```

I created files for the exercise:

```bash
touch lost-book.md
touch lost-student-id.md

git add lost-book.md lost-student-id.md
git add my-story.md terminal-history.md
```

I also practiced inspecting the repository history and working with branches:

```bash
git log
git log --graph --oneline --all --decorate
```

My recorded merge commands included:

```bash
git merge book-recoard master
git merge master wallet-record
git merge wallet-record master
```

These commands attempt to merge the named branch into the currently checked-out branch. The current branch and repository history determine the actual result.

### Understanding Merge Conflicts

A merge conflict can occur when Git cannot automatically reconcile competing changes.

For example, two branches may modify the same line of a file differently. During a merge, Git may mark the file as conflicted and insert markers such as:

```text
<<<<<<< HEAD
Current branch content
=======
Incoming branch content
>>>>>>> feature-branch
```

To resolve the conflict, I must review the competing changes, edit the file to produce the correct final content, remove the conflict markers, and stage the resolved file.

I should then complete the merge and inspect the resulting history.

### What I Learned

* `git branch` lists branches.
* `git switch` changes the current branch.
* `git merge` integrates changes from another branch into the current branch.
* Conflicts require reviewing the actual changes rather than blindly choosing one version.
* `git log --graph --oneline --all --decorate` helps me understand how branches and commits relate to one another.

I also learned that the primary branch may be named `main` or `master`, depending on the repository. I should check the actual branch name before switching or merging.

---

## Chapter 4: Working with Remote Repositories

### My Learning Experience

I connected my local project to GitHub and practiced transferring changes between local and remote repositories.

A local branch is a branch I work on directly. A remote-tracking branch, such as `origin/main`, records the state of a remote branch as last observed by Git.

I also simulated collaboration by cloning the repository into another directory to represent a second developer's computer.

### Commands I Practiced

I renamed the primary branch and configured a remote repository:

```bash
git branch -M main
git remote add origin <repository-url>
git remote -v
git status
```

I then practiced staging, committing, and pushing changes:

```bash
git add .gitignore
git commit -m "Update Git ignore configuration"
git push -u origin main
```

To simulate another computer, I cloned the repository into a separate directory:

```bash
cd ..
mkdir rafi-computer
cd rafi-computer

git clone <repository-url>
cd git-lost-and-found-shop
```

I also practiced remote synchronization:

```bash
git pull origin main
git pull origin feature-branch

git branch -M feature-branch
git push origin feature-branch:feature-branch
```

The placeholder `<repository-url>` should be replaced with the actual GitHub repository URL when executing the command.

### Understanding `fetch`, `pull`, and `push`

**`git fetch`** downloads remote changes and updates remote-tracking references without automatically integrating them into the current local branch.

**`git pull`** fetches remote changes and integrates them into the current branch, normally through a merge or rebase depending on the configuration and options.

**`git push`** publishes local commits to a remote repository.

I used `git pull` directly during my collaboration exercise rather than separately running `git fetch` first. Therefore, I understand the conceptual difference, but I still need a dedicated fetch-and-inspect exercise to demonstrate that workflow practically.

### What I Learned

* `git remote -v` displays configured remote repositories.
* `git clone` creates a local copy of a remote repository.
* `git fetch` lets me inspect remote updates before integrating them.
* `git pull` retrieves and integrates remote changes.
* `git push` publishes local commits.
* Remote-tracking branches help me compare local history with the remote repository.

---

## Chapter 5: Stash, Revert, Reset, and Recovery

### My Learning Experience

This chapter focused on managing unfinished work, undoing changes, and understanding recovery techniques.

I practiced `git stash`, renamed and removed files, inspected commit history, and experimented with `git revert`, `git reset`, and `git reflog`.

### Stashing Unfinished Work

I used:

```bash
git stash -m "Uncompleted work"
git stash pop
```

`git stash` temporarily saves eligible local modifications so I can switch tasks without creating an ordinary commit.

`git stash pop` attempts to restore the latest stash and remove the stash entry if restoration succeeds. Conflicts may occur, so I should always inspect the result.

### Renaming and Removing Files

I practiced renaming a tracked file:

```bash
git mv record.md all-record.md
```

I also removed an obsolete tracked file:

```bash
git rm lost-student-id.md
```

These operations change the index and working tree. I must commit the resulting changes if I want them recorded in repository history.

### Inspecting History

I used:

```bash
git log
git log --oneline
git log --stat
```

These commands helped me inspect commits, their messages, and the files affected by each change.

### Reverting a Commit

I practiced:

```bash
git revert HEAD~1 --no-edit
```

`git revert` creates a new commit that reverses the changes introduced by a selected commit. It preserves the existing commit history instead of moving the branch backwards.

The exact commit affected depends on the current `HEAD` and repository history at the time the command runs.

### Resetting a Branch

I experimented with:

```bash
git reset --hard HEAD~1
```

A hard reset moves the current branch reference to the selected commit and resets the index and working tree to match it. Changes may be lost if they exist only in the discarded commit or in uncommitted work.

I also experimented with force-pushing a branch:

```bash
git push origin main --force
```

This taught me that rewriting shared branch history can affect collaborators and remove commits from the branch's visible history.

### My Production Safety Lesson

Although destructive commands can be useful in a controlled practice environment, I should not casually use `git reset --hard` or `git push --force` on a shared or production branch.

Before attempting recovery, I should:

1. Inspect `git status`.
2. Confirm the current branch.
3. Review recent commits with `git log`.
4. Preserve important work before making destructive changes.
5. Prefer `git revert` when undoing published changes.
6. Coordinate with collaborators before rewriting shared history.

### Using `git reflog`

I used:

```bash
git reflog
```

The reflog records recent movements of local references, such as `HEAD`. It can help locate a previous commit after a reset or branch movement.

However, it is not a permanent backup and does not record every uncommitted change or every failed command. Recovery depends on the commit or object still being available.

### What I Learned

Git provides several ways to undo or recover changes, but each has different consequences.

* `git stash` temporarily saves eligible unfinished changes.
* `git revert` creates a new commit that reverses an earlier commit.
* `git reset` moves a branch reference and can change the staging area or working tree.
* `git reflog` helps investigate recent local reference movements.

Understanding these differences is essential for safe Git operations in DevOps work.

---

## Chapter 6: Final Verification

### My Learning Experience

At the end of the project, I reviewed the commit graph, branches, repository status, and local reference history.

I used:

```bash
git log --graph --all --oneline
git log --all --graph --all --oneline --decorate
git branch
git log
git reflog
git status
git push -u origin main
```

These commands helped me inspect repository history and verify the current working-tree state.

A clean `git status` is a useful checkpoint, but it does not prove that every task has been completed. I must also inspect the remote branches and tags when the assignment requires them.

### Final Learning Summary

| Topic                     | My Practice                                                   |
| ------------------------- | ------------------------------------------------------------- |
| Repository initialization | `git init`                                                    |
| Staging and commits       | `git add`, `git commit`                                       |
| Change inspection         | `git status`, `git diff`                                      |
| Ignore rules              | `.gitignore`, `git check-ignore`                              |
| Branching                 | `git branch`, `git switch`                                    |
| Merging                   | `git merge`                                                   |
| Remote repositories       | `git remote`, `git clone`                                     |
| Remote synchronization    | `git pull`, `git push`                                        |
| Fetch workflow            | Concept learned; separate practical verification still needed |
| Temporary changes         | `git stash`, `git stash pop`                                  |
| File operations           | `git mv`, `git rm`                                            |
| Undo and recovery         | `git revert`, `git reset`, `git reflog`                       |
| Version tags              | Created a local tag; remote publication should be verified    |
| Final verification        | `git log`, `git branch`, `git status`                         |

## Final Reflection

This project gave me practical experience with Git and GitHub. I learned how to manage changes, create commits, organize work into branches, resolve conflicts, connect a local repository to GitHub, and investigate repository history.

The most important lesson was that Git commands can have different effects on local work, commit history, and shared remote branches. I should inspect the repository state before running commands that may discard changes or rewrite history.

I will continue practicing these workflows in separate test branches and repositories before applying them to shared projects or production environments.
