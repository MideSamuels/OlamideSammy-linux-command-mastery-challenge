olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                   day-07-ownership                  day-14-dnf-yum
day-01-file-navigation    day-08-privilege-escalation       day-15-provisioning-checkpoint
day-02-file-operations    day-09-integrity-firewall         day-16-environment-variables
day-03-file-inspection    day-10-security-audit-checkpoint  day-17-shell-configuration
day-04-filesystem-search  day-11-user-management            day-18-vim-fundamentals
day-05-links-checkpoint   day-12-groups                     day-19-vim-search-replace
day-06-permissions        day-13-apt-package-management     day-20-text-processing-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd  day-20-text-processing-checkpoint/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep "ERROR" day20-practice.log
grep: day20-practice.log: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ nano day20-practice.log
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ ls
README.md  commands.md  day20-practice.log  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep "ERROR" day20-practice.log
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:40:00 ERROR Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep -r "ERROR" logs
grep: logs: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ mkdir logs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ cp day20-practice.log logs/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep -r "ERROR" logs
logs/day20-practice.log:2026-09-14T08:15:00 ERROR Database connection failed
logs/day20-practice.log:2026-09-14T08:15:00 ERROR Database connection failed
logs/day20-practice.log:2026-09-14T08:30:00 ERROR Network connection failed
logs/day20-practice.log:2026-09-14T08:15:00 ERROR Database connection failed
logs/day20-practice.log:2026-09-14T08:30:00 ERROR Network connection failed
logs/day20-practice.log:2026-09-14T08:40:00 ERROR Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep -i "error" day20-practice.log
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:40:00 ERROR Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ sort day20-practice.log
2026-09-14T08:10:00 INFO System started
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:20:00 INFO User logged in
2026-09-14T08:25:00 WARNING High memory usage
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:35:00 INFO Backup completed
2026-09-14T08:40:00 ERROR Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ sort -n numbers.txt
sort: cannot read: numbers.txt: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ nano numbers.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ ls
README.md  commands.md  day20-practice.log  drill.md  evidence.md  logs  numbers.txt
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ sort -n numbers.txt
5
10
20
30
50
100
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ sort day20-practice.log | uniq
2026-09-14T08:10:00 INFO System started
2026-09-14T08:15:00 ERROR Database connection failed
2026-09-14T08:20:00 INFO User logged in
2026-09-14T08:25:00 WARNING High memory usage
2026-09-14T08:30:00 ERROR Network connection failed
2026-09-14T08:35:00 INFO Backup completed
2026-09-14T08:40:00 ERROR Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ cut -d',' -f1 users.csv
cut: users.csv: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ nano users.csv
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ cut -d',' -f1 users.csv
name
Samuel
David
John
Mary

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ awk '{print $1}' day20-practice.log
2026-09-14T08:10:00
2026-09-14T08:15:00
2026-09-14T08:20:00
2026-09-14T08:15:00
2026-09-14T08:25:00
2026-09-14T08:30:00
2026-09-14T08:15:00
2026-09-14T08:35:00
2026-09-14T08:30:00
2026-09-14T08:40:00
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ sed 's/ERROR/ALERT/g' day20-practice.log
2026-09-14T08:10:00 INFO System started
2026-09-14T08:15:00 ALERT Database connection failed
2026-09-14T08:20:00 INFO User logged in
2026-09-14T08:15:00 ALERT Database connection failed
2026-09-14T08:25:00 WARNING High memory usage
2026-09-14T08:30:00 ALERT Network connection failed
2026-09-14T08:15:00 ALERT Database connection failed
2026-09-14T08:35:00 INFO Backup completed
2026-09-14T08:30:00 ALERT Network connection failed
2026-09-14T08:40:00 ALERT Authentication failed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-20-text-processing-checkpoint$ grep "ERROR" day20-practice.log | awk '{print $1}' | sort | uniq
2026-09-14T08:15:00
2026-09-14T08:30:00
2026-09-14T08:40:00
