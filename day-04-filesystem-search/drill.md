
# Day 4 Drill: Searching the Filesystem

## Objective

Practice searching the Linux filesystem for specific files and checking disk usage and available storage space.

## Steps Completed

1. Found every `.conf` file under `/etc`.
2. Found every file larger than 1 MB under `/var`.
3. Reported the total disk usage of `/home`.
4. Reported the remaining free space on the root filesystem.

## Commands Used

find /etc -name "*.conf"
find /var -type f -size +1M
du -sh /home
df -h /
