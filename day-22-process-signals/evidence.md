olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[2] 959
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]-   907 Running                    sleep 300 &
[2]+   959 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 907
[1]-  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[2]+   959 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill -9 959
[2]+  Killed                     sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[1] 1044
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1044 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill -HUP 1044
[1]+  Hangup                     sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
sleep 300 &
[1] 1081
[2] 1087
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]-  1081 Running                    sleep 300 &
[2]+  1087 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ killall sleep
[1]-  Terminated                 sleep 300
[2]+  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[1] 1125
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1125 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pkill sleep
[1]+  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[1] 1164
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
[1]+  Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ fg
sleep 300
jobs
^C
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300
^Z
[1]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ bg
[1]+ sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1202 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1202
[1]+  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1202
-bash: kill: (1202) - No such process
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300
^Z
[1]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ nohup sleep 300 &
[2] 1305
nohup: ignoring input and appending output to 'nohup.out'
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
[2]-  1305 Running                    nohup sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1305
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ disown %2
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1305
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300
^Z
[2]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
[1]-  Stopped                    sleep 300
[2]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ bg %2
[2]+ sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
[1]+  Stopped                    sleep 300
[2]-  Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ fg %2
sleep 300
^Z
[2]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
[1]-  Stopped                    sleep 300
[2]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1614
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1604
-bash: kill: (1604) - No such process
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill 1614
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs
[1]-  Stopped                    sleep 300
[2]+  Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1614
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]-  1258 Stopped                    sleep 300
[2]+  1614 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill -9 1614
[2]+  Killed                     sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[2] 1759
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1759
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill -HUP 1759
[2]-  Hangup                     sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
sleep 300 &
[2] 1807
[3] 1813
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
1807
1813
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pkill sleep
[2]   Terminated                 sleep 300
[3]-  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ killall sleep
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1258
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1258 Stopped                    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ kill %1

[1]+  Stopped                    sleep 300
[1]+  Terminated                 sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ nohup sleep 300 > nohup-test.log 2>&1 &
[1] 1919
-bash: nohup-test.log: No such file or directory
[1]+  Exit 1                     nohup sleep 300 > nohup-test.log 2>&1
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pwd
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ ls -la
total 8
drwxr-xr-x  0 olamide olamide    0 Sep 27 23:59 .
drwxr-xr-x 25 olamide olamide 4096 Sep 27 23:59 ..
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ nohup sleep 300 > /home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals/nohup-test.log 2>&1 &
[1] 1948
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1948
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ ls -l nohup-test.log
ls: cannot access 'nohup-test.log': No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ ls -l /home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals/nohup-test.log
-rw-r--r-- 1 olamide olamide 0 Sep 28 00:15 /home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals/nohup-test.log
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ ps -p 1948 -o pid,ppid,stat,cmd
    PID    PPID STAT CMD
   1948     347 S    sleep 300
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ sleep 300 &
[2] 1998
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]-  1948 Running                    nohup sleep 300 > /home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals/nohup-test.log 2>&1 &
[2]+  1998 Running                    sleep 300 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ disown %2
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ jobs -l
[1]+  1948 Running                    nohup sleep 300 > /home/olamide/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals/nohup-test.log 2>&1 &
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-22-process-signals$ pgrep sleep
1948
1998
