olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-04-filesystem-search     day-09-integrity-firewall         day-14-dnf-yum
README.md               day-05-links-checkpoint      day-10-security-audit-checkpoint  day-15-provisioning-checkpoint
day-01-file-navigation  day-06-permissions           day-11-user-management            day-16-environment-variables
day-02-file-operations  day-07-ownership             day-12-groups
day-03-file-inspection  day-08-privilege-escalation  day-13-apt-package-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-17-shell-configuration/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-04-filesystem-search     day-09-integrity-firewall         day-14-dnf-yum
README.md               day-05-links-checkpoint      day-10-security-audit-checkpoint  day-15-provisioning-checkpoint
day-01-file-navigation  day-06-permissions           day-11-user-management            day-16-environment-variables
day-02-file-operations  day-07-ownership             day-12-groups                     day-17-shell-configuration
day-03-file-inspection  day-08-privilege-escalation  day-13-apt-package-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-17-shell-configuration/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ touch README.md drill.md eviden
ce.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano ~/.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ source ~/.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ echo $DAY17_VAR
LinuxConfiguration
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ day17
Day 17 configuration is working
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ cat ~/.bash_profile
cat: /home/olamide/.bash_profile: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ sudo nano /etc/environment
[sudo: authenticate] Password:
sudo: Authentication failed, try again.
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ sudo nano /etc/bash.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ alias
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'
alias day17='echo "Day 17 configuration is working"'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias grep='grep --color=auto'
alias l='ls -CF'
alias la='ls -A'
alias ll='ls -alF'
alias ls='ls --color=auto'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ alias day17
alias day17='echo "Day 17 configuration is working"'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ unalias day17
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ alias day17
-bash: alias: day17: not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ source ~/.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ type day17
day17 is aliased to `echo "Day 17 configuration is working"'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ type cd
cd is a shell builtin
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ type cd
cd is a shell builtin
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ whereis bash
bash: /usr/bin/bash /usr/share/man/man1/bash.1.gz
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ nano ~/.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ source ~/.bashrc
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ echo $DAY17_VAR
LinuxConfiguration
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ day17
Day 17 configuration is working
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ alias day17
alias day17='echo "Day 17 configuration is working"'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ type day17
day17 is aliased to `echo "Day 17 configuration is working"'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ echo $DAY17_VAR
LinuxConfiguration
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ day17
Day 17 configuration is working
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-17-shell-configuration$ alias day17
which bash
whereis bash
alias day17='echo "Day 17 configuration is working"'
/usr/bin/bash
bash: /usr/bin/bash /usr/share/man/man1/bash.1.gz
