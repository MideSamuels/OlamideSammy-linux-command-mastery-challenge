olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ rm README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-03-file-inspection    day-06-permissions           day-09-integrity-firewall         day-12-groups
day-01-file-navigation  day-04-filesystem-search  day-07-ownership             day-10-security-audit-checkpoint
day-02-file-operations  day-05-links-checkpoint   day-08-privilege-escalation  day-11-user-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-12-groups
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ less drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupadd devs
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupdel devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a devuser1 devs
gpasswd: user 'devuser1' does not exist
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -d devuser1 devs
gpasswd: group 'devs' does not exist in /etc/group
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent passwd devuser1
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ groups devuser1
groups: 'devuser1': no such user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ id -Gn devuser1
id: 'devuser1': no such user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ newgrp devs
Command 'newgrp' not found, but can be installed with:
sudo apt install util-linux-extra
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo apt install util-linux-extra
Installing:
  util-linux-extra

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 42
  Download size: 346 kB
  Space needed: 1331 kB / 1024 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 util-linux-extra amd64 2.41.3-3ubuntu2 [346 kB]
Fetched 346 kB in 3s (121 kB/s)
Selecting previously unselected package util-linux-extra.
(Reading database ... 36435 files and directories currently installed.)
Preparing to unpack .../util-linux-extra_2.41.3-3ubuntu2_amd64.deb ...
Unpacking util-linux-extra (2.41.3-3ubuntu2) ...
Setting up util-linux-extra (2.41.3-3ubuntu2) ...
Processing triggers for man-db (2.13.1-1build1) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ newgrp devs
newgrp: no such group
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ id -Gn
olamide adm cdrom sudo dip plugdev users
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ cat /etc/group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:syslog,olamide
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
fax:x:21:
voice:x:22:
cdrom:x:24:olamide
floppy:x:25:
tape:x:26:
sudo:x:27:olamide
audio:x:29:
dip:x:30:olamide
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
shadow:x:42:
utmp:x:43:
video:x:44:
sasl:x:45:
plugdev:x:46:olamide
staff:x:50:
games:x:60:
users:x:100:olamide,interactiveuser
nogroup:x:65534:
systemd-journal:x:999:
systemd-network:x:998:
crontab:x:997:
dhcpcd:x:996:
messagebus:x:995:
syslog:x:101:
input:x:994:
sgx:x:993:
clock:x:992:
kvm:x:991:
render:x:990:
systemd-resolve:x:989:
_chrony:x:988:
_ssh:x:102:
landscape:x:103:
polkitd:x:987:
admin:x:104:
netdev:x:105:
olamide:x:1000:
plocate:x:106:
homeuser:x:1002:
challengeuser:x:1003:
interactiveuser:x:1004:
day11user:x:1005:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a homeuser devs
gpasswd: group 'devs' does not exist in /etc/group
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a day11user devs
gpasswd: user 'day11user' does not exist
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupadd devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
devs:x:1006:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a homeuser devs
Adding user homeuser to group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a day11user devs
gpasswd: user 'day11user' does not exist
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
devs:x:1006:homeuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -d homeuser devs
Removing user homeuser from group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
devs:x:1006:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupdel devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ newgrp users
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ id -Gn
users adm cdrom sudo dip plugdev olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ exit
exit
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupadd devs
getent group devs
devs:x:1006:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a homeuser devs
Adding user homeuser to group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a day11user devs
gpasswd: user 'day11user' does not exist
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a interactiveuser devs
Adding user interactiveuser to group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
devs:x:1006:homeuser,interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -a interactiveuser devs
getent group devs
Adding user interactiveuser to group devs
devs:x:1006:homeuser,interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent passwd homeuser
homeuser:x:1002:1002::/home/homeuser:/bin/sh
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ groups homeuser
homeuser : homeuser devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ id -Gn homeuser
homeuser devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ newgrp devs
Password:
newgrp: permission denied
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ newgrp devs
Password:
newgrp: permission denied
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ cat /etc/group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:syslog,olamide
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
fax:x:21:
voice:x:22:
cdrom:x:24:olamide
floppy:x:25:
tape:x:26:
sudo:x:27:olamide
audio:x:29:
dip:x:30:olamide
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
shadow:x:42:
utmp:x:43:
video:x:44:
sasl:x:45:
plugdev:x:46:olamide
staff:x:50:
games:x:60:
users:x:100:olamide,interactiveuser
nogroup:x:65534:
systemd-journal:x:999:
systemd-network:x:998:
crontab:x:997:
dhcpcd:x:996:
messagebus:x:995:
syslog:x:101:
input:x:994:
sgx:x:993:
clock:x:992:
kvm:x:991:
render:x:990:
systemd-resolve:x:989:
_chrony:x:988:
_ssh:x:102:
landscape:x:103:
polkitd:x:987:
admin:x:104:
netdev:x:105:
olamide:x:1000:
plocate:x:106:
homeuser:x:1002:
challengeuser:x:1003:
interactiveuser:x:1004:
day11user:x:1005:
devs:x:1006:homeuser,interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo gpasswd -d homeuser devs
Removing user homeuser from group devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
devs:x:1006:interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ sudo groupdel devs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-12-groups$ getent group devs
