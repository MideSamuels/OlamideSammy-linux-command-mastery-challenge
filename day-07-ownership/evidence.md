olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE    day-01-file-navigation  day-03-file-inspection    day-05-links-checkpoint
README.md  day-02-file-operations  day-04-filesystem-search  day-06-permissions
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-07-ownership/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE    commands.md             day-02-file-operations  day-04-filesystem-search  day-06-permissions  drill.md
README.md  day-01-file-navigation  day-03-file-inspection  day-05-links-checkpoint   day-07-ownership    evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ rm drill.md evidence.md commands.md README.me
rm: cannot remove 'README.me': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ rm drill.md evidence.md commands.md README.md
rm: cannot remove 'drill.md': No such file or directory
rm: cannot remove 'evidence.md': No such file or directory
rm: cannot remove 'commands.md': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-02-file-operations  day-04-filesystem-search  day-06-permissions
day-01-file-navigation  day-03-file-inspection  day-05-links-checkpoint   day-07-ownership
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-07-ownership
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ touch practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ sudo chown olamide practice.txt
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l practice.txt
-rw-r--r-- 1 olamide olamide 0 Aug 26 20:58 practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ id
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ sudo chown olamide:olamide practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l practice.txt
-rw-r--r-- 1 olamide olamide 0 Aug 26 20:58 practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ mkdir ownership-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ touch ownership-test/file.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ sudo chown -R olamide:olamide ownership-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l ownership-test
total 0
-rw-r--r-- 1 olamide olamide 0 Aug 26 21:00 file.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ sudo chgrp olamide practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l practice.txt
-rw-r--r-- 1 olamide olamide 0 Aug 26 20:58 practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ chmod u+s practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l practice.txt
-rwSr--r-- 1 olamide olamide 0 Aug 26 20:58 practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ mkdir sgid-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ chmod g+s sgid-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -ld sgid-test
drwxr-sr-x 2 olamide olamide 4096 Aug 26 21:08 sgid-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ mkdir sticky-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ chmod +t sticky-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -ld sticky-test
drwxr-xr-t 2 olamide olamide 4096 Aug 26 21:09 sticky-test
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ find / -perm /4000 2>/dev/null
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-07-ownership/practice.txt
/snap/core22/2437/usr/bin/chfn
/snap/core22/2437/usr/bin/chsh
/snap/core22/2437/usr/bin/gpasswd
/snap/core22/2437/usr/bin/mount
/snap/core22/2437/usr/bin/newgrp
/snap/core22/2437/usr/bin/passwd
/snap/core22/2437/usr/bin/su
/snap/core22/2437/usr/bin/sudo
/snap/core22/2437/usr/bin/umount
/snap/core22/2437/usr/lib/dbus-1.0/dbus-daemon-launch-helper
/snap/core22/2437/usr/lib/openssh/ssh-keysign
/snap/core22/2437/usr/libexec/polkit-agent-helper-1


^C
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ find / -perm /4000 2>/dev/null
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-07-ownership/practice.txt
/snap/core22/2437/usr/bin/chfn
/snap/core22/2437/usr/bin/chsh
/snap/core22/2437/usr/bin/gpasswd
/snap/core22/2437/usr/bin/mount
/snap/core22/2437/usr/bin/newgrp
/snap/core22/2437/usr/bin/passwd
/snap/core22/2437/usr/bin/su
/snap/core22/2437/usr/bin/sudo
/snap/core22/2437/usr/bin/umount
/snap/core22/2437/usr/lib/dbus-1.0/dbus-daemon-launch-helper
/snap/core22/2437/usr/lib/openssh/ssh-keysign
/snap/core22/2437/usr/libexec/polkit-agent-helper-1
^C
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ getfacl practice.txt
Command 'getfacl' not found, but can be installed with:
sudo apt install acl
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ sudo apt install acl
Installing:
  acl

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 29
  Download size: 39.4 kB
  Space needed: 197 kB / 1024 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 acl amd64 2.3.2-2 [39.4 kB]
Fetched 39.4 kB in 1s (43.8 kB/s)
Selecting previously unselected package acl.
(Reading database ... 35924 files and directories currently installed.)
Preparing to unpack .../archives/acl_2.3.2-2_amd64.deb ...
Unpacking acl (2.3.2-2) ...
Setting up acl (2.3.2-2) ...
Processing triggers for man-db (2.13.1-1build1) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ getfacl practice.txt
# file: practice.txt
# owner: olamide
# group: olamide
# flags: s--
user::rw-
group::r--
other::r--

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ setfacl -m u:olamide:r practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ getfacl practice.txt
# file: practice.txt
# owner: olamide
# group: olamide
# flags: s--
user::rw-
user:olamide:r--
group::r--
mask::r--
other::r--

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ mkdir shared-project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -ld shared-project
drwxr-xr-x 2 olamide olamide 4096 Aug 26 21:17 shared-project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ chmod g+s shared-project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -ld shared-project
drwxr-sr-x 2 olamide olamide 4096 Aug 26 21:17 shared-project
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ touch shared-project/test.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l shared-project
total 0
-rw-r--r-- 1 olamide olamide 0 Aug 26 21:18 test.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ find / -perm /4000 2>/dev/null
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-07-ownership/practice.txt
/snap/core22/2437/usr/bin/chfn
/snap/core22/2437/usr/bin/chsh
/snap/core22/2437/usr/bin/gpasswd
/snap/core22/2437/usr/bin/mount
/snap/core22/2437/usr/bin/newgrp
/snap/core22/2437/usr/bin/passwd
/snap/core22/2437/usr/bin/su
/snap/core22/2437/usr/bin/sudo
/snap/core22/2437/usr/bin/umount
/snap/core22/2437/usr/lib/dbus-1.0/dbus-daemon-launch-helper
/snap/core22/2437/usr/lib/openssh/ssh-keysign
/snap/core22/2437/usr/libexec/polkit-agent-helper-1
^C
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ ls -l shared-project
total 0
-rw-r--r-- 1 olamide olamide 0 Aug 26 21:18 test.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$ id
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-07-ownership$
