# Day 3 Drill: Reading & Inspecting Files

## Objective
Practice reading and inspecting a Linux log file by viewing its contents, navigating through it, examining specific sections, counting its lines, identifying its file type, and inspecting its metadata.

## Steps Completed
1. Selected a log file on the Ubuntu system for inspection.
2. Viewed the complete contents of the log file using cat.
3. Paged through the log file using less.
4. Displayed the first 15 lines using head -n.
5. Displayed the last 15 lines using tail.
6. Counted the total number of lines using wc -l.
7. Identified the file type using file.
8. Inspected the file's detailed metadata using stat.

## Commands Used
cat /var/log/syslog
less /var/log/syslog
head -n 15 /var/log/syslog
tail -n 15 /var/log/syslog
wc -l /var/log/syslog
file /var/log/syslog
stat /var/log/syslog

