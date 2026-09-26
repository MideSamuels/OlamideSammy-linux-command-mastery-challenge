# Day 21 Drill: Viewing Processes

## Objective

Find the PID of a running process by name, view it in `top`, show it as part of the process tree, and identify which process is using port 80.

## Steps Completed

1. Used `pgrep` to find the PID of a running process by name.
2. Used `top` to view the running process and system activity.
3. Used `pstree` to show the process as part of the process tree.
4. Used `lsof -i` to identify which process is using port 80.
5. Recorded the relevant terminal output as evidence.

## Commands Actually Run

```bash
pgrep bash
top
pstree -p
lsof -i :80
```

## Results

The `pgrep bash` command returned the PID of the running Bash process. I then used `top` to view the running processes and confirm the process information.

The `pstree -p` command displayed the parent-child relationships between processes and showed the Bash process within the process tree.

The `lsof -i :80` command was used to check which process was using port 80. No process was using port 80 during the practice.

Overall, the drill helped me understand how to find process IDs, monitor running processes, view process relationships, and identify processes associated with network ports.

## Problems Encountered

I initially needed to understand how to identify the correct process from the list of running processes. Using `pgrep bash` made it easier to find the PID of the Bash process directly.

There was also no process using port 80 during the practice, so `lsof -i :80` did not return a process associated with that port.

## Evidence

Terminal output from the completed Day 21 Viewing Processes drill is stored in [**evidence.md**](./evidence.md).
