olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-02-file-operations    day-05-links-checkpoint  day-08-privilege-escalation
README.md               day-03-file-inspection    day-06-permissions       day-09-integrity-firewall
day-01-file-navigation  day-04-filesystem-search  day-07-ownership
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$  mkdir day-10-security-audit-checkpoint/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-02-file-operations    day-05-links-checkpoint  day-08-privilege-escalation
README.md               day-03-file-inspection    day-06-permissions       day-09-integrity-firewall
day-01-file-navigation  day-04-filesystem-search  day-07-ownership         day-10-security-audit-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-10-security-audit-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ touch README.md drill.md evidence.md c
ommands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ less drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ find / -perm /4000 2>/dev/null
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
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ last
Command 'last' not found, but can be installed with:
sudo apt install wtmpdb
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo apt install wtmpdb
[sudo: authenticate] Password:
Installing:
  wtmpdb

Installing dependencies:
  libpam-wtmpdb  libwtmpdb0

Summary:
  Upgrading: 0, Installing: 3, Removing: 0, Not Upgrading: 42
  Download size: 43.0 kB
  Space needed: 174 kB / 1024 GB available

Continue? [Y/n] Y
Get:1 http://archive.ubuntu.com/ubuntu resolute/universe amd64 libwtmpdb0 amd64 0.75.0-5ubuntu1 [11.9 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/universe amd64 libpam-wtmpdb amd64 0.75.0-5ubuntu1 [9544 B]
Get:3 http://archive.ubuntu.com/ubuntu resolute/universe amd64 wtmpdb amd64 0.75.0-5ubuntu1 [21.6 kB]
Fetched 43.0 kB in 1s (34.1 kB/s)
Selecting previously unselected package libwtmpdb0:amd64.
(Reading database ... 36311 files and directories currently installed.)
Preparing to unpack .../libwtmpdb0_0.75.0-5ubuntu1_amd64.deb ...
Unpacking libwtmpdb0:amd64 (0.75.0-5ubuntu1) ...
Selecting previously unselected package libpam-wtmpdb:amd64.
Preparing to unpack .../libpam-wtmpdb_0.75.0-5ubuntu1_amd64.deb ...
Unpacking libpam-wtmpdb:amd64 (0.75.0-5ubuntu1) ...
Selecting previously unselected package wtmpdb.
Preparing to unpack .../wtmpdb_0.75.0-5ubuntu1_amd64.deb ...
Unpacking wtmpdb (0.75.0-5ubuntu1) ...
Setting up libwtmpdb0:amd64 (0.75.0-5ubuntu1) ...
Setting up libpam-wtmpdb:amd64 (0.75.0-5ubuntu1) ...
Setting up wtmpdb (0.75.0-5ubuntu1) ...
Converting wtmp login records into wtmpdb database ... done
Created symlink '/etc/systemd/system/default.target.wants/wtmpdb-update-boot.service' → '/usr/lib/systemd/system/wtmpdb-update-boot.service'.
Processing triggers for man-db (2.13.1-1build1) ...
Processing triggers for libc-bin (2.43-2ubuntu2.3) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ lastlog
Command 'lastlog' not found, did you mean:
  command 'lastlog2' from deb lastlog2 (2.41.3-3ubuntu2)
Try: sudo apt install <deb name>
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$  sudo apt install <deb name>
-bash: syntax error near unexpected token `newline'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo apt update
sudo apt install lastlog2
Get:1 http://security.ubuntu.com/ubuntu resolute-security InRelease [137 kB]
Hit:2 http://archive.ubuntu.com/ubuntu resolute InRelease
Get:3 http://archive.ubuntu.com/ubuntu resolute-updates InRelease [137 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute-backports InRelease [137 kB]
Get:5 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Components [46.7 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Components [98.2 kB]
Get:7 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Packages [252 kB]
Get:8 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Components [43.2 kB]
Get:9 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Components [188 kB]
Get:10 http://archive.ubuntu.com/ubuntu resolute-backports/universe amd64 Components [1056 B]
Fetched 1041 kB in 10s (109 kB/s)
42 packages can be upgraded. Run 'apt list --upgradable' to see them.
Installing:
  lastlog2

Installing dependencies:
  liblastlog2-2  libpam-lastlog2

Summary:
  Upgrading: 0, Installing: 3, Removing: 0, Not Upgrading: 42
  Download size: 81.7 kB
  Space needed: 227 kB / 1024 GB available

Continue? [Y/n] Y
Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 liblastlog2-2 amd64 2.41.3-3ubuntu2 [26.7 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/universe amd64 lastlog2 amd64 2.41.3-3ubuntu2 [27.9 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/universe amd64 libpam-lastlog2 amd64 2.41.3-3ubuntu2 [27.1 kB]
Fetched 81.7 kB in 2s (40.9 kB/s)
Selecting previously unselected package liblastlog2-2:amd64.
(Reading database ... 36339 files and directories currently installed.)
Preparing to unpack .../liblastlog2-2_2.41.3-3ubuntu2_amd64.deb ...
Unpacking liblastlog2-2:amd64 (2.41.3-3ubuntu2) ...
Selecting previously unselected package lastlog2.
Preparing to unpack .../lastlog2_2.41.3-3ubuntu2_amd64.deb ...
Unpacking lastlog2 (2.41.3-3ubuntu2) ...
Selecting previously unselected package libpam-lastlog2:amd64.
Preparing to unpack .../libpam-lastlog2_2.41.3-3ubuntu2_amd64.deb ...
Unpacking libpam-lastlog2:amd64 (2.41.3-3ubuntu2) ...
Setting up liblastlog2-2:amd64 (2.41.3-3ubuntu2) ...
Setting up libpam-lastlog2:amd64 (2.41.3-3ubuntu2) ...
Setting up lastlog2 (2.41.3-3ubuntu2) ...
Processing triggers for man-db (2.13.1-1build1) ...
Processing triggers for libc-bin (2.43-2ubuntu2.3) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ lastlog2
lastlog2: Couldn't read entries for all users
lastlog2: Cannot open database (/var/lib/lastlog/lastlog2.db): unable to open database file
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ dpkg -l | grep lastlog
ii  lastlog2                          2.41.3-3ubuntu2                            amd64        Read lastlog2 database
ii  liblastlog2-2:amd64               2.41.3-3ubuntu2                            amd64        lastlog2 database shared library
ii  libpam-lastlog2:amd64             2.41.3-3ubuntu2                            amd64        lastlog2 database PAM module
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ ls -la /var/lib/lastlog/
total 8
drwxr-xr-x  2 root root 4096 Mar 13 12:09 .
drwxr-xr-x 34 root root 4096 Aug 29 21:54 ..
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ w
 21:56:37 up 41 min,  1 user,  load average: 0.54, 0.72, 0.36
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU  WHAT
olamide  pts/1    -                21:15   41:01   0.07s  0.07s -bash
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ who
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ groups
olamide adm cdrom sudo dip plugdev users
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ groups olamide
olamide : olamide adm cdrom sudo dip plugdev users
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ passwd
Changing password for olamide.
Current password:
New password:
Retype new password:
The password has not been changed.
New password:
Retype new password:
passwd: password updated successfully
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo chage -l olamide
Last password change                                    : Aug 29, 2026
Password expires                                        : never
Password inactive                                       : never
Account expires                                         : never
Minimum number of days between password change          : 0
Maximum number of days between password change          : 99999
Number of days of warning before password expires       : 7
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo lastb
sudo: 'lastb': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ apt-file search bin/lastb
Command 'apt-file' not found, but can be installed with:
sudo apt install apt-file
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo apt install apt-file
Installing:
  apt-file

Installing dependencies:
  libapt-pkg-perl  libregexp-assemble-perl

Summary:
  Upgrading: 0, Installing: 3, Removing: 0, Not Upgrading: 42
  Download size: 164 kB
  Space needed: 541 kB / 1024 GB available

Continue? [Y/n] Y
Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 libapt-pkg-perl amd64 0.1.43 [70.5 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/universe amd64 libregexp-assemble-perl all 0.38-2 [69.5 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/universe amd64 apt-file all 3.3ubuntu2 [24.5 kB]
Fetched 164 kB in 2s (94.5 kB/s)
Selecting previously unselected package libapt-pkg-perl.
(Reading database ... 36361 files and directories currently installed.)
Preparing to unpack .../libapt-pkg-perl_0.1.43_amd64.deb ...
Unpacking libapt-pkg-perl (0.1.43) ...
Selecting previously unselected package libregexp-assemble-perl.
Preparing to unpack .../libregexp-assemble-perl_0.38-2_all.deb ...
Unpacking libregexp-assemble-perl (0.38-2) ...
Selecting previously unselected package apt-file.
Preparing to unpack .../apt-file_3.3ubuntu2_all.deb ...
Unpacking apt-file (3.3ubuntu2) ...
Setting up libapt-pkg-perl (0.1.43) ...
Setting up libregexp-assemble-perl (0.38-2) ...
Setting up apt-file (3.3ubuntu2) ...
The system-wide cache is empty. You may want to run 'apt-file update'
as root to update the cache.
Processing triggers for man-db (2.13.1-1build1) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo apt update
sudo apt install apt-file
Hit:1 http://archive.ubuntu.com/ubuntu resolute InRelease
Hit:2 http://security.ubuntu.com/ubuntu resolute-security InRelease
Hit:3 http://archive.ubuntu.com/ubuntu resolute-updates InRelease
Hit:4 http://archive.ubuntu.com/ubuntu resolute-backports InRelease
Get:5 http://security.ubuntu.com/ubuntu resolute-security amd64 Contents (deb) [15.1 MB]
Get:6 http://archive.ubuntu.com/ubuntu resolute amd64 Contents (deb) [56.9 MB]
Get:7 http://archive.ubuntu.com/ubuntu resolute-updates amd64 Contents (deb) [16.6 MB]
Get:8 http://archive.ubuntu.com/ubuntu resolute-backports amd64 Contents (deb) [10.2 kB]
Fetched 88.7 MB in 2min 4s (717 kB/s)
42 packages can be upgraded. Run 'apt list --upgradable' to see them.
apt-file is already the newest version (3.3ubuntu2).
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 42
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ apt-file search bin/lastb
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo lastb
sudo: 'lastb': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ history | grep sudo
  506  sudo updatedb
  508  sudo updatedb
  510  sudo apt install plocate
  517  sudo apt install plocate
  524  sudo updatedb
  572  sudo snap install tree  # version 2.1.3+pkg-5852
  789  sudo chown olamide practice.txt
  792  sudo chown olamide:olamide practice.txt
  796  sudo chown -R olamide:olamide ownership-test
  798  sudo chgrp olamide practice.txt
  810  sudo apt install acl
  873  sudo ls /root
  874  sudo -i
  875  sudo -u root whoami
  877  sudo ls /root
  878  sudo -l
  879  sudo visudo
  885  sudo ls /root
  886  sudo -l
  917  sudo chattr +i practice.txt
  919  sudo ufw status
  920  sudo ufw enable
  921  sudo ufw allow 22
  923  sudo apt update
  924  sudo apt install ufw
  925  sudo ufw status
  926  sudo ufw allow 22
  927  sudo ufw allow 443
  928  sudo ufw status
  929  sudo ufw enable
  930  sudo ufw status
  933  sudo chattr +i integrity.txt
  935  sudo ufw status
  936  sudo ufw allow 22
  937  sudo ufw allow 443
  938  sudo ufw enable
  939  sudo ufw status
  985  sudo chattr -i integrity.txt
 1022  sudo apt install wtmpdb
 1024  sudo apt update
 1025  sudo apt install lastlog2
 1034  sudo chage -l olamide
 1035  sudo lastb
 1037  sudo apt install apt-file
 1038  sudo apt update
 1039  sudo apt install apt-file
 1041  sudo lastb
 1042  history | grep sudo
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ last
Cannot open database (/var/log/wtmp.db) read-only: unable to open database file
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ ls -l /var/log/wtmp.db
ls: cannot access '/var/log/wtmp.db': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo ls -l /var/log/wtmp.db
ls: cannot access '/var/log/wtmp.db': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ v
v: command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ w
 22:08:41 up 53 min,  1 user,  load average: 0.00, 0.08, 0.17
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU  WHAT
olamide  pts/1    -                21:15   53:05   0.07s  0.07s -bash
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ who
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ lastlog
Command 'lastlog' not found, did you mean:
  command 'lastlog2' from deb lastlog2 (2.41.3-3ubuntu2)
Try: sudo apt install <deb name>
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ lastlog2
lastlog2: Couldn't read entries for all users
lastlog2: Cannot open database (/var/lib/lastlog/lastlog2.db): unable to open database file
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ history | grep sudo
  506  sudo updatedb
  508  sudo updatedb
  510  sudo apt install plocate
  517  sudo apt install plocate
  524  sudo updatedb
  572  sudo snap install tree  # version 2.1.3+pkg-5852
  789  sudo chown olamide practice.txt
  792  sudo chown olamide:olamide practice.txt
  796  sudo chown -R olamide:olamide ownership-test
  798  sudo chgrp olamide practice.txt
  810  sudo apt install acl
  873  sudo ls /root
  874  sudo -i
  875  sudo -u root whoami
  877  sudo ls /root
  878  sudo -l
  879  sudo visudo
  885  sudo ls /root
  886  sudo -l
  917  sudo chattr +i practice.txt
  919  sudo ufw status
  920  sudo ufw enable
  921  sudo ufw allow 22
  923  sudo apt update
  924  sudo apt install ufw
  925  sudo ufw status
  926  sudo ufw allow 22
  927  sudo ufw allow 443
  928  sudo ufw status
  929  sudo ufw enable
  930  sudo ufw status
  933  sudo chattr +i integrity.txt
  935  sudo ufw status
  936  sudo ufw allow 22
  937  sudo ufw allow 443
  938  sudo ufw enable
  939  sudo ufw status
  985  sudo chattr -i integrity.txt
 1022  sudo apt install wtmpdb
 1024  sudo apt update
 1025  sudo apt install lastlog2
 1034  sudo chage -l olamide
 1035  sudo lastb
 1037  sudo apt install apt-file
 1038  sudo apt update
 1039  sudo apt install apt-file
 1041  sudo lastb
 1042  history | grep sudo
 1045  sudo ls -l /var/log/wtmp.db
 1051  history | grep sudo
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo lastb
sudo: 'lastb': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-10-security-audit-checkpoint$ sudo chage -l olamide
Last password change                                    : Aug 29, 2026
Password expires                                        : never
Password inactive                                       : never
Account expires                                         : never
Minimum number of days between password change          : 0
Maximum number of days between password change          : 99999
Number of days of warning before password expires       : 7

