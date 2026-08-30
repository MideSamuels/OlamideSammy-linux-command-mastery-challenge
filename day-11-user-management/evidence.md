olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-11-user-management/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-02-file-operations    day-05-links-checkpoint  day-08-privilege-escalation       day-11-user-management
README.md               day-03-file-inspection    day-06-permissions       day-09-integrity-firewall
day-01-file-navigation  day-04-filesystem-search  day-07-ownership         day-10-security-audit-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-11-user-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo useradd drilluser
[sudo: authenticate] Password:
sudo: Authentication failed, try again.
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo useradd -m homeuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo useradd -m -s /bin/bash challengeuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo adduser interactiveuser
New password:
Retype new password:
passwd: password updated successfully
Changing the user information for interactiveuser
Enter the new value, or press ENTER for the default
        Full Name []: Samuel
        Room Number []: 33
        Work Phone []: 09036134333
        Home Phone []: 09036134333
        Other []: 33
Is the information correct? [Y/n] Y
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo passwd challengeuser
New password:
Retype new password:
passwd: password updated successfully
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo usermod -aG <group> challengeuser
-bash: group: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ getent group
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
drilluser:x:1001:
homeuser:x:1002:
challengeuser:x:1003:
interactiveuser:x:1004:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ getent group users
users:x:100:olamide,interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo usermod -aG users challengeuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ groups challengeuser
challengeuser : challengeuser users
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo usermod -s /bin/bash challengeuser
usermod: no changes
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo usermod -l renameduser challengeuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo userdel drilluser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo userdel -r renameduser
userdel: renameduser mail spool (/var/mail/renameduser) not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ getent passwd renameduser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls -ld /home/challengeuser
ls: cannot access '/home/challengeuser': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls -ld /home/renameduser
ls: cannot access '/home/renameduser': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo useradd -m -s /bin/bash challengeuser
useradd: group challengeuser exists - if you want to add this user to that group, use -g.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls -ld /home/challengeuser
ls: cannot access '/home/challengeuser': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo useradd -m -s /bin/bash day11user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls -ld /home/day11user
drwxr-x--- 2 day11user day11user 4096 Aug 30 22:29 /home/day11user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo passwd day11user
New password:
Retype new password:
passwd: password updated successfully
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ getent group users
users:x:100:olamide,interactiveuser
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ groups day11user
day11user : day11user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo usermod -l renameduser day11user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ getent passwd renameduser
renameduser:x:1005:1005::/home/day11user:/bin/bash
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ sudo userdel -r renameduser
userdel: renameduser mail spool (/var/mail/renameduser) not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-11-user-management$ ls -ld /home/day11user
ls: cannot access '/home/day11user': No such file or directory
