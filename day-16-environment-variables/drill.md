# Day 16 Drill: Environment Variables

## Objective

Set a temporary environment variable, confirm it exists, unset it, then add a directory to the PATH for the current session only and prove that the shell can find a script inside it.

## Steps Completed

1. Displayed the current environment variables using `printenv`.
2. Checked the value of the `HOME` environment variable using `printenv HOME`.
3. Created a temporary environment variable using `export`.
4. Confirmed that the temporary environment variable exists using `echo $DAY16_VAR` and `export | grep`.
5. Removed the temporary environment variable using `unset`.
6. Displayed the current `PATH` using `echo $PATH`.
7. Created a practice directory for the PATH exercise.
8. Created a simple executable script inside the practice directory.
9. Made the script executable using `chmod +x`.
10. Confirmed the script worked using its full path.
11. Added the practice directory to the current session's `PATH` using `export PATH=$PATH:`.
12. Confirmed that the practice directory was added to the `PATH`.
13. Proved that the shell could find and execute the script using `which` and the script name.
14. Used `source` safely to demonstrate reloading commands in the current shell.
15. Displayed the system-wide environment configuration using `cat /etc/environment`.

## Evidence

Terminal output from the completed Day 16 Environment Variables drill is stored in [evidence.md](./evidence.md).
