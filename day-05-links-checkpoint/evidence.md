olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge$ cd day-05-links-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ touch README.md drill.md evidence.md commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ls
README.md  commands.md  drill.md  evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ nano commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ less commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ nano README.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ nano drill.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ tree .
Command 'tree' not found, but can be installed with:
sudo snap install tree  # version 2.1.3+pkg-5852, or
sudo apt  install tree  # version 2.3.1-1
See 'snap info tree' for additional versions.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ sudo snap install tree  # version 2.1.3+pkg-5852
[sudo: authenticate] Password:
Download snap "snapd" (27710) from channel "stable"                                                                29%  243kB/s 2m34s
2026-08-24T22:21:38+01:00 INFO Waiting for automatic snapd restart...
2026-08-24T22:21:39+01:00 INFO Waiting for automatic snapd restart...
2026-08-24T22:21:40+01:00 INFO Waiting for automatic snapd restart...
tree 2.1.3+pkg-5852 from 林博仁 Buo-ren Lin (brlin) installed
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ tree .
.
├── README.md
├── commands.md
├── drill.md
└── evidence.md

1 directory, 4 files
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ tree -L 2 .
.
├── README.md
├── commands.md
├── drill.md
└── evidence.md

1 directory, 4 files
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ln commands.md hardlink.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ^C
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ln -s /etc/hosts hosts-link
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ readlink hosts-link
/etc/hosts
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ls -l hosts-link
lrwxrwxrwx 1 olamide olamide 10 Aug 24 22:30 hosts-link -> /etc/hosts
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ readlink day-05-links-checkpoint/hosts-link
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ readlink hosts-link
/etc/hosts
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ realpath day-05-links-checkpoint/hosts-link
realpath: day-05-links-checkpoint/hosts-link: No such file or directory
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ realpath hosts-link
/etc/hosts
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ basename "$PWD/commands.md"
commands.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ dirname "$PWD/commands.md"
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ pushd /etc
/etc ~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint
olamide@Sammy:/etc$ popd
~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ls -lt
total 16
lrwxrwxrwx 1 olamide olamide  10 Aug 24 22:30 hosts-link -> /etc/hosts
-rw-r--r-- 1 olamide olamide 728 Aug 24 22:15 drill.md
-rw-r--r-- 1 olamide olamide 878 Aug 24 22:05 README.md
-rw-r--r-- 2 olamide olamide 853 Aug 24 21:51 hardlink.md
-rw-r--r-- 2 olamide olamide 853 Aug 24 21:51 commands.md
-rw-r--r-- 1 olamide olamide   0 Aug 24 21:43 evidence.md
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ln -s /etc/hosts hosts-link
ln: Already exists
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ realpath hosts-link
/etc/hosts
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ tree -L 2 /etc
/etc
├── PackageKit
│   ├── PackageKit.conf
│   └── Vendor.conf
├── X11
│   ├── Xreset
│   ├── Xreset.d
│   ├── Xresources
│   ├── Xsession
│   ├── Xsession.d
│   ├── Xsession.options
│   ├── rgb.txt
│   ├── xkb
│   └── xorg.conf.d
├── adduser.conf
├── alternatives
│   ├── README
│   ├── awk -> /usr/bin/gawk
│   ├── awk.1.gz -> /usr/share/man/man1/gawk.1.gz
│   ├── builtins.7.gz -> /usr/share/man/man7/bash-builtins.7.gz
│   ├── editor -> /bin/nano
│   ├── editor.1.gz -> /usr/share/man/man1/nano.1.gz
│   ├── ex -> /usr/bin/vim.basic
│   ├── ex.1.gz -> /usr/share/man/man1/vim.1.gz
│   ├── ex.da.1.gz -> /usr/share/man/da/man1/vim.1.gz
│   ├── ex.de.1.gz -> /usr/share/man/de/man1/vim.1.gz
│   ├── ex.fr.1.gz -> /usr/share/man/fr/man1/vim.1.gz
│   ├── ex.it.1.gz -> /usr/share/man/it/man1/vim.1.gz
│   ├── ex.ja.1.gz -> /usr/share/man/ja/man1/vim.1.gz
│   ├── ex.pl.1.gz -> /usr/share/man/pl/man1/vim.1.gz
│   ├── ex.ru.1.gz -> /usr/share/man/ru/man1/vim.1.gz
│   ├── ex.tr.1.gz -> /usr/share/man/tr/man1/vim.1.gz
│   ├── infobrowser -> /usr/bin/info
│   ├── infobrowser.1.gz -> /usr/share/man/man1/info.1.gz
│   ├── jsondiff -> /usr/bin/json-patch-jsondiff
│   ├── locate -> /usr/bin/plocate
│   ├── locate.1.gz -> /usr/share/man/man1/plocate.1.gz
│   ├── lzcat -> /usr/bin/xzcat
│   ├── lzcat.1.gz -> /usr/share/man/man1/xzcat.1.gz
│   ├── lzcmp -> /usr/bin/xzcmp
│   ├── lzcmp.1.gz -> /usr/share/man/man1/xzcmp.1.gz
│   ├── lzdiff -> /usr/bin/xzdiff
│   ├── lzdiff.1.gz -> /usr/share/man/man1/xzdiff.1.gz
│   ├── lzegrep -> /usr/bin/xzegrep
│   ├── lzegrep.1.gz -> /usr/share/man/man1/xzegrep.1.gz
│   ├── lzfgrep -> /usr/bin/xzfgrep
│   ├── lzfgrep.1.gz -> /usr/share/man/man1/xzfgrep.1.gz
│   ├── lzgrep -> /usr/bin/xzgrep
│   ├── lzgrep.1.gz -> /usr/share/man/man1/xzgrep.1.gz
│   ├── lzless -> /usr/bin/xzless
│   ├── lzless.1.gz -> /usr/share/man/man1/xzless.1.gz
│   ├── lzma -> /usr/bin/xz
│   ├── lzma.1.gz -> /usr/share/man/man1/xz.1.gz
│   ├── lzmore -> /usr/bin/xzmore
│   ├── lzmore.1.gz -> /usr/share/man/man1/xzmore.1.gz
│   ├── nawk -> /usr/bin/gawk
│   ├── nawk.1.gz -> /usr/share/man/man1/gawk.1.gz
│   ├── nc -> /bin/nc.openbsd
│   ├── nc.1.gz -> /usr/share/man/man1/nc_openbsd.1.gz
│   ├── netcat -> /bin/nc.openbsd
│   ├── netcat.1.gz -> /usr/share/man/man1/nc_openbsd.1.gz
│   ├── newt-palette -> /etc/newt/palette.ubuntu
│   ├── pager -> /usr/bin/less
│   ├── pager.1.gz -> /usr/share/man/man1/less.1.gz
│   ├── pico -> /bin/nano
│   ├── pico.1.gz -> /usr/share/man/man1/nano.1.gz
│   ├── pinentry -> /usr/bin/pinentry-curses
│   ├── pinentry.1.gz -> /usr/share/man/man1/pinentry-curses.1.gz
│   ├── pybabel -> /usr/bin/pybabel-python3
│   ├── rmt -> /usr/sbin/rmt-tar
│   ├── rmt.8.gz -> /usr/share/man/man8/rmt-tar.8.gz
│   ├── rview -> /usr/bin/vim.basic
│   ├── rvim -> /usr/bin/vim.basic
│   ├── sudo -> /usr/lib/cargo/bin/sudo
│   ├── sudo.8.gz -> /usr/share/man/man8/sudo-rs.8.gz
│   ├── sudoedit -> /usr/lib/cargo/bin/sudo
│   ├── sudoedit.8.gz -> /usr/share/man/man8/sudo-rs.8.gz
│   ├── sudoers.5.gz -> /usr/share/man/man5/sudoers-rs.5.gz
│   ├── unlzma -> /usr/bin/unxz
│   ├── unlzma.1.gz -> /usr/share/man/man1/unxz.1.gz
│   ├── updatedb -> /usr/sbin/updatedb.plocate
│   ├── updatedb.8.gz -> /usr/share/man/man8/updatedb.plocate.8.gz
│   ├── vi -> /usr/bin/vim.basic
│   ├── vi.1.gz -> /usr/share/man/man1/vim.1.gz
│   ├── vi.da.1.gz -> /usr/share/man/da/man1/vim.1.gz
│   ├── vi.de.1.gz -> /usr/share/man/de/man1/vim.1.gz
│   ├── vi.fr.1.gz -> /usr/share/man/fr/man1/vim.1.gz
│   ├── vi.it.1.gz -> /usr/share/man/it/man1/vim.1.gz
│   ├── vi.ja.1.gz -> /usr/share/man/ja/man1/vim.1.gz
│   ├── vi.pl.1.gz -> /usr/share/man/pl/man1/vim.1.gz
│   ├── vi.ru.1.gz -> /usr/share/man/ru/man1/vim.1.gz
│   ├── vi.tr.1.gz -> /usr/share/man/tr/man1/vim.1.gz
│   ├── view -> /usr/bin/vim.basic
│   ├── view.1.gz -> /usr/share/man/man1/vim.1.gz
│   ├── view.da.1.gz -> /usr/share/man/da/man1/vim.1.gz
│   ├── view.de.1.gz -> /usr/share/man/de/man1/vim.1.gz
│   ├── view.fr.1.gz -> /usr/share/man/fr/man1/vim.1.gz
│   ├── view.it.1.gz -> /usr/share/man/it/man1/vim.1.gz
│   ├── view.ja.1.gz -> /usr/share/man/ja/man1/vim.1.gz
│   ├── view.pl.1.gz -> /usr/share/man/pl/man1/vim.1.gz
│   ├── view.ru.1.gz -> /usr/share/man/ru/man1/vim.1.gz
│   ├── view.tr.1.gz -> /usr/share/man/tr/man1/vim.1.gz
│   ├── vim -> /usr/bin/vim.basic
│   ├── vimdiff -> /usr/bin/vim.basic
│   ├── visudo -> /usr/lib/cargo/bin/visudo
│   ├── visudo.8.gz -> /usr/share/man/man8/visudo-rs.8.gz
│   ├── vtrgb -> /etc/console-setup/vtrgb
│   ├── which -> /usr/bin/which.debianutils
│   ├── which.1.gz -> /usr/share/man/man1/which.debianutils.1.gz
│   ├── which.de1.gz -> /usr/share/man/de/man1/which.debianutils.1.gz
│   ├── which.es1.gz -> /usr/share/man/es/man1/which.debianutils.1.gz
│   ├── which.fr1.gz -> /usr/share/man/fr/man1/which.debianutils.1.gz
│   ├── which.it1.gz -> /usr/share/man/it/man1/which.debianutils.1.gz
│   ├── which.ja1.gz -> /usr/share/man/ja/man1/which.debianutils.1.gz
│   ├── which.pl1.gz -> /usr/share/man/pl/man1/which.debianutils.1.gz
│   ├── which.sl1.gz -> /usr/share/man/sl/man1/which.debianutils.1.gz
│   └── x-cursor-theme -> /usr/share/icons/Adwaita/cursor.theme
├── apparmor
│   ├── init
│   └── parser.conf
├── apparmor.d
│   ├── abi
│   ├── abstractions
│   ├── disable
│   ├── force-complain
│   ├── local
│   ├── lsb_release
│   ├── nvidia_modprobe
│   ├── sbin.dhclient
│   └── tunables
├── apport
│   ├── crashdb.conf
│   └── report-ignore
├── apt
│   ├── apt.conf.d
│   ├── auth.conf.d
│   ├── keyrings
│   ├── preferences.d
│   ├── sources.list
│   ├── sources.list.d
│   └── trusted.gpg.d
├── bash.bashrc
├── bash_completion
├── bash_completion.d
│   ├── 000_bash_completion_compat.bash
│   └── git-prompt
├── bindresvport.blacklist
├── binfmt.d
├── byobu
│   ├── backend
│   └── socketdir
├── ca-certificates
│   └── update.d
├── ca-certificates.conf
├── ca-certificates.conf.dpkg-old
├── chrony
│   ├── chrony.conf
│   ├── chrony.keys
│   ├── conf.d
│   ├── nts-bootstrap-staging-ubuntu.crt
│   ├── nts-bootstrap-ubuntu.crt
│   └── sources.d
├── cloud
│   ├── clean.d
│   ├── cloud-init.disabled
│   ├── cloud.cfg
│   ├── cloud.cfg.d
│   └── templates
├── console-setup
│   ├── ISO-8859-1.acm
│   ├── Uni2-Fixed16.psf.gz
│   ├── cached_ISO-8859-1.acm.gz
│   ├── cached_ISO-8859-1_del.kmap.gz
│   ├── cached_UTF-8_del.kmap.gz
│   ├── cached_Uni2-Fixed16.psf.gz
│   ├── cached_setup_font.sh
│   ├── cached_setup_keyboard.sh
│   ├── cached_setup_terminal.sh
│   ├── compose.ARMSCII-8.inc
│   ├── compose.CP1251.inc
│   ├── compose.CP1255.inc
│   ├── compose.CP1256.inc
│   ├── compose.GEORGIAN-ACADEMY.inc
│   ├── compose.GEORGIAN-PS.inc
│   ├── compose.IBM1133.inc
│   ├── compose.ISIRI-3342.inc
│   ├── compose.ISO-8859-1.inc
│   ├── compose.ISO-8859-10.inc
│   ├── compose.ISO-8859-11.inc
│   ├── compose.ISO-8859-13.inc
│   ├── compose.ISO-8859-14.inc
│   ├── compose.ISO-8859-15.inc
│   ├── compose.ISO-8859-16.inc
│   ├── compose.ISO-8859-2.inc
│   ├── compose.ISO-8859-3.inc
│   ├── compose.ISO-8859-4.inc
│   ├── compose.ISO-8859-5.inc
│   ├── compose.ISO-8859-6.inc
│   ├── compose.ISO-8859-7.inc
│   ├── compose.ISO-8859-8.inc
│   ├── compose.ISO-8859-9.inc
│   ├── compose.KOI8-R.inc
│   ├── compose.KOI8-U.inc
│   ├── compose.TIS-620.inc
│   ├── compose.VISCII.inc
│   ├── remap.inc
│   ├── vtrgb
│   └── vtrgb.vga
├── credstore  [error opening dir]
├── credstore.encrypted  [error opening dir]
├── cron.d
│   └── e2scrub_all
├── cron.daily
│   ├── apport
│   ├── apt-compat
│   ├── dpkg
│   ├── logrotate
│   ├── man-db
│   └── plocate
├── cron.hourly
├── cron.monthly
├── cron.weekly
│   └── man-db
├── cron.yearly
├── crontab
├── dbus-1
│   ├── session.d
│   └── system.d
├── dconf
│   └── db
├── debconf.conf
├── debian_version
├── default
│   ├── apport
│   ├── chrony
│   ├── console-setup
│   ├── cron
│   ├── dbus
│   ├── keyboard
│   ├── locale -> ../locale.conf
│   ├── motd-news
│   ├── networkd-dispatcher
│   ├── rsync
│   └── useradd
├── deluser.conf
├── depmod.d
│   └── ubuntu.conf
├── dhcp
│   └── dhclient-exit-hooks.d
├── dhcpcd.conf
├── dpkg
│   ├── dpkg.cfg
│   ├── dpkg.cfg.d
│   └── origins
├── e2scrub.conf
├── environment
├── environment.d
│   └── 90qt-a11y.conf
├── ethertypes
├── fonts
│   ├── conf.avail
│   ├── conf.d
│   └── fonts.conf
├── fstab
├── fuse.conf
├── gai.conf
├── glvnd
│   └── egl_vendor.d
├── gnutls
│   └── config
├── gprofng.rc
├── groff
│   ├── man.local
│   └── mdoc.local
├── group
├── group-
├── gshadow
├── gshadow-
├── gss
│   └── mech.d
├── gtk-3.0
│   ├── im-multipress.conf
│   └── settings.ini
├── host.conf
├── hostname
├── hosts
├── init.d
│   ├── apparmor
│   ├── apport
│   ├── chrony
│   ├── console-setup.sh
│   ├── cron
│   ├── dbus
│   ├── keyboard-setup.sh
│   ├── procps
│   ├── rsync
│   ├── screen-cleanup
│   ├── unattended-upgrades
│   └── x11-common
├── inputrc
├── issue
├── issue.net
├── kernel
│   ├── install.d
│   └── postinst.d
├── landscape
│   └── client.conf
├── ld.so.cache
├── ld.so.conf
├── ld.so.conf.d
│   ├── ld.wsl.conf
│   ├── libc.conf
│   └── x86_64-linux-gnu.conf
├── ldap
│   └── ldap.conf
├── legal
├── libaudit.conf
├── locale.conf
├── locale.gen
├── localtime -> /usr/share/zoneinfo/Africa/Lagos
├── logcheck
│   └── ignore.d.server
├── login.defs
├── logrotate.conf
├── logrotate.d
│   ├── alternatives
│   ├── apport
│   ├── apt
│   ├── btmp
│   ├── chrony
│   ├── cloud-init-base
│   ├── dpkg
│   ├── landscape-client
│   ├── rsyslog
│   ├── ubuntu-pro-client
│   ├── unattended-upgrades
│   └── wtmp
├── lsb-release
├── machine-id
├── magic
├── magic.mime
├── manpath.config
├── mime.types
├── mke2fs.conf
├── modprobe.d
│   ├── blacklist-ath_pci.conf
│   ├── blacklist-firewire.conf
│   ├── blacklist-framebuffer.conf
│   ├── blacklist-rare-network.conf
│   ├── blacklist.conf
│   └── iwlwifi.conf
├── modules
├── modules-load.d
│   └── modules.conf -> ../modules
├── mtab -> ../proc/self/mounts
├── nanorc
├── netconfig
├── netplan
├── network
│   ├── if-post-down.d
│   ├── if-pre-up.d
│   └── if-up.d
├── networkd-dispatcher
│   ├── carrier.d
│   ├── degraded.d
│   ├── dormant.d
│   ├── no-carrier.d
│   ├── off.d
│   └── routable.d
├── networks
├── newt
│   ├── palette -> /etc/alternatives/newt-palette
│   ├── palette.original
│   └── palette.ubuntu
├── nsswitch.conf
├── opt
├── os-release -> ../usr/lib/os-release
├── pam.conf
├── pam.d
│   ├── chfn
│   ├── chpasswd
│   ├── chsh
│   ├── common-account
│   ├── common-auth
│   ├── common-password
│   ├── common-session
│   ├── common-session-noninteractive
│   ├── cron
│   ├── login
│   ├── newusers
│   ├── other
│   ├── passwd
│   ├── remote
│   ├── runuser
│   ├── runuser-l
│   ├── su
│   ├── su-l
│   ├── sudo
│   └── sudo-i
├── passwd
├── passwd-
├── perl
│   └── Net
├── pm
│   └── sleep.d
├── polkit-1
│   └── rules.d
├── ppp
│   ├── ip-down.d
│   └── ip-up.d
├── profile
├── profile.d
│   ├── 01-locale-fix.sh
│   ├── 70-systemd-shell-extra.sh -> /usr/lib/systemd/profile.d/70-systemd-shell-extra.sh
│   ├── 80-systemd-osc-context.sh -> /usr/lib/systemd/profile.d/80-systemd-osc-context.sh
│   ├── Z97-byobu.sh
│   ├── Z99-cloud-locale-test.sh
│   ├── Z99-cloudinit-warnings.sh
│   ├── apps-bin-path.sh
│   ├── bash_completion.sh
│   ├── gawk.csh
│   ├── gawk.sh
│   └── update-motd.sh
├── protocols
├── python3
│   └── debian_config
├── python3.14
│   └── sitecustomize.py
├── rc0.d
│   ├── K01chrony -> ../init.d/chrony
│   └── K01unattended-upgrades -> ../init.d/unattended-upgrades
├── rc1.d
│   └── K01chrony -> ../init.d/chrony
├── rc2.d
│   ├── S01apport -> ../init.d/apport
│   ├── S01chrony -> ../init.d/chrony
│   ├── S01console-setup.sh -> ../init.d/console-setup.sh
│   ├── S01cron -> ../init.d/cron
│   ├── S01dbus -> ../init.d/dbus
│   ├── S01rsync -> ../init.d/rsync
│   └── S01unattended-upgrades -> ../init.d/unattended-upgrades
├── rc3.d
│   ├── S01apport -> ../init.d/apport
│   ├── S01chrony -> ../init.d/chrony
│   ├── S01console-setup.sh -> ../init.d/console-setup.sh
│   ├── S01cron -> ../init.d/cron
│   ├── S01dbus -> ../init.d/dbus
│   ├── S01rsync -> ../init.d/rsync
│   └── S01unattended-upgrades -> ../init.d/unattended-upgrades
├── rc4.d
│   ├── S01apport -> ../init.d/apport
│   ├── S01chrony -> ../init.d/chrony
│   ├── S01console-setup.sh -> ../init.d/console-setup.sh
│   ├── S01cron -> ../init.d/cron
│   ├── S01dbus -> ../init.d/dbus
│   ├── S01rsync -> ../init.d/rsync
│   └── S01unattended-upgrades -> ../init.d/unattended-upgrades
├── rc5.d
│   ├── S01apport -> ../init.d/apport
│   ├── S01chrony -> ../init.d/chrony
│   ├── S01console-setup.sh -> ../init.d/console-setup.sh
│   ├── S01cron -> ../init.d/cron
│   ├── S01dbus -> ../init.d/dbus
│   ├── S01rsync -> ../init.d/rsync
│   └── S01unattended-upgrades -> ../init.d/unattended-upgrades
├── rc6.d
│   ├── K01chrony -> ../init.d/chrony
│   └── K01unattended-upgrades -> ../init.d/unattended-upgrades
├── rcS.d
│   ├── S01apparmor -> ../init.d/apparmor
│   ├── S01keyboard-setup.sh -> ../init.d/keyboard-setup.sh
│   ├── S01procps -> ../init.d/procps
│   ├── S01screen-cleanup -> ../init.d/screen-cleanup
│   └── S01x11-common -> ../init.d/x11-common
├── resolv.conf -> /mnt/wsl/resolv.conf
├── rmt -> /usr/sbin/rmt
├── rpc
├── rsyslog.conf
├── rsyslog.d
│   ├── 21-cloudinit.conf
│   └── 50-default.conf
├── screenrc
├── security
│   ├── access.conf
│   ├── capability.conf
│   ├── faillock.conf
│   ├── group.conf
│   ├── limits.conf
│   ├── limits.d
│   ├── namespace.conf
│   ├── namespace.d
│   ├── namespace.init
│   ├── opasswd
│   ├── pam_env.conf
│   ├── pwhistory.conf
│   ├── sepermit.conf
│   └── time.conf
├── selinux
│   └── semanage.conf
├── sensors.d
├── sensors3.conf
├── services
├── sgml
│   ├── catalog -> /var/lib/sgml-base/supercatalog
│   └── xml-core.cat
├── shadow
├── shadow-
├── shells
├── skel
├── ssh
│   ├── ssh_config
│   └── ssh_config.d
├── ssl
│   ├── certs
│   ├── openssl.cnf
│   └── private
├── subgid
├── subgid-
├── subuid
├── subuid-
├── sudo.conf
├── sudo_logsrvd.conf
├── sudoers
├── sudoers.d
│   └── README
├── supercat
│   ├── spcrc-crontab
│   └── spcrc-crontab-light
├── sysctl.d
│   └── README.sysctl
├── systemd
│   ├── journald.conf
│   ├── logind.conf
│   ├── network
│   ├── networkd.conf
│   ├── pstore.conf
│   ├── resolved.conf
│   ├── sleep.conf
│   ├── system
│   ├── system-generators
│   ├── system.conf
│   ├── user
│   └── user.conf
├── terminfo
│   └── README
├── timezone
├── tmpfiles.d
│   └── screen-cleanup.conf
├── ubuntu-advantage
│   └── uaclient.conf
├── ucf.conf
├── udev
│   ├── hwdb.d
│   ├── iocost.conf
│   ├── rules.d
│   └── udev.conf
├── update-manager
│   ├── meta-release
│   ├── release-upgrades
│   └── release-upgrades.d
├── update-motd.d
│   ├── 00-header
│   ├── 10-help-text
│   ├── 50-landscape-sysinfo -> /usr/share/landscape/landscape-sysinfo.wrapper
│   ├── 50-motd-news
│   ├── 91-contract-ua-esm-status
│   ├── 91-release-upgrade
│   ├── 92-unattended-upgrades
│   └── 99-wsl
├── updatedb.conf
├── vconsole.conf -> default/keyboard
├── vim
│   ├── vimrc
│   └── vimrc.tiny
├── vtrgb -> /etc/alternatives/vtrgb
├── vulkan
│   ├── explicit_layer.d
│   ├── icd.d
│   └── implicit_layer.d
├── wgetrc
├── wsl-distribution.conf
├── wsl.conf
├── xattr.conf
├── xdg
│   ├── Xwayland-session.d
│   ├── autostart
│   ├── systemd
│   ├── user-dirs.conf
│   └── user-dirs.defaults
├── xml
│   ├── catalog
│   ├── catalog.old
│   ├── polkitd.xml
│   ├── polkitd.xml.old
│   ├── xml-core.xml
│   └── xml-core.xml.old
└── zsh_command_not_found

158 directories, 439 files
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-05-links-checkpoint$ ls -l hosts-link
lrwxrwxrwx 1 olamide olamide 10 Aug 24 22:30 hosts-link -> /etc/hosts

