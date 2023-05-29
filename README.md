# Gym-Git-Exercise-Solutions
## Exercise 1
### Bundle 1
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
  
