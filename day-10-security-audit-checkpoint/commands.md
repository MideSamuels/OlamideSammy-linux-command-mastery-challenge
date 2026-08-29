Day 10: Security Checkpoint & Audit

| **Command** | **Purpose** |
|---|---|
| `find / -perm /4000` | Audit the system for SUID files |
| `last` | Show recent login history |
| `lastlog` | Show the last login of users |
| `w` | Show who is currently logged in |
| `who` | Display currently logged-in users |
| `groups` | Show the groups a user belongs to |
| `passwd` | Change or manage a user's password |
| `chage -l` | Display password aging information |
| `lastb` | Show failed login attempts |
| `history \| grep sudo` | Find sudo commands in shell history |
