# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercise 1
...

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ git --version
git version 2.40.1.windows.1

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ git config --global user.name "Theddy23"

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ git config --global user.email "theresiangassa98@gmail.com"

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ mkdir GymExercise

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ cd GymExercise

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise
$ git init
Initialized empty Git repository in C:/Users/THEDDY/GymExercise/.git/

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (master)
$ git branch -m master main

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ ls
Index.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Index.html

nothing added to commit but untracked files present (use "git add" to track)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git add Index.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Index.html


THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git commit -m "First commit of the Index File"
[main (root-commit) 0551a62] First commit of the Index File
 1 file changed, 13 insertions(+)
 create mode 100644 Index.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git remote add origin https://github.com/theddy23/Gym-Git-Exercise-Solutions.git

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git branch -M main

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git push -u origin main
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/theddy23/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git pull origin main
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 608 bytes | 40.00 KiB/s, done.
From https://github.com/theddy23/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
fatal: refusing to merge unrelated histories

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git pull --rebase origin main
From https://github.com/theddy23/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Successfully rebased and updated refs/heads/main.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 518 bytes | 518.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
   9ceed6a..df0b01d  main -> main
branch 'main' set up to track 'origin/main'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git branch dev

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git checkout dev
Switched to branch 'dev'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git branch test

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git checkout test
Switched to branch 'test'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (test)
$ git checkout dev
Switched to branch 'dev'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git branch -d test
Deleted branch test (was df0b01d).
...
  
### Exercise 2
THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ ls
Index.html  README.md  home.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash push -m "Stash Saving the Home Page" home.html
error: pathspec ':(,prefix:0)home.html' did not match any file(s) known to git
Did you forget to 'git add'?

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git add home.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash push -m "Stash Saving the Home Page" home.html
Saved working directory and index state On dev: Stash Saving the Home Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git add about.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash push -m "Stash Saving the About Page" about.html
Saved working directory and index state On dev: Stash Saving the About Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git add team.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash push -m "Stash Saving the Team Page" team.html
Saved working directory and index state On dev: Stash Saving the Team Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash list
stash@{0}: On dev: Stash Saving the Team Page
stash@{1}: On dev: Stash Saving the About Page
stash@{2}: On dev: Stash Saving the Home Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (214c2c2d6a43fdf42b43e27b8588d1b1c76e5826)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash list
stash@{0}: On dev: Stash Saving the Team Page
stash@{1}: On dev: Stash Saving the Home Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (d454a72f45b4dfdc3074d6e732a358ec077b885b)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git commit -m "Firt Commit After Stash Saving"
[dev bd75e8a] Firt Commit After Stash Saving
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git push -u origin dev
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (10/10), 1.47 KiB | 501.00 KiB/s, done.
Total 10 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/theddy23/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash list
stash@{0}: On dev: Stash Saving the Team Page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (921f4c6b1882601a7ec948172d35237a30c3ccff)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git reset --hard
HEAD is now at bd75e8a Firt Commit After Stash Saving

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
...
## Bundle 2
  ### Exercise 1
...
  THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git branch ft/bundle-2

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/bundle-2)
$ git add services.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html


THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/bundle-2)
$ git commit -m "Committing service page in branch three"
[ft/bundle-2 290b6ae] Committing service page in branch three
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 494 bytes | 247.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/theddy23/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
...

  
  
  
