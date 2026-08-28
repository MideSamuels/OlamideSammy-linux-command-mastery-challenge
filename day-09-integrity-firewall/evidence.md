olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir  day-09-integrity-firewall/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-02-file-operations    day-05-links-checkpoint  day-08-privilege-escalation
README.md               day-03-file-inspection    day-06-permissions       day-09-integrity-firewall
day-01-file-navigation  day-04-filesystem-search  day-07-ownership
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-09-integrity-firewall
mkdir: day-09-integrity-firewall: File exists
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-09-integrity-firewall
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ touch README.md drill.md evidenc
e.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ less drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ echo "Linux Day 9 practice" > practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ md5sum practice.txt
354fa273fb6306f44006c7282c0a8689  practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sha256sum practice.txt
7984763854da09b0c2af57a151dd6ddae659ba3c45ef9fd449063ac474bdcbae  practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ gpg --gen-key
gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

gpg: directory '/home/olamide/.gnupg' created
gpg: keybox '/home/olamide/.gnupg/pubring.kbx' created
Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Olamide
Email address: olamidesam20@gmail.com
You selected this USER-ID:
    "Olamide <olamidesam20@gmail.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit? N
Real name: Olamide
You selected this USER-ID:
    "Olamide <olamidesam20@gmail.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit? O
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: /home/olamide/.gnupg/trustdb.gpg: trustdb created
gpg: directory '/home/olamide/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/olamide/.gnupg/openpgp-revocs.d/CE0862184F55DF79BF15843D0C5D870148DF34F4.rev'
public and secret key created and signed.

pub   ed25519 2026-08-28 [SC] [expires: 2029-08-27]
      CE0862184F55DF79BF15843D0C5D870148DF34F4
uid                      Olamide <olamidesam20@gmail.com>
sub   cv25519 2026-08-28 [E] [expires: 2029-08-27]

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ gpg --list-keys
gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
gpg: next trustdb check due at 2029-08-27
/home/olamide/.gnupg/pubring.kbx
--------------------------------
pub   ed25519 2026-08-28 [SC] [expires: 2029-08-27]
      CE0862184F55DF79BF15843D0C5D870148DF34F4
uid           [ultimate] Olamide <olamidesam20@gmail.com>
sub   cv25519 2026-08-28 [E] [expires: 2029-08-27]

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ gpg --encrypt --recipient olamide practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ ls -l
total 20
-rw-r--r-- 1 olamide olamide 944 Aug 28 20:32 README.md
-rw-r--r-- 1 olamide olamide 580 Aug 28 20:37 commands.md
-rw-r--r-- 1 olamide olamide 582 Aug 28 20:35 drill.md
-rw-r--r-- 1 olamide olamide   0 Aug 28 20:24 evidence.md
-rw-r--r-- 1 olamide olamide  21 Aug 28 20:47 practice.txt
-rw-r--r-- 1 olamide olamide 184 Aug 28 20:52 practice.txt.gpg
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ gpg --decrypt practice.txt.gpg > decrypted.txt
gpg: encrypted with cv25519 key, ID A607591CB7079766, created 2026-08-28
      "Olamide <olamidesam20@gmail.com>"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo chattr +i practice.txt
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ lsattr practice.txt
----i---------e------- practice.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
sudo: 'ufw': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw enable
sudo: 'ufw': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw allow 22
sudo: 'ufw': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw allow 443
sudo: 'ufw': command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo apt update
Hit:1 http://archive.ubuntu.com/ubuntu resolute InRelease
Get:2 http://security.ubuntu.com/ubuntu resolute-security InRelease [137 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute-updates InRelease [137 kB]
Get:4 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Packages [424 kB]
Get:5 http://archive.ubuntu.com/ubuntu resolute-backports InRelease [137 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Packages [549 kB]
Get:7 http://security.ubuntu.com/ubuntu resolute-security/main Translation-en [97.9 kB]
Get:8 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Components [46.6 kB]
Get:9 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Packages [159 kB]
Get:10 http://security.ubuntu.com/ubuntu resolute-security/universe Translation-en [51.2 kB]
Get:11 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Components [43.2 kB]
Get:12 http://security.ubuntu.com/ubuntu resolute-security/restricted amd64 Packages [361 kB]
Get:13 http://security.ubuntu.com/ubuntu resolute-security/restricted Translation-en [70.0 kB]
Get:14 http://archive.ubuntu.com/ubuntu resolute-updates/main Translation-en [128 kB]
Get:15 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Components [97.8 kB]
Get:16 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Packages [252 kB]
Get:17 http://archive.ubuntu.com/ubuntu resolute-updates/universe Translation-en [84.4 kB]
Get:18 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Components [188 kB]
Get:19 http://archive.ubuntu.com/ubuntu resolute-updates/restricted amd64 Packages [371 kB]
Get:20 http://archive.ubuntu.com/ubuntu resolute-updates/restricted Translation-en [71.7 kB]
Get:21 http://archive.ubuntu.com/ubuntu resolute-backports/universe amd64 Packages [3132 B]
Get:22 http://archive.ubuntu.com/ubuntu resolute-backports/universe Translation-en [7988 B]
Get:23 http://archive.ubuntu.com/ubuntu resolute-backports/universe amd64 Components [1056 B]
Fetched 3417 kB in 7s (494 kB/s)
57 packages can be upgraded. Run 'apt list --upgradable' to see them.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo apt install ufw
Installing:
  ufw

Installing dependencies:
  iptables  libip4tc2  libip6tc2  libnetfilter-conntrack3  libnfnetlink0  libnftables1  libnftnl11  nftables

Suggested packages:
  firewalld

Summary:
  Upgrading: 0, Installing: 9, Removing: 0, Not Upgrading: 57
  Download size: 1201 kB
  Space needed: 5270 kB / 1024 GB available

Continue? [Y/n] Y
Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 libip4tc2 amd64 1.8.11-2ubuntu3 [24.2 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/main amd64 libip6tc2 amd64 1.8.11-2ubuntu3 [24.4 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/main amd64 libnfnetlink0 amd64 1.0.2-3build1 [15.1 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute/main amd64 libnetfilter-conntrack3 amd64 1.1.1-1 [47.5 kB]
Get:5 http://archive.ubuntu.com/ubuntu resolute/main amd64 libnftnl11 amd64 1.3.1-1 [72.3 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute/main amd64 iptables amd64 1.8.11-2ubuntu3 [381 kB]
Get:7 http://archive.ubuntu.com/ubuntu resolute/main amd64 libnftables1 amd64 1.1.6-1 [390 kB]
Get:8 http://archive.ubuntu.com/ubuntu resolute/main amd64 nftables amd64 1.1.6-1 [76.2 kB]
Get:9 http://archive.ubuntu.com/ubuntu resolute/main amd64 ufw all 0.36.2-9build1 [170 kB]
Fetched 1201 kB in 7s (174 kB/s)
Preconfiguring packages ...
Selecting previously unselected package libip4tc2:amd64.
(Reading database ... 35934 files and directories currently installed.)
Preparing to unpack .../0-libip4tc2_1.8.11-2ubuntu3_amd64.deb ...
Unpacking libip4tc2:amd64 (1.8.11-2ubuntu3) ...
Selecting previously unselected package libip6tc2:amd64.
Preparing to unpack .../1-libip6tc2_1.8.11-2ubuntu3_amd64.deb ...
Unpacking libip6tc2:amd64 (1.8.11-2ubuntu3) ...
Selecting previously unselected package libnfnetlink0:amd64.
Preparing to unpack .../2-libnfnetlink0_1.0.2-3build1_amd64.deb ...
Unpacking libnfnetlink0:amd64 (1.0.2-3build1) ...
Selecting previously unselected package libnetfilter-conntrack3:amd64.
Preparing to unpack .../3-libnetfilter-conntrack3_1.1.1-1_amd64.deb ...
Unpacking libnetfilter-conntrack3:amd64 (1.1.1-1) ...
Selecting previously unselected package libnftnl11:amd64.
Preparing to unpack .../4-libnftnl11_1.3.1-1_amd64.deb ...
Unpacking libnftnl11:amd64 (1.3.1-1) ...
Selecting previously unselected package iptables.
Preparing to unpack .../5-iptables_1.8.11-2ubuntu3_amd64.deb ...
Unpacking iptables (1.8.11-2ubuntu3) ...
Selecting previously unselected package libnftables1:amd64.
Preparing to unpack .../6-libnftables1_1.1.6-1_amd64.deb ...
Unpacking libnftables1:amd64 (1.1.6-1) ...
Selecting previously unselected package nftables.
Preparing to unpack .../7-nftables_1.1.6-1_amd64.deb ...
Unpacking nftables (1.1.6-1) ...
Selecting previously unselected package ufw.
Preparing to unpack .../8-ufw_0.36.2-9build1_all.deb ...
Unpacking ufw (0.36.2-9build1) ...
Setting up libip4tc2:amd64 (1.8.11-2ubuntu3) ...
Setting up libip6tc2:amd64 (1.8.11-2ubuntu3) ...
Setting up libnftnl11:amd64 (1.3.1-1) ...
Setting up libnfnetlink0:amd64 (1.0.2-3build1) ...
Setting up libnftables1:amd64 (1.1.6-1) ...
Setting up nftables (1.1.6-1) ...
Setting up libnetfilter-conntrack3:amd64 (1.1.1-1) ...
Setting up iptables (1.8.11-2ubuntu3) ...
update-alternatives: using /usr/sbin/iptables-legacy to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-legacy to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/iptables-nft to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-nft to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/arptables-nft to provide /usr/sbin/arptables (arptables) in auto mode
update-alternatives: using /usr/sbin/ebtables-nft to provide /usr/sbin/ebtables (ebtables) in auto mode
Setting up ufw (0.36.2-9build1) ...
Creating config file /etc/ufw/before.rules with new version
Creating config file /etc/ufw/before6.rules with new version
Creating config file /etc/ufw/after.rules with new version
Creating config file /etc/ufw/after6.rules with new version
Created symlink '/etc/systemd/system/multi-user.target.wants/ufw.service' → '/usr/lib/systemd/system/ufw.service'.
Processing triggers for libc-bin (2.43-2ubuntu2.3) ...
Processing triggers for rsyslog (8.2512.0-1ubuntu4.1) ...
Processing triggers for man-db (2.13.1-1build1) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: inactive
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw allow 22
Rules updated
Rules updated (v6)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw allow 443
Rules updated
Rules updated (v6)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: inactive
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: inactive
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw enable
Firewall is active and enabled on system startup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
22                         ALLOW       Anywhere
443                        ALLOW       Anywhere
22 (v6)                    ALLOW       Anywhere (v6)
443 (v6)                   ALLOW       Anywhere (v6)

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ echo "Linux integrity practice" > integrity.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sha256sum integrity.txt
aaee1c1f589c993c11f450234868b4078cfffcaf9c354c21c48ecaa24d39b2a4  integrity.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo chattr +i integrity.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ lsattr integrity.txt
----i---------e------- integrity.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
22                         ALLOW       Anywhere
443                        ALLOW       Anywhere
22 (v6)                    ALLOW       Anywhere (v6)
443 (v6)                   ALLOW       Anywhere (v6)

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw allow 22
sudo ufw allow 443
Skipping adding existing rule
Skipping adding existing rule (v6)
Skipping adding existing rule
Skipping adding existing rule (v6)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw enable
Firewall is active and enabled on system startup
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-09-integrity-firewall$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
22                         ALLOW       Anywhere
443                        ALLOW       Anywhere
22 (v6)                    ALLOW       Anywhere (v6)
443 (v6)                   ALLOW       Anywhere (v6)
