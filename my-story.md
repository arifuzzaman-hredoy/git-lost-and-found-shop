Challenge/Chapter 1:

The working directory is the primary location where all project related work is executed and all project files are contained. 'Working' signifies the functional workspace, while 'directory' denotes a specific folder or location. Therefore, the specific folder in which we manage our project files is referred to as the working directory.
The staging area is where project files are moved when we add them for tracking. Staging a file means preparing it to be recorded into the Git history. When a new file is created or modified in the working directory, its changes are not automatically tracked by Git. For this reason, we must stage the file. Once staged, its status is updated and captured by Git.
The local repository is created when we initialize Git within a project using the git init command. This action generates a hidden .git folder inside the project, which stores and maintains the complete history and metadata of the local repository.
Additionally, we can verify whether files are staged or unstaged using the git status command, and we can review the exact modifications made to the files by using the git diff command.

this is my working  directory  :
/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop

cmd use :
git config list
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
git commit -m "add README.md my-story.md and record.md in staged"
git diff --staged record.md
git commit -m "Resolv Item data in record.md"
git add bazar-notes.txt
git commit -m "Add bazar list"
git rm --cached bazar-notes.txt
git restore --staged .
git commit -m "Remove bazar list file form repo"






Challange 2 :

Essentially, we include files in the .gitignore file that we do not want to push to the remote repository or move into the staging area. If a file is listed inside the .gitignore file, Git will completely bypass it, and it will not appear in the git status output.
However, if we stage a file before adding it to the .gitignore file, it will remain tracked in the staging area and will not be ignored. To fix this and ensure Git ignores the file, we must unstage (remove it from the index) by caching it. Once unstaged, Git will properly respect the ignore rules for that file.
To verify whether a file is actively being ignored, we can use the command git check-ignore -v <path> for a specific file, or use git status --ignored to view a comprehensive list of all ignored files in the project.
Additionally, once we unstage the file and apply the ignore rule, we will see that it no longer appears in the staging area. We can also confirm this by reviewing the commit history; if the file has been correctly untracked, it will no longer show up in subsequent commit file lists or version histories.

cmd:
git status
git add my-story.md
git commit -m "Explai Challenge of Chapter 1 in my story file"
git add .gitignore terminal-history.md
git commit -m "Add .gitignore and Terminal-History File"
cat .gitignore
git add draft/private-customers.txt
git commit -m "Add private-customers.txt file into staged and with blank .gitignore file"
git rm --cached draft/private-customers.txt
git commit -m "Again unstaged private-customers.txt file and add something in gitignore file also again staged gitignore file again"
git status --ignored
git check-ignore -v draft/private-customers.txt



Challange/Chapter 3 :

First of all, what are branches? A branch represents an isolated, independent line of development within a codebase. Branches are primarily utilized because a single software project often involves multiple developers or engineering teams working simultaneously. To facilitate this parallel workflow, separate branches are created for individual developers. This allows them to make changes independently within their respective branches and then push or submit a pull request. Consequently, the maintainer of the main branch can review and merge those changes. Once merged, the code from these development branches is integrated directly into the main branch. In essence, branching allows multiple developers to collaborate on the same project without interfering with each other's work.
A branch conflict (merge conflict) occurs when overlapping changes are made to the exact same part of a file. For instance, if I modify a specific line in an index.html file within my branch, and another developer modifies the exact same line of that same file in their branch, and we both commit and push our respective changes, a conflict will arise during the merge process. Whether merging into the main branch or between development branches, Git gets conflicted because two different modifications have been introduced to the same line.
When you attempt to merge, Git cannot automatically resolve this and will mark the file as conflicted, embedding conflict markers directly into the code. Upon opening the conflicted file in a code editor, you will typically be presented with four options to resolve it: keep the current changes (Incoming Change), keep the existing main branch changes (Current Change), accept both changes, or perform a custom edit. If you select any of the first three automated options, the conflict markers are automatically removed by the editor. However, if you choose to make a custom change, you must manually resolve the code differences and delete the conflict markers yourself before finalizing the merge.

cmd:
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
git commit -m "message"
git reset HEAD~1 lost-student-id.md
git log
git log --graph --oneline --all --decorate
git merge book-recoard master
git merge master wallet-record
git merge wallet-record master

Challange 4 :

First of all, what is the difference between git fetch and git pull?
• git fetch downloads the latest changes from a remote branch (such as origin/main or origin/master) and stores them in your local repository. However, it does not automatically merge these changes into your active local working directory. It simply updates your local repository's history with the remote changes, keeping them isolated until you decide to integrate them.
• git pull downloads the remote changes and immediately merges them directly into your current local working directory.
Therefore, the primary difference is that git fetch only retrieves the data without altering your local files, whereas git pull combines fetching and merging into a single step.
The core distinction between git push and git pull revolves around the direction of data transfer.
• git push uploads your locally committed changes to a remote repository like GitHub, updating the specified remote branch with your latest work.
• git pull downloads the updated code from a remote branch to bring your local working directory up to date. In short, git push sends your code to the cloud, while git pull brings code down from the cloud.
Finally, the difference between a local branch and a remote-tracking branch lies in their function and editability.
• A local branch is your active working workspace where you continuously make code changes, commit updates, and maintain your active development history. You have full read and write permissions on local branches.
• A remote-tracking branch is a read-only reference point that mirrors the state of the branch in the remote repository (e.g., origin/main). When you perform a git fetch, the incoming data is stored inside these remote-tracking branches. You cannot directly write code or make commits to a remote-tracking branch; it serves purely as a pointer to let your local system know what exists on GitHub or the remote server.

Currently, in my project workflow, I bypassed the git fetch command and utilized git pull directly. First, a new branch named feature was created from Rafi's computer. After making several code modifications on Rafi's machine within that branch, the updated changes were pushed to GitHub under the remote feature branch. Subsequently, from my local machine, I executed a pull command targeted at that specific remote feature branch. As a result of this action, the updated remote code was brought down and automatically merged into my local workspace.

cmd:
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git remote -v
git status
git add .gitignore
git commit -m "message"
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
git merge main main
git add lost-wallet.md
git commit -m "message"
git pull origin feature-branch
git branch -M feature-branch
git push origin feature-branch:feature-branch


Challange 5 :

First of all, what are branches? A branch represents an isolated, independent line of development within a codebase. Branches are primarily utilized because a single software project often involves multiple developers or engineering teams working simultaneously. To facilitate this parallel workflow, separate branches are created for individual developers. This allows them to make changes independently within their respective branches and then push or submit a pull request. Consequently, the maintainer of the main branch can review and merge those changes. Once merged, the code from these development branches is integrated directly into the main branch. In essence, branching allows multiple developers to collaborate on the same project without interfering with each other's work.
A branch conflict (merge conflict) occurs when overlapping changes are made to the exact same part of a file. For instance, if I modify a specific line in an index.html file within my branch, and another developer modifies the exact same line of that same file in their branch, and we both commit and push our respective changes, a conflict will arise during the merge process. Whether merging into the main branch or between development branches, Git gets conflicted because two different modifications have been introduced to the same line.
When you attempt to merge, Git cannot automatically resolve this and will mark the file as conflicted, embedding conflict markers directly into the code. Upon opening the conflicted file in a code editor, you will typically be presented with four options to resolve it: keep the current changes (Incoming Change), keep the existing main branch changes (Current Change), accept both changes, or perform a custom edit. If you select any of the first three automated options, the conflict markers are automatically removed by the editor. However, if you choose to make a custom change, you must manually resolve the code differences and delete the conflict markers yourself before finalizing the merge. This covers the essentials of merging and conflict markers.
Moving on, git stash is used to temporarily hide or shelve your current changes. It does not move the files to the staging area, nor does git status display them as untracked files anymore. Instead, it saves them in a temporary storage state from which they can be easily restored later. This command is highly useful when you are in the middle of a task but need to immediately switch to another branch or work on a different issue without committing incomplete work.
Next is the git revert command, which is used to safely undo a specific commit in your repository history. By using git revert, you create a entirely new commit that introduces the exact opposite changes of the target commit, effectively rolling back the project state to the previous commit without altering existing history.
The git reset command is a powerful tool with multiple modes used to undo changes.
• git reset --soft undoes the commit but keeps your changes intact, leaving the modified files in the staging area (tracked state).
• git reset --mixed (the default mode) undoes the commit and unstages the files, moving the changes back to your working directory as untracked or modified files.
• git reset --hard completely deletes the commit, clears the staging area, and discards all modifications from your working directory, resetting everything to the exact state of the previous commit.
Furthermore, git reflog acts like a safety net or a recycle bin (similar to the Windows Recycle Bin or Trash). If you accidentally delete a commit or execute a destructive git reset --hard, you can recover your lost data using the reflog. git reflog functions like a diary that comprehensively logs every single action, transaction, and state change within your Git repository—capturing both successful and unsuccessful actions. While the standard git log only displays the successful commit history, git reflog records absolutely everything, allowing you to restore files even after a hard reset.
In my specific project workflow, I utilized git stash to move my incomplete files to a safe, temporary space. This allowed me to switch to a different branch and complete my work there. After committing the changes on that branch, I returned to my original workspace and used the pop method (git stash pop) to successfully restore my shelved changes and finalize the commit.
On the other hand, I applied the git reset --hard command to completely delete a specific commit on the main branch, as well as on two other separate branches I had created. Finally, I used git reflog to inspect the full repository ledger. Because commits contain critical data, performing a hard reset carries a significant risk of data loss. While it is acceptable to experiment with these destructive commands within a test assignment or a practice project to learn how they work, executing a hard reset directly on the main branch should strictly be avoided in a real-world enterprise production environment.

cmd:
git stash -m "Uncompleted work"
git stash pop
git mv record.md all-record.md
git rm lost-student-id.md
git add lost-book.md
git commit -m "message"
git log
git log --oneline
git log --stat
git reset lost-book.md
git revert HEAD~1 --no-edit
git reset --hard HEAD~1
git push origin main
git push origin main --force
git switch -c test-hard
git switch main
git switch -c recovery-test
git tag -a v1.0.0 -m "Release Version are ready"
git reflog
git branch

Chapter 6 :

Yes, I have confirmed everything is oke right now

cmd:
git log --graph --all --oneline
git log -a --graph --all --oneline
git log --graph --all --oneline --decorate
git branch
git log
git reflog
git status
git push -u origin main

