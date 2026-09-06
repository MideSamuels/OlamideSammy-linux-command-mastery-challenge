# Day 15 Users & Packages Checkpoint


10 Commands

| #  | Command                        | Purpose                                                                                 |                                                                         |
| -- | ------------------------------ | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| 1  | `id <user>`                    | Display a user's identity, UID, GID, and group membership                               |                                                                         |
| 2  | `getent passwd <user>`         | Display information about a user account from the passwd database                       |                                                                         |
| 3  | `useradd -m -G`                | Create a new user with a home directory and add the user to specified groups            |                                                                         |
| 4  | `passwd <user>`                | Set or change the password for a user                                                   |                                                                         |
| 5  | `apt list --installed`         | List packages currently installed on the system                                         |                                                                         |
| 6  | `apt list --upgradable`        | List installed packages that have available upgrades                                    |                                                                         |
| 7  | `apt update && apt install -y` | Update the package information and install a package without prompting for confirmation |                                                                         |
| 8  | `dpkg -l                       | grep`                                                                                   | Search the list of installed packages for a specific package or keyword |
| 9  | `apt autoremove`               | Remove packages that were automatically installed and are no longer required            |                                                                         |
| 10 | `history`                      | Display previously executed commands in the current shell                               |                                                                         |
