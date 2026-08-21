olamide@Sammy:~$ ls
Backup                                        Practice  day-02         linux-command-mastery-challenge
OlamideSammy-linux-command-mastery-challenge  backup    file.txt.save  practice
olamide@Sammy:~$ cd OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-02-file-operations
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE  README.md  day-01-file-navigation  day-02-file-operations
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-02-file-operations
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ touch README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ touch commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ touch drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mkdir evidence/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
README.md  commands.md  drill.md  evidence
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mkdir Project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mkdir Project/iotbtech/linux
mkdir: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mkdir -p Project/iotbtech/linux
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ touch file.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ cp Project Backup
cp: -r not specified; omitting directory 'Project'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ cp file.txt new.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ cp -r Project Backup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mv file.txt Project/iotbtech/linux
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm file.txt
rm: cannot remove 'file.txt': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm Project/iotbtech/linux/file.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm -r Project/iotbtech/linux
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
Backup  Project  README.md  commands.md  drill.md  evidence  new.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rmdir Backup
rmdir: failed to remove 'Backup': Directory not empty
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm -r Backup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm -r Project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
README.md  commands.md  drill.md  evidence  new.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm new.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
README.md  commands.md  drill.md  evidence
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mkdir -p practice/2026/april
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ touch practice/2026/april/file1.txt practice/2026/april/file2.txt practice/2026/april/file3.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ cp -r practice backup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ mv practice/2026/april/file1.txt practice/2026/april/renamed-file.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm practice/2026/april/file2.txt practice/2026/april/file3.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rmdir practice/2026/april
rmdir: failed to remove 'practice/2026/april': Directory not empty
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
README.md  backup  commands.md  drill.md  evidence  practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm -r backup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ rm -r practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ ls
README.md  commands.md  drill.md  evidence
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE  README.md  day-01-file-navigation  day-02-file-operations
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        day-02-file-operations/

nothing added to commit but untracked files present (use "git add" to track)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git add day-02-file-operations/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git commit -m "Complete Day 2: Creating, Copying, Moving, Deleting"
[main b8f2e0d] Complete Day 2: Creating, Copying, Moving, Deleting
 3 files changed, 50 insertions(+)
 create mode 100644 day-02-file-operations/README.md
 create mode 100644 day-02-file-operations/commands.md
 create mode 100644 day-02-file-operations/drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git push origin main
To github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git pull --rebase origin main
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1.09 KiB | 373.00 KiB/s, done.
From github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge
 * branch            main       -> FETCH_HEAD
   d237c94..8eb4b61  main       -> origin/main
Successfully rebased and updated refs/heads/main.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.44 KiB | 738.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge.git
   8eb4b61..e10050a  main -> main
