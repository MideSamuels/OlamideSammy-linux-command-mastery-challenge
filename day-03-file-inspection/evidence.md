olamide@Sammy:/var/log$  cd ~
olamide@Sammy:~$ mkdir day-03
olamide@Sammy:~$ cd day-03
olamide@Sammy:~/day-03$ touch practice.md
olamide@Sammy:~/day-03$ nano practice.md
olamide@Sammy:~/day-03$ cat practice.md
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
olamide@Sammy:~/day-03$ less practice.md
olamide@Sammy:~/day-03$ head practice.md
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
olamide@Sammy:~/day-03$ head -n 15 practice.md
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
olamide@Sammy:~/day-03$ tail practice.md
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
olamide@Sammy:~/day-03$ tail -f practice.md
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
I love Ubuntu
^C
olamide@Sammy:~/day-03$ wc practice.md
 30  90 420 practice.md
olamide@Sammy:~/day-03$ wc -l practice.md
30 practice.md
olamide@Sammy:~/day-03$ file practice.md
practice.md: ASCII text
olamide@Sammy:~/day-03$ stat practice.md
  File: practice.md
  size: 420             Blocks: 8          IO Block: 4096   regular file
Device: 8,48    Inode: 36254       Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/ olamide)   Gid: ( 1000/ olamide)
Access: 2026-08-22 19:26:42.484868969 +0100
Modify: 2026-08-22 19:26:15.640867561 +0100
Change: 2026-08-22 19:26:15.640867561 +0100
 Birth: 2026-08-22 19:21:39.152870015 +0100
