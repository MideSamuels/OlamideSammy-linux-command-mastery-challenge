olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.5  0.1  24252 14680 ?        Ss   22:27   0:05 /sbin/init
root           2  0.0  0.0   3120  2176 ?        Sl   22:27   0:00 /init
root           8  0.0  0.0   3120  1792 ?        Sl   22:27   0:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10
root          60  0.0  0.2  50400 16128 ?        S<s  22:27   0:00 /usr/lib/systemd/systemd-journald
systemd+      99  0.0  0.1  22400 13824 ?        Ss   22:27   0:00 /usr/lib/systemd/systemd-resolved
root         108  1.0  0.1  35500 11776 ?        Ss   22:27   0:10 /usr/lib/systemd/systemd-udevd
root         124  0.0  0.0  85476  1284 ?        Ssl  22:27   0:00 snapfuse /var/lib/snapd/snaps/snapd_27710.snap /snap/snapd/27710 -
root         127  0.2  0.1 454136 12628 ?        Ssl  22:27   0:02 snapfuse /var/lib/snapd/snaps/snapd_27738.snap /snap/snapd/27738 -
root         130  0.0  0.0 159340  1668 ?        Ssl  22:27   0:00 snapfuse /var/lib/snapd/snaps/core22_2437.snap /snap/core22/2437 -
root         138  0.0  0.0 159340  1412 ?        Ssl  22:27   0:00 snapfuse /var/lib/snapd/snaps/tree_54.snap /snap/tree/54 -o ro,nod
root         183  0.0  0.0   2880  1920 ?        Ss   22:27   0:00 /bin/sh /usr/lib/systemd/scripts/chronyd-starter.sh -n -F 1
root         184  0.0  0.0   4464  2944 ?        Ss   22:27   0:00 /usr/sbin/cron -f -P
message+     185  0.0  0.0   8816  4992 ?        Ss   22:27   0:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --sy
root         224  0.0  0.3  44080 28980 ?        Ss   22:27   0:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --run-startup-trigge
root         231  0.1  0.4 1998928 39460 ?       Ssl  22:27   0:01 /snap/snapd/current/usr/lib/snapd/snapd
root         232  0.0  0.1  18412  8832 ?        Ss   22:27   0:00 /usr/lib/systemd/systemd-logind
syslog       271  0.0  0.0 220532  5376 ?        Ssl  22:27   0:00 /usr/sbin/rsyslogd -n -iNONE
_chrony      306  0.0  0.1  23840 10876 ?        S    22:27   0:00 /usr/sbin/chronyd -n -F 1 -x
_chrony      316  0.0  0.0  12080  2276 ?        S    22:27   0:00 /usr/sbin/chronyd -n -F 1 -x
root         340  0.0  0.0   5528  2688 hvc0     Ss+  22:27   0:00 /usr/sbin/agetty --noreset --noclear --issue-file=/etc/issue:/etc/
root         342  0.0  0.4 123384 31988 ?        Ssl  22:27   0:00 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade
root         354  0.0  0.0   5484  2560 tty1     Ss+  22:27   0:00 /usr/sbin/agetty --noreset --noclear --issue-file=/etc/issue:/etc/
root         409  0.0  0.0   3128   900 ?        Ss   22:27   0:00 /init
root         410  0.0  0.0   3144  1160 ?        S    22:27   0:00 /init
olamide      411  0.0  0.0   6260  5248 pts/0    Ss   22:27   0:00 -bash
root         413  0.0  0.0  10464  6656 ?        Ss   22:27   0:00 login -- olamide
olamide      510  0.0  0.1  22528 13056 ?        Ss   22:27   0:00 /usr/lib/systemd/systemd --user
olamide      512  0.0  0.0  24328  4104 ?        S    22:27   0:00 (sd-pam)
olamide      544  0.0  0.0   6260  4992 pts/1    Ss+  22:27   0:00 -bash
olamide     1264  0.0  0.0   7152  4096 pts/0    R+   22:44   0:00 ps aux
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 22:27 ?        00:00:05 /sbin/init
root           2       1  0 22:27 ?        00:00:00 /init
root           8       2  0 22:27 ?        00:00:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10 --log-truncate
root          60       1  0 22:27 ?        00:00:00 /usr/lib/systemd/systemd-journald
systemd+      99       1  0 22:27 ?        00:00:00 /usr/lib/systemd/systemd-resolved
root         108       1  1 22:27 ?        00:00:11 /usr/lib/systemd/systemd-udevd
root         124       1  0 22:27 ?        00:00:00 snapfuse /var/lib/snapd/snaps/snapd_27710.snap /snap/snapd/27710 -o ro,nodev,allo
root         127       1  0 22:27 ?        00:00:02 snapfuse /var/lib/snapd/snaps/snapd_27738.snap /snap/snapd/27738 -o ro,nodev,allo
root         130       1  0 22:27 ?        00:00:00 snapfuse /var/lib/snapd/snaps/core22_2437.snap /snap/core22/2437 -o ro,nodev,allo
root         138       1  0 22:27 ?        00:00:00 snapfuse /var/lib/snapd/snaps/tree_54.snap /snap/tree/54 -o ro,nodev,allow_other,
root         183       1  0 22:27 ?        00:00:00 /bin/sh /usr/lib/systemd/scripts/chronyd-starter.sh -n -F 1
root         184       1  0 22:27 ?        00:00:00 /usr/sbin/cron -f -P
message+     185       1  0 22:27 ?        00:00:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activatio
root         224       1  0 22:27 ?        00:00:00 /usr/bin/python3 /usr/bin/networkd-dispatcher --run-startup-triggers
root         231       1  0 22:27 ?        00:00:01 /snap/snapd/current/usr/lib/snapd/snapd
root         232       1  0 22:27 ?        00:00:00 /usr/lib/systemd/systemd-logind
syslog       271       1  0 22:27 ?        00:00:00 /usr/sbin/rsyslogd -n -iNONE
_chrony      306     183  0 22:27 ?        00:00:00 /usr/sbin/chronyd -n -F 1 -x
_chrony      316     306  0 22:27 ?        00:00:00 /usr/sbin/chronyd -n -F 1 -x
root         340       1  0 22:27 hvc0     00:00:00 /usr/sbin/agetty --noreset --noclear --issue-file=/etc/issue:/etc/issue.d:/run/is
root         342       1  0 22:27 ?        00:00:00 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade-shutdown --wai
root         354       1  0 22:27 tty1     00:00:00 /usr/sbin/agetty --noreset --noclear --issue-file=/etc/issue:/etc/issue.d:/run/is
root         409       2  0 22:27 ?        00:00:00 /init
root         410     409  0 22:27 ?        00:00:00 /init
olamide      411     410  0 22:27 pts/0    00:00:00 -bash
root         413       2  0 22:27 ?        00:00:00 login -- olamide
olamide      510       1  0 22:27 ?        00:00:00 /usr/lib/systemd/systemd --user
olamide      512     510  0 22:27 ?        00:00:00 (sd-pam)
olamide      544     413  0 22:27 pts/1    00:00:00 -bash
root        1285     108  0 22:45 ?        00:00:00 (udev-worker)
root        1286     108  0 22:45 ?        00:00:00 (udev-worker)
olamide     1292     411  0 22:45 pts/0    00:00:00 ps -ef
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ ps -u olamide
    PID TTY          TIME CMD
    411 pts/0    00:00:00 bash
    510 ?        00:00:00 systemd
    512 ?        00:00:00 (sd-pam)
    544 pts/1    00:00:00 bash
   1306 pts/0    00:00:00 ps
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ top
top - 22:45:58 up 19 min,  1 user,  load average: 0.00, 0.00, 0.00
Tasks:  32 total,   1 running,  31 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.1 us,  0.8 sy,  0.0 ni, 99.0 id,  0.0 wa,  0.0 hi,  0.1 si,  0.0 st
MiB Mem :   7765.2 total,   7266.3 free,    492.6 used,    156.6 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   7272.6 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
   1321 root      20   0   35504   6444   3200 S   0.7   0.1   0:00.03 (udev-worker)
    108 root      20   0   35500  11776   8832 S   0.3   0.1   0:11.47 systemd-udevd
    231 root      20   0 1998928  39460  25856 S   0.3   0.5   0:01.99 snapd
   1322 root      20   0   35504   6444   3200 S   0.3   0.1   0:00.02 (udev-worker)
      1 root      20   0   24252  14680  11096 S   0.0   0.2   0:05.35 systemd
      2 root      20   0    3120   2176   2048 S   0.0   0.0   0:00.01 init-systemd(Ub
      8 root      20   0    3120   1792   1792 S   0.0   0.0   0:00.00 init
     60 root      19  -1   50400  16128  15104 S   0.0   0.2   0:00.76 systemd-journal
     99 systemd+  20   0   22400  13824  11520 S   0.0   0.2   0:00.48 systemd-resolve
    124 root      20   0   85476   1284   1152 S   0.0   0.0   0:00.00 snapfuse
    127 root      20   0  454136  12628   1280 S   0.0   0.2   0:02.96 snapfuse
    130 root      20   0  159340   1668   1408 S   0.0   0.0   0:00.00 snapfuse
    138 root      20   0  159340   1412   1280 S   0.0   0.0   0:00.00 snapfuse
    183 root      20   0    2880   1920   1792 S   0.0   0.0   0:00.10 chronyd-starter
    184 root      20   0    4464   2944   2816 S   0.0   0.0   0:00.05 cron
    185 message+  20   0    8816   4992   4480 S   0.0   0.1   0:00.14 dbus-daemon
    224 root      20   0   44080  28980  14080 S   0.0   0.4   0:00.53 networkd-dispat
    232 root      20   0   18412   8832   7808 S   0.0   0.1   0:00.21 systemd-logind
    271 syslog    20   0  220532   5376   4352 S   0.0   0.1   0:00.13 rsyslogd
    306 _chrony   20   0   23840  10876   6912 S   0.0   0.1   0:00.14 chronyd
    316 _chrony   20   0   12080   2276   1664 S   0.0   0.0   0:00.00 chronyd
    340 root      20   0    5528   2688   2560 S   0.0   0.0   0:00.02 agetty
    342 root      20   0  123384  31988  17536 S   0.0   0.4   0:00.31 unattended-upgr
    354 root      20   0    5484   2560   2432 S   0.0   0.0   0:00.01 agetty
    409 root      20   0    3128    900    768 S   0.0   0.0   0:00.00 SessionLeader
    410 root      20   0    3144   1160   1024 S   0.0   0.0   0:00.62 Relay(411)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ htop
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pgrep bash
411
544
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pstree
systemd─┬─2*[agetty]
        ├─chronyd-starter───chronyd───chronyd
        ├─cron
        ├─dbus-daemon
        ├─init-systemd(Ub─┬─SessionLeader───Relay(411)───bash───pstree
        │                 ├─init───{init}
        │                 ├─login───bash
        │                 └─{init-systemd(Ub}
        ├─networkd-dispat
        ├─rsyslogd───3*[{rsyslogd}]
        ├─snapd───10*[{snapd}]
        ├─snapfuse───{snapfuse}
        ├─snapfuse───6*[{snapfuse}]
        ├─2*[snapfuse───2*[{snapfuse}]]
        ├─systemd───(sd-pam)
        ├─systemd-journal
        ├─systemd-logind
        ├─systemd-resolve
        ├─systemd-udevd───2*[(udev-worker)]
        └─unattended-upgr───{unattended-upgr}
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pstree
systemd─┬─2*[agetty]
        ├─chronyd-starter───chronyd───chronyd
        ├─cron
        ├─dbus-daemon
        ├─init-systemd(Ub─┬─SessionLeader───Relay(411)───bash───pstree
        │                 ├─init───{init}
        │                 ├─login───bash
        │                 └─{init-systemd(Ub}
        ├─networkd-dispat
        ├─rsyslogd───3*[{rsyslogd}]
        ├─snapd───10*[{snapd}]
        ├─snapfuse───{snapfuse}
        ├─snapfuse───6*[{snapfuse}]
        ├─2*[snapfuse───2*[{snapfuse}]]
        ├─systemd───(sd-pam)
        ├─systemd-journal
        ├─systemd-logind
        ├─systemd-resolve
        ├─systemd-udevd
        └─unattended-upgr───{unattended-upgr}
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ lsof -i
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ jobs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ nice sleep 60 &
[1] 1441
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pgrep sleep
1441
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ renice 10 -p <PID>
-bash: syntax error near unexpected token `newline'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pgrep bash
411
544
[1]+  Done                       nice sleep 60
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ top
top - 22:49:55 up 23 min,  1 user,  load average: 0.58, 0.18, 0.06
Tasks:  32 total,   1 running,  31 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.1 us,  0.3 sy,  0.0 ni, 99.6 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7765.2 total,   7261.2 free,    494.1 used,    160.7 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   7271.2 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
    108 root      20   0   35500  11776   8832 S   0.7   0.1   0:13.30 systemd-udevd
   1503 root      20   0   35504   6444   3200 S   0.3   0.1   0:00.01 (udev-worker)
      1 root      20   0   24252  14680  11096 S   0.0   0.2   0:05.35 systemd
      2 root      20   0    3120   2176   2048 S   0.0   0.0   0:00.01 init-systemd(Ub
      8 root      20   0    3120   1792   1792 S   0.0   0.0   0:00.00 init
     60 root      19  -1   50400  16128  15104 S   0.0   0.2   0:00.76 systemd-journal
     99 systemd+  20   0   22400  13824  11520 S   0.0   0.2   0:00.48 systemd-resolve
    124 root      20   0   85476   1284   1152 S   0.0   0.0   0:00.00 snapfuse
    127 root      20   0  454136  12628   1280 S   0.0   0.2   0:02.96 snapfuse
    130 root      20   0  159340   1668   1408 S   0.0   0.0   0:00.00 snapfuse
    138 root      20   0  159340   1412   1280 S   0.0   0.0   0:00.00 snapfuse
    183 root      20   0    2880   1920   1792 S   0.0   0.0   0:00.10 chronyd-starter
    184 root      20   0    4464   2944   2816 S   0.0   0.0   0:00.05 cron
    185 message+  20   0    8816   4992   4480 S   0.0   0.1   0:00.14 dbus-daemon
    224 root      20   0   44080  28980  14080 S   0.0   0.4   0:00.53 networkd-dispat
    231 root      20   0 1998928  39460  25856 S   0.0   0.5   0:02.11 snapd
    232 root      20   0   18412   8832   7808 S   0.0   0.1   0:00.21 systemd-logind
    271 syslog    20   0  220532   5376   4352 S   0.0   0.1   0:00.13 rsyslogd
    306 _chrony   20   0   23840  10876   6912 S   0.0   0.1   0:00.14 chronyd
    316 _chrony   20   0   12080   2276   1664 S   0.0   0.0   0:00.00 chronyd
    340 root      20   0    5528   2688   2560 S   0.0   0.0   0:00.02 agetty
    342 root      20   0  123384  31988  17536 S   0.0   0.4   0:00.31 unattended-upgr
    354 root      20   0    5484   2560   2432 S   0.0   0.0   0:00.01 agetty
    409 root      20   0    3128    900    768 S   0.0   0.0   0:00.00 SessionLeader
    410 root      20   0    3144   1160   1024 S   0.0   0.0   0:00.66 Relay(411)
    411 olamide   20   0    6904   5760   3584 S   0.0   0.1   0:00.45 bash
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pstree
systemd─┬─2*[agetty]
        ├─chronyd-starter───chronyd───chronyd
        ├─cron
        ├─dbus-daemon
        ├─init-systemd(Ub─┬─SessionLeader───Relay(411)───bash───pstree
        │                 ├─init───{init}
        │                 ├─login───bash
        │                 └─{init-systemd(Ub}
        ├─networkd-dispat
        ├─rsyslogd───3*[{rsyslogd}]
        ├─snapd───10*[{snapd}]
        ├─snapfuse───{snapfuse}
        ├─snapfuse───6*[{snapfuse}]
        ├─2*[snapfuse───2*[{snapfuse}]]
        ├─systemd───(sd-pam)
        ├─systemd-journal
        ├─systemd-logind
        ├─systemd-resolve
        ├─systemd-udevd───2*[(udev-worker)]
        └─unattended-upgr───{unattended-upgr}
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ lsof -i
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ :80
:80: command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ :80
:80: command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ pgrep bash
411
544
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$ lsof -i :80
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-21-viewing-processes$
