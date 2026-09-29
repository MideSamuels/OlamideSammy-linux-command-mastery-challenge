olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl --version
systemd 259 (259.5-0ubuntu3.4)
+PAM +AUDIT +SELINUX +APPARMOR +IMA +IPE +SMACK +SECCOMP +GCRYPT -GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 -IDN +KMOD +LIBCRYPTSETUP +LIBCRYPTSETUP_PLUGINS +LIBFDISK +PCRE2 +PWQUALITY +P11KIT +QRENCODE +TPM2 +BZIP2 +LZ4 +XZ +ZLIB +ZSTD +BPF_FRAMEWORK +BTF -XKBCOMMON -UTMP +SYSVINIT +LIBARCHIVE
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl list-units --type=service
  UNIT                                     LOAD   ACTIVE     SUB          DESCRIPTION
  chrony.service                           loaded active     running      chrony, an NTP client/server
  console-getty.service                    loaded active     running      Console Getty
  console-setup.service                    loaded active     exited       Set console font and keymap
  cron.service                             loaded active     running      Regular background program processing daemon
  dbus.service                             loaded active     running      D-Bus System Message Bus
  getty@tty1.service                       loaded active     running      Getty on tty1
  keyboard-setup.service                   loaded active     exited       Set the console keyboard layout
  kmod-static-nodes.service                loaded active     exited       Create List of Static Device Nodes
  netplan-configure.service                loaded active     exited       Netplan Backend Configuration
  networkd-dispatcher.service              loaded active     running      Dispatcher daemon for systemd-networkd
  rsyslog.service                          loaded active     running      System Logging Service
  setvtrgb.service                         loaded active     exited       Set console scheme
  snapd.seeded.service                     loaded active     exited       Wait until snapd is fully seeded
  snapd.service                            loaded active     running      Snap Daemon
  systemd-binfmt.service                   loaded active     exited       Set Up Additional Binary Formats
  systemd-journal-flush.service            loaded active     exited       Flush Journal to Persistent Storage
  systemd-journald.service                 loaded active     running      Journal Service
  systemd-logind.service                   loaded active     running      User Login Management
  systemd-modules-load.service             loaded active     exited       Load Kernel Modules
  systemd-remount-fs.service               loaded active     exited       Remount Root and Kernel File Systems
  systemd-resolved.service                 loaded active     running      Network Name Resolution
  systemd-sysctl.service                   loaded active     exited       Apply Kernel Variables
  systemd-tmpfiles-setup-dev-early.service loaded active     exited       Create Static Device Nodes in /dev gracefully
  systemd-tmpfiles-setup-dev.service       loaded active     exited       Create Static Device Nodes in /dev
  systemd-tmpfiles-setup.service           loaded active     exited       Create System Files and Directories
  systemd-udev-load-credentials.service    loaded active     exited       Load udev Rules from Credentials
  systemd-udev-trigger.service             loaded active     exited       Coldplug All udev Devices
  systemd-udevd.service                    loaded active     running      Rule-based Manager for Device Events and Files
  systemd-user-sessions.service            loaded active     exited       Permit User Sessions
  ufw.service                              loaded active     exited       Uncomplicated firewall
  unattended-upgrades.service              loaded active     running      Unattended Upgrades Shutdown
lines 1-32
[1]+  Stopped                    systemctl list-units --type=service
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ [200~sudo systemctl start cron~
[200~sudo: command not found
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl start cron
[sudo: authenticate] Password:
sudo: Authentication failed, try again.
[sudo: authenticate] Password:
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl stop cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl restart cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl reload cron
Failed to reload cron.service: Job type reload is not applicable for unit cron.service.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl enable cron
Synchronizing state of cron.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install enable cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl disable cron
Synchronizing state of cron.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install disable cron
Removed '/etc/systemd/system/multi-user.target.wants/cron.service'.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl enable --now cron
Synchronizing state of cron.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install enable cron
Created symlink '/etc/systemd/system/multi-user.target.wants/cron.service' → '/usr/lib/systemd/system/cron.service'.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl status cron --no-pager
● cron.service - Regular background program processing daemon
     Loaded: loaded (/usr/lib/systemd/system/cron.service; enabled; preset: enabled)
     Active: active (running) since Tue 2026-09-29 21:10:56 WAT; 1min 45s ago
 Invocation: 2d295249d5054e72abe2f0ccdb4424eb
       Docs: man:cron(8)
   Main PID: 1739 (cron)
      Tasks: 1 (limit: 9306)
     Memory: 356K (peak: 1.7M)
        CPU: 44ms
     CGroup: /system.slice/cron.service
             └─1739 /usr/sbin/cron -f -P

Sep 29 21:10:56 Sammy systemd[1]: Started cron.service - Regular background program processing daemon.
Sep 29 21:10:56 Sammy (cron)[1739]: cron.service: Referenced but unset environment variable evaluates to an empty string: EXTRA_OPTS
Sep 29 21:10:56 Sammy cron[1739]: (CRON) INFO (pidfile fd = 3)
Sep 29 21:10:56 Sammy cron[1739]: (CRON) INFO (Skipping @reboot jobs -- not system startup)
Hint: Some lines were ellipsized, use -l to show in full.
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl is-active cron
active
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl is-enabled cron
enabled
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl stop cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl is-active cron
inactive
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl restart cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ sudo systemctl enable --now cron
Synchronizing state of cron.service with SysV service script with /usr/lib/systemd/systemd-sysv-install.
Executing: /usr/lib/systemd/systemd-sysv-install enable cron
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl is-active cron
active
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$ systemctl is-enabled cron
enabled
olamide@Sammy:~/OlamideSammy-linux-command-mastery-challenge/day-23-systemctl-basics$
