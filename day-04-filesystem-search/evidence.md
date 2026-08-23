olamide@Sammy:~$ find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -name "*.md"
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/drill.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/README.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
olamide@Sammy:~$ find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -type f
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/drill.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/README.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
olamide@Sammy:~$ find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -size +1k
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/README.md
olamide@Sammy:~$ find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -mtime -7
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/drill.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/README.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
olamide@Sammy:~$ find ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search -perm 644
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/drill.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/evidence.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/README.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
olamide@Sammy:~$ locate ~/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
/var/lib/plocate/plocate.db: No such file or directory
olamide@Sammy:~$ sudo updatedb
[sudo: authenticate] Password:

^C

olamide@Sammy:~$ locate commands.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-01-file-navigation/commands.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-02-file-operations/commands.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-03-file-inspection/commands.md
/home/olamide/OlamideSammy-linux-command-mastery-challenge/day-04-filesystem-search/commands.md
/home/olamide/linux-command-mastery-challenge/day-01-file-navigation/commands.md
olamide@Sammy:~$ find /etc -name "*.conf"
/etc/chrony/conf.d/ubuntu-nts.conf
/etc/chrony/chrony.conf
/etc/sudo.conf
/etc/wsl-distribution.conf
/etc/updatedb.conf
/etc/rsyslog.conf
/etc/ucf.conf
/etc/fonts/conf.d/49-sansserif.conf
/etc/fonts/conf.d/40-nonlatin.conf
/etc/fonts/conf.d/58-dejavu-lgc-sans.conf
/etc/fonts/conf.d/20-unhint-small-vera.conf
/etc/fonts/conf.d/10-sub-pixel-rgb.conf
/etc/fonts/conf.d/11-lcdfilter-default.conf
/etc/fonts/conf.d/10-yes-antialias.conf
/etc/fonts/conf.d/58-dejavu-lgc-serif.conf
/etc/fonts/conf.d/71-ubuntulegacy.conf
/etc/fonts/conf.d/57-dejavu-sans.conf
/etc/fonts/conf.d/10-scale-bitmap-fonts.conf
/etc/fonts/conf.d/70-no-bitmaps-except-emoji.conf
/etc/fonts/conf.d/10-hinting-slight.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.d/45-latin.conf
/etc/fonts/conf.d/51-local.conf
/etc/fonts/conf.d/50-user.conf
/etc/fonts/conf.d/57-dejavu-serif.conf
/etc/fonts/conf.d/65-nonlatin.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-sans.conf
/etc/fonts/conf.d/80-delicious.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-lgc-serif.conf
/etc/fonts/conf.d/45-generic.conf
/etc/fonts/conf.d/60-generic.conf
/etc/fonts/conf.d/30-metric-aliases.conf
/etc/fonts/conf.d/48-spacing.conf
/etc/fonts/conf.d/69-unifont.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-serif.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-sans-mono.conf
/etc/fonts/conf.d/60-latin.conf
/etc/fonts/conf.d/20-unhint-small-dejavu-lgc-sans.conf
/etc/fonts/conf.d/57-dejavu-sans-mono.conf
/etc/fonts/conf.d/90-synthetic.conf
/etc/fonts/conf.d/58-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.d/65-fonts-persian.conf
/etc/fonts/fonts.conf
/etc/fonts/conf.avail/58-dejavu-lgc-sans.conf
/etc/fonts/conf.avail/58-dejavu-lgc-serif.conf
/etc/fonts/conf.avail/57-dejavu-sans.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.avail/57-dejavu-serif.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-sans.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-serif.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-serif.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-sans-mono.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-sans.conf
/etc/fonts/conf.avail/57-dejavu-sans-mono.conf
/etc/fonts/conf.avail/58-dejavu-lgc-sans-mono.conf
/etc/mke2fs.conf
/etc/dhcpcd.conf
/etc/gai.conf
/etc/ld.so.conf.d/libc.conf
/etc/ld.so.conf.d/x86_64-linux-gnu.conf
/etc/ld.so.conf.d/ld.wsl.conf
/etc/host.conf
/etc/xdg/user-dirs.conf
/etc/landscape/client.conf
/etc/wsl.conf
/etc/libaudit.conf
/etc/apt/apt.conf.d/20apt-esm-hook.conf
/etc/apt/apt.conf.d/20snapd.conf
/etc/selinux/semanage.conf
/etc/sensors3.conf
/etc/xattr.conf
/etc/pam.conf
/etc/environment.d/90qt-a11y.conf
/etc/PackageKit/Vendor.conf
/etc/PackageKit/PackageKit.conf
/etc/udev/udev.conf
/etc/udev/iocost.conf
/etc/modprobe.d/blacklist.conf
/etc/modprobe.d/blacklist-rare-network.conf
/etc/modprobe.d/blacklist-firewire.conf
/etc/modprobe.d/blacklist-ath_pci.conf
/etc/modprobe.d/blacklist-framebuffer.conf
/etc/modprobe.d/iwlwifi.conf
/etc/deluser.conf
/etc/modules-load.d/modules.conf
/etc/e2scrub.conf
/etc/ld.so.conf
/etc/nsswitch.conf
/etc/debconf.conf
/etc/systemd/resolved.conf
/etc/systemd/pstore.conf
/etc/systemd/sleep.conf
/etc/systemd/networkd.conf
/etc/systemd/journald.conf
/etc/systemd/system.conf
/etc/systemd/user.conf
/etc/systemd/logind.conf
/etc/adduser.conf
find: ‘/etc/polkit-1/rules.d’: Permission denied
/etc/fuse.conf
find: ‘/etc/credstore.encrypted’: Permission denied
/etc/ldap/ldap.conf
/etc/ubuntu-advantage/uaclient.conf
find: ‘/etc/credstore’: Permission denied
/etc/apparmor/parser.conf
/etc/ssh/ssh_config.d/20-systemd-ssh-proxy.conf
find: ‘/etc/ssl/private’: Permission denied
/etc/depmod.d/ubuntu.conf
/etc/tmpfiles.d/screen-cleanup.conf
/etc/vconsole.conf
/etc/security/group.conf
/etc/security/time.conf
/etc/security/pwhistory.conf
/etc/security/sepermit.conf
/etc/security/capability.conf
/etc/security/limits.conf
/etc/security/limits.d/10-coredump-debian.conf
/etc/security/faillock.conf
/etc/security/access.conf
/etc/security/pam_env.conf
/etc/security/namespace.conf
/etc/dbus-1/system.d/com.ubuntu.SoftwareProperties.conf
/etc/rsyslog.d/21-cloudinit.conf
/etc/rsyslog.d/50-default.conf
/etc/logrotate.conf
/etc/sudo_logsrvd.conf
/etc/gtk-3.0/im-multipress.conf
/etc/apport/crashdb.conf
/etc/locale.conf
/etc/resolv.conf
/etc/ca-certificates.conf
olamide@Sammy:~$ find /var -type f -size +1M
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/log/chrony’: Permission denied
find: ‘/var/log/private’: Permission denied
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000.journal
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@0006591adda499d9-183dbddaf8f59f54.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659195fc4363d-05ea8e28f5adbac6.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@000651413af8b999-ddbfc9cb155e48ec.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659bccbacd8e1-b613d3a83ee69c44.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system.journal
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659a45270433d-6666c0513d68d40c.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@00065150de655ac9-720172d71c2a5259.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@00065919600867b5-b7bdf2fc9f42c05d.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@00065976b3255e46-d62235293a2a0873.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@000659a452b93dce-a063f366532f7586.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659636ca9139a-eed4a9c2e75b29d7.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@00065784d5a34905-f19f20101d6b362e.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@0006514106a06252-f90515b1d1d21c96.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@0006515130f6d7eb-27e7acff63f16db2.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@0006515130be4b42-d4647ed9afdcb77b.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@000651a0d84fdfed-364eee067a34643f.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@00065976b381c9ba-20d9d8f2ed99823b.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000651a0d80c77d9-ffffde3ddb2fda7b.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@f468f021a93f481bb14dc31dbc76cf22-0000000000001729-00065784d5a0b836.journal
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@f468f021a93f481bb14dc31dbc76cf22-00000000000015dc-000651a0d84f8144.journal
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@00065150ddd8b865-9c9097153d2f89c9.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@000659bbc0212fa5-1b8e40da50697498.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@f468f021a93f481bb14dc31dbc76cf22-00000000000019b2-00065784d5e11609.journal
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659543eb86148-0da184d940778378.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@0006591added1150-eb17558d101070bf.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659769b73b078-567e1277ebc22b49.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000651413abc1774-dce3f2d52991cedf.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/system@000659bbbf9a2347-39563141829489ce.journal~
/var/log/journal/0acb22f75c0b460d88e11fbc100389c5/user-1000@000659bcd35860cb-c10d4f6cae0dadd4.journal~
find: ‘/var/cache/private’: Permission denied
/var/cache/debconf/templates.dat
/var/cache/debconf/templates.dat-old
/var/cache/apt/srcpkgcache.bin
/var/cache/apt/pkgcache.bin
find: ‘/var/cache/apt/archives/partial’: Permission denied
/var/cache/swcatalog/cache/C-os-catalog.xb
find: ‘/var/cache/ldconfig’: Permission denied
/var/cache/snapd/commands.db
find: ‘/var/tmp/systemd-private-b0bd504d595e4330bd15e11ac185d3b8-chrony.service-ip7gLT’: Permission denied
find: ‘/var/tmp/systemd-private-b0bd504d595e4330bd15e11ac185d3b8-polkit.service-5cPKDH’: Permission denied
find: ‘/var/tmp/systemd-private-b0bd504d595e4330bd15e11ac185d3b8-systemd-logind.service-ULhwUC’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
/var/lib/plocate/plocate.db
/var/lib/command-not-found/commands.db
find: ‘/var/lib/private’: Permission denied
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_universe_i18n_Translation-en
find: ‘/var/lib/apt/lists/partial’: Permission denied
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_main_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute-updates_universe_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_restricted_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_main_i18n_Translation-en
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute-updates_restricted_i18n_Translation-en
/var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_resolute-security_restricted_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_universe_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute-updates_main_i18n_Translation-en
/var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_resolute-security_main_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_universe_dep11_Components-amd64.yml.gz
/var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_resolute-security_restricted_i18n_Translation-en
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute-updates_restricted_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_multiverse_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute-updates_main_binary-amd64_Packages
/var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_resolute_universe_cnf_Commands-amd64
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
/var/lib/ubuntu-advantage/apt-esm/var/cache/apt/srcpkgcache.bin
/var/lib/ubuntu-advantage/apt-esm/var/cache/apt/pkgcache.bin
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
olamide@Sammy:~$ du -sh /home
4.3M    /home
olamide@Sammy:~$ df -h /
Filesystem      Size  Used Avail Use% Mounted on
/dev/sdd       1007G  1.8G  954G   1% /
olamide@Sammy:~$
