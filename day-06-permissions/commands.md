| **Command** | **Purpose** |
|---|---|
| `ls -l` | Display the permission string, ownership, and other file details |
| `chmod` | Change file and directory permissions |
| `chmod + / -` | Add or remove permissions using the relative method |
| `chmod =` | Set specific permissions using the assignment method |
| `chmod 755` | Set permissions to `rwxr-xr-x` |
| `chmod 644` | Set permissions to `rw-r--r--` |
| `chmod 600` | Set permissions to `rw-------` |
| `chmod -R` | Apply permission changes recursively |
| `umask` | Display the default permission mask |
| `umask -S` | Display the default permission mask in symbolic form |
| `stat -c '%A %U %G'` | Display permissions, owner, and group |
