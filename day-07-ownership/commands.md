Day 07 — Ownership & Special Bits


| **Command** | **Purpose** |
|---|---|
| `chown` | Change the owner of a file or directory |
| `chown user:group` | Change both the owner and group of a file or directory |
| `chown -R` | Change ownership recursively |
| `chgrp` | Change the group ownership of a file or directory |
| `chmod u+s` | Set the SUID (Set User ID) bit |
| `chmod g+s` | Set the SGID (Set Group ID) bit |
| `chmod +t` | Set the sticky bit |
| `find -perm /4000` | Find files with the SUID permission set |
| `getfacl` | Display Access Control List (ACL) permissions |
| `setfacl -m` | Modify ACL permissions for a file or directory |
