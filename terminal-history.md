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

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch -M main
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* main
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git remote add origin https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git remote -v
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (fetch)
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (push)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bazar-notes.txt

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .gitignore
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "add bazard notes md file into gitignore file"
[main 6456c63] add bazard notes md file into gitignore file
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add .
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "now full project are ready for go Github in Chapter 4 middle position"
On branch main
nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin main
Enumerating objects: 53, done.
Counting objects: 100% (53/53), done.
Delta compression using up to 12 threads
Compressing objects: 100% (49/49), done.
Writing objects: 100% (53/53), 12.07 KiB | 94.00 KiB/s, done.
Total 53 (delta 19), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (19/19), done.
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project$ mkdir rafi-computer
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project$ cd rafi-computer
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ ls
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ ls -a
.  ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ git clone https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
Cloning into 'git-lost-and-found-shop'...
remote: Enumerating objects: 53, done.
remote: Counting objects: 100% (53/53), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 53 (delta 19), reused 53 (delta 19), pack-reused 0 (from 0)
Receiving objects: 100% (53/53), 12.07 KiB | 726.00 KiB/s, done.
Resolving deltas: 100% (19/19), done.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ ls
git-lost-and-found-shop
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ cd git-lost-and-found-shop
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ code .
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ ls 
README.md     lost-student-id.md  my-story.md  terminal-history.md
lost-book.md  lost-wallet.md      record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project$ ls
'Docker Ngrok Setup'         devops-task-manager
'Docker Ngrok Setup Mine'    git-lost-and-found-shop
 devops-real-world-project   rafi-computer
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project$ cd  git-lost-and-found-shop
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ ls
README.md        draft         lost-student-id.md  record.md
bazar-notes.txt  lost-book.md  my-story.md         terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (1/1), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 317 bytes | 6.00 KiB/s, done.
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
   6456c63..3ce1e57  main       -> origin/main
Updating 6456c63..3ce1e57
Fast-forward
 lost-wallet.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git merge main main
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-wallet.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-wallet
.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Some changes in lost-wallet file form main computer in main branch"
[main 6c2974b] Some changes in lost-wallet file form main computer in main branch
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 356 bytes | 27.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
   3ce1e57..6c2974b  main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin feature-branch
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 354 bytes | 8.00 KiB/s, done.
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            feature-branch -> FETCH_HEAD
 * [new branch]      feature-branch -> origin/feature-branch
Updating 6c2974b..6145ae2
Fast-forward
 lost-wallet.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 




------------Rafi's Computer------------



hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ touch lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        lost-wallet.md

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git branch
* main
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        lost-wallet.md

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ ls -la
total 68
drwxr-xr-x 1 hredoy hredoy  4096 Oct 25 11:53 .
drwxr-xr-x 1 hredoy hredoy  4096 Oct 25 11:52 ..
drwxr-xr-x 1 hredoy hredoy  4096 Oct 25 11:56 .git
-rwxr-xr-x 1 hredoy hredoy    53 Oct 25 11:52 .gitignore
-rwxr-xr-x 1 hredoy hredoy   242 Oct 25 11:52 README.md
-rw-r--r-- 1 hredoy hredoy   118 Oct 25 11:52 lost-book.md
-rw-r--r-- 1 hredoy hredoy    99 Oct 25 11:52 lost-student-id.md
-rw-r--r-- 1 hredoy hredoy    35 Oct 25 11:53 lost-wallet.md
-rwxr-xr-x 1 hredoy hredoy  4342 Oct 25 11:52 my-story.md
-rwxr-xr-x 1 hredoy hredoy    91 Oct 25 11:52 record.md
-rwxr-xr-x 1 hredoy hredoy 59467 Oct 25 11:52 terminal-history.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        lost-wallet.md

nothing added to commit but untracked files present (use "git add" to track)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git add lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   lost-wallet.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git commit -m "add lost wallet list file form rafi computer"
[main 3ce1e57] add lost wallet list file form rafi computer
 1 file changed, 1 insertion(+)
 create mode 100644 lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 337 bytes | 30.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
   6456c63..3ce1e57  main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git remote -v
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (fetch)
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (push)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git remote -v
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (fetch)
origin  https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git (push)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ cd ..
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ cat git-lost-and-found-shop
cat: git-lost-and-found-shop: Is a directory
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ ls git-lost-and-found-shop
README.md     lost-student-id.md  my-story.md  terminal-history.md
lost-book.md  lost-wallet.md      record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer$ cd git-lost-and-found-shop
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ cat lost-student-id.md
# Here is the list of lost Student ID card
1. Md Karim Uddin
2. Arifuzzamn Hredoy
3. Rifat Islamhredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ cat lost-wallet.md
# This is the list for lost wallet hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull -u origin main
error: unknown switch `u'
usage: git pull [<options>] [<repository> [<refspec>...]]

    -v, --[no-]verbose    be more verbose
    -q, --[no-]quiet      be more quiet
    --[no-]progress       force progress reporting
    --[no-]recurse-submodules[=<on-demand>]
                          control for recursive fetching of submodules

Options related to merging
    -r, --[no-]rebase[=(false|true|merges|interactive)]
                          incorporate changes by rebasing rather than merging
    -n                    do not show a diffstat at the end of the merge
    --[no-]stat           show a diffstat at the end of the merge
    --[no-]compact-summary
                          show a compact-summary at the end of the merge
    --[no-]log[=<n>]      add (at most <n>) entries from shortlog to merge commit message
    --[no-]signoff[=...]  add a Signed-off-by trailer
    --[no-]squash         create a single commit instead of doing a merge
    --[no-]commit         perform a commit if the merge succeeds (default)
    --[no-]edit           edit message before committing
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    --[no-]ff             allow fast-forward
    --ff-only             abort if fast-forward is not possible
    --[no-]verify         control use of pre-merge-commit and commit-msg hooks
    --[no-]verify-signatures
                          verify that the named commit has a valid GPG signature
    --[no-]autostash      automatically stash/stash pop before and after
    -s, --[no-]strategy <strategy>
                          merge strategy to use
    -X, --[no-]strategy-option <option=value>
                          option for selected merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    --[no-]allow-unrelated-histories
                          allow merging unrelated histories

Options related to fetching
    --[no-]all            fetch from all remotes
    -a, --[no-]append     append to .git/FETCH_HEAD instead of overwriting
    --[no-]upload-pack <path>
                          path to upload pack on remote end
    -f, --[no-]force      force overwrite of local branch
    -t, --[no-]tags       fetch all tags and associated objects
    -p, --[no-]prune      prune remote-tracking branches no longer on remote
    -j, --[no-]jobs[=<n>] number of submodules pulled in parallel
    --[no-]dry-run        dry run
    -k, --[no-]keep       keep downloaded pack
    --[no-]depth <depth>  deepen history of shallow clone
    --[no-]shallow-since <time>
                          deepen history of shallow repository based on time
    --[no-]shallow-exclude <ref>
                          deepen history of shallow clone, excluding ref
    --[no-]deepen <n>     deepen history of shallow clone
    --unshallow           convert to a complete repository
    --[no-]update-shallow accept refs that update .git/shallow
    --refmap <refmap>     specify fetch refmap
    -o, --[no-]server-option <server-specific>
                          option to transmit
    -4, --[no-]ipv4       use IPv4 addresses only
    -6, --[no-]ipv6       use IPv6 addresses only
    --[no-]negotiation-tip <revision>
                          report that we have only objects reachable from this object
    --[no-]show-forced-updates
                          check for forced-updates on all updated branches
    --[no-]set-upstream   set upstream for git pull/fetch

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull origin main
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 336 bytes | 9.00 KiB/s, done.
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
   3ce1e57..6c2974b  main       -> origin/main
Updating 3ce1e57..6c2974b
Fast-forward
 lost-wallet.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git branch -M feature-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git branch
* feature-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git add lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git commit -m "Change branch name form rafi's computer"
[feature-branch 6145ae2] Change branch name form rafi's computer
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git branch
* feature-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git pull origin future-branch:future-branch
fatal: couldn't find remote ref future-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git push origin future-branch:future-branch
error: src refspec future-branch does not match any
error: failed to push some refs to 'https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git branch
* feature-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ git push origin feature-branch:feature-branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 374 bytes | 37.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'feature-branch' on GitHub by visiting:
remote:      https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop/pull/new/feature-branch
remote: 
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
 * [new branch]      feature-branch -> feature-branch
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/rafi-computer/git-lost-and-found-shop$ 











Chapter 5 Terminal History :

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git config pull.rebase false
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md
        modified:   lost-wallet.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git pull origin main
From https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop
 * branch            main       -> FETCH_HEAD
Already up to date.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Solve problem that do in lost wallet section"
[main e2dea27] Solve problem that do in lost wallet section
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin main
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 5.58 KiB | 168.00 KiB/s, done.
Total 8 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 4 local objects.
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
   f416c5d..e2dea27  main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git stash -m  "Uncompleted work"
Saved working directory and index state On main: Uncompleted work
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-wallet.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-wallet.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-wallet.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-wallet.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Again solve the problem of lost wallet"
[main e66537a] Again solve the problem of lost wallet
 1 file changed, 2 insertions(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 353 bytes | 29.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
   e2dea27..e66537a  main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (4c98e4fbb2cf84229d1ad239c97a0e825bf5bf14)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git mv record.md
usage: git mv [-v] [-f] [-n] [-k] <source> <destination>
   or: git mv [-v] [-f] [-n] [-k] <source>... <destination-directory>

    -v, --[no-]verbose    be verbose
    -n, --[no-]dry-run    dry run
    -f, --[no-]force      force move/rename even if target exists
    -k                    skip move/rename errors
    --[no-]sparse         allow updating entries outside of the sparse-checkout cone

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git mv record.md all-record.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git rm lost-student
-id.md
rm 'lost-student-id.md'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    record.md -> all-record.md
        deleted:    lost-student-id.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record"
[main e96ff81] again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
 3 files changed, 7 insertions(+), 4 deletions(-)
 rename record.md => all-record.md (100%)
 delete mode 100644 lost-student-id.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log
commit e96ff81cd4c6b02fa3e6db382a5aca213eb2b917 (HEAD -> main)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 14:30:51 2026 +0600

    again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record

commit e66537abebc0a925ac84708b09599bf75b42ca67 (origin/main)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 14:25:31 2026 +0600

    Again solve the problem of lost wallet

commit e2dea27f18754e29584ad2b94c38ff24f38d4e72
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log --oneline
e96ff81 (HEAD -> main) again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
e66537a (origin/main) Again solve the problem of lost wallet
e2dea27 Solve problem that do in lost wallet section
1227763 Merge branch 'main' of https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop come code form github and also push new code form my computer
4a377c1 Chapter 4 is completed any add deatils into my story and terminal history
f416c5d Merge pull request #1 from arifuzzaman-hredoy/feature-branch
6145ae2 (origin/feature-branch) Change branch name form rafi's computer
6c2974b Some changes in lost-wallet file form main computer in main branch
3ce1e57 add lost wallet list file form rafi computer
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log stat
fatal: ambiguous argument 'stat': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log --stat
commit e96ff81cd4c6b02fa3e6db382a5aca213eb2b917 (HEAD -> main)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 14:30:51 2026 +0600

    again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record

 record.md => all-record.md | 0
 lost-book.md               | 7 +++++++
 lost-student-id.md         | 4 ----
 3 files changed, 7 insertions(+), 4 deletions(-)

commit e66537abebc0a925ac84708b09599bf75b42ca67 (origin/main)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 14:25:31 2026 +0600
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Chnage lost book item ICT to Social Science"
[main 4ea03f5] Chnage lost book item ICT to Social Science
 1 file changed, 1 insertion(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   lost-book.md

no changes added to commit (use "git add" and/or "git commit -a")
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git add lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git commit -m "Chnage lost book item Social Science to ICT"
[main 249520d] Chnage lost book item Social Science to ICT
 1 file changed, 1 insertion(+), 1 deletion(-)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset lost-book.md
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin 
main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 914 bytes | 53.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
   e66537a..249520d  main -> main
branch 'main' set up to track 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git revert HEAD~1 --no-edit
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset --hard HEAD~1
HEAD is now at 4ea03f5 Chnage lost book item ICT to Social Science
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push origin main
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push origin main --force
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop.git
 + 249520d...4ea03f5 main -> main (forced update)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* main
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch -c test-
hard
Switched to a new branch 'test-hard'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
  main
* test-hard
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset --hard HEAD~1
HEAD is now at e96ff81 again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch -c recovery-test 
Switched to a new branch 'recovery-test'
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reset --hard HEAD~1
HEAD is now at e96ff81 again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git tag -a v1.0.0 "Release Version are ready"
fatal: Failed to resolve 'Release Version are ready' as a valid ref.
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git tag -a v1.0.0 -m "Release Version are ready"
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reflog
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{0}: checkout: moving from recovery-test to main
e96ff81 (test-hard, recovery-test) HEAD@{1}: reset: moving to HEAD~1
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{2}: checkout: moving from main to recovery-test
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{3}: checkout: moving from test-hard to main
e96ff81 (test-hard, recovery-test) HEAD@{4}: reset: moving to HEAD~1
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{5}: checkout: moving from main to test-hard
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{6}: reset: moving to HEAD~1
249520d HEAD@{7}: commit: Chnage lost book item Social Science to ICT
4ea03f5 (HEAD -> main, tag: v1.0.0, origin/main) HEAD@{8}: commit: Chnage lost book item ICT to Social Science
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git push -u origin main
branch 'main' set up to track 'origin/main'.
Everything up-to-date
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 













Chapter 6 Terminal History :

hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log --graph --all --oneline
* e51473c (HEAD -> main, origin/main) Fully Complete Chapter 5
* 4ea03f5 (tag: v1.0.0) Chnage lost book item ICT to Social Science
* e96ff81 (test-hard, recovery-test) again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
* e66537a Again solve the problem of lost wallet
* e2dea27 Solve problem that do in lost wallet section
*   1227763 Merge branch 'main' of https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop come code form github and also push new code form my computer
|\  
| *   f416c5d Merge pull request #1 from arifuzzaman-hredoy/feature-branch
| |\  
* | | 4a377c1 Chapter 4 is completed any add deatils into my story and te
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log -a  --graph
 --all --oneline
* e51473c (HEAD -> main, origin/main) Fully Complete Chapter 5
* 4ea03f5 (tag: v1.0.0) Chnage lost book item ICT to Social Science
* e96ff81 (test-hard, recovery-test) again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
* e66537a Again solve the problem of lost wallet
* e2dea27 Solve problem that do in lost wallet section
*   1227763 Merge branch 'main' of https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop come code form github and also push new code form my computer
|\  
| *   f416c5d Merge pull request #1 from arifuzzaman-hredoy/feature-branch
| |\  
* | | 4a377c1 Chapter 4 is completed any add deatils into my story and te
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log --graph --all --oneline --decorate
* e51473c (HEAD -> main, origin/main) Fully Complete Chapter 5
* 4ea03f5 (tag: v1.0.0) Chnage lost book item ICT to Social Science
* e96ff81 (test-hard, recovery-test) again come start work and complete of lost book file by stash(pop) also remove lost student id file and rename record to all record
* e66537a Again solve the problem of lost wallet
* e2dea27 Solve problem that do in lost wallet section
*   1227763 Merge branch 'main' of https://github.com/arifuzzaman-hredoy/git-lost-and-found-shop come code form github and also push new code form my computer
|\  
| *   f416c5d Merge pull request #1 from arifuzzaman-hredoy/feature-branch
| |\  
* | | 4a377c1 Chapter 4 is completed any add deatils into my story and te
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git branch
  book-recoard
* main
  recovery-test
  test-hard
  wallet-record
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git log
commit e51473c9bd5c897acc02571f8c70a31264738a53 (HEAD -> main, origin/main)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 15:27:23 2026 +0600

    Fully Complete Chapter 5

commit 4ea03f5ccb8bf9beb97198154fec9dd9a4861258 (tag: v1.0.0)
Author: Arifuzzaman Hredoy <arifuzzamanhredoy@gmail.com>
Date:   Sun Oct 25 14:34:10 2026 +0600

    Chnage lost book item ICT to Social Science

commit e96ff81cd4c6b02fa3e6db382a5aca213eb2b917 (test-hard, recovery-test)
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git reflog
e51473c (HEAD -> main, origin/main) HEAD@{0}: commit: Fully Complete Chapter 5
4ea03f5 (tag: v1.0.0) HEAD@{1}: checkout: moving from recovery-test to main
e96ff81 (test-hard, recovery-test) HEAD@{2}: reset: moving to HEAD~1
4ea03f5 (tag: v1.0.0) HEAD@{3}: checkout: moving from main to recovery-test
4ea03f5 (tag: v1.0.0) HEAD@{4}: checkout: moving from test-hard to main
e96ff81 (test-hard, recovery-test) HEAD@{5}: reset: moving to HEAD~1
4ea03f5 (tag: v1.0.0) HEAD@{6}: checkout: moving from main to test-hard
4ea03f5 (tag: v1.0.0) HEAD@{7}: reset: moving to HEAD~1
249520d HEAD@{8}: commit: Chnage lost book item Social Science to ICT
4ea03f5 (tag: v1.0.0) HEAD@{9}: commit: Chnage lost book item ICT to Social Science
e96ff81 (test-hard, recovery-test) HEAD@{10}: commit: again come start wo
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
hredoy@HREDOY:/mnt/g/My Skill Learn Plan/Technology/Cloud & DevOps/DevSecOps/DevOps/Portfolio Project/git-lost-and-found-shop$ 