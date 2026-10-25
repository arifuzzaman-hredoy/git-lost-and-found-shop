# OSTAD | DEVOPS | GIT ASSIGNMENT 01

# The Lost-and-Found Shop
*A story-driven journey through Git and GitHub*

**Total Marks:** 100  
**Difficulty:** Beginner → Early Intermediate  
**Submission:** GitHub repository link + `my-story.md`

## Recommended GitHub Repository Name

`git-lost-and-found-shop`

## GitHub Repository Description

> Story-driven Git and GitHub practice project covering repository setup, commits, `.gitignore`, branching, merging conflicts, remotes, clone, fetch, pull, push, stash, history, recovery, and tags.

---

## The Story

A small community has opened a **Lost-and-Found Shop**. People bring in lost books, student ID cards, wallets, and other items, and the shop maintains a record of each item so it can be returned to its owner.

You have been asked to manage the shop's digital record book using Git. Your teammate Rafi will later contribute from another computer. Some temporary notes and private customer information must never be published to GitHub.

Your job is to build the repository step by step, keep a meaningful history, collaborate safely, and prove that you understand how Git works. **This assignment gives you tasks and challenges—not the commands or full solutions. Find the commands yourself.**

## Chapter 1 — Opening the Shop (15 Marks)

The shop is opening for the first time. You need to create its record book and establish a reliable history.

### Tasks
- Set your Git author name and email.
- Create a new local repository named `lost-found-shop`.
- Add a `README.md` explaining the purpose of the shop.
- Add a `records.md` containing at least three fictional lost-item records.
- Make a small mistake in one record, inspect the changes, correct it, and inspect the changes again.
- Stage the intended files and review what is staged before committing.
- Create meaningful commits that describe the changes.
- Create a temporary `bazar-notes.txt` file, stage it, then remove it from the staging area without deleting the file.

### Challenge
In `my-story.md`, explain the difference between the working directory, staging area, and local repository. Describe how you checked unstaged and staged changes.

## Chapter 2 — Protecting Private Notes (10 Marks)

The shop manager gives you private customer notes and temporary files. These should remain on your computer and must not be included in the public repository.

### Tasks
- Create a fictional `private-customers.txt` file and a few temporary files or a draft directory.
- Create and configure a `.gitignore` file so private notes and the chosen temporary files are excluded.
- Verify which files are ignored and which files are tracked.
- Check that the private file is not included in the repository's tracked files.
- Explain what happens if a file is already tracked before you add a matching ignore rule.

### Challenge
Show how you verified that the ignore rules work. Use only fictional data; never put real personal information, passwords, tokens, or secrets in this repository.

**Security rule:** Accidentally publishing a real secret is a serious mistake. Do not push confidential information to GitHub.

## Chapter 3 — The New Records Team (20 Marks)

The shop gets busier, so the manager asks you to work on new item categories separately. Avoid mixing unrelated work into one commit.

### Tasks
- Create a separate branch for adding book records.
- Add `lost-book.md` and `lost-student-id.md` in separate meaningful commits.
- Merge the completed work into the main branch.
- Create another branch to fix an incorrect date in a wallet record.
- Make a deliberate change to the same line on two branches so that a merge conflict occurs.
- Resolve the conflict carefully, complete the merge, and verify the final content.
- Review the branch list and commit graph.

### Challenge
Explain why branches are useful, how the conflict happened, and how you confirmed that the conflict markers were removed.

## Chapter 4 — Rafi Joins from Another Computer (20 Marks)

Rafi wants to contribute a lost-wallet record from his own computer. The shop's records now need to be shared through GitHub.

### Tasks
- Create a GitHub repository for your project and connect your local repository to it.
- Publish the main branch to GitHub.
- Clone the repository into a separate directory to represent Rafi's computer.
- In the cloned copy, add `lost-wallet.md`, commit the change, and publish it.
- In your original working copy, retrieve the remote updates and inspect the remote-tracking branch.
- Integrate Rafi's change into your local main branch.
- Make another change in your original copy and publish it.
- Update the cloned copy so it receives the latest change.
- Publish at least one feature branch to GitHub.

### Challenge
In `my-story.md`, explain the differences between:
- `fetch` and `pull`
- `push` and `pull`
- a local branch and a remote-tracking branch

Do not merely write definitions—describe what happened in your own repository.

## Chapter 5 — An Emergency at the Shop (20 Marks)

A customer is waiting, but your book-record work is incomplete. At the same time, you discover an urgent wallet-record bug. You must pause one task, fix the other, and then safely resume your original work.

### Tasks
- Make an incomplete change to `lost-book.md` and temporarily set it aside without committing it.
- Switch to the wallet-fix task, correct the issue, and commit the fix.
- Return to your earlier work and restore the changes you set aside.
- Rename a tracked file using Git-aware file operations.
- Remove an obsolete tracked file using Git.
- Inspect the repository history, including file-level change summaries and a particular commit's details.
- Create a test change that can be safely undone, then undo it while preserving an understandable history.
- Create a separate branch named `recovery-test` and practise a destructive reset only on that test branch.
- Create a version tag named `v1.0.0`.
- Inspect the reference log to understand how Git records movements of branch references.

### Challenge
Explain when you would use stash, revert, reset, and reflog. Describe the risk of destructive operations and why you used a separate test branch.

**Safety rule:** Never run a destructive reset on your main branch or on work you need to keep.

## Chapter 6 — Final Shop Audit (5 Marks)

The manager is ready to review the shop's record system.

### Tasks
- Confirm the working tree is clean, or clearly document any intentional remaining changes.
- Review local branches, remote branches, tags, and commit history.
- Confirm that the required records and README are present.
- Confirm that private and temporary files have not been published.
- Make sure the repository has a clear, useful description on GitHub.

## Submission Requirements (10 Marks)

Submit all of the following:

1. **GitHub repository link** for `git-lost-and-found-shop`.
2. A `my-story.md` file inside the repository documenting:
   - What you did in each chapter.
   - The important commands you discovered and used.
   - What you learned and any mistakes you corrected.
   - Answers to each chapter's challenge.
   - Selected screenshots or terminal outputs as evidence.
3. At least **12 meaningful commits**. Avoid making many meaningless commits just to reach the number.
4. At least **3 useful local branches** used during the exercise.
5. At least one feature branch published to GitHub.
6. Evidence of the final branch list, commit graph, tags, and repository status in your report.

## Marking Scheme

| Section | Marks |
|---|---:|
| Chapter 1 — Opening the Shop | 15 |
| Chapter 2 — Protecting Private Notes | 10 |
| Chapter 3 — The New Records Team | 20 |
| Chapter 4 — Rafi Joins from Another Computer | 20 |
| Chapter 5 — An Emergency at the Shop | 20 |
| Chapter 6 — Final Shop Audit | 5 |
| Submission quality and evidence | 10 |
| **Total** | **100** |

## Final Reminder

This is a practical assignment. Do not copy a ready-made solution. Discover the commands, run them, inspect the results, and explain what happened in your own words. Use fictional data only and never publish secrets.
