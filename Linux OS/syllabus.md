# LINUX OPERATING SYSTEM

## Chapter 1: Introduction to Linux

* Definition and history of Linux (Unix, GNU, Linus Torvalds)
* Open source philosophy and licensing (GPL, MIT)
* Linux kernel vs distributions
* Popular distributions: Ubuntu, Fedora, Debian, CentOS, Arch, openSUSE
* Linux use cases: servers, embedded systems, desktops, cloud, containers

---

## Chapter 2: Installation and Setup

* Choosing a Linux distribution for learning
* Creating bootable USB drives (`Rufus`, `balenaEtcher`, `dd`)
* Installing Linux using VirtualBox and VMware
* Dual booting concepts
* Partitioning basics: `/`, `/home`, `swap`
* Windows Subsystem for Linux (WSL)

---

## Chapter 3: Command Line Basics

* Shell basics: Bash and Zsh
* Navigation commands: `pwd`, `ls`, `cd`
* Directory operations: `mkdir`, `rmdir`
* File operations: `touch`, `cp`, `mv`, `rm`
* Viewing files: `cat`, `less`, `head`, `tail`
* Wildcards and globbing (`*`, `?`, `[abc]`)
* Command history and auto-completion
* Getting help: `man`, `info`, `--help`

---

## Chapter 4: Linux Filesystem

* Filesystem Hierarchy Standard (FHS)
* Important directories: `/bin`, `/sbin`, `/etc`, `/var`, `/usr`, `/home`, `/proc`
* Absolute vs relative paths
* File types in Linux
* Hard links vs symbolic links
* File searching: `find`, `locate`, `which`, `whereis`
* Disk usage: `du`, `df`, `lsblk`
* Mounting basics with `mount`

---

## Chapter 5: File Permissions and Ownership

* Understanding `ls -l`
* Users, groups, and others
* Changing permissions using `chmod`
* Ownership management: `chown`, `chgrp`
* Special permissions: `setuid`, `setgid`, sticky bit
* Umask – default permission mask

---

## Chapter 6: Process Management

* Processes, PID, and PPID
* Process states: running, sleeping, zombie
* Managing processes: `ps`, `top`, `htop`, `pgrep`
* Signals and process control: `kill`, `killall`, `pkill`
* Foreground and background jobs: `&`, `jobs`, `fg`, `bg`
* Process priorities: `nice`, `renice`
* System load monitoring: `uptime`, `vmstat`

---

## Chapter 7: Package Management

* Package formats: `.deb`, `.rpm`
* APT package manager: `apt update`, `apt install`, `apt remove`, `apt upgrade`
* DNF/YUM basics
* Adding repositories (PPA, EPEL)
* Installing software from source: `./configure`, `make`, `make install`
* Alternative package formats: Snap, Flatpak, AppImage

---

## Chapter 8: Shell Scripting (Bash)

* Shebang (`#!/bin/bash`) and script execution
* Variables: user-defined, environment, special variables (`$?`, `$@`, `$#`)
* User input with `read`
* Command substitution `$(...)`
* Conditional statements: `if`, `else`, `test`, `[ ]`, `[[ ]]`
* Loops: `for`, `while`, `until`
* Arrays and positional parameters
* Case statements
* Functions and exit codes
* Debugging scripts: `set -x`, `set -e`

---

## Chapter 9: Text Editors and Stream Processing

* `nano` basics
* `vim` basics: modes, navigation, editing, saving and quitting
* Text searching with `grep`
* Stream editing using `sed`
* Data extraction using `awk`
* Pipes and redirections: `|`, `>`, `>>`, `2>`
* Regular expressions

---

## Chapter 10: Networking Basics

* IPv4 and IPv6 basics
* Network interfaces and addressing
* Networking tools: `ip`, `ifconfig`, `ping`, `traceroute`, `ss`, `netstat`
* DNS tools: `/etc/resolv.conf`, `dig`, `nslookup`
* Download tools: `wget`, `curl`
* Remote access: `ssh`, `scp`, `rsync`
* Firewall basics using `ufw`

---

## Chapter 11: System Administration

* User management: `useradd`, `usermod`, `passwd`, `userdel`
* Group management: `groupadd`, `gpasswd`
* `sudo` and `/etc/sudoers`
* System logging: `syslog`, `journalctl`
* Task scheduling: `cron`, `crontab`, `at`
* systemd basics: `systemctl`, services, targets
* Archiving and compression: `tar`, `gzip`, `zip`, `unzip`

---

## Chapter 12: Security Fundamentals

* Principle of least privilege
* Password policies and `/etc/login.defs`
* Firewall concepts: UFW, firewalld basics
* File integrity: `md5sum`, `sha256sum`
* Auditing with `auditd`
* SELinux and AppArmor basics
* Encryption tools: `gpg`, `openssl`

---

## Chapter 13: Monitoring and Troubleshooting

* System monitoring: `top`, `htop`, `free`, `vmstat`
* Disk and I/O monitoring: `iostat`, `iotop`
* Network monitoring: `iftop`, `nethogs`
* Logs and debugging: `dmesg`, `journalctl`, `strace`
* Basic troubleshooting techniques
* Monitoring system performance and resource usage

---

## Chapter 14: Advanced Shell Environment

* Shell startup files: `/etc/profile`, `~/.bashrc`, `~/.profile`
* Shell variables vs environment variables
* Using `export`
* Aliases and shell functions
* Shell history management: `history`, `!!`, `!$`
* Prompt customization using `PS1`
* Terminal multiplexers: `screen`, `tmux`
* Background execution: `nohup`, `disown`

---

## Chapter 15: Linux Internals

* Linux boot process: BIOS/UEFI, GRUB, Kernel, initramfs, systemd
* Runlevels and systemd targets
* Kernel modules: `lsmod`, `modprobe`
* `/proc` and `/sys` filesystems
* System calls overview: `fork()`, `exec()`, `read()`, `write()`
* Virtual memory and swapping
* IPC basics: pipes, signals

---

## Chapter 16: Storage Management

* Disk partitioning: MBR vs GPT, `fdisk`, `parted`
* Filesystems: ext4, xfs, btrfs basics
* Mounting and unmounting: `mount`, `umount`, `/etc/fstab`
* Swap management: `swapon`, `swapoff`
* LVM basics: Physical Volume (PV), Volume Group (VG), Logical Volume (LV)
* RAID concepts overview

---

## Chapter 17: Linux in Cloud & DevOps (Basics)

* Linux cloud servers: AWS EC2, DigitalOcean, GCP basics
* SSH keys and server access
* Basic server hardening
* `fail2ban` basics
* Docker introduction: containers vs virtual machines, Docker architecture
* Basic Docker commands: `docker run`, `docker ps`, `docker exec`, `docker stop`

---

## Chapter 18: Important Interview Topics

* Linux vs Unix
* Linux boot process
* Hard link vs symbolic link
* Zombie vs orphan process
* Difference between `kill`, `killall`, and `pkill`
* How `sudo` works
* `cron` vs systemd timers
* Difference between TCP and UDP
* Common Linux configuration files
* Frequently asked Linux commands
* Important troubleshooting commands

---

## ⭐ Support

If this repository adds value to your learning, consider giving it a ⭐ to show your support.
