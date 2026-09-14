# Day 20 Drill: Text Processing & Pipes

## Objective

From a raw log file, build one pipeline that filters for `error` entries, extracts the timestamp column, sorts the results, and removes duplicates, all in a single chained command.

## Steps Completed

1. Created and opened a raw log file containing timestamps and different log entries.
2. Used `grep` to filter the log file for `ERROR` entries.
3. Used `grep -r` to search recursively for `ERROR` entries in a directory.
4. Used `grep -i` to search for `error` without considering uppercase or lowercase.
5. Used `sort` to sort the log entries alphabetically.
6. Used `sort -n` to sort numerical values in ascending order.
7. Used `uniq` to remove duplicate entries from sorted output.
8. Used `cut -d',' -f` to extract a specific column from comma-separated data.
9. Used `awk '{print $1}'` to extract the timestamp field from the log entries.
10. Used `sed 's/old/new/g'` to replace text in the log output.
11. Used the pipe operator `|` to connect multiple commands together.
12. Built one pipeline to filter `ERROR` entries, extract timestamps, sort them, and remove duplicates.

## Final Pipeline

```bash
grep "ERROR" day20-practice.log | awk '{print $1}' | sort | uniq
```

## Evidence

Terminal output from the completed Day 20 Text Processing & Pipes checkpoint is stored in [evidence.md](./evidence.md).
