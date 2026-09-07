olamide@Sammy:~$ cd ~/OlamideSammy-linux-command-mastery-challenge
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-04-filesystem-search     day-09-integrity-firewall         day-14-dnf-yum
README.md               day-05-links-checkpoint      day-10-security-audit-checkpoint  day-15-provisioning-checkpoint
day-01-file-navigation  day-06-permissions           day-11-user-management
day-02-file-operations  day-07-ownership             day-12-groups
day-03-file-inspection  day-08-privilege-escalation  day-13-apt-package-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ mkdir day-16-environment-variables/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ ls
LICENSE                 day-04-filesystem-search     day-09-integrity-firewall         day-14-dnf-yum
README.md               day-05-links-checkpoint      day-10-security-audit-checkpoint  day-15-provisioning-checkpoint
day-01-file-navigation  day-06-permissions           day-11-user-management            day-16-environment-variables
day-02-file-operations  day-07-ownership             day-12-groups
day-03-file-inspection  day-08-privilege-escalation  day-13-apt-package-management
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-16-environment-variables/
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ touch README.md drill.md evid
ence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ less README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ printenv
SHELL=/bin/bash
WSL2_GUI_APPS_ENABLED=1
WSL_DISTRO_NAME=Ubuntu
NAME=Sammy
PWD=/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables
LOGNAME=olamide
HOME=/home/olamide
LANG=C.UTF-8
WSL_INTEROP=/run/WSL/349_interop
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.dz=01;31:*.gz=01;31:*.lrz=01;31:*.lz=01;31:*.lzo=01;31:*.xz=01;31:*.zst=01;31:*.tzst=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.alz=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.cab=01;31:*.wim=01;31:*.swm=01;31:*.dwm=01;31:*.esd=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.swp=00;90:*.tmp=00;90:*.dpkg-dist=00;90:*.dpkg-old=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:
WAYLAND_DISPLAY=wayland-0
LESSCLOSE=/usr/bin/lesspipe %s %s
TERM=xterm-256color
LESSOPEN=| /usr/bin/lesspipe %s
USER=olamide
DISPLAY=:0
SHLVL=1
XDG_RUNTIME_DIR=/run/user/1000/
WSLENV=
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
HOSTTYPE=x86_64
PULSE_SERVER=unix:/mnt/wslg/PulseServer
OLDPWD=/home/olamide/OlamideSammy-linux-command-mastery-challenge
_=/usr/bin/printenv
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ printenv HOME
/home/olamide
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $VAR

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ export
declare -x DBUS_SESSION_BUS_ADDRESS="unix:path=/run/user/1000/bus"
declare -x DISPLAY=":0"
declare -x HOME="/home/olamide"
declare -x HOSTTYPE="x86_64"
declare -x LANG="C.UTF-8"
declare -x LESSCLOSE="/usr/bin/lesspipe %s %s"
declare -x LESSOPEN="| /usr/bin/lesspipe %s"
declare -x LOGNAME="olamide"
declare -x LS_COLORS="rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.dz=01;31:*.gz=01;31:*.lrz=01;31:*.lz=01;31:*.lzo=01;31:*.xz=01;31:*.zst=01;31:*.tzst=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.alz=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.cab=01;31:*.wim=01;31:*.swm=01;31:*.dwm=01;31:*.esd=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.swp=00;90:*.tmp=00;90:*.dpkg-dist=00;90:*.dpkg-old=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:"
declare -x NAME="Sammy"
declare -x OLDPWD="/home/olamide/OlamideSammy-linux-command-mastery-challenge"
declare -x PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin"
declare -x PULSE_SERVER="unix:/mnt/wslg/PulseServer"
declare -x PWD="/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables"
declare -x SHELL="/bin/bash"
declare -x SHLVL="1"
declare -x TERM="xterm-256color"
declare -x USER="olamide"
declare -x WAYLAND_DISPLAY="wayland-0"
declare -x WSL2_GUI_APPS_ENABLED="1"
declare -x WSLENV=""
declare -x WSL_DISTRO_NAME="Ubuntu"
declare -x WSL_INTEROP="/run/WSL/349_interop"
declare -x XDG_DATA_DIRS="/usr/local/share:/usr/share:/var/lib/snapd/desktop"
declare -x XDG_RUNTIME_DIR="/run/user/1000/"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ unset
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ env
SHELL=/bin/bash
WSL2_GUI_APPS_ENABLED=1
WSL_DISTRO_NAME=Ubuntu
NAME=Sammy
PWD=/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables
LOGNAME=olamide
HOME=/home/olamide
LANG=C.UTF-8
WSL_INTEROP=/run/WSL/349_interop
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.dz=01;31:*.gz=01;31:*.lrz=01;31:*.lz=01;31:*.lzo=01;31:*.xz=01;31:*.zst=01;31:*.tzst=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.alz=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.cab=01;31:*.wim=01;31:*.swm=01;31:*.dwm=01;31:*.esd=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.swp=00;90:*.tmp=00;90:*.dpkg-dist=00;90:*.dpkg-old=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:
WAYLAND_DISPLAY=wayland-0
LESSCLOSE=/usr/bin/lesspipe %s %s
TERM=xterm-256color
LESSOPEN=| /usr/bin/lesspipe %s
USER=olamide
DISPLAY=:0
SHLVL=1
XDG_RUNTIME_DIR=/run/user/1000/
WSLENV=
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
HOSTTYPE=x86_64
PULSE_SERVER=unix:/mnt/wslg/PulseServer
OLDPWD=/home/olamide/OlamideSammy-linux-command-mastery-challenge
_=/usr/bin/env
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ source
-bash: source: filename argument required
source: usage: source [-p path] filename [arguments]
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ export PATH=$PATH:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ cat /etc/environment
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ export DAY16_VAR="LinuxEnvironment"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $DAY16_VAR
LinuxEnvironment
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ export | grep DAY16_VAR
declare -x DAY16_VAR="LinuxEnvironment"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ unset DAY16_VAR
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $DAY16_VAR

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ mkdir -p ~/day16-path-practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ nano ~/day16-path-practice/day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ chmod +x ~/day16-path-practice/day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ ~/day16-path-practice/day16-script
Day 16 PATH practice successful
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ ~/day16-path-practice/day16-script
Day 16 PATH practice successful
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ which day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ source /dev/null
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ cat /etc/environment
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $DAY16_VAR

olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH | tr ':' '\n' | grep day16-path-practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ which day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ day16-script
day16-script: command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ ls -l ~/day16-path-practice/
total 4
-rwxr-xr-x 1 olamide olamide 51 Sep  7 23:44 day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ ls -l ~/day16-path-practice/
total 4
-rwxr-xr-x 1 olamide olamide 51 Sep  7 23:44 day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.6.3.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files/Amazon/AWSCLIV2/:/mnt/c/terraform:/mnt/c/Users/olami/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/olami/AppData/Local/Programs/Microsoft VS Code/bin:/mnt/c/Users/olami/AppData/Local/Programs/DockerDesktop/resources/bin:/snap/bin:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH | tr ':' '\n' | grep day16-path-practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH | tr ':' '\n' | grep day16-path-practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ export PATH="$PATH:$HOME/day16-path-practice"
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ echo $PATH | tr ':' '\n' | grep day16-path-practice
/home/olamide/day16-path-practice
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ which day16-script
/home/olamide/day16-path-practice/day16-script
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$ day16-script
Day 16 PATH practice successful
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-16-environment-variables$
