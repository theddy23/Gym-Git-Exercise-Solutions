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
  
### Exercise 2
...
  THEDDY@DESKTOP-QE5FBN1 MINGW64 ~
$ cd "C:\Users\THEDDY\GymExercise"

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign|MERGING)
$ git merge --abort

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

nothing to commit, working tree clean

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ checkout main
bash: checkout: command not found

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index 16479fa..9da2ca8 100644
--- a/services.html
+++ b/services.html
@@ -8,6 +8,6 @@
 </head>
 <body>
     <h1> Our Services</h1>
-    <p> We Bake Delicious Cakes For All Ocassions</p>
+    <p> We Bake Delicious Cakes.</p>
 </body>
 </html>
\ No newline at end of file

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git merge
Already up to date.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git diff ft/service-redesign..main service.html
fatal: ambiguous argument 'service.html': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

nothing to commit, working tree clean

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git push
Everything up-to-date
...
  
 ## Bundle 3
  ### Exercise 1
  
  ...
THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git branch ft/team-page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/service-redesign)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ ls
Index.html  README.md  about.html  home.html  services.html  team.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git add team.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git commit -m "commiting Team page"
[ft/team-page ca809e7] commiting Team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 472 bytes | 472.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/theddy23/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git branch ft/contact-page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git log
commit ca809e78e9411990ce010fd4fa01221f12e02597 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:26:15 2023 +0300

    commiting Team page

commit c54d4a8ee9a1888a4b9b1e23fde82a64250ab6d0 (origin/ft/service-redesign, ft/service-redesign)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Tue May 30 11:22:03 2023 +0300

    Commiting in services page in branch four

commit 64135be815547adc248a44f594f1d7bfb1a8b6d3 (origin/main)
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 11:12:43 2023 +0300

    Update README.md

commit 81294285a047c1de75938ea223919f6f23c4beb8
Merge: f8472a2 290b6ae
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
:...skipping...
commit ca809e78e9411990ce010fd4fa01221f12e02597 (HEAD -> ft/team-page, origin/ft
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:26:15 2023 +0300

    commiting Team page

commit c54d4a8ee9a1888a4b9b1e23fde82a64250ab6d0 (origin/ft/service-redesign, ft/
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Tue May 30 11:22:03 2023 +0300

    Commiting in services page in branch four

commit 64135be815547adc248a44f594f1d7bfb1a8b6d3 (origin/main)
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 11:12:43 2023 +0300

    Update README.md

commit 81294285a047c1de75938ea223919f6f23c4beb8
Merge: f8472a2 290b6ae
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 11:01:23 2023 +0300

    Merge pull request #1 from theddy23/ft/bundle-2

    Added Services page in branch three

commit 290b6aec30fffd21018daec193d9eeeefa72be8e (origin/ft/bundle-2, ft/bundle-2
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Tue May 30 10:54:14 2023 +0300

    Committing service page in branch three

commit f8472a2d0e439dc506d78d0c9f86ce29fae3efde
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 10:48:45 2023 +0300

    Update README.md

commit dcda2b3f71a2563e1c9712306aed7aa229bc9a21
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Mon May 29 14:00:37 2023 +0300

    Update README.md

commit bd75e8aa4e2bae0c45d9baf677a1abda09e11ba0 (origin/dev, dev)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Mon May 29 13:26:30 2023 +0300

:
commit ca809e78e9411990ce010fd4fa01221f12e02597 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:26:15 2023 +0300

    commiting Team page

commit c54d4a8ee9a1888a4b9b1e23fde82a64250ab6d0 (origin/ft/service-redesign, ft/service-redesign)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Tue May 30 11:22:03 2023 +0300

    Commiting in services page in branch four

commit 64135be815547adc248a44f594f1d7bfb1a8b6d3 (origin/main)
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 11:12:43 2023 +0300

    Update README.md

commit 81294285a047c1de75938ea223919f6f23c4beb8
Merge: f8472a2 290b6ae
Author: theddy23 <133653719+theddy23@users.noreply.github.com>
Date:   Tue May 30 11:01:23 2023 +0300

    Merge pull request #1 from theddy23/ft/bundle-2

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git cherry pick ca809e78e9411990ce010fd4fa01221f12e02597
fatal: unknown commit pick

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git cherry-pick ca809e78e9411990ce010fd4fa01221f12e02597
[ft/contact-page d88d3d5] commiting Team page
 Date: Wed May 31 11:26:15 2023 +0300
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git add contact.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git commit -m "commiting the contact page"
[ft/contact-page 097b446] commiting the contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git push -u origin ft/contact-page
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1.05 KiB | 359.00 KiB/s, done.
Total 9 (delta 5), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/theddy23/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git branch ft/faq-page

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git add faq.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git commit -m "commiting the faq page"
[ft/faq-page 8dab083] commiting the faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 470 bytes | 470.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/theddy23/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/theddy23/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git revert ca809e78e9411990ce010fd4fa01221f12e02597
hint: Waiting for your editor to close the file... error: There was a problem with the editor 'vi'.
Please supply the message using either -m or -F option.

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git log
commit 8dab0830229108672f41c102e7314cbf7c633e8c (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:50:40 2023 +0300

    commiting the faq page

commit 097b446f2ee6537d7a4df6d2d0c0c73718fe6247 (origin/ft/contact-page, ft/contact-page)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:41:44 2023 +0300

    commiting the contact page

commit d88d3d5ddcbb1e4a1177785fd7ca7c8a23947b4e
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Wed May 31 11:26:15 2023 +0300

    commiting Team page

commit f9a2fb099dc37f2366e9923f26d38b6f4ee3175b (main)
Author: Theddy23 <theresiangassa98@gmail.com>
Date:   Tue May 30 11:26:43 2023 +0300

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git revert  d88d3d5ddcbb1e4a1177785fd7ca7c8a23947b4e
error: your local changes would be overwritten by revert.
hint: commit your changes or stash them to proceed.
fatal: revert failed

THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git status
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    team.html


THEDDY@DESKTOP-QE5FBN1 MINGW64 ~/GymExercise (ft/faq-page)
$ git push
Everything up-to-date
...

  
  

  
  
  
