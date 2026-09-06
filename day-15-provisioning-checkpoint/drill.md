# Day 15 Drill: Users & Packages Checkpoint

## Objective

Provision a complete new team member account on Ubuntu by creating the user, assigning groups, setting a password, and installing the three tools required for their role in a single documented sequence.

## Steps Completed

1. Verified the user's identity and group information using id.
2. Checked the user's account information using getent passwd.
3. Created a new team member account with a home directory and assigned groups using useradd -m -G.
4. Set a password for the new user using passwd.
5. Listed all installed packages using apt list --installed.
6. Checked for packages with available upgrades using apt list --upgradable.
7. Updated the package information and installed the required tools using apt update && apt install -y.
8. Verified the installed tools by searching the package list using dpkg -l | grep.
9. Cleaned up unnecessary packages using apt autoremove.
10. Reviewed the command history using history.

## Evidence

Terminal output from the completed Day 15 Users & Packages Checkpoint drill is stored in `evidence.md` (./evidence.md).
