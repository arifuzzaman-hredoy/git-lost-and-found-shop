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

