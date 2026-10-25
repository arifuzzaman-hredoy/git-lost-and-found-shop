# 🏪 The Lost-and-Found Shop

### My Git & GitHub Practice Project

Welcome to **The Lost-and-Found Shop** — my personal project for learning and practicing Git and GitHub through a story-driven workflow.

This project represents my journey from basic Git commands to repository management, branching, merging, conflict resolution, remote repositories, collaboration, and recovery techniques.

> **Project Type:** Personal Learning & Practice Project
> **Primary Focus:** Git and GitHub
> **Status:** Ongoing Learning Project

---

## 🎯 Project Objectives

The main goals of this project are to:

* Understand how Git tracks changes.
* Practice the working directory, staging area, and local repository.
* Create meaningful commits and maintain a useful history.
* Use `.gitignore` to exclude unnecessary files.
* Create and manage branches.
* Merge branches and resolve merge conflicts.
* Connect a local repository to GitHub.
* Practice cloning, fetching, pulling, and pushing.
* Temporarily save unfinished work with Git stash.
* Rename files and manage tracked files.
* Understand commit recovery, reset, revert, and reflog.
* Learn versioning with Git tags.
* Develop safe Git habits suitable for real-world DevOps workflows.

---

## 🧰 Tools & Technologies

| Tool                        | Purpose                   |
| --------------------------- | ------------------------- |
| Git                         | Version control           |
| GitHub                      | Remote repository hosting |
| Linux Terminal / WSL Ubuntu | Command-line practice     |
| Markdown                    | Documentation             |
| VS Code                     | Editing project files     |

---

## 📂 Project Structure

```text
git-lost-and-found-shop/
├── .gitignore
├── README.md
├── all-record.md
├── lost-book.md
├── lost-wallet.md
├── my-story.md
├── terminal-history.md
└── screenshort/
    ├── CodeBase.png
    └── Commit.png
```

*Note: This is the documented project structure. The actual repository contents may change as the project develops.*

---

## 📚 My Git Learning Chapters

### Chapter 1 — Git Fundamentals

* Initialize a repository.
* Configure Git identity.
* Inspect repository status.
* Stage and commit changes.
* Compare file changes using `git diff`.
* Understand the working directory, staging area, and local repository.

### Chapter 2 — `.gitignore` & File Tracking

* Create and update `.gitignore`.
* Exclude files and directories from Git tracking.
* Inspect ignored files.
* Understand the difference between ignoring a file and untracking an already tracked file.

### Chapter 3 — Branching & Merging

* Create and switch branches.
* Work on separate branches.
* Merge branches.
* Understand merge conflicts.
* Inspect the commit graph.

### Chapter 4 — Remote Repositories

* Connect a local repository to GitHub.
* Clone repositories.
* Inspect remote configurations.
* Understand the differences between `fetch`, `pull`, and `push`.
* Practice synchronizing local and remote branches.

### Chapter 5 — Stash, History & Recovery

* Temporarily save unfinished changes.
* Restore stashed work.
* Rename and remove tracked files.
* Inspect commit history and reflog.
* Understand the differences between `revert` and `reset`.
* Learn how to recover from mistakes safely.

### Chapter 6 — Tags & Final Verification

* Create and inspect Git tags.
* Review commit history.
* Verify repository and branch status.
* Inspect remote configuration.
* Review important Git safety practices.

---

# 🛠️ Git Commands Reference — Commands I Practiced

This section organizes Git commands from my practice journey into categories for quick reference.

**Important:** Commands are examples from my learning notes and may require different filenames, branch names, or commit references depending on the repository's current state.

## 1. Git Configuration

Configure my Git identity and inspect settings.

```bash
git config --list
git config --global user.name "Arifuzzaman Hredoy"
git config --global user.email "your-email@example.com"
```

Replace the example email with your own Git commit email.

## 2. Repository Initialization & Inspection

Initialize a repository and inspect its state and history.

```bash
git init
git status
git status --ignored
git log
git log --oneline
git log --stat
git log --graph --oneline --all
git log --graph --all --oneline --decorate
git log --all --graph --oneline --decorate
git reflog
ls -l
ls -la
cat .gitignore
```

## 3. Staging & Change Inspection

Stage files, inspect changes, and unstage changes.

```bash
git add README.md my-story.md record.md
git add .gitignore terminal-history.md
git add .
git diff
git diff --staged
git diff --staged my-story.md
git diff --staged record.md
git restore --staged .
git reset HEAD~1 -- lost-student-id.md
```

**Note:** `git add .` can stage multiple changes under the current directory. Inspect `git status` before staging.

## 4. Commits

Save changes in the local repository.

```bash
git commit -m "Add README, learning story, and record files"
git commit -m "Resolve item data in record.md"
git commit -m "Add bazar list"
git commit -m "Document Chapter 1 in my learning story"
git commit -m "Add Git ignore rules and terminal history"
git commit -m "Update Git ignore configuration"
```

These are examples of commit messages from my practice notes. Use messages that accurately describe the changes being committed.

## 5. `.gitignore` & Ignored Files

Inspect ignore rules and stop tracking files without deleting local copies.

```bash
git check-ignore -v draft/private-customers.txt
git status --ignored
git rm --cached bazar-notes.txt
git rm --cached draft/private-customers.txt
```

Remember:

* `.gitignore` prevents eligible untracked files from being added accidentally.
* Adding a tracked file to `.gitignore` does not automatically untrack it.
* `git rm --cached` removes a file from Git's index while keeping the local copy.

## 6. Branch Management

List, create, rename, and switch branches.

```bash
git branch
git branch book-recoard
git branch wallet-record
git switch book-recoard
git switch master
git switch wallet-record
git branch -M main
git branch -M feature-branch
git switch -c test-hard
git switch main
git switch -c recovery-test
```

Some branch names above come from my original practice notes. Use the actual branch names available in your repository.

## 7. Merging & Conflict Resolution

Merge branches and inspect the resulting history.

```bash
git merge book-recoard master
git merge master wallet-record
git merge wallet-record master
git log --graph --oneline --all --decorate
```

Before merging, verify the current branch and repository status. The branch checked out when the merge starts is important to the result.

## 8. Remote Repositories & Collaboration

Connect a local repository to GitHub, clone a repository, and synchronize changes.

```bash
git remote add origin <repository-url>
git remote -v
git clone <repository-url>
git pull origin main
git pull origin feature-branch
git push -u origin main
git push origin feature-branch:feature-branch
```

Replace `<repository-url>` with the actual repository URL.

## 9. Fetch & Remote-Tracking Branches

Download remote updates and inspect remote-tracking branches.

```bash
git fetch origin
git branch -r
git branch -vv
git log --graph --oneline --all --decorate
```

**Key distinction:**

* `git fetch` downloads remote updates without merging them into the current branch.
* `git pull` fetches updates and then integrates them into the current branch.
* `git push` sends local commits to a remote repository.

A separate fetch-and-inspect exercise remains part of my future practice.

## 10. Stash — Temporarily Save Changes

Temporarily save unfinished changes and restore them later.

```bash
git stash -m "Uncompleted work"
git stash pop
```

After restoring a stash, inspect `git status` to confirm the result.

## 11. File Operations

Rename or remove tracked files.

```bash
git mv record.md all-record.md
git rm lost-student-id.md
git rm --cached bazar-notes.txt
```

* `git mv` renames or moves a tracked file.
* `git rm` removes a tracked file from the working tree and index.
* `git rm --cached` removes it from the index but keeps the local copy.

## 12. Undo & Recovery

Inspect commits and learn different recovery techniques.

```bash
git revert HEAD~1 --no-edit
git reset --hard HEAD~1
git reflog
git show <commit-hash>
git branch recovery-branch <commit-hash>
```

**Safety warning:**

* `git revert` creates a new commit that reverses the changes introduced by an earlier commit.
* `git reset` moves the current branch reference and can change the staging area or working tree, depending on the mode.
* `git reflog` helps inspect recent movements of local references.
* `git reset --hard` can permanently discard uncommitted changes.
* Never run destructive recovery commands without understanding their impact and checking for work that must be preserved.

Practice risky recovery operations in a dedicated test repository or branch.

## 13. Tags & Versioning

Create and inspect an annotated tag.

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git tag -n
git show v1.0.0
```

Publish a tag to GitHub when it points to the intended commit:

```bash
git push origin v1.0.0
```

A locally created tag is not automatically published to the remote repository. Verify the remote tag after pushing.

## 14. Final Verification

Review the repository before finishing a task.

```bash
git status
git branch
git branch -vv
git remote -v
git log --graph --all --oneline --decorate
git reflog
```

These commands help verify the working tree, branches, remotes, commit history, and recent recovery information.

---

## 📖 Project Documentation

* **[My Git Learning Story](./my-story.md)** — My learning journey, chapter summaries, and lessons learned.
* **[Terminal History](./terminal-history.md)** — A record of commands from my practice sessions.
* **[All Records](./all-record.md)** — Combined record information for the project.
* **[Lost Book](./lost-book.md)** — Practice data for the lost-book scenario.
* **[Lost Wallet](./lost-wallet.md)** — Practice data for the lost-wallet scenario.
* **[Screenshots](./screenshort/)** — Screenshots documenting parts of the project.

---

## 🧠 Lessons Learned

Through this project, I am learning that:

1. Git tracks changes, while GitHub hosts remote repositories.
2. A commit records a snapshot of tracked project content.
3. The staging area allows me to choose what goes into a commit.
4. `.gitignore` does not automatically stop tracking files already committed.
5. Branches support isolated work and controlled integration.
6. Merge conflicts require reviewing and resolving competing changes.
7. `fetch`, `pull`, and `push` have different purposes.
8. Stash is useful for temporarily saving unfinished work.
9. `revert`, `reset`, and `reflog` solve different history-management problems.
10. Local tags must be pushed separately to publish them to GitHub.
11. Reviewing repository status before risky operations helps prevent accidental data loss.
12. Files containing secrets or sensitive personal information should never be committed to a public repository.

---

## 🚀 Future Learning Goals

My next steps are to:

* Practice `git fetch` and compare remote-tracking branches.
* Learn to resolve more complex merge conflicts.
* Practice pull requests and code reviews.
* Learn branch protection and GitHub collaboration workflows.
* Practice safe recovery in a separate test repository.
* Verify and publish release tags.
* Learn GitHub Actions for automated testing and CI/CD.
* Integrate Git workflows into my DevOps portfolio projects.

---

## 👨‍💻 About This Project

This is a **personal Git and GitHub learning project**, created to improve my command-line skills, version-control knowledge, and confidence with real-world development workflows.

It is a practice project, not an official course assignment submission.

**Author:** Arifuzzaman Hredoy
**Project:** The Lost-and-Found Shop
**Focus:** Git, GitHub, Linux Terminal, and DevOps fundamentals
**Status:** Learning in progress

---

⭐ *Learning Git one command, one commit, and one lesson at a time.*
