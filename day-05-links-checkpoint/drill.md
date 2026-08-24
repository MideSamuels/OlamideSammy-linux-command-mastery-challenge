# Day 5 Drill: Paths, Links & Tree Structures

## Objective
Practice creating symbolic links, resolving file paths, viewing directory structures, and understanding the difference between hard links and symbolic links.

## Steps Completed
1. Created a symbolic link to a configuration file  - ‘ln -s /etc/hosts ~/hosts-link’
2. Resolved the real path of the symbolic link  - ‘realpath ~/hosts-link`
3. Printed a two-level tree of ‘etc’  - ‘tree -L 2 /etc’
4. Explained in my own words the difference between a hard link and a symbolic link.

## Hard Link vs Symbolic Link
A hard link points directly to the same file data as the original file, while a symbolic link points to the path of another file or directory.
