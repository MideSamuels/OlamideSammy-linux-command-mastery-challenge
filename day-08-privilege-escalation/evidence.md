olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE    day-01-file-navigation  day-03-file-inspection    day-05-links-checkpoint  day-07-ownership
README.md  day-02-file-operations  day-04-filesystem-search  day-06-permissions
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-08-privilege-escalation/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE    day-01-file-navigation  day-03-file-inspection    day-05-links-checkpoint  day-07-ownership
README.md  day-02-file-operations  day-04-filesystem-search  day-06-permissions       day-08-privilege-escalation
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-08-privilege-escalation/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ touch README.md drill.md evide
nce.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ less drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo ls /root
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo -i
Welcome to Ubuntu 26.04 LTS (GNU/Linux 6.6.87.2-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://docs.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu Aug 27 20:09:13 WAT 2026

  System load:  0.0                 Processes:             41
  Usage of /:   0.2% of 1006.85GB   Users logged in:       0
  Memory usage: 5%                  IPv4 address for eth0: 172.26.17.127
  Swap usage:   0%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

This message is shown once a day. To disable it please create the
/root/.hushlogin file.
root@Sammy:~# whoami
root
root@Sammy:~# exit
logout
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo -u root whoami
root
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ ls /root
ls: cannot open directory '/root': Permission denied
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo !!
sudo ls /root
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo -l
User olamide may run the following commands on Sammy:
    (ALL : ALL) ALL
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo visudo
visudo: /tmp/sudoers-oGIzTs/sudoers unchanged
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ su -s /bin/bash olamide
Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ whoami
olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ exit
exit
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ su - olamide
Password:
olamide@Sammy:~$ whoami
olamide
olamide@Sammy:~$ exit
logout
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ whoami
olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ id
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ ls /root
ls: cannot open directory '/root': Permission denied
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo !!
sudo ls /root
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ sudo -l
User olamide may run the following commands on Sammy:
    (ALL : ALL) ALL
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ whoami
olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$ id
uid=1000(olamide) gid=1000(olamide) groups=1000(olamide),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users)
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-08-privilege-escalation$


