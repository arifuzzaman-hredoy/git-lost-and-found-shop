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

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
* master
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch book-recoard
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoard
M       my-story.md
M       terminal-history.md
Switched to branch 'book-recoard'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
* book-recoard
  master
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ ls
README.md        draft        record.md
bazar-notes.txt  my-story.md  terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ touch lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ touch lost-student-id.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        lost-book.md
        lost-student-id.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add -m "Add lost book file in book-recoard branch"
error: unknown switch `m'
usage: git add [<options>] [--] <pathspec>...

    -n, --[no-]dry-run    dry run
    -v, --[no-]verbose    be verbose

    -i, --[no-]interactive
                          interactive picking
    -p, --[no-]patch      select hunks interactively
    -U, --unified <n>     generate diffs with <n> lines context
    --inter-hunk-context <n>
                          show context between diff hunks up to the specified number of lines
    -e, --[no-]edit       edit current diff and apply
    -f, --[no-]force      allow adding otherwise ignored files
    -u, --[no-]update     update tracked files
    --[no-]renormalize    renormalize EOL of tracked files (implies -u)
    -N, --[no-]intent-to-add
                          record only the fact that the path will be added later
    -A, --[no-]all        add changes from all tracked and untracked files
    --[no-]ignore-removal ignore paths removed in the working tree (same as --no-all)
    --[no-]refresh        don't add, only refresh the index
    --[no-]ignore-errors  just skip files which cannot be added because of errors
    --[no-]ignore-missing check if - even missing - files are ignored in dry run
    --[no-]sparse         allow updating entries outside of the sparse-checkout cone
    --[no-]chmod (+|-)x   override the executable bit of the listed files
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add -b "Add los
t book file in book-recoard branch"
error: unknown switch `b'
usage: git add [<options>] [--] <pathspec>...

    -n, --[no-]dry-run    dry run
    -v, --[no-]verbose    be verbose

    -i, --[no-]interactive
                          interactive picking
    -p, --[no-]patch      select hunks interactively
    -U, --unified <n>     generate diffs with <n> lines context
    --inter-hunk-context <n>
                          show context between diff hunks up to the specified number of lines
    -e, --[no-]edit       edit current diff and apply
    -f, --[no-]force      allow adding otherwise ignored files
    -u, --[no-]update     update tracked files
    --[no-]renormalize    renormalize EOL of tracked files (implies -u)
    -N, --[no-]intent-to-add
                          record only the fact that the path will be added later
    -A, --[no-]all        add changes from all tracked and untracked files
    --[no-]ignore-removal ignore paths removed in the working tree (same as --no-all)
    --[no-]refresh        don't add, only refresh the index
    --[no-]ignore-errors  just skip files which cannot be added because of errors
    --[no-]ignore-missing check if - even missing - files are ignored in dry run
    --[no-]sparse         allow updating entries outside of the sparse-checkout cone
    --[no-]chmod (+|-)x   override the executable bit of the listed files
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt
        lost-book.md
        lost-student-id.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md lost-student-id.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add 
lost book file in book-recoard branch"
[book-recoard 26ec7be] Add lost book file in book-recoard branch
 2 files changed, 8 insertions(+)
 create mode 100644 lost-book.md
 create mode 100644 lost-student-id.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add lost student ID file in book-recoard branch"
On branch book-recoard
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch master
M       my-story.md
M       terminal-history.md
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add my-story.md terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   my-story.md
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge book-recoards master
merge: book-recoards - not something we can merge
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* master
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoards
fatal: invalid reference: book-recoards
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoard
M       my-story.md
M       terminal-history.md
Switched to branch 'book-recoard'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add lost student ID file in book-recoard branch"
[book-recoard 6189006] Add lost student ID file in book-recoard branch
 2 files changed, 285 insertions(+), 2 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset HEAD~1 my-sotry.md terminal-history.md
Unstaged changes after reset:
M       terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   terminal-history.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset HEAD~1 my-sotry.md
Unstaged changes after reset:
M       terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   terminal-history.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset HEAD~1 lost-student-id.md
Unstaged changes after reset:
M       terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   terminal-history.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
* book-recoard
  master
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch master
M       terminal-history.md
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoard
error: Your local changes to the following files would be overwritten by checkout:
        terminal-history.md
Please commit your changes or stash them before you switch branches.
Aborting
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add terminal-history
fatal: pathspec 'terminal-history' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   terminal-history.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoard
Switched to branch 'book-recoard'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch book-recoard
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch book-recoard
Already on 'book-recoard'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch master
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge book-recoard master
Updating 6e89fd0..6189006
Fast-forward
 lost-book.md        |   4 +
 lost-student-id.md  |   4 +
 my-story.md         |  13 ++-
 terminal-history.md | 274 ++++++++++++++++++++++++++++++++++++++++++++-
 4 files changed, 293 insertions(+), 2 deletions(-)
 create mode 100644 lost-book.md
 create mode 100644 lost-student-id.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* master
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book
fatal: pathspec 'lost-book' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Add date into lost-book file"
[master 1cb4be9] Add date into lost-book file
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch wallet-record
Switched to branch 'wallet-record'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
  master
* wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch wallet-record
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge master wallet-record
Updating 6189006..1cb4be9
Fast-forward
 lost-book.md | 6 +++---
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch wallet-record
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "something chnage date in lost book file"
[wallet-record 4eff2e1] something chnage date in lost book file
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch master
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge wallet-record master
Updating 1cb4be9..4eff2e1
Fast-forward
 lost-book.md | 6 +++---
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* master
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch wallet-reocrd
fatal: invalid reference: wallet-reocrd
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch wallet-record
M       lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-sgit switch master
M       lost-book.md
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.txt
fatal: pathspec 'lost-book.txt' did not match any files
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Again something changes in date into master banch"
[master aee4552] Again something changes in date into master banch
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch wallet-record
Switched to branch 'wallet-record'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch wallet-record
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Again something c
hange into date in lost book in wallet-record branch"
[wallet-record 4fef5da] Again something change into date in lost book in wallet-record branch
 1 file changed, 3 insertions(+), 3 deletions(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch master
Switched to branch 'master'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge wallet-record master
Auto-merging lost-book.md
CONFLICT (content): Merge conflict in lost-book.md
Automatic merge failed; fix conflicts and then commit the result.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   lost-book.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Fix merge problem in lost book file for date issue"
[master b00e2b4] Fix merge problem in lost book file for date issue
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSec
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* master
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log
commit b00e2b40459ffeaecfae11e96d1903ee06db27e4 (HEAD -> master)
Merge: aee4552 4fef5da
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 10:50:30 2026 +0600

    Fix merge problem in lost book file for date issue

commit 4fef5da48686604e796a2de8194c6d4c1af547d2 (wallet-record)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 10:48:41 2026 +0600

    Again something change into date in lost book in wallet-record branch

commit aee4552f456963b5d60671a868ea657ca9ef9abc
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log --graph --oneline --all --decorate
*   b00e2b4 (HEAD -> master) Fix merge problem in lost book file for date issue
|\  
| * 4fef5da (wallet-record) Again something change into date in lost book in wallet-record branch
* | aee4552 Again something changes in date into master banch
|/  
* 4eff2e1 something chnage date in lost book file
* 1cb4be9 Add date into lost-book file
* 6189006 (book-recoard) Add lost student ID file in book-recoard branch
* 26ec7be Add lost book file in book-recoard branch
* 6e89fd0 Again unstaged private-customers.txt file and add something in gitignore file also again staged gitignore file again
* c73a6fe Add private-customers.txt file into staged and with blank .gitignore file
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 









Chapter 4 :

