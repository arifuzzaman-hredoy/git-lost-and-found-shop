# Git Lost and Found Shop — Learning Notes

A chapter-wise record of Git and GitHub practice for the **Git Lost and Found Shop** project.

## Project Working Directory

```text
/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop
```

> This path is specific to the original computer. Use the path where the repository is actually stored on your own machine.

---

## Chapter 1 — Git Basics

### Key Concepts

**Working directory:** The project folder where files are created, edited, and organized.

**Staging area:** The area where selected changes are prepared for the next commit. Use `git add` to stage changes.

**Local repository:** Git stores repository metadata and commit history in the hidden `.git` directory. The `git init` command initializes a repository in the current directory.

Use `git status` to check the state of files and `git diff` to inspect changes that have not yet been staged. Use `git diff --staged` to inspect staged changes.

### Commands Used

```bash
git config --list
git config --global user.name "Arifuzzaman Hredoy"
git config --global user.email "arifuzzamanhredoy@gmail.com"

git init
ls -l
ls -la
git status

git add README.md my-story.md record.md
git log
git diff
git diff --staged
git diff --staged my-story.md

git commit -m "Add README, story, and record files"
git diff --staged record.md
git commit -m "Resolve item data in record.md"

git add bazar-notes.txt
git commit -m "Add bazar list"
git rm --cached bazar-notes.txt
git restore --staged .
git commit -m "Remove bazar list file from repository"
```

**Notes:**
- `git config --list` is the standard command for listing Git configuration.
- `git rm --cached <file>` removes a file from Git's index but keeps the local copy. It does not, by itself, remove the file from earlier commits.
- `git restore --staged .` unstages staged changes; it does not delete the files.

---

## Chapter 2 — Ignoring Files with `.gitignore`

### Key Concepts

The `.gitignore` file specifies untracked files and paths that Git should ignore. Ignored files generally do not appear in the normal `git status` output.

Adding a file to `.gitignore` does **not** automatically stop Git tracking a file that is already tracked. To stop tracking a file while keeping it on disk, use:

```bash
git rm --cached <path>
```

Use `git check-ignore -v <path>` to identify the ignore rule matching a path. Use `git status --ignored` to show ignored files.

### Commands Used

```bash
git status
git add my-story.md
git commit -m "Explain Chapter 1 challenge in my story file"

git add .gitignore terminal-history.md
git commit -m "Add .gitignore and terminal history file"

cat .gitignore

git add draft/private-customers.txt
git commit -m "Add private customers file"

git rm --cached draft/private-customers.txt
git commit -m "Stop tracking private customers file and update gitignore"

git status --ignored
git check-ignore -v draft/private-customers.txt
```

**Important:** Ensure `.gitignore` contains the correct rule for the file, for example:

```gitignore
draft/private-customers.txt
```

Do not commit passwords, API keys, private customer data, or other secrets. If a secret has already been committed, adding it to `.gitignore` does not remove it from Git history.

---

## Chapter 3 — Branching and Merging

### Key Concepts

A **branch** is a movable reference to a line of development. Branches let you develop changes separately and integrate them later.

A **merge conflict** can occur when Git cannot automatically combine changes—for example, when different branches change overlapping lines in the same file. Resolve the conflict in the affected file, remove conflict markers (`<<<<<<<`, `=======`, and `>>>>>>>`), then stage the resolved file and complete the merge.

### Commands Used

```bash
git branch
git branch book-recoard
git branch wallet-record

git switch book-recoard
git switch master
git switch wallet-record

touch lost-book.md
touch lost-student-id.md

git add lost-book.md lost-student-id.md
git add my-story.md terminal-history.md
git commit -m "Add lost-and-found records"

git reset HEAD~1 -- lost-student-id.md

git log
git log --graph --oneline --all --decorate
```

### Merge Syntax

To merge one branch **into the branch you are currently on**, switch to the destination branch first and then merge the source branch:

```bash
git switch master
git merge book-recoard

git switch master
git merge wallet-record
```

The original notes included these commands:

```bash
git merge book-recoard master
git merge master wallet-record
git merge wallet-record master
```

These are not the usual syntax for merging one named branch into another. Use the destination-branch workflow shown above. Also note that some repositories use `main` instead of `master`; use the branch name that actually exists in your repository.

---

## Chapter 4 — GitHub and Remote Repositories

### `git fetch` vs. `git pull`

- `git fetch` downloads remote updates and updates remote-tracking references. It does not automatically merge those changes into the current branch.
- `git pull` fetches updates and then integrates them into the current branch, usually by merging or rebasing depending on configuration.

### `git push` vs. `git pull`

- `git push` sends local commits to a remote repository.
- `git pull` downloads remote changes and integrates them into the current local branch.

### Local Branch vs. Remote-Tracking Branch

A **local branch**, such as `main`, is a branch you can check out and commit to. A **remote-tracking branch**, such as `origin/main`, records the state of a branch observed on the remote. Fetching updates remote-tracking references.

### Commands Used

Replace `USERNAME` and `REPO` with the correct GitHub username and repository name.

```bash
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git remote -v
git status

git add .gitignore
git commit -m "Update gitignore"
git add .
git push -u origin main

cd ..
mkdir rafi-computer
cd rafi-computer

ls
ls -a

git clone https://github.com/USERNAME/REPO.git
cd git-lost-and-found-shop
code .

git pull origin main
git add lost-wallet.md
git commit -m "Update lost wallet record"
git pull origin feature-branch
git push origin feature-branch:feature-branch
```

**Notes:**
- Run `git remote add origin ...` only if the remote named `origin` does not already exist. Check with `git remote -v`.
- `git pull origin feature-branch` integrates the remote `feature-branch` into the **currently checked-out local branch**. To work on a local feature branch, use `git switch feature-branch` first, or create a tracking branch if needed.
- `git merge main main` is not a normal merge workflow and has been omitted from the recommended command sequence.
- `git branch -M feature-branch` renames the current local branch; it does not simply switch to an existing feature branch.

---

## Chapter 5 — Stash, Undo, Recovery, and Tags

### Key Concepts

**`git stash`:** Temporarily saves eligible uncommitted changes so you can work on something else. Use `git stash pop` to reapply the latest stash and remove it from the stash list if the application succeeds. Untracked files are not included by default; use `git stash -u` if you also need to stash untracked files.

**`git revert`:** Creates a new commit that reverses the changes introduced by an earlier commit. It is generally safer for shared history.

**`git reset`:**
- `git reset --soft <commit>` moves the current branch reference while keeping changes staged.
- `git reset --mixed <commit>` (the default mode) moves the branch reference and leaves changes unstaged in the working directory.
- `git reset --hard <commit>` moves the branch reference and resets the index and working tree. Uncommitted changes can be lost.

**`git reflog`:** Shows recent movements of local references, which can help locate commits after a reset or branch movement. It is not a permanent backup, so do not rely on it as the only recovery method.

### Commands Used

```bash
git stash -m "Uncompleted work"
git stash pop

git mv record.md all-record.md
git rm lost-student-id.md
git add lost-book.md
git commit -m "Update lost book record"

git log
git log --oneline
git log --stat

git reset -- lost-book.md
git revert HEAD~1 --no-edit
git reset --hard HEAD~1

git push origin main
git push origin main --force

git switch -c test-hard
git switch main
git switch -c recovery-test

git tag -a v1.0.0 -m "Release version ready"
git reflog
git branch
```

**Safety warning:** `git reset --hard HEAD~1` can discard uncommitted work and move the current branch back one commit. `git push --force` can overwrite remote history. Avoid these commands on shared branches unless you understand the impact and have coordinated with collaborators. Prefer `git push --force-with-lease` over `--force` when rewriting a remote branch is genuinely necessary.

**File rename note:** `git mv record.md all-record.md` is the complete rename command. A command such as `git mv record.md` is incomplete because it has no destination.

---

## Chapter 6 — Reviewing Repository History

### Commands Used

```bash
git log --graph --all --oneline
git log --all --graph --oneline
git log --graph --all --oneline --decorate
git branch
git log
git reflog
git status
git push -u origin main
```

### Final Check

Before pushing, check the current branch and working tree:

```bash
git branch --show-current
git status
git log --oneline -5
git remote -v
```

If the current branch is `main` and the remote is correctly configured, push with:

```bash
git push -u origin main
```

Only run the push if you intend to publish the current branch's commits to that remote.

---

## Quick Safety Checklist

- [ ] Confirm the repository and branch with `git status` and `git branch --show-current`.
- [ ] Review staged changes with `git diff --staged` before committing.
- [ ] Keep private data and secrets out of commits.
- [ ] Check the target branch before merging or pulling.
- [ ] Understand the consequences before using `git reset --hard` or force-pushing.
- [ ] Use descriptive commit messages.
