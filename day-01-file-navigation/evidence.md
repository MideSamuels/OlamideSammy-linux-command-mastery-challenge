olamide@Sammy:~$ pwd
/home/olamide
olamide@Sammy:~$ cd/var/log
-bash: cd/var/log: No such file or directory
olamide@Sammy:~$ cd /var/log
olamide@Sammy:/var/log$ cd ~
olamide@Sammy:~$ cd _
-bash: cd: _: No such file or directory
olamide@Sammy:~$ cd -
/var/log
olamide@Sammy:/var/log$ ls -lh
total 2.2M
lrwxrwxrwx  1 root      root              39 Apr 20 19:05 README -> ../../usr/share/doc/systemd/README.logs
-rw-r--r--  1 root      root            8.0K Aug 18 17:45 alternatives.log
-rw-r--r--  1 root      root             18K Apr 20 19:07 alternatives.log.1
drwxr-xr-x  2 root      root            4.0K Aug 18 17:45 apt
-rw-r-----  1 syslog    adm             4.5K Aug 19 14:17 auth.log
-rw-r-----  1 syslog    adm              13K Aug 15 18:36 auth.log.1
-rw-r--r--  1 root      root            145K Apr 20 19:06 bootstrap.log
-rw-rw----  1 root      utmp               0 Aug 15 19:04 btmp
-rw-rw----  1 root      utmp               0 Apr 20 19:05 btmp.1
drwxr-x---  2 _chrony   _chrony         4.0K May  7 18:41 chrony
drwxr-xr-x  2 root      root            4.0K Apr 16 18:50 dist-upgrade
-rw-r-----  1 root      adm              34K Aug 19 10:57 dmesg
-rw-r-----  1 root      adm              34K Aug 18 17:44 dmesg.0
-rw-r-----  1 root      adm              11K Aug 18 16:50 dmesg.1.gz
-rw-r-----  1 root      adm              11K Aug 15 20:23 dmesg.2.gz
-rw-r-----  1 root      adm              11K Aug 15 18:36 dmesg.3.gz
-rw-r-----  1 root      adm              11K Jul 26 15:58 dmesg.4.gz
-rw-r--r--  1 root      root             79K Aug 18 17:45 dpkg.log
-rw-r--r--  1 root      root            271K Apr 20 19:07 dpkg.log.1
-rw-r--r--  1 root      root             790 Apr 20 19:07 fontconfig.log
drwxr-sr-x+ 3 root      systemd-journal 4.0K May  7 18:41 journal
-rw-r-----  1 syslog    adm             130K Aug 19 12:45 kern.log
-rw-r-----  1 syslog    adm             313K Aug 15 18:46 kern.log.1
drwxr-xr-x  2 landscape landscape       4.0K May  7 18:41 landscape
-rw-rw-r--  1 root      utmp               0 Apr 20 19:05 lastlog
drwx------  2 root      root            4.0K Apr 20 19:05 private
-rw-r-----  1 syslog    adm             314K Aug 19 14:29 syslog
-rw-r-----  1 syslog    adm             696K Aug 15 19:04 syslog.1
drwxr-x---  2 root      adm             4.0K Aug 15 19:04 unattended-upgrades
-rw-rw-r--  1 root      utmp            8.3K Aug 19 10:57 wtmp
olamide@Sammy:/var/log$
