Chapter 1 Hostory:

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git config list
user.name=Arifuzzamman Hredoy
user.email=arifuzzamanhredoy@gmail.com
credential.https://github.com.helper=
credential.https://github.com.helper=!/usr/bin/gh auth git-credential
credential.https://gist.github.com.helper=
credential.https://gist.github.com.helper=!/usr/bin/gh auth git-credential
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git config --global user.name "Arifuzzaman Hredoy"
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git config --global user.email "arifuzzamanhredoy@gmail.com"
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git config list
user.name=Arifuzzaman Hredoy
user.email=arifuzzamanhredoy@gmail.com
credential.https://github.com.helper=
credential.https://github.com.helper=!/usr/bin/gh auth git-credential
credential.https://gist.github.com.helper=
credential.https://gist.github.com.helper=!/usr/bin/gh auth git-credential
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: will change to "main" in Git 3.0. To configure the initial branch name
hint: to use in all of your new repositories, which will suppress this warning,
hint: call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
hint:
hint: Disable this message with "git config set advice.defaultBranchName false"
Initialized empty Git repository in /mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop/.git/
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ ls -l
total 0
-rwxr--r-- 1 hredoy hredoy 0 Oct 25 08:34 my-story.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ ls -la
total 0
drwxr-xr-x 1 hredoy hredoy 4096 Oct 25 08:38 .
drwxr-xr-x 1 hredoy hredoy 4096 Oct 25 08:30 ..
drwxr-xr-x 1 hredoy hredoy 4096 Oct 25 08:38 .git
-rwxr--r-- 1 hredoy hredoy    0 Oct 25 08:34 my-story.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        my-story.md
        record.md

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add README.md my-story.md record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   my-story.md
        new file:   record.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   my-story.md
        new file:   record.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   record.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log
fatal: your current branch 'master' does not have any commits yet
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff
diff --git a/record.md b/record.md
index 8fde37b..82cfd34 100755
--- a/record.md
+++ b/record.md
@@ -1,4 +1,4 @@
 # There is Lost Item list 
 1. Black Color Wallet
-2. 2000 Cash Money
+2. 1500 Cash Money^M
 3. A student ID card
\ No newline at end of file
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged
diff --git a/README.md b/README.md
new file mode 100755
index 0000000..7aae55c
--- /dev/null
+++ b/README.md
@@ -0,0 +1 @@
+The perpouse of the shop is that we are small community has opened a Lost-and-Found Shop. People bring in lost books, student ID cards, wallets, and other items, and the shop maintains a record of each item so it can be returned to its owner.
\ No newline at end of file
diff --git a/my-story.md b/my-story.md
new file mode 100755
index 0000000..e69de29
diff --git a/record.md b/record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged my-record.md
fatal: ambiguous argument 'my-record.md': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged my-story.md
diff --git a/my-story.md b/my-story.md
new file mode 100755
index 0000000..e69de29
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged my-record.md
fatal: ambiguous argument 'my-record.md': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   my-story.md
        new file:   record.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "add README.md my-story.md and record.md in staged"
[master (root-commit) 81ed2f4] add README.md my-story.md and record.md in staged
 3 files changed, 5 insertions(+)
 create mode 100755 README.md
 create mode 100755 my-story.md
 create mode 100755 record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
* master
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff
diff --git a/record.md b/record.md
index 8fde37b..82cfd34 100755
--- a/record.md
+++ b/record.md
@@ -1,4 +1,4 @@
 # There is Lost Item list 
 1. Black Color Wallet
-2. 2000 Cash Money
+2. 1500 Cash Money^M
 3. A student ID card
\ No newline at end of file
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged my-record.md
fatal: ambiguous argument 'my-record.md': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   record.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add my-record.md
fatal: pathspec 'my-record.md' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged  
record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff
diff --git a/record.md b/record.md
index 8fde37b..82cfd34 100755
--- a/record.md
+++ b/record.md
@@ -1,4 +1,4 @@
 # There is Lost Item list 
 1. Black Color Wallet
-2. 2000 Cash Money
+2. 1500 Cash Money^M
 3. A student ID card
\ No newline at end of file
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   record.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git diff --staged  record.md
diff --git a/record.md b/record.md
index 8fde37b..82cfd34 100755
--- a/record.md
+++ b/record.md
@@ -1,4 +1,4 @@
 # There is Lost Item list 
 1. Black Color Wallet
-2. 2000 Cash Money
+2. 1500 Cash Money^M
 3. A student ID card
\ No newline at end of file
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   record.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Resolv Item data in record.md"
[master efcf536] Resolv Item data in record.md
 1 file changed, 1 insertion(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add bazar-notes.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add bazar list"
[master 9f50c63] Add bazar list
 1 file changed, 1 insertion(+)
 create mode 100755 bazar-notes.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git rm --cached bazar-notes.txt
rm 'bazar-notes.txt'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    bazar-notes.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    bazar-notes.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add bazard-notes.txt
fatal: pathspec 'bazard-notes.txt' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add bazar-notes
.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git restore --staged bazar-notes.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git restore --staged .
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git rm --cached bazar-notes.txt
rm 'bazar-notes.txt'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    bazar-notes.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Remove bazar list file form repo"
[master 17bf95c] Remove bazar list file form repo
 1 file changed, 1 deletion(-)
 delete mode 100755 bazar-notes.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 








Chapter 2 History :

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        bazar-notes.txt
        terminal-history.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add my-story.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Explai Challenge of Chapter 1 in my story file"
[master 9f3d926] Explai Challenge of Chapter 1 in my story file
 1 file changed, 8 insertions(+)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        bazar-notes.txt
        terminal-history.md

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore terminal-history
fatal: pathspec 'terminal-history' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
        new file:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add .gitignore and Terminal-History File"
[master 622dfc3] Add .gitignore and Terminal-History File
 2 files changed, 303 insertions(+)
 create mode 100755 .gitignore
 create mode 100755 terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        draft/

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cat .gitignnore
cat: .gitignnore: No such file or directory
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cat .gitignore 
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        draft/

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cat .gitignore 
draft/*
draft/private-customers.txthredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        draft/

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add draft/private-coustomers.txt
fatal: pathspec 'draft/private-coustomers.txt' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cd draft
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop/draft$ git add private-coustomers.txt
fatal: pathspec 'private-coustomers.txt' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop/draft$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add private-cus
tomers.txt
fatal: pathspec 'private-customers.txt' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cd draft
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop/draft$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add draft/private-customers.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   draft/private-customers.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore
        new file:   draft/private-customers.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add private-customers.txt file into staged and with blank .gitignore file"
[master c73a6fe] Add private-customers.txt file into staged and with blank .gitignore file
 2 files changed, 2 deletions(-)
 create mode 100755 draft/private-customers.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git rm --cached draft/private-customers.txt
rm 'draft/private-customers.txt'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore
        deleted:    draft/private-customers.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore
        deleted:    draft/private-customers.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        draft/

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore
        deleted:    draft/private-customers.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore
        deleted:    draft/private-customers.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Again unstaged private-customers.txt file and add something in gitignore file also again staged gitignore file again"
[master 6e89fd0] Again unstaged private-customers.txt file and add something in gitignore file also again staged gitignore file again
 2 files changed, 2 insertions(+)
 delete mode 100755 draft/private-customers.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git check-ignore -v
fatal: no path specified
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status --ignored
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

Ignored files:
  (use "git add -f <file>..." to include in what will be committed)
        draft/

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git check-ignore -v draft/private-customers.txt
.gitignore:2:draft/private-customers.txt        draft/private-customers.txt
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 






Chapter 3 History :

