olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE    day-01-file-navigation  day-03-file-inspection    day-05-links-checkpoint
README.md  day-02-file-operations  day-04-filesystem-search  day-06-permissions
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-06-permissions
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls
README.md  commands.md  drill.md  evidence.md  permissions-test  practice.sh  umask-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ rm -rf permission-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ rm practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ rm umask-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls
README.md  commands.md  drill.md  evidence.md  permissions-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ rm -r permission-test
rm: cannot remove 'permission-test': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ rm -r permissions-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ touch practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rw-r--r-- 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u-x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod a+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u=rwx,g=rx,o=rx practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 755 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 644 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rw-r--r-- 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 600 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rw------- 1 olamide olamide 0 Aug 25 20:46 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ mkdir permissions-test
touch permissions-test/file1
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod -R 755 permissions-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l permissions-test
total 0
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:49 file1
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -ld permissions-test
drwxr-xr-x 2 olamide olamide 4096 Aug 25 20:49 permissions-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ umask
0022
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ touch umask-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l umask-test
-rw-r--r-- 1 olamide olamide 0 Aug 25 20:50 umask-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ umask -S
u=rwx,g=rx,o=rx
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ stat -c '%A %U %G' practice.sh
-rw------- olamide olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ touch practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rw------- 1 olamide olamide 0 Aug 25 20:55 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod go+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwx--x--x 1 olamide olamide 0 Aug 25 20:55 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod go+x practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwx--x--x 1 olamide olamide 0 Aug 25 20:55 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod go+r practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:55 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u=rwx,g=rx,o=rx practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:55 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 755 practice.sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
-rwxr-xr-x 1 olamide olamide 0 Aug 25 20:55 practice.sh
