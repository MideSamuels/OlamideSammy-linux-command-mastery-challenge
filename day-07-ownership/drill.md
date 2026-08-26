Day 7 Drill: Ownership & Special Bits

Objective

Practice managing ownership and special permissions using chown, chgrp, chmod, and find.

Steps Completed

Created the shared-project directory.
Applied the SGID bit using chmod g+s.
Created test.txt inside the shared directory.
Confirmed the SGID permission using ls -ld.
Audited the system for SUID files using find -perm /4000.
Special Permissions

SGID: Allows files created in the shared directory to inherit the directory's group.

SUID: Allows a file to run with the permissions of its owner.

Sticky bit: Restricts deletion of files in a shared directory.

Evidence

Terminal transcript of the completed Day 7 drill is stored in evidence.md
