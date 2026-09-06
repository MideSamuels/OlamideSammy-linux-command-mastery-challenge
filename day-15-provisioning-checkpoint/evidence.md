olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-03-file-inspection    day-07-ownership                  day-11-user-management
README.md               day-04-filesystem-search  day-08-privilege-escalation       day-12-groups
day-01-file-navigation  day-05-links-checkpoint   day-09-integrity-firewall         day-13-apt-package-management
day-02-file-operations  day-06-permissions        day-10-security-audit-checkpoint  day-14-dnf-yum
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-15-provisioning-checkpoint/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-15-provisioning-checkpoint/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ touch README.md drill.md ev
idence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ less drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ id $USER
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ id $USER
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo useradd -m -G users day15user
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo passwd day15user
New password:
Retype new password:
passwd: password updated successfully
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ apt list --installed
acl/resolute,now 2.3.2-2 amd64 [installed]
adduser/resolute,now 3.153ubuntu1 all [installed,automatic]
adwaita-icon-theme/resolute,now 50.0-1 all [installed,automatic]
alacritty/resolute,now 0.16.1-2ubuntu1 amd64 [installed,automatic]
apparmor/resolute-updates,now 5.0.2-0ubuntu1~26.04.1 amd64 [installed,automatic]
apport-core-dump-handler/resolute-updates,now 2.34.1-0ubuntu0.1 all [installed,automatic]
apport-symptoms/resolute,now 0.25build1 all [installed,automatic]
apport/resolute-updates,now 2.34.1-0ubuntu0.1 all [installed,automatic]
appstream/resolute,now 1.1.2-1 amd64 [installed,automatic]
apt-file/resolute,now 3.3ubuntu2 all [installed]
apt/resolute,now 3.2.0 amd64 [installed,automatic]
at-spi2-common/resolute-updates,now 2.60.4-0ubuntu0.1 all [installed,automatic]
at-spi2-core/resolute-updates,now 2.60.4-0ubuntu0.1 amd64 [installed,automatic]
base-files/resolute-updates,now 14ubuntu6.2 amd64 [installed,automatic]
base-passwd/resolute,now 3.6.8 amd64 [installed,automatic]
bash-completion/resolute,now 1:2.16.0-8build1 all [installed,automatic]
bash/resolute,now 5.3-2ubuntu1 amd64 [installed]
bc/resolute,now 1.07.1-4build1 amd64 [installed,automatic]
binutils-common/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
binutils-x86-64-linux-gnu/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
binutils/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
bsdextrautils/resolute-updates,resolute-security,now 2.41.3-3ubuntu2.2 amd64 [installed,automatic]
bsdutils/resolute-updates,resolute-security,now 1:2.41.3-3ubuntu2.2 amd64 [installed,automatic]
bubblewrap/resolute-updates,resolute-security,now 0.11.1-1ubuntu0.1 amd64 [installed,automatic]
build-essential/resolute-updates,resolute-security,now 12.12ubuntu2.26.04.2 amd64 [installed,automatic]
byobu/resolute-updates,now 6.11-0ubuntu3.1 all [installed,automatic]
bzip2/resolute-updates,resolute-security,now 1.0.8-6ubuntu0.1 amd64 [installed,automatic]
ca-certificates/resolute-updates,resolute-security,now 20260601~26.04.1 all [installed,automatic]
chrony/resolute,now 4.8-2ubuntu1 amd64 [installed,automatic]
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ apt list --upgradable
dirmngr/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gnupg-l10n/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 all [upgradable from: 2.4.8-4ubuntu3]
gnupg-utils/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gnupg/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 all [upgradable from: 2.4.8-4ubuntu3]
gpg-agent/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpg-wks-client/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpg/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgconf/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgsm/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgv/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
libaudit-common/resolute-updates 1:4.1.2-1ubuntu0.1 all [upgradable from: 1:4.1.2-1build1]
libaudit1/resolute-updates 1:4.1.2-1ubuntu0.1 amd64 [upgradable from: 1:4.1.2-1build1]
libevent-core-2.1-7t64/resolute-updates,resolute-security 2.1.12-stable-10ubuntu0.1 amd64 [upgradable from: 2.1.12-stab>
libgcrypt20/resolute-updates,resolute-security 1.12.0-2ubuntu1.1 amd64 [upgradable from: 1.12.0-2ubuntu1]
libpam-modules-bin/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libpam-modules/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libpam-runtime/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 all [upgradable from: 1.7.0-5ubuntu3.1]
libpam0g/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libssh2-1t64/resolute-updates,resolute-security 1.11.1-1ubuntu0.26.04.4 amd64 [upgradable from: 1.11.1-1ubuntu0.26.04.3]
openssh-client/resolute-updates,resolute-security 1:10.2p1-2ubuntu3.6 amd64 [upgradable from: 1:10.2p1-2ubuntu3.5]
python3-pyasn1/resolute-updates,resolute-security 0.6.3-1ubuntu0.1 all [upgradable from: 0.6.3-1]
python3-software-properties/resolute-updates 0.120.1 all [upgradable from: 0.120]
software-properties-common/resolute-updates 0.120.1 all [upgradable from: 0.120]
sudo-rs/resolute-updates,resolute-security 0.2.13-0ubuntu1.2 amd64 [upgradable from: 0.2.13-0ubuntu1]
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo apt update && sudo apt install -y tree curl htop
Hit:1 http://archive.ubuntu.com/ubuntu resolute InRelease
Get:2 http://archive.ubuntu.com/ubuntu resolute-updates InRelease [137 kB]
Get:3 http://security.ubuntu.com/ubuntu resolute-security InRelease [137 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute-backports InRelease [137 kB]
Get:5 http://security.ubuntu.com/ubuntu resolute-security/main amd64 Components [46.7 kB]
Get:6 http://security.ubuntu.com/ubuntu resolute-security/universe amd64 Components [43.5 kB]
Get:7 http://archive.ubuntu.com/ubuntu resolute-updates/main amd64 Components [97.9 kB]
Get:8 http://archive.ubuntu.com/ubuntu resolute-updates/universe amd64 Components [188 kB]
Get:9 http://archive.ubuntu.com/ubuntu resolute-backports/universe amd64 Components [1056 B]
Fetched 788 kB in 7s (118 kB/s)
24 packages can be upgraded. Run 'apt list --upgradable' to see them.
curl is already the newest version (8.18.0-1ubuntu2.4).
curl set to manually installed.
Installing:
  htop  tree

Suggested packages:
  lm-sensors  strace

Summary:
  Upgrading: 0, Installing: 2, Removing: 0, Not Upgrading: 24
  Download size: 230 kB
  Space needed: 575 kB / 1023 GB available

Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 htop amd64 3.4.1-5build2 [177 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/universe amd64 tree amd64 2.3.1-1 [53.5 kB]
Fetched 230 kB in 2s (147 kB/s)
Selecting previously unselected package htop.
(Reading database ... 81842 files and directories currently installed.)
Preparing to unpack .../htop_3.4.1-5build2_amd64.deb ...
Unpacking htop (3.4.1-5build2) ...
Selecting previously unselected package tree.
Preparing to unpack .../tree_2.3.1-1_amd64.deb ...
Unpacking tree (2.3.1-1) ...
Setting up htop (3.4.1-5build2) ...
Setting up tree (2.3.1-1) ...
Processing triggers for man-db (2.13.1-1build1) ...
Processing triggers for hicolor-icon-theme (0.18-2build1) ...
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ dpkg -l | grep -E 'tree|curl|htop'
ii  curl                                             8.18.0-1ubuntu2.4                          amd64        command line tool for transferring data with URL syntax
ii  htop                                             3.4.1-5build2                              amd64        interactive processes viewer
ii  libcurl3t64-gnutls:amd64                         8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
ii  libcurl4t64:amd64                                8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
ii  libhtml-tree-perl                                5.07-3                                     all          Perl module to represent and create HTML syntax trees
ii  libxml-twig-perl                                 1:3.54-1build1                             all          Perl module for processing huge XML documents in tree mode
ii  libxml-xpathengine-perl                          0.14-2                                     all          re-usable XPath engine for DOM-like trees
ii  node-functional-red-black-tree                   1.0.1+20181105-8                           all          fully persistent balanced binary search tree - Node.js library
ii  node-postcss-value-parser                        4.2.0-1                                    all          Transforms css values and at-rule params into the tree
ii  node-regjsgen                                    0.8.0+ds-1                                 all          Regular expression from abstract syntax trees in Node.js
ii  python3-pycurl                                   7.45.7-3build1                             amd64        Python bindings to libcurl (Python 3)
ii  tree                                             2.3.1-1                                    amd64        displays an indented directory tree, in color
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo apt autoremove
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 24
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ history
  362  cd ..
  363  git status
  364  ls
  365  rm -rf day-01-file-navigation/.git
  366  ls -la day-01-file-navigation
  367  git status
  368  git commit -m "Day 1: Linux Fundamentals & Navigation"
  369  git push origin main
  370  git remote -v
  371  git add day-01-file-navigation/
  372  git status
  373  git commit -m "Day 1: Linux Fundamentals & Navigation"
  374  git push origin main
  375  git remote -v
  376  git remote set-url origin git@github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge.git
  377  git remote -v
  378  git push origin main
  379  ls
  380  cd day-01-file-navigation
  381  ls
  382  cd ~/var/lo
  383  cd ~/var/log
  384  /var/log
  385  cd ~
  386  cd ~/OlamideSammy-linux-command-mastery-challenge
  387  cd ~
  388  cd OlamideSammy-linux-command-mastery-challenge
  389  cd ~
  390  ls
  391  cd OlamideSammy-linux-command-mastery-challenge
  392  cd ~/ linux-command-mastery-challenge
  393  cd ~/linux-command-mastery-challenge
  394  less /var/log/syslog
  395  cd ~/OlamideSammy-linux-command-mastery-challenge
  396  ls
  397  mkdir  day-03-file-inspection/
  398  ls
  399  cd day-03-file-navigation
  400  cd day-03-file-inspection
  401  touch README.md
  402  touch commands.md
  403  touch drill.md
  404  ls
  405  tou
  406  nano README.md
  407  less README.md
  408  nano README.md
  409  touch commands.md
  410  less
  411  nano commands.md
  412  nano drill.md
  413  cat README.md
  414  less commands.md
  415  less drill.md
  416  cd day-03-file-navigation
  417  cd ~/OlamideSammy-linux-command-mastery-challenge
  418  cd day-03-file-navigation
  419  cat ev
  420  cd day-03-file-inspection
  421  less
  422  nano drill.md
  423  less drill.md
  424  nano c
  425  less drill.md
  426  less commands.md
  427  nano drill.md
  428  nano commands.md
  429  less commands.md
  430  nano d
  431  less dri
  432  less ev
  433  nano r
  434  nano evidence.md
  435  less R
  436  cd ~/OlamideSammy-linux-command-mastery-challenge
  437  git status
  438  ls -la day-03-file-inspection/
  439  cd d
  440  cd day-03-file-inspection
  441  cat evidence.md
  442  cd ~/OlamideSammy-linux-command-mastery-challenge
  443  git status
  444  git add day-03-file-inspection/
  445  git status
  446  less README.md
  447  less day-03-file-inspection/READ.md
  448  less day-03-file-inspection/README.md
  449  git commit -m "Day 3: Reading & Inspecting Files"
  450  git push origin main
  451  git pull --rebase origin main
  452  git status
  453  git push origin main
  454  git status
  455  cd /var/log/syslog
  456  cd /var/log
  457  cat /var/log/syslog
  458  less /var/log/syslog
  459  tail -n 15 /var/log/syslog
  460  wc -l /var/log/syslog
  461  file /var/log/syslog
  462  stat /var/log/syslog
  463  clear
  464  mkdir day-03
  465  cd day-03
  466  touch practice.md
  467  nano practice.md
  468  cat practice.md
  469  less practice.md
  470  head practice.md
  471  head -n 15 practice.md
  472  tail practice.md
  473  tail -f practice.md
  474  wc practice.md
  475  wc -l practice.md
  476  file practice.md
  477  stat practice.md
  478  cd da
  479  ls
  480  mkdir day-04-filesystem-search
  481  ls
  482  cd day-04-filesystem-search
  483  touch ev
  484  ls
  485  touch evidence.md
  486  less c
  487  nano commands.md
  488  less d
  489  nano README.md
  490  nano drill.md
  491  less drill.md
  492  cd ~/OlamideSammy-linux-command-mastery-challenge
  493  less R
  494  less d
  495  less drill.md
  496  find ~/day-04-filesystem-search -name "*.md"
  497  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  498  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/ -type
  499  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type
  500  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  501  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  502  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  503  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  504  du ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
  505  du -sh ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
  506  sudo updatedb
  507  locate practice.md
  508  sudo updatedb
  509  locate README.md
  510  sudo apt install plocate
  511  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  512  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  513  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  514  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  515  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  516  locate ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
  517  sudo apt install plocate
  518  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  519  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  520  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  521  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  522  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  523  locate ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
  524  sudo updatedb
  525  locate commands.md
  526  find /etc -name "*.conf"
  527  find /var -type f -size +1M
  528  du -sh /home
  529  df -h /
  530  cd ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
  531  cd ~/OlamideSammy-linux-command-mastery-challenge/
  532  cd day-04-filesystem-search/evidence.md
  533  cd day-04-filesystem-search
  534  less e
  535  nano evidence.md
  536  less evidence.md
  537  cd ~/OlamideSammy-linux-command-mastery-challenge/
  538  git status
  539  git add day-04-filesystem-search/
  540  git status
  541  git commit -m "Add day 4 filesystem searching practice"
  542  git commit -m "Add Day 4 filesystem searching practice"
  543  git commit -m "Add day 4 filesystem searching practice"
  544  git push origin main
  545  git pull --rebase origin main
  546  git status
  547  git push origin main
  548  clear
  549  ls
  550  cd ~/OlamideSammy-linux-command-mastery-challenge/
  551  touch commands.md evidence.md README.md drill.md
  552  ls
  553  rm evidence.md
  554  ls
  555  rm drill.md
  556  rm commands.md
  557  ls
  558  rm README.md
  559  ls
  560  mkdir day-05-links-checkpoint
  561  ls
  562  cd day-05-links-checkpoint
  563  touch README.md drill.md evidence.md commands.md
  564  ls
  565  nano commands.md
  566  less commands.md
  567  nano commands.md
  568  less commands.md
  569  nano README.md
  570  nano drill.md
  571  tree .
  572  sudo snap install tree  # version 2.1.3+pkg-5852
  573  tree .
  574  tree -L 2 .
  575  ln commands.md hardlink.md
  576  ln -s /etc/hosts hosts-link
  577  readlink hosts-link
  578  nano RE
  579  readlink day-05-links-checkpoint/hosts-link
  580  readlink hosts-link
  581  realpath day-05-links-checkpoint/hosts-link
  582  realpath hosts-link
  583  basename "$PWD/commands.md"
  584  dirname "$PWD/commands.md"
  585  pushd /etc
  586  popd
  587  ls -lt
  588  ln -s /etc/hosts hosts-link
  589  realpath hosts-link
  590  tree -L 2 /etc
  591  less
  592  nano drill.md
  593  nano commands.md
  594  nano drill.md
  595  nano e
  596  less README.md
  597  nano evidence.md
  598  git status
  599  cd ..
  600  ls -la
  601  git status
  602  git restore README.md
  603  git status
  604  git add day-05-links-checkpoint/
  605  git status
  606  rm day-05-links-checkpoint/hardlink.md
  607  rm  day-05-links-checkpoint/hosts-link
  608  git status
  609  ~/OlamideSammy-linux-command-mastery-challenge
  610  git add -A
  611  git status
  612  cd day
  613  git status
  614  git commit -m "Add Day 5 links and checkpoints"
  615  git push origin main
  616  git pull --rebase origin main
  617  Successfully rebased and updated refs/heads/main.
  618  git push origin main
  619  cd day-05-links-checkpoint
  620  ls
  621  nano read.md
  622  ls
  623  nano README.md
  624  git status
  625  git push origin main
  626  ~/OlamideSammy-linux-command-mastery-challenge
  627  cd ~/OlamideSammy-linux-command-mastery-challenge
  628  git status
  629  git push origin main
  630  git pull --rebase origin main
  631  git add day-05-links-checkpoint/README.md
  632  git commit -m "Update Day 5 README"
  633  git pull --rebase origin main
  634  git push origin main
  635  ~/OlamideSammy-linux-command-mastery-challenge
  636  clear
  637  to
  638  ls
  639  mkdir day-06-permissions/
  640  ls
  641  cd day-06-permissions
  642  touch commands.md evidence.md README.md drill.md
  643  nano c
  644  nano README.md
  645  nano commands.md
  646  nano drill.md
  647  touch practice.sh
  648  ls -l practice.sh
  649  chmod u+x practice.sh
  650  chmod go+x practice.sh
  651  chmod u+x practice.sh
  652  chmod go+x practice.sh
  653  ls -l practice.sh
  654  chmod u=rwx,g=rx,o=rx practice.sh
  655  ls -l practice.sh
  656  chmod 755 practice.sh
  657  ls -l practice.sh
  658  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  659  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u=rwx,g=rx,o=rx practice.sh
  660  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
  661  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  662  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 755 practice.sh
  663  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
  664  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  665  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  666  chmod 644 practice.sh
  667  ls -l practice.sh
  668  chmod 600 practice.sh
  669  ls -l practice.sh
  670  mkdir permissions-test
  671  touch permissions-test/file1
  672  chmod -R 755 permissions-test
  673  ls -l permissions-test
  674  umask
  675  nano e
  676  ls -l umask-test
  677  umask -S
  678  stat -c '%A %U %G' practice.sh
  679  ls
  680  nano evidence.md
  681  cd ~/OlamideSammy-linux-command-mastery-challenge
  682  git status
  683  git add day-06-permissions/
  684  git status
  685  rm practice.sh
  686  rm day-06-permissions/practice.sh
  687  rm - r  day-06-permissions/permissions-test/file1
  688  rm -r  day-06-permissions/permissions-test/file1
  689  rm -r day-06-permissions/umask-test
  690  ls
  691  ls ~/day-06-permissions
  692  git add day-06-permissions/
  693  git status
  694  git commit -m "Add Day 6 permissions practice"
  695  git push origin main
  696  git pull --rebase origin main
  697  git status
  698  git push origin main
  699  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  700  olamide@Sammy: cd ~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  701  olamide@Sammy: cd day-06-permissions
  702  ls
  703  nano README.md
  704  cd ~/OlamideSammy-linux-command-mastery-challenge/
  705  git status
  706  git push origin main
  707  git pull --rebase origin main
  708  git commit -m "Add Day 6 permissions practice"
  709  git pull --rebase origin main
  710  git push origin main
  711  git add day-06-permissions/README.md
  712  git status
  713  git commit -m "Update Day 6 README"
  714  git pull --rebase origin main
  715  git push origin main
  716  cd day-06-permissions/
  717  nano README.md
  718  cd ~/OlamideSammy-linux-command-mastery-challenge/
  719  git status
  720  git add day-06-permissions/README.md
  721  git status
  722  git commit -m "Update Day 6 README"
  723  git pull --rebase origin main
  724  git push origin main
  725  cd ~/OlamideSammy-linux-command-mastery-challenge
  726  ls
  727  cd day-06-permissions
  728  ls
  729  rm -rf permission-test
  730  rm practice.sh
  731  rm umask-test
  732  ls
  733  rm -r permission-test
  734  rm -r permissions-test
  735  ls
  736  touch practice.sh
  737  ls -l practice.sh
  738  chmod u+x practice.sh
  739  chmod u-x practice.sh
  740  chmod a+x practice.sh
  741  ls -l practice.sh
  742  chmod u=rwx,g=rx,o=rx practice.sh
  743  ls -l practice.sh
  744  chmod 755 practice.sh
  745  ls -l practice.sh
  746  chmod 644 practice.sh
  747  ls -l practice.sh
  748  chmod 600 practice.sh
  749  ls -l practice.sh
  750  mkdir permissions-test
  751  touch permissions-test/file1
  752  chmod -R 755 permissions-test
  753  ls -l permissions-test
  754  ls -ld permissions-test
  755  umask
  756  touch umask-test
  757  ls -l umask-test
  758  umask -S
  759  stat -c '%A %U %G' practice.sh
  760  touch practice.sh
  761  ls -l practice.sh
  762  chmod u+x practice.sh
  763  chmod go+x practice.sh
  764  ls -l practice.sh
  765  chmod u+x practice.sh
  766  chmod go+x practice.sh
  767  ls -l practice.sh
  768  chmod go+r practice.sh
  769  ls -l practice.sh
  770  chmod u=rwx,g=rx,o=rx practice.sh
  771  ls -l practice.sh
  772  chmod 755 practice.sh
  773  ls -l practice.sh
  774  cd ~/OlamideSammy-linux-command-mastery-challenge
  775  ls
  776  mkdir day-07-ownership/
  777  touch README.md drill.md evidence.md commands.md
  778  ls
  779  rm drill.md evidence.md commands.md README.me
  780  rm drill.md evidence.md commands.md README.md
  781  less R
  782  cd day-07-ownership
  783  nano
  784  nano d
  785   README.md
  786  less commands.md
  787  less README.md
  788  touch practice.txt
  789  sudo chown olamide practice.txt
  790  ls -l practice.txt
  791  id
  792  sudo chown olamide:olamide practice.txt
  793  ls -l practice.txt
  794  mkdir ownership-test
  795  touch ownership-test/file.txt
  796  sudo chown -R olamide:olamide ownership-test
  797  ls -l ownership-test
  798  sudo chgrp olamide practice.txt
  799  ls -l practice.txt
  800  chmod u+s practice.txt
  801  ls -l practice.txt
  802  mkdir sgid-test
  803  chmod g+s sgid-test
  804  ls -ld sgid-test
  805  mkdir sticky-test
  806  chmod +t sticky-test
  807  ls -ld sticky-test
  808  find / -perm /4000 2>/dev/null
  809  getfacl practice.txt
  810  sudo apt install acl
  811  getfacl practice.txt
  812  setfacl -m u:olamide:r practice.txt
  813  getfacl practice.txt
  814  mkdir shared-project
  815  ls -ld shared-project
  816  chmod g+s shared-project
  817  ls -ld shared-project
  818  touch shared-project/test.txt
  819  ls -l shared-project
  820  find / -perm /4000 2>/dev/null
  821  ls -l shared-project
  822  id
  823  nan
  824  less c
  825  less dr
  826  less drill.md
  827  less evidence.md
  828  less drill.md
  829  nano drill.md
  830  less drill.md
  831  ls
  832  rm sgid-test
  833  rm pr
  834  ls
  835  rm practice.txt
  836  ls
  837  rm - r ownership-test
  838  rm -r ownership-test
  839  ls
  840  cd ~/OlamideSammy-linux-command-mastery-challenge
  841  git status
  842  git restore README.md
  843  git status
  844  git add day-07-ownership/
  845  git status
  846  rm -r  day-07-ownership/hared project directory, applying the SGID bit, and auditing the system for SUID files.
  847  cd day-07-ownership
  848  rm -r  day-07-ownership/hared project directory, applying the SGID bit, and auditing the system for SUID files.
  849  rm -r project directory, applying the SGID bit, and auditing the system for SUID files.
  850  rm -r hared project directory, applying the SGID bit, and auditing the system for SUID files.
  851  cd ..
  852  git status
  853  git commit -m "Add Day 7 ownership and special bits practice"
  854  git pull --rebase origin main
  855  git push origin main
  856  whoami
  857  exit
  858  whoami
  859  exit
  860  cd ~/OlamideSammy-linux-command-mastery-challenge
  861  ls
  862  nan
  863  ls
  864  cd day-08-privilege-escalation/
  865  touch README.md drill.md evidence.md commands.md
  866  less
  867  nano commands.md
  868  less R
  869  nano README.md
  870  less d
  871  nan
  872  less drill.md
  873  sudo ls /root
  874  sudo -i
  875  sudo -u root whoami
  876  ls /root
  877  sudo ls /root
  878  sudo -l
  879  sudo visudo
  880  su -s /bin/bash olamide
  881  su - olamide
  882  whoami
  883  id
  884  ls /root
  885  sudo ls /root
  886  sudo -l
  887  whoami
  888  id
  889  nano drill.md
  890  nano evidence.md
  891  ls
  892  cd ~/OlamideSammy-linux-command-mastery-challenge
  893  git status
  894  git add day-08-privilege-escalation/
  895  git status
  896  git commit -m "Add Day 8 privilege escalation practice"
  897  git pull --rebase origin main
  898  git push origin main
  899  cd
  900  mkdir  day-09-integrity-firewall/
  901  less
  902  touch README.md drill.md evidence.md commands.md
  903  nano README.md
  904  less README.md
  905  nano comm
  906  less drill.md
  907  nano commands.md
  908  less commands.md
  909  echo "Linux Day 9 practice" > practice.txt
  910  md5sum practice.txt
  911  sha256sum practice.txt
  912  gpg --gen-key
  913  gpg --list-keys
  914  gpg --encrypt --recipient olamide practice.txt
  915  ls -l
  916  gpg --decrypt practice.txt.gpg > decrypted.txt
  917  sudo chattr +i practice.txt
  918  lsattr practice.txt
  919  sudo ufw status
  920  sudo ufw enable
  921  sudo ufw allow 22
  922  to
  923  sudo apt update
  924  sudo apt install ufw
  925  sudo ufw status
  926  sudo ufw allow 22
  927  sudo ufw allow 443
  928  sudo ufw status
  929  sudo ufw enable
  930  sudo ufw status
  931  echo "Linux integrity practice" > integrity.txt
  932  sha256sum integrity.txt
  933  sudo chattr +i integrity.txt
  934  lsattr integrity.txt
  935  sudo ufw status
  936  sudo ufw allow 22
  937  sudo ufw allow 443
  938  sudo ufw enable
  939  sudo ufw status
  940  nano evidence.md
  941  git status
  942  cd..
  943  ls
  944  cd -
  945  ls
  946  git status
  947  git add day-09-integrity-firewall/
  948  git status
  949  cd ..
  950  cd -
  951  cd ~
  952  cd ..
  953  cd~
  954  cd ~
  955  cd
  956  cd ~/OlamideSammy-linux-command-mastery-challenge
  957  rm  day-09-integrity-firewall/decrypted.txt
  958  rm   day-09-integrity-firewall/practice.txt.gpg
  959  rm  day-09-integrity-firewall/practice.txt
  960  ls
  961  cd day-09-intergrity-firewall
  962  cd day-09-integrity-firewall
  963  ls
  964  rm integrity.txt
  965  cd ~/OlamideSammy-linux-command-mastery-challenge
  966  git add day-09-integrity-firewall/
  967  git status
  968  git commit -m "Add Day 9 integrity and firewall practice"
  969  git pull --rebase origin main
  970  git push origin main
  971  git status
  972  git rebase --edit-todo
  973  git status
  974  git rebase --edit-todo
  975  git rebase --continue
  976  git status
  977  git add day-09-integrity-firewall/
  978  git commit -m "Add Day 9 integrity and firewall practice"
  979  git push origin main
  980  git status
  981  cd day-09-integrity-firewall
  982  ls
  983  rm p
  984  rm practice.txt
  985  sudo chattr -i integrity.txt
  986  lsattr integrity.txt
  987  rm integrity.txt
  988  rm practice.txt
  989  less R
  990  touch README.md drill.md evidence.md commands.md
  991  nano README.md
  992  nano co
  993  nano README.md
  994  less co
  995  nano commands.md
  996  nano drill.md
  997  less ev
  998  nano drill.md
  999  nano evidence.md
 1000  less evidence.md
 1001  cd ..
 1002  git status
 1003  git add day-09-integrity-firewall/
 1004  git status
 1005  git commit -m "Add Day 9 integrity and firewall practice"
 1006  git pull --rebase origin main
 1007  git push origin main
 1008  cd ~/OlamideSammy-linux-command-mastery-challenge
 1009  ls
 1010  cd day-10-security-audit-checkpoint
 1011  touch README.md drill.md evidence.md commands.md
 1012  less
 1013  nano README.md
 1014  less c
 1015  nano c
 1016  nano commands.md
 1017  less d
 1018  nano drill.md
 1019  less drill.md
 1020  find / -perm /4000 2>/dev/null
 1021  last
 1022  sudo apt install wtmpdb
 1023  lastlog
 1024  sudo apt update
 1025  sudo apt install lastlog2
 1026  lastlog2
 1027  dpkg -l | grep lastlog
 1028  ls -la /var/lib/lastlog/
 1029  w
 1030  who
 1031  groups
 1032  groups olamide
 1033  passwd
 1034  sudo chage -l olamide
 1035  sudo lastb
 1036  apt-file search bin/lastb
 1037  sudo apt install apt-file
 1038  sudo apt update
 1039  sudo apt install apt-file
 1040  apt-file search bin/lastb
 1041  sudo lastb
 1042  history | grep sudo
 1043  last
 1044  ls -l /var/log/wtmp.db
 1045  sudo ls -l /var/log/wtmp.db
 1046  v
 1047  w
 1048  who
 1049  lastlog
 1050  less e
 1051  history | grep sudo
 1052  sudo lastb
 1053  sudo chage -l olamide
 1054  nano evidence.md
 1055  less evidence.md
 1056  cd ..
 1057  git status
 1058  git add day-10-security-audit-checkpoint/
 1059  git status
 1060  git commit -m "Day 10 security audit checkpoint"
 1061  git pull --rebase origin main
 1062  git push origin main
 1063  id -Gn
 1064  exit
 1065  cd ~/OlamideSammy-linux-command-mastery-challenge
 1066  mkdir day-11-user-management/
 1067  nano d
 1068  cd day-11-user-management
 1069  nano
 1070  to
 1071  nano README.md
 1072  less co
 1073  nano README.md
 1074  nano commands.md
 1075  less commands.md
 1076  nano commands.md
 1077  nano README.md
 1078  nano drill.md
 1079  sudo useradd drilluser
 1080  sudo useradd -m homeuser
 1081  sudo useradd -m -s /bin/bash challengeuser
 1082  sudo adduser interactiveuser
 1083  sudo passwd challengeuser
 1084  sudo usermod -aG <group> challengeuser
 1085  gietent group
 1086  getent group users
 1087  sudo usermod -aG users challengeuser
 1088  groups challengeuser
 1089  sudo usermod -s /bin/bash challengeuser
 1090  sudo usermod -l renameduser challengeuser
 1091  sudo userdel drilluser
 1092  sudo userdel -r renameduser
 1093  getent passwd renameduser
 1094  ls -ld /home/challengeuser
 1095  ls -ld /home/renameduser
 1096  sudo useradd -m -s /bin/bash challengeuser
 1097  ls -ld /home/challengeuser
 1098  sudo useradd -m -s /bin/bash day11user
 1099  ls -ld /home/day11user
 1100  sudo passwd day11user
 1101  getent group users
 1102  git
 1103  sudo usermod -l renameduser day11user
 1104  getent passwd renameduser
 1105  sudo userdel -r renameduser
 1106  ls -ld /home/day11user
 1107  cd ..
 1108  git s
 1109  git add day-10-user-management/
 1110  git add day-11-user-management/
 1111  git
 1112  git pull --rebase origin main
 1113  git push origin main
 1114  clear
 1115  mkdir day-12-groups/
 1116  touch README.md drill.md evidence.md commands.md
 1117  rm README.md drill.md evidence.md commands.md
 1118  less R
 1119  cd day-12-groups
 1120  touch README.md drill.md evidence.md commands.md
 1121  nano README.md
 1122  less c
 1123  less d
 1124  nano drill.md
 1125  less drill.md
 1126  sudo groupadd devs
 1127  sudo groupdel devs
 1128  sudo gpasswd -a devuser1 devs
 1129  sudo gpasswd -d devuser1 devs
 1130  getent group devs
 1131  getent passwd devuser1
 1132  groups devuser1
 1133  id -Gn devuser1
 1134  newgrp devs
 1135  sudo apt install util-linux-extra
 1136  newgrp devs
 1137  id -Gn
 1138  cat /etc/group
 1139  sudo gpasswd -a homeuser devs
 1140  sudo gpasswd -a day11user devs
 1141  sudo groupadd devs
 1142  getent group devs
 1143  sudo gpasswd -a homeuser devs
 1144  sudo gpasswd -a day11user devs
 1145  getent group devs
 1146  sudo gpasswd -d homeuser devs
 1147  getent group devs
 1148  sudo groupdel devs
 1149  getent group devs
 1150  newgrp users
 1151  sudo groupadd devs
 1152  getent group devs
 1153  sudo gpasswd -a homeuser devs
 1154  sudo gpasswd -a day11user devs
 1155  sudo gpasswd -a interactiveuser devs
 1156  getent group devs
 1157  sudo gpasswd -a interactiveuser devs
 1158  getent group devs
 1159  getent passwd homeuser
 1160  groups homeuser
 1161  id -Gn homeuser
 1162  newgrp devs
 1163  cat /etc/group
 1164  sudo gpasswd -d homeuser devs
 1165  getent group devs
 1166  sudo groupdel devs
 1167  getent group devs
 1168  nano evidence.md
 1169  git status
 1170  cd..
 1171  cd ..
 1172  git status
 1173  git restore README.md
 1174  git status
 1175  ls -la day-12-groups/
 1176  git diff -- day-12-groups/
 1177  cat day-12-groups/README.md
 1178  cat day-12-groups/commands.md
 1179  git add day-12-groups/
 1180  git pu
 1181  git commit -m "Day 12 groups and access circles"
 1182  git pus
 1183  git push origin main
 1184  cd ~/OlamideSammy-linux-command-mastery-challenge
 1185  to
 1186  mkdir  day-13-apt-package-management/
 1187  touch README.md drill.md evidence.md commands.md
 1188  nano c
 1189  ls
 1190  rm README.md drill.md evidence.md commands.md
 1191  less
 1192  cd day-13-apt-package-management
 1193  nano README.md
 1194  less co
 1195  nano commands.md
 1196  less d
 1197  nano drill.md
 1198  less e
 1199  sudo apt update
 1200  sudo apt upgrade
 1201  apt search tree
 1202  apt show tree
 1203  sudo apt install tree
 1204  tree --version
 1205  apt list --installed
 1206  apt list --installed 2>/dev/null | grep '^tree/'
 1207  sudo apt remove tree
 1208  sudo apt autoremove
 1209  sudo apt purge tree
 1210  sudo apt clean
 1211  nano evidence.md
 1212  less evidence.md
 1213  sudo apt update
 1214  sudo apt upgrade
 1215  sudo apt full-upgrade
 1216  sudo apt install tree
 1217  apt show tree
 1218  dpkg -l
 1219  dpkg -L tree
 1220  sudo apt remove tree
 1221  sudo apt purge tree
 1222  sudo apt autoremove
 1223  apt search tree
 1224  nano ev
 1225  nano evidence.md
 1226  cd ..
 1227  git s
 1228  git status
 1229  git restore README.md
 1230  git status
 1231  ls -la day-13-apt-package-management/
 1232  git commit -m "Day 13 package management"
 1233  git add day-13-apt-package-management/
 1234  git commit -m "Day 13 package management"
 1235  git pu
 1236  git pull --rebase origin main
 1237  git push origin main
 1238  cd ~/OlamideSammy-linux-command-mastery-challenge
 1239  ls
 1240  mkdir   day-14-dnf-yum/
 1241  ls
 1242  cd   day-14-dnf-yum/
 1243  touch README.md drill.md evidence.md commands.md
 1244  nano README.md
 1245  nano commands.md
 1246  nano drill.md
 1247  nano README.md
 1248  cd ~/OlamideSammy-linux-command-mastery-challenge
 1249  nano c
 1250  cd day-14-dnf-yum
 1251  ls
 1252  rm README.md.save
 1253  less R
 1254  nano README.md
 1255  less c
 1256  nano commands.md
 1257  less dr
 1258  nano commands.md
 1259  less commands.md
 1260  nano drill.md
 1261  less drill.md
 1262  nano drill.md
 1263  less drill.md
 1264  dnf --version
 1265  sudo apt install dnf
 1266  dnf --version
 1267  sudo dnf update
 1268  less drill.md
 1269  sudo apt update
 1270  sudo apt install
 1271  sudo apt remove
 1272  apt search
 1273  sudo apt install
 1274  sudo snap install
 1275  sudo add-apt-repository
 1276  pip / npm install
 1277  sudo apt install python3-pip
 1278  pip / npm install
 1279  cd pip-practice
 1280  python3 -m venv venv
 1281  source venv/bin/activate
 1282  ll
 1283  mkdir pip-practice
 1284  mkdir pip-practice
 1285  cd pip-practice
 1286  python3 -m venv venv
 1287  source venv/bin/activate
 1288  pip install requests
 1289  python3 -m venv venv
 1290  source venv/bin/activate
 1291  pip show requests
 1292  deactivate
 1293  node --version
 1294  npm --version
 1295  sudo apt update
 1296  sudo apt install -y nodejs npm
 1297  node --version
 1298  npm --version
 1299  mkdir npm-practice
 1300  cd npm-practice
 1301  npm init -y
 1302  npm install express
 1303  npm list express
 1304  cd ~/OlamideSammy-linux-command-mastery-challenge
 1305  git status
 1306  git add day-14-dnf-yum/
 1307  git status
 1308  cd day-14-dnf-yum/
 1309  ls
 1310  rm-rf pip-practice
 1311  cd
 1312  ls
 1313  cd ~/OlamideSammy-linux-command-mastery-challenge
 1314  git status
 1315  cd day-14-dnf-yum/
 1316  ls
 1317  cd ~/OlamideSammy-linux-command-mastery-challenge
 1318  ls -la day-14-dnf-yum/
 1319  git add day-14-dnf-yum/README.md day-14-dnf-yum/commands.md day-14-dnf-yum/drill.md
 1320  git commit -m "Add Day 14 documentation"
 1321  git push origin main
 1322  git pull --rebase origin main
 1323  git stash push -u -m "Day 14 work"
 1324  git pull --rebase origin main
 1325  git stash pop
 1326  git status
 1327  echo "node_modules/" >> .gitignore
 1328  git rm -r --cached day-14-dnf-yum/pip-practice/pip-practice/npm-practice/node_modules
 1329  git add day-14-dnf-yum .gitignore
 1330  git commit -m "Day 14 DNF YUM and alternative install practice"
 1331  cd
 1332  cd day-14-dnf-yum/
 1333  nano evidence.md
 1334  cd ~/OlamideSammy-linux-command-mastery-challenge
 1335  git status
 1336  git add day-14-dnf-yum
 1337  git pull --rebase origin main
 1338  git push origin main
 1339  git commit -m "day-14-dnf-yum"
 1340  git push origin main
 1341  cd ~/OlamideSammy-linux-command-mastery-challenge
 1342* less R
 1343  mkdir day-15-provisioning-checkpoint/
 1344  cd day-15-provisioning-checkpoint/
 1345  touch README.md drill.md evidence.md commands.md
 1346  nano README.md
 1347  less README.md
 1348  nano README.md
 1349  nano commands.md
 1350* less d
 1351  nano drill.md
 1352  less drill.md
 1353  id $USER
 1354  sudo useradd -m -G users day15user
 1355  sudo passwd day15user
 1356  apt list --installed
 1357  apt list --upgradable
 1358  sudo apt update && sudo apt install -y tree curl htop
 1359  dpkg -l | grep -E 'tree|curl|htop'
 1360  sudo apt autoremove
 1361  history
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ id $USER
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ getent passwd $USER
olamide:x:1000:1000::/home/olamide:/bin/bash
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ getent group users
users:x:100:olamide,interactiveuser,day15user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo useradd -m -G users day15user
useradd: user 'day15user' already exists
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ id day15user
uid=1005(day15user) gid=1006(day15user) groups=1006(day15user),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo passwd day15user
New password:
Retype new password:
passwd: password updated successfully
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ apt list --installed
acl/resolute,now 2.3.2-2 amd64 [installed]
adduser/resolute,now 3.153ubuntu1 all [installed,automatic]
adwaita-icon-theme/resolute,now 50.0-1 all [installed,automatic]
alacritty/resolute,now 0.16.1-2ubuntu1 amd64 [installed,automatic]
apparmor/resolute-updates,now 5.0.2-0ubuntu1~26.04.1 amd64 [installed,automatic]
apport-core-dump-handler/resolute-updates,now 2.34.1-0ubuntu0.1 all [installed,automatic]
apport-symptoms/resolute,now 0.25build1 all [installed,automatic]
apport/resolute-updates,now 2.34.1-0ubuntu0.1 all [installed,automatic]
appstream/resolute,now 1.1.2-1 amd64 [installed,automatic]
apt-file/resolute,now 3.3ubuntu2 all [installed]
apt/resolute,now 3.2.0 amd64 [installed,automatic]
at-spi2-common/resolute-updates,now 2.60.4-0ubuntu0.1 all [installed,automatic]
at-spi2-core/resolute-updates,now 2.60.4-0ubuntu0.1 amd64 [installed,automatic]
base-files/resolute-updates,now 14ubuntu6.2 amd64 [installed,automatic]
base-passwd/resolute,now 3.6.8 amd64 [installed,automatic]
bash-completion/resolute,now 1:2.16.0-8build1 all [installed,automatic]
bash/resolute,now 5.3-2ubuntu1 amd64 [installed]
bc/resolute,now 1.07.1-4build1 amd64 [installed,automatic]
binutils-common/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
binutils-x86-64-linux-gnu/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
binutils/resolute,now 2.46-3ubuntu2 amd64 [installed,automatic]
bsdextrautils/resolute-updates,resolute-security,now 2.41.3-3ubuntu2.2 amd64 [installed,automatic]
bsdutils/resolute-updates,resolute-security,now 1:2.41.3-3ubuntu2.2 amd64 [installed,automatic]
bubblewrap/resolute-updates,resolute-security,now 0.11.1-1ubuntu0.1 amd64 [installed,automatic]
build-essential/resolute-updates,resolute-security,now 12.12ubuntu2.26.04.2 amd64 [installed,automatic]
byobu/resolute-updates,now 6.11-0ubuntu3.1 all [installed,automatic]
bzip2/resolute-updates,resolute-security,now 1.0.8-6ubuntu0.1 amd64 [installed,automatic]
ca-certificates/resolute-updates,resolute-security,now 20260601~26.04.1 all [installed,automatic]
chrony/resolute,now 4.8-2ubuntu1 amd64 [installed,automatic]
cloud-guest-utils/resolute,now 0.33-1build1 all [installed,automatic]
cloud-init-base/resolute-updates,now 26.1-0ubuntu3~26.04.1 all [installed,automatic]
cloud-init/resolute-updates,now 26.1-0ubuntu3~26.04.1 all [installed,automatic]
command-not-found/resolute,now 23.04.0build1 all [installed,automatic]
console-setup-linux/resolute-updates,now 1.237ubuntu3.1 all [installed,automatic]
console-setup/resolute-updates,now 1.237ubuntu3.1 all [installed,automatic]
coreutils-from-uutils/resolute,now 0.0.0~ubuntu25 all [installed]
coreutils/resolute,now 9.5-1ubuntu2+0.0.0~ubuntu25 all [installed]
cpp-15-x86-64-linux-gnu/resolute,now 15.2.0-16ubuntu1 amd64 [installed,automatic]
cpp-15/resolute,now 15.2.0-16ubuntu1 amd64 [installed,automatic]
cpp-x86-64-linux-gnu/resolute,now 4:15.2.0-5ubuntu1 amd64 [installed,automatic]
cpp/resolute,now 4:15.2.0-5ubuntu1 amd64 [installed,automatic]
cron-daemon-common/resolute,now 3.0pl1-200ubuntu1 all [installed,automatic]
cron/resolute,now 3.0pl1-200ubuntu1 amd64 [installed,automatic]
curl/resolute-updates,resolute-security,now 8.18.0-1ubuntu2.4 amd64 [installed]
dash/resolute,now 0.5.12-12ubuntu3 amd64 [installed]
dbus-bin/resolute,now 1.16.2-2ubuntu4 amd64 [installed,automatic]
dbus-daemon/resolute,now 1.16.2-2ubuntu4 amd64 [installed,automatic]
dbus-session-bus-common/resolute,now 1.16.2-2ubuntu4 all [installed,automatic]
dbus-system-bus-common/resolute,now 1.16.2-2ubuntu4 all [installed,automatic]
dbus-user-session/resolute,now 1.16.2-2ubuntu4 amd64 [installed,automatic]
dbus-x11/resolute,now 1.16.2-2ubuntu4 amd64 [installed,automatic]
dbus/resolute,now 1.16.2-2ubuntu4 amd64 [installed,automatic]
dconf-gsettings-backend/resolute,now 0.49.0-4 amd64 [installed,automatic]
dconf-service/resolute,now 0.49.0-4 amd64 [installed,automatic]
debconf-i18n/resolute,now 1.5.92 all [installed,automatic]
debconf/resolute,now 1.5.92 all [installed,automatic]
debianutils/resolute,now 5.23.2build1 amd64 [installed,automatic]
deltarpm/resolute,now 3.6.5+dfsg-3build1 amd64 [installed,automatic]
dhcpcd-base/resolute,now 1:10.3.0-7 amd64 [installed,automatic]
diffutils/resolute-updates,resolute-security,now 1:3.12-1ubuntu0.1 amd64 [installed]
dirmngr/resolute,now 2.4.8-4ubuntu3 amd64 [installed,upgradable to: 2.4.8-4ubuntu3.1]
distro-info-data/resolute-updates,resolute-security,now 0.72-0ubuntu0.26.04.1 all [installed,automatic]
distro-info/resolute,now 1.15 amd64 [installed,automatic]
dmsetup/resolute,now 2:1.02.205-2ubuntu3 amd64 [installed,automatic]
dnf-data/resolute,now 4.24.0-1build1 all [installed,automatic]
dnf/resolute,now 4.24.0-1build1 all [installed]
dpkg-dev/resolute,now 1.23.7ubuntu1 all [installed,automatic]
dpkg/resolute,now 1.23.7ubuntu1 amd64 [installed]
e2fsprogs/resolute,now 1.47.2-3ubuntu4 amd64 [installed,automatic]
eatmydata/resolute,now 131-2build1 all [installed,automatic]
ed/resolute,now 1.22.4-1 amd64 [installed,automatic]
eject/resolute-updates,resolute-security,now 2.41.3-3ubuntu2.2 amd64 [installed,automatic]
eslint/resolute,now 6.4.0~dfsg+~6.1.9-12 all [installed,automatic]
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ apt list --upgradable
dirmngr/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gnupg-l10n/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 all [upgradable from: 2.4.8-4ubuntu3]
gnupg-utils/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gnupg/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 all [upgradable from: 2.4.8-4ubuntu3]
gpg-agent/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpg-wks-client/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpg/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgconf/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgsm/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
gpgv/resolute-updates,resolute-security 2.4.8-4ubuntu3.1 amd64 [upgradable from: 2.4.8-4ubuntu3]
libaudit-common/resolute-updates 1:4.1.2-1ubuntu0.1 all [upgradable from: 1:4.1.2-1build1]
libaudit1/resolute-updates 1:4.1.2-1ubuntu0.1 amd64 [upgradable from: 1:4.1.2-1build1]
libevent-core-2.1-7t64/resolute-updates,resolute-security 2.1.12-stable-10ubuntu0.1 amd64 [upgradable from: 2.1.12-stab>
libgcrypt20/resolute-updates,resolute-security 1.12.0-2ubuntu1.1 amd64 [upgradable from: 1.12.0-2ubuntu1]
libpam-modules-bin/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libpam-modules/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libpam-runtime/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 all [upgradable from: 1.7.0-5ubuntu3.1]
libpam0g/resolute-updates,resolute-security 1.7.0-5ubuntu3.2 amd64 [upgradable from: 1.7.0-5ubuntu3.1]
libssh2-1t64/resolute-updates,resolute-security 1.11.1-1ubuntu0.26.04.4 amd64 [upgradable from: 1.11.1-1ubuntu0.26.04.3]
openssh-client/resolute-updates,resolute-security 1:10.2p1-2ubuntu3.6 amd64 [upgradable from: 1:10.2p1-2ubuntu3.5]
python3-pyasn1/resolute-updates,resolute-security 0.6.3-1ubuntu0.1 all [upgradable from: 0.6.3-1]
python3-software-properties/resolute-updates 0.120.1 all [upgradable from: 0.120]
software-properties-common/resolute-updates 0.120.1 all [upgradable from: 0.120]
sudo-rs/resolute-updates,resolute-security 0.2.13-0ubuntu1.2 amd64 [upgradable from: 0.2.13-0ubuntu1]
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ sudo apt update && sudo apt install -y tree curl htop
Hit:1 http://security.ubuntu.com/ubuntu resolute-security InRelease
Hit:2 http://archive.ubuntu.com/ubuntu resolute InRelease
Hit:3 http://archive.ubuntu.com/ubuntu resolute-updates InRelease
Hit:4 http://archive.ubuntu.com/ubuntu resolute-backports InRelease
24 packages can be upgraded. Run 'apt list --upgradable' to see them.
tree is already the newest version (2.3.1-1).
curl is already the newest version (8.18.0-1ubuntu2.4).
htop is already the newest version (3.4.1-5build2).
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 24
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ dpkg -l | grep -E 'tree|curl|htop'
ii  curl                                             8.18.0-1ubuntu2.4                          amd64        command line tool for transferring data with URL syntax
ii  htop                                             3.4.1-5build2                              amd64        interactive processes viewer
ii  libcurl3t64-gnutls:amd64                         8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
ii  libcurl4t64:amd64                                8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
ii  libhtml-tree-perl                                5.07-3                                     all          Perl module to represent and create HTML syntax trees
ii  libxml-twig-perl                                 1:3.54-1build1                             all          Perl module for processing huge XML documents in tree mode
ii  libxml-xpathengine-perl                          0.14-2                                     all          re-usable XPath engine for DOM-like trees
ii  node-functional-red-black-tree                   1.0.1+20181105-8                           all          fully persistent balanced binary search tree - Node.js library
ii  node-postcss-value-parser                        4.2.0-1                                    all          Transforms css values and at-rule params into the tree
ii  node-regjsgen                                    0.8.0+ds-1                                 all          Regular expression from abstract syntax trees in Node.js
ii  python3-pycurl                                   7.45.7-3build1                             amd64        Python bindings to libcurl (Python 3)
ii  tree                                             2.3.1-1                                    amd64        displays an indented directory tree, in color
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ dpkg -l | grep -E 'tree|curl|htop'
ii  curl                                             8.18.0-1ubuntu2.4                          amd64        command line tool for transferring data with URL syntax
ii  htop                                             3.4.1-5build2                              amd64        interactive processes viewer
ii  libcurl3t64-gnutls:amd64                         8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
ii  libcurl4t64:amd64                                8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
ii  libhtml-tree-perl                                5.07-3                                     all          Perl module to represent and create HTML syntax trees
ii  libxml-twig-perl                                 1:3.54-1build1                             all          Perl module for processing huge XML documents in tree mode
ii  libxml-xpathengine-perl                          0.14-2                                     all          re-usable XPath engine for DOM-like trees
ii  node-functional-red-black-tree                   1.0.1+20181105-8                           all          fully persistent balanced binary search tree - Node.js library
ii  node-postcss-value-parser                        4.2.0-1                                    all          Transforms css values and at-rule params into the tree
ii  node-regjsgen                                    0.8.0+ds-1                                 all          Regular expression from abstract syntax trees in Node.js
ii  python3-pycurl                                   7.45.7-3build1                             amd64        Python bindings to libcurl (Python 3)
ii  tree                                             2.3.1-1                                    amd64        displays an indented directory tree, in color
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ history
  373  git commit -m "Day 1: Linux Fundamentals & Navigation"
  374  git push origin main
  375  git remote -v
  376  git remote set-url origin git@github.com:MideSamuels/OlamideSammy-linux-command-mastery-challenge.git
  377  git remote -v
  378  git push origin main
  379  ls
  380  cd day-01-file-navigation
  381  ls
  382  cd ~/var/lo
  383  cd ~/var/log
  384  /var/log
  385  cd ~
  386  cd ~/OlamideSammy-linux-command-mastery-challenge
  387  cd ~
  388  cd OlamideSammy-linux-command-mastery-challenge
  389  cd ~
  390  ls
  391  cd OlamideSammy-linux-command-mastery-challenge
  392  cd ~/ linux-command-mastery-challenge
  393  cd ~/linux-command-mastery-challenge
  394  less /var/log/syslog
  395  cd ~/OlamideSammy-linux-command-mastery-challenge
  396  ls
  397  mkdir  day-03-file-inspection/
  398  ls
  399  cd day-03-file-navigation
  400  cd day-03-file-inspection
  401  touch README.md
  402  touch commands.md
  403  touch drill.md
  404  ls
  405  tou
  406  nano README.md
  407  less README.md
  408  nano README.md
  409  touch commands.md
  410  less
  411  nano commands.md
  412  nano drill.md
  413  cat README.md
  414  less commands.md
  415  less drill.md
  416  cd day-03-file-navigation
  417  cd ~/OlamideSammy-linux-command-mastery-challenge
  418  cd day-03-file-navigation
  419  cat ev
  420  cd day-03-file-inspection
  421  less
  422  nano drill.md
  423  less drill.md
  424  nano c
  425  less drill.md
  426  less commands.md
  427  nano drill.md
  428  nano commands.md
  429  less commands.md
  430  nano d
  431  less dri
  432  less ev
  433  nano r
  434  nano evidence.md
  435  less R
  436  cd ~/OlamideSammy-linux-command-mastery-challenge
  437  git status
  438  ls -la day-03-file-inspection/
  439  cd d
  440  cd day-03-file-inspection
  441  cat evidence.md
  442  cd ~/OlamideSammy-linux-command-mastery-challenge
  443  git status
  444  git add day-03-file-inspection/
  445  git status
  446  less README.md
  447  less day-03-file-inspection/READ.md
  448  less day-03-file-inspection/README.md
  449  git commit -m "Day 3: Reading & Inspecting Files"
  450  git push origin main
  451  git pull --rebase origin main
  452  git status
  453  git push origin main
  454  git status
  455  cd /var/log/syslog
  456  cd /var/log
  457  cat /var/log/syslog
  458  less /var/log/syslog
  459  tail -n 15 /var/log/syslog
  460  wc -l /var/log/syslog
  461  file /var/log/syslog
  462  stat /var/log/syslog
  463  clear
  464  mkdir day-03
  465  cd day-03
  466  touch practice.md
  467  nano practice.md
  468  cat practice.md
  469  less practice.md
  470  head practice.md
  471  head -n 15 practice.md
  472  tail practice.md
  473  tail -f practice.md
  474  wc practice.md
  475  wc -l practice.md
  476  file practice.md
  477  stat practice.md
  478  cd da
  479  ls
  480  mkdir day-04-filesystem-search
  481  ls
  482  cd day-04-filesystem-search
  483  touch ev
  484  ls
  485  touch evidence.md
  486  less c
  487  nano commands.md
  488  less d
  489  nano README.md
  490  nano drill.md
  491  less drill.md
  492  cd ~/OlamideSammy-linux-command-mastery-challenge
  493  less R
  494  less d
  495  less drill.md
  496  find ~/day-04-filesystem-search -name "*.md"
  497  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  498  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/ -type
  499  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type
  500  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  501  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  502  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  503  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  504  du ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
  505  du -sh ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
  506  sudo updatedb
  507  locate practice.md
  508  sudo updatedb
  509  locate README.md
  510  sudo apt install plocate
  511  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  512  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  513  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  514  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  515  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  516  locate ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
  517  sudo apt install plocate
  518  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
  519  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
  520  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
  521  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
  522  find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
  523  locate ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
  524  sudo updatedb
  525  locate commands.md
  526  find /etc -name "*.conf"
  527  find /var -type f -size +1M
  528  du -sh /home
  529  df -h /
  530  cd ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
  531  cd ~/OlamideSammy-linux-command-mastery-challenge/
  532  cd day-04-filesystem-search/evidence.md
  533  cd day-04-filesystem-search
  534  less e
  535  nano evidence.md
  536  less evidence.md
  537  cd ~/OlamideSammy-linux-command-mastery-challenge/
  538  git status
  539  git add day-04-filesystem-search/
  540  git status
  541  git commit -m "Add day 4 filesystem searching practice"
  542  git commit -m "Add Day 4 filesystem searching practice"
  543  git commit -m "Add day 4 filesystem searching practice"
  544  git push origin main
  545  git pull --rebase origin main
  546  git status
  547  git push origin main
  548  clear
  549  ls
  550  cd ~/OlamideSammy-linux-command-mastery-challenge/
  551  touch commands.md evidence.md README.md drill.md
  552  ls
  553  rm evidence.md
  554  ls
  555  rm drill.md
  556  rm commands.md
  557  ls
  558  rm README.md
  559  ls
  560  mkdir day-05-links-checkpoint
  561  ls
  562  cd day-05-links-checkpoint
  563  touch README.md drill.md evidence.md commands.md
  564  ls
  565  nano commands.md
  566  less commands.md
  567  nano commands.md
  568  less commands.md
  569  nano README.md
  570  nano drill.md
  571  tree .
  572  sudo snap install tree  # version 2.1.3+pkg-5852
  573  tree .
  574  tree -L 2 .
  575  ln commands.md hardlink.md
  576  ln -s /etc/hosts hosts-link
  577  readlink hosts-link
  578  nano RE
  579  readlink day-05-links-checkpoint/hosts-link
  580  readlink hosts-link
  581  realpath day-05-links-checkpoint/hosts-link
  582  realpath hosts-link
  583  basename "$PWD/commands.md"
  584  dirname "$PWD/commands.md"
  585  pushd /etc
  586  popd
  587  ls -lt
  588  ln -s /etc/hosts hosts-link
  589  realpath hosts-link
  590  tree -L 2 /etc
  591  less
  592  nano drill.md
  593  nano commands.md
  594  nano drill.md
  595  nano e
  596  less README.md
  597  nano evidence.md
  598  git status
  599  cd ..
  600  ls -la
  601  git status
  602  git restore README.md
  603  git status
  604  git add day-05-links-checkpoint/
  605  git status
  606  rm day-05-links-checkpoint/hardlink.md
  607  rm  day-05-links-checkpoint/hosts-link
  608  git status
  609  ~/OlamideSammy-linux-command-mastery-challenge
  610  git add -A
  611  git status
  612  cd day
  613  git status
  614  git commit -m "Add Day 5 links and checkpoints"
  615  git push origin main
  616  git pull --rebase origin main
  617  Successfully rebased and updated refs/heads/main.
  618  git push origin main
  619  cd day-05-links-checkpoint
  620  ls
  621  nano read.md
  622  ls
  623  nano README.md
  624  git status
  625  git push origin main
  626  ~/OlamideSammy-linux-command-mastery-challenge
  627  cd ~/OlamideSammy-linux-command-mastery-challenge
  628  git status
  629  git push origin main
  630  git pull --rebase origin main
  631  git add day-05-links-checkpoint/README.md
  632  git commit -m "Update Day 5 README"
  633  git pull --rebase origin main
  634  git push origin main
  635  ~/OlamideSammy-linux-command-mastery-challenge
  636  clear
  637  to
  638  ls
  639  mkdir day-06-permissions/
  640  ls
  641  cd day-06-permissions
  642  touch commands.md evidence.md README.md drill.md
  643  nano c
  644  nano README.md
  645  nano commands.md
  646  nano drill.md
  647  touch practice.sh
  648  ls -l practice.sh
  649  chmod u+x practice.sh
  650  chmod go+x practice.sh
  651  chmod u+x practice.sh
  652  chmod go+x practice.sh
  653  ls -l practice.sh
  654  chmod u=rwx,g=rx,o=rx practice.sh
  655  ls -l practice.sh
  656  chmod 755 practice.sh
  657  ls -l practice.sh
  658  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  659  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod u=rwx,g=rx,o=rx practice.sh
  660  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
  661  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  662  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ chmod 755 practice.sh
  663  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$ ls -l practice.sh
  664  -rwxr-xr-x 1 olamide olamide 0 Aug 25 20:12 practice.sh
  665  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  666  chmod 644 practice.sh
  667  ls -l practice.sh
  668  chmod 600 practice.sh
  669  ls -l practice.sh
  670  mkdir permissions-test
  671  touch permissions-test/file1
  672  chmod -R 755 permissions-test
  673  ls -l permissions-test
  674  umask
  675  nano e
  676  ls -l umask-test
  677  umask -S
  678  stat -c '%A %U %G' practice.sh
  679  ls
  680  nano evidence.md
  681  cd ~/OlamideSammy-linux-command-mastery-challenge
  682  git status
  683  git add day-06-permissions/
  684  git status
  685  rm practice.sh
  686  rm day-06-permissions/practice.sh
  687  rm - r  day-06-permissions/permissions-test/file1
  688  rm -r  day-06-permissions/permissions-test/file1
  689  rm -r day-06-permissions/umask-test
  690  ls
  691  ls ~/day-06-permissions
  692  git add day-06-permissions/
  693  git status
  694  git commit -m "Add Day 6 permissions practice"
  695  git push origin main
  696  git pull --rebase origin main
  697  git status
  698  git push origin main
  699  olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  700  olamide@Sammy: cd ~/OlamideSammy-linux-command-mastery-challenge/day-06-permissions$
  701  olamide@Sammy: cd day-06-permissions
  702  ls
  703  nano README.md
  704  cd ~/OlamideSammy-linux-command-mastery-challenge/
  705  git status
  706  git push origin main
  707  git pull --rebase origin main
  708  git commit -m "Add Day 6 permissions practice"
  709  git pull --rebase origin main
  710  git push origin main
  711  git add day-06-permissions/README.md
  712  git status
  713  git commit -m "Update Day 6 README"
  714  git pull --rebase origin main
  715  git push origin main
  716  cd day-06-permissions/
  717  nano README.md
  718  cd ~/OlamideSammy-linux-command-mastery-challenge/
  719  git status
  720  git add day-06-permissions/README.md
  721  git status
  722  git commit -m "Update Day 6 README"
  723  git pull --rebase origin main
  724  git push origin main
  725  cd ~/OlamideSammy-linux-command-mastery-challenge
  726  ls
  727  cd day-06-permissions
  728  ls
  729  rm -rf permission-test
  730  rm practice.sh
  731  rm umask-test
  732  ls
  733  rm -r permission-test
  734  rm -r permissions-test
  735  ls
  736  touch practice.sh
  737  ls -l practice.sh
  738  chmod u+x practice.sh
  739  chmod u-x practice.sh
  740  chmod a+x practice.sh
  741  ls -l practice.sh
  742  chmod u=rwx,g=rx,o=rx practice.sh
  743  ls -l practice.sh
  744  chmod 755 practice.sh
  745  ls -l practice.sh
  746  chmod 644 practice.sh
  747  ls -l practice.sh
  748  chmod 600 practice.sh
  749  ls -l practice.sh
  750  mkdir permissions-test
  751  touch permissions-test/file1
  752  chmod -R 755 permissions-test
  753  ls -l permissions-test
  754  ls -ld permissions-test
  755  umask
  756  touch umask-test
  757  ls -l umask-test
  758  umask -S
  759  stat -c '%A %U %G' practice.sh
  760  touch practice.sh
  761  ls -l practice.sh
  762  chmod u+x practice.sh
  763  chmod go+x practice.sh
  764  ls -l practice.sh
  765  chmod u+x practice.sh
  766  chmod go+x practice.sh
  767  ls -l practice.sh
  768  chmod go+r practice.sh
  769  ls -l practice.sh
  770  chmod u=rwx,g=rx,o=rx practice.sh
  771  ls -l practice.sh
  772  chmod 755 practice.sh
  773  ls -l practice.sh
  774  cd ~/OlamideSammy-linux-command-mastery-challenge
  775  ls
  776  mkdir day-07-ownership/
  777  touch README.md drill.md evidence.md commands.md
  778  ls
  779  rm drill.md evidence.md commands.md README.me
  780  rm drill.md evidence.md commands.md README.md
  781  less R
  782  cd day-07-ownership
  783  nano
  784  nano d
  785   README.md
  786  less commands.md
  787  less README.md
  788  touch practice.txt
  789  sudo chown olamide practice.txt
  790  ls -l practice.txt
  791  id
  792  sudo chown olamide:olamide practice.txt
  793  ls -l practice.txt
  794  mkdir ownership-test
  795  touch ownership-test/file.txt
  796  sudo chown -R olamide:olamide ownership-test
  797  ls -l ownership-test
  798  sudo chgrp olamide practice.txt
  799  ls -l practice.txt
  800  chmod u+s practice.txt
  801  ls -l practice.txt
  802  mkdir sgid-test
  803  chmod g+s sgid-test
  804  ls -ld sgid-test
  805  mkdir sticky-test
  806  chmod +t sticky-test
  807  ls -ld sticky-test
  808  find / -perm /4000 2>/dev/null
  809  getfacl practice.txt
  810  sudo apt install acl
  811  getfacl practice.txt
  812  setfacl -m u:olamide:r practice.txt
  813  getfacl practice.txt
  814  mkdir shared-project
  815  ls -ld shared-project
  816  chmod g+s shared-project
  817  ls -ld shared-project
  818  touch shared-project/test.txt
  819  ls -l shared-project
  820  find / -perm /4000 2>/dev/null
  821  ls -l shared-project
  822  id
  823  nan
  824  less c
  825  less dr
  826  less drill.md
  827  less evidence.md
  828  less drill.md
  829  nano drill.md
  830  less drill.md
  831  ls
  832  rm sgid-test
  833  rm pr
  834  ls
  835  rm practice.txt
  836  ls
  837  rm - r ownership-test
  838  rm -r ownership-test
  839  ls
  840  cd ~/OlamideSammy-linux-command-mastery-challenge
  841  git status
  842  git restore README.md
  843  git status
  844  git add day-07-ownership/
  845  git status
  846  rm -r  day-07-ownership/hared project directory, applying the SGID bit, and auditing the system for SUID files.
  847  cd day-07-ownership
  848  rm -r  day-07-ownership/hared project directory, applying the SGID bit, and auditing the system for SUID files.
  849  rm -r project directory, applying the SGID bit, and auditing the system for SUID files.
  850  rm -r hared project directory, applying the SGID bit, and auditing the system for SUID files.
  851  cd ..
  852  git status
  853  git commit -m "Add Day 7 ownership and special bits practice"
  854  git pull --rebase origin main
  855  git push origin main
  856  whoami
  857  exit
  858  whoami
  859  exit
  860  cd ~/OlamideSammy-linux-command-mastery-challenge
  861  ls
  862  nan
  863  ls
  864  cd day-08-privilege-escalation/
  865  touch README.md drill.md evidence.md commands.md
  866  less
  867  nano commands.md
  868  less R
  869  nano README.md
  870  less d
  871  nan
  872  less drill.md
  873  sudo ls /root
  874  sudo -i
  875  sudo -u root whoami
  876  ls /root
  877  sudo ls /root
  878  sudo -l
  879  sudo visudo
  880  su -s /bin/bash olamide
  881  su - olamide
  882  whoami
  883  id
  884  ls /root
  885  sudo ls /root
  886  sudo -l
  887  whoami
  888  id
  889  nano drill.md
  890  nano evidence.md
  891  ls
  892  cd ~/OlamideSammy-linux-command-mastery-challenge
  893  git status
  894  git add day-08-privilege-escalation/
  895  git status
  896  git commit -m "Add Day 8 privilege escalation practice"
  897  git pull --rebase origin main
  898  git push origin main
  899  cd
  900  mkdir  day-09-integrity-firewall/
  901  less
  902  touch README.md drill.md evidence.md commands.md
  903  nano README.md
  904  less README.md
  905  nano comm
  906  less drill.md
  907  nano commands.md
  908  less commands.md
  909  echo "Linux Day 9 practice" > practice.txt
  910  md5sum practice.txt
  911  sha256sum practice.txt
  912  gpg --gen-key
  913  gpg --list-keys
  914  gpg --encrypt --recipient olamide practice.txt
  915  ls -l
  916  gpg --decrypt practice.txt.gpg > decrypted.txt
  917  sudo chattr +i practice.txt
  918  lsattr practice.txt
  919  sudo ufw status
  920  sudo ufw enable
  921  sudo ufw allow 22
  922  to
  923  sudo apt update
  924  sudo apt install ufw
  925  sudo ufw status
  926  sudo ufw allow 22
  927  sudo ufw allow 443
  928  sudo ufw status
  929  sudo ufw enable
  930  sudo ufw status
  931  echo "Linux integrity practice" > integrity.txt
  932  sha256sum integrity.txt
  933  sudo chattr +i integrity.txt
  934  lsattr integrity.txt
  935  sudo ufw status
  936  sudo ufw allow 22
  937  sudo ufw allow 443
  938  sudo ufw enable
  939  sudo ufw status
  940  nano evidence.md
  941  git status
  942  cd..
  943  ls
  944  cd -
  945  ls
  946  git status
  947  git add day-09-integrity-firewall/
  948  git status
  949  cd ..
  950  cd -
  951  cd ~
  952  cd ..
  953  cd~
  954  cd ~
  955  cd
  956  cd ~/OlamideSammy-linux-command-mastery-challenge
  957  rm  day-09-integrity-firewall/decrypted.txt
  958  rm   day-09-integrity-firewall/practice.txt.gpg
  959  rm  day-09-integrity-firewall/practice.txt
  960  ls
  961  cd day-09-intergrity-firewall
  962  cd day-09-integrity-firewall
  963  ls
  964  rm integrity.txt
  965  cd ~/OlamideSammy-linux-command-mastery-challenge
  966  git add day-09-integrity-firewall/
  967  git status
  968  git commit -m "Add Day 9 integrity and firewall practice"
  969  git pull --rebase origin main
  970  git push origin main
  971  git status
  972  git rebase --edit-todo
  973  git status
  974  git rebase --edit-todo
  975  git rebase --continue
  976  git status
  977  git add day-09-integrity-firewall/
  978  git commit -m "Add Day 9 integrity and firewall practice"
  979  git push origin main
  980  git status
  981  cd day-09-integrity-firewall
  982  ls
  983  rm p
  984  rm practice.txt
  985  sudo chattr -i integrity.txt
  986  lsattr integrity.txt
  987  rm integrity.txt
  988  rm practice.txt
  989  less R
  990  touch README.md drill.md evidence.md commands.md
  991  nano README.md
  992  nano co
  993  nano README.md
  994  less co
  995  nano commands.md
  996  nano drill.md
  997  less ev
  998  nano drill.md
  999  nano evidence.md
 1000  less evidence.md
 1001  cd ..
 1002  git status
 1003  git add day-09-integrity-firewall/
 1004  git status
 1005  git commit -m "Add Day 9 integrity and firewall practice"
 1006  git pull --rebase origin main
 1007  git push origin main
 1008  cd ~/OlamideSammy-linux-command-mastery-challenge
 1009  ls
 1010  cd day-10-security-audit-checkpoint
 1011  touch README.md drill.md evidence.md commands.md
 1012  less
 1013  nano README.md
 1014  less c
 1015  nano c
 1016  nano commands.md
 1017  less d
 1018  nano drill.md
 1019  less drill.md
 1020  find / -perm /4000 2>/dev/null
 1021  last
 1022  sudo apt install wtmpdb
 1023  lastlog
 1024  sudo apt update
 1025  sudo apt install lastlog2
 1026  lastlog2
 1027  dpkg -l | grep lastlog
 1028  ls -la /var/lib/lastlog/
 1029  w
 1030  who
 1031  groups
 1032  groups olamide
 1033  passwd
 1034  sudo chage -l olamide
 1035  sudo lastb
 1036  apt-file search bin/lastb
 1037  sudo apt install apt-file
 1038  sudo apt update
 1039  sudo apt install apt-file
 1040  apt-file search bin/lastb
 1041  sudo lastb
 1042  history | grep sudo
 1043  last
 1044  ls -l /var/log/wtmp.db
 1045  sudo ls -l /var/log/wtmp.db
 1046  v
 1047  w
 1048  who
 1049  lastlog
 1050  less e
 1051  history | grep sudo
 1052  sudo lastb
 1053  sudo chage -l olamide
 1054  nano evidence.md
 1055  less evidence.md
 1056  cd ..
 1057  git status
 1058  git add day-10-security-audit-checkpoint/
 1059  git status
 1060  git commit -m "Day 10 security audit checkpoint"
 1061  git pull --rebase origin main
 1062  git push origin main
 1063  id -Gn
 1064  exit
 1065  cd ~/OlamideSammy-linux-command-mastery-challenge
 1066  mkdir day-11-user-management/
 1067  nano d
 1068  cd day-11-user-management
 1069  nano
 1070  to
 1071  nano README.md
 1072  less co
 1073  nano README.md
 1074  nano commands.md
 1075  less commands.md
 1076  nano commands.md
 1077  nano README.md
 1078  nano drill.md
 1079  sudo useradd drilluser
 1080  sudo useradd -m homeuser
 1081  sudo useradd -m -s /bin/bash challengeuser
 1082  sudo adduser interactiveuser
 1083  sudo passwd challengeuser
 1084  sudo usermod -aG <group> challengeuser
 1085  gietent group
 1086  getent group users
 1087  sudo usermod -aG users challengeuser
 1088  groups challengeuser
 1089  sudo usermod -s /bin/bash challengeuser
 1090  sudo usermod -l renameduser challengeuser
 1091  sudo userdel drilluser
 1092  sudo userdel -r renameduser
 1093  getent passwd renameduser
 1094  ls -ld /home/challengeuser
 1095  ls -ld /home/renameduser
 1096  sudo useradd -m -s /bin/bash challengeuser
 1097  ls -ld /home/challengeuser
 1098  sudo useradd -m -s /bin/bash day11user
 1099  ls -ld /home/day11user
 1100  sudo passwd day11user
 1101  getent group users
 1102  git
 1103  sudo usermod -l renameduser day11user
 1104  getent passwd renameduser
 1105  sudo userdel -r renameduser
 1106  ls -ld /home/day11user
 1107  cd ..
 1108  git s
 1109  git add day-10-user-management/
 1110  git add day-11-user-management/
 1111  git
 1112  git pull --rebase origin main
 1113  git push origin main
 1114  clear
 1115  mkdir day-12-groups/
 1116  touch README.md drill.md evidence.md commands.md
 1117  rm README.md drill.md evidence.md commands.md
 1118  less R
 1119  cd day-12-groups
 1120  touch README.md drill.md evidence.md commands.md
 1121  nano README.md
 1122  less c
 1123  less d
 1124  nano drill.md
 1125  less drill.md
 1126  sudo groupadd devs
 1127  sudo groupdel devs
 1128  sudo gpasswd -a devuser1 devs
 1129  sudo gpasswd -d devuser1 devs
 1130  getent group devs
 1131  getent passwd devuser1
 1132  groups devuser1
 1133  id -Gn devuser1
 1134  newgrp devs
 1135  sudo apt install util-linux-extra
 1136  newgrp devs
 1137  id -Gn
 1138  cat /etc/group
 1139  sudo gpasswd -a homeuser devs
 1140  sudo gpasswd -a day11user devs
 1141  sudo groupadd devs
 1142  getent group devs
 1143  sudo gpasswd -a homeuser devs
 1144  sudo gpasswd -a day11user devs
 1145  getent group devs
 1146  sudo gpasswd -d homeuser devs
 1147  getent group devs
 1148  sudo groupdel devs
 1149  getent group devs
 1150  newgrp users
 1151  sudo groupadd devs
 1152  getent group devs
 1153  sudo gpasswd -a homeuser devs
 1154  sudo gpasswd -a day11user devs
 1155  sudo gpasswd -a interactiveuser devs
 1156  getent group devs
 1157  sudo gpasswd -a interactiveuser devs
 1158  getent group devs
 1159  getent passwd homeuser
 1160  groups homeuser
 1161  id -Gn homeuser
 1162  newgrp devs
 1163  cat /etc/group
 1164  sudo gpasswd -d homeuser devs
 1165  getent group devs
 1166  sudo groupdel devs
 1167  getent group devs
 1168  nano evidence.md
 1169  git status
 1170  cd..
 1171  cd ..
 1172  git status
 1173  git restore README.md
 1174  git status
 1175  ls -la day-12-groups/
 1176  git diff -- day-12-groups/
 1177  cat day-12-groups/README.md
 1178  cat day-12-groups/commands.md
 1179  git add day-12-groups/
 1180  git pu
 1181  git commit -m "Day 12 groups and access circles"
 1182  git pus
 1183  git push origin main
 1184  cd ~/OlamideSammy-linux-command-mastery-challenge
 1185  to
 1186  mkdir  day-13-apt-package-management/
 1187  touch README.md drill.md evidence.md commands.md
 1188  nano c
 1189  ls
 1190  rm README.md drill.md evidence.md commands.md
 1191  less
 1192  cd day-13-apt-package-management
 1193  nano README.md
 1194  less co
 1195  nano commands.md
 1196  less d
 1197  nano drill.md
 1198  less e
 1199  sudo apt update
 1200  sudo apt upgrade
 1201  apt search tree
 1202  apt show tree
 1203  sudo apt install tree
 1204  tree --version
 1205  apt list --installed
 1206  apt list --installed 2>/dev/null | grep '^tree/'
 1207  sudo apt remove tree
 1208  sudo apt autoremove
 1209  sudo apt purge tree
 1210  sudo apt clean
 1211  nano evidence.md
 1212  less evidence.md
 1213  sudo apt update
 1214  sudo apt upgrade
 1215  sudo apt full-upgrade
 1216  sudo apt install tree
 1217  apt show tree
 1218  dpkg -l
 1219  dpkg -L tree
 1220  sudo apt remove tree
 1221  sudo apt purge tree
 1222  sudo apt autoremove
 1223  apt search tree
 1224  nano ev
 1225  nano evidence.md
 1226  cd ..
 1227  git s
 1228  git status
 1229  git restore README.md
 1230  git status
 1231  ls -la day-13-apt-package-management/
 1232  git commit -m "Day 13 package management"
 1233  git add day-13-apt-package-management/
 1234  git commit -m "Day 13 package management"
 1235  git pu
 1236  git pull --rebase origin main
 1237  git push origin main
 1238  cd ~/OlamideSammy-linux-command-mastery-challenge
 1239  ls
 1240  mkdir   day-14-dnf-yum/
 1241  ls
 1242  cd   day-14-dnf-yum/
 1243  touch README.md drill.md evidence.md commands.md
 1244  nano README.md
 1245  nano commands.md
 1246  nano drill.md
 1247  nano README.md
 1248  cd ~/OlamideSammy-linux-command-mastery-challenge
 1249  nano c
 1250  cd day-14-dnf-yum
 1251  ls
 1252  rm README.md.save
 1253  less R
 1254  nano README.md
 1255  less c
 1256  nano commands.md
 1257  less dr
 1258  nano commands.md
 1259  less commands.md
 1260  nano drill.md
 1261  less drill.md
 1262  nano drill.md
 1263  less drill.md
 1264  dnf --version
 1265  sudo apt install dnf
 1266  dnf --version
 1267  sudo dnf update
 1268  less drill.md
 1269  sudo apt update
 1270  sudo apt install
 1271  sudo apt remove
 1272  apt search
 1273  sudo apt install
 1274  sudo snap install
 1275  sudo add-apt-repository
 1276  pip / npm install
 1277  sudo apt install python3-pip
 1278  pip / npm install
 1279  cd pip-practice
 1280  python3 -m venv venv
 1281  source venv/bin/activate
 1282  ll
 1283  mkdir pip-practice
 1284  mkdir pip-practice
 1285  cd pip-practice
 1286  python3 -m venv venv
 1287  source venv/bin/activate
 1288  pip install requests
 1289  python3 -m venv venv
 1290  source venv/bin/activate
 1291  pip show requests
 1292  deactivate
 1293  node --version
 1294  npm --version
 1295  sudo apt update
 1296  sudo apt install -y nodejs npm
 1297  node --version
 1298  npm --version
 1299  mkdir npm-practice
 1300  cd npm-practice
 1301  npm init -y
 1302  npm install express
 1303  npm list express
 1304  cd ~/OlamideSammy-linux-command-mastery-challenge
 1305  git status
 1306  git add day-14-dnf-yum/
 1307  git status
 1308  cd day-14-dnf-yum/
 1309  ls
 1310  rm-rf pip-practice
 1311  cd
 1312  ls
 1313  cd ~/OlamideSammy-linux-command-mastery-challenge
 1314  git status
 1315  cd day-14-dnf-yum/
 1316  ls
 1317  cd ~/OlamideSammy-linux-command-mastery-challenge
 1318  ls -la day-14-dnf-yum/
 1319  git add day-14-dnf-yum/README.md day-14-dnf-yum/commands.md day-14-dnf-yum/drill.md
 1320  git commit -m "Add Day 14 documentation"
 1321  git push origin main
 1322  git pull --rebase origin main
 1323  git stash push -u -m "Day 14 work"
 1324  git pull --rebase origin main
 1325  git stash pop
 1326  git status
 1327  echo "node_modules/" >> .gitignore
 1328  git rm -r --cached day-14-dnf-yum/pip-practice/pip-practice/npm-practice/node_modules
 1329  git add day-14-dnf-yum .gitignore
 1330  git commit -m "Day 14 DNF YUM and alternative install practice"
 1331  cd
 1332  cd day-14-dnf-yum/
 1333  nano evidence.md
 1334  cd ~/OlamideSammy-linux-command-mastery-challenge
 1335  git status
 1336  git add day-14-dnf-yum
 1337  git pull --rebase origin main
 1338  git push origin main
 1339  git commit -m "day-14-dnf-yum"
 1340  git push origin main
 1341  cd ~/OlamideSammy-linux-command-mastery-challenge
 1342* less R
 1343  mkdir day-15-provisioning-checkpoint/
 1344  cd day-15-provisioning-checkpoint/
 1345  touch README.md drill.md evidence.md commands.md
 1346  nano README.md
 1347  less README.md
 1348  nano README.md
 1349  nano commands.md
 1350* less d
 1351  nano drill.md
 1352  less drill.md
 1353  id $USER
 1354  sudo useradd -m -G users day15user
 1355  sudo passwd day15user
 1356  apt list --installed
 1357  apt list --upgradable
 1358  sudo apt update && sudo apt install -y tree curl htop
 1359  dpkg -l | grep -E 'tree|curl|htop'
 1360  sudo apt autoremove
 1361  history
 1362  id $USER
 1363  getent passwd $USER
 1364  getent group users
 1365  sudo useradd -m -G users day15user
 1366  id day15user
 1367  sudo passwd day15user
 1368  apt list --installed
 1369  apt list --upgradable
 1370  sudo apt update && sudo apt install -y tree curl htop
 1371  dpkg -l | grep -E 'tree|curl|htop'
 1372  history
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ id day15user
uid=1005(day15user) gid=1006(day15user) groups=1006(day15user),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ ls -ld /home/day15user
drwxr-x--- 2 day15user day15user 4096 Sep  6 22:45 /home/day15user
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-15-provisioning-checkpoint$ dpkg -l | grep -E 'tree|curl|htop'
ii  curl                                             8.18.0-1ubuntu2.4                          amd64        command line tool for transferring data with URL syntax
ii  htop                                             3.4.1-5build2                              amd64        interactive processes viewer
ii  libcurl3t64-gnutls:amd64                         8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
ii  libcurl4t64:amd64                                8.18.0-1ubuntu2.4                          amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
ii  libhtml-tree-perl                                5.07-3                                     all          Perl module to represent and create HTML syntax trees
ii  libxml-twig-perl                                 1:3.54-1build1                             all          Perl module for processing huge XML documents in tree mode
ii  libxml-xpathengine-perl                          0.14-2                                     all          re-usable XPath engine for DOM-like trees
ii  node-functional-red-black-tree                   1.0.1+20181105-8                           all          fully persistent balanced binary search tree - Node.js library
ii  node-postcss-value-parser                        4.2.0-1                                    all          Transforms css values and at-rule params into the tree
ii  node-regjsgen                                    0.8.0+ds-1                                 all          Regular expression from abstract syntax trees in Node.js
ii  python3-pycurl                                   7.45.7-3build1                             amd64        Python bindings to libcurl (Python 3)
ii  tree                                             2.3.1-1                                    amd64        displays an indented directory tree, in color

