Challenge 1:

The working directory is the primary location where all project related work is executed and all project files are contained. 'Working' signifies the functional workspace, while 'directory' denotes a specific folder or location. Therefore, the specific folder in which we manage our project files is referred to as the working directory.
The staging area is where project files are moved when we add them for tracking. Staging a file means preparing it to be recorded into the Git history. When a new file is created or modified in the working directory, its changes are not automatically tracked by Git. For this reason, we must stage the file. Once staged, its status is updated and captured by Git.
The local repository is created when we initialize Git within a project using the git init command. This action generates a hidden .git folder inside the project, which stores and maintains the complete history and metadata of the local repository.
Additionally, we can verify whether files are staged or unstaged using the git status command, and we can review the exact modifications made to the files by using the git diff command.




Challange 2 :

Essentially, we include files in the .gitignore file that we do not want to push to the remote repository or move into the staging area. If a file is listed inside the .gitignore file, Git will completely bypass it, and it will not appear in the git status output.
However, if we stage a file before adding it to the .gitignore file, it will remain tracked in the staging area and will not be ignored. To fix this and ensure Git ignores the file, we must unstage (remove it from the index) by caching it. Once unstaged, Git will properly respect the ignore rules for that file.
To verify whether a file is actively being ignored, we can use the command git check-ignore -v <path> for a specific file, or use git status --ignored to view a comprehensive list of all ignored files in the project.
Additionally, once we unstage the file and apply the ignore rule, we will see that it no longer appears in the staging area. We can also confirm this by reviewing the commit history; if the file has been correctly untracked, it will no longer show up in subsequent commit file lists or version histories.

Challange 3 :

First of all, what are branches? A branch represents an isolated, independent line of development within a codebase. Branches are primarily utilized because a single software project often involves multiple developers or engineering teams working simultaneously. To facilitate this parallel workflow, separate branches are created for individual developers. This allows them to make changes independently within their respective branches and then push or submit a pull request. Consequently, the maintainer of the main branch can review and merge those changes. Once merged, the code from these development branches is integrated directly into the main branch. In essence, branching allows multiple developers to collaborate on the same project without interfering with each other's work.
A branch conflict (merge conflict) occurs when overlapping changes are made to the exact same part of a file. For instance, if I modify a specific line in an index.html file within my branch, and another developer modifies the exact same line of that same file in their branch, and we both commit and push our respective changes, a conflict will arise during the merge process. Whether merging into the main branch or between development branches, Git gets conflicted because two different modifications have been introduced to the same line.
When you attempt to merge, Git cannot automatically resolve this and will mark the file as conflicted, embedding conflict markers directly into the code. Upon opening the conflicted file in a code editor, you will typically be presented with four options to resolve it: keep the current changes (Incoming Change), keep the existing main branch changes (Current Change), accept both changes, or perform a custom edit. If you select any of the first three automated options, the conflict markers are automatically removed by the editor. However, if you choose to make a custom change, you must manually resolve the code differences and delete the conflict markers yourself before finalizing the merge.

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


Challange 5 :

