# Day 12 Drill: Groups & Access Circles

## Objective

Create and manage a Linux group by creating a group named devs, adding two users to it, confirming group membership, removing one member, and deleting the group.

## Steps Completed

1. Created a group named devs using groupadd.
2. Added two users to the devs group using gpasswd -a.
3. Confirmed the group and its members using getent group.
4. Removed one user from the devs group using gpasswd -d.
5. Confirmed the updated group membership using getent group.
6. Deleted the devs group using groupdel.

## Evidence

Terminal output from the completed Day 12 groups and access circles drill is stored in [evidence.md](./evidence.md).
