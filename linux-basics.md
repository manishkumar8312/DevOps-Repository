# Linux Command Reference

Linux is a powerful open-source operating system widely used in servers, cloud platforms, DevOps environments, and embedded systems. Most interactions with Linux systems are performed through the **command-line interface (CLI)** using the terminal.

This document provides a structured overview of commonly used Linux commands along with their purpose and usage.

---

# 1. File and Directory Management

### Theory

Linux stores all data in a **hierarchical file system** starting from the root directory `/`.
Files and directories are organized in a tree-like structure.

Common operations include:

* Navigating directories
* Creating files and folders
* Copying and moving files
* Deleting files

These operations are fundamental for working in Linux environments.

---

### Commands

| Command                     | Description                          |
| --------------------------- | ------------------------------------ |
| `pwd`                       | Display current working directory    |
| `ls`                        | List directory contents              |
| `ls -l`                     | List files with detailed information |
| `ls -a`                     | Show hidden files                    |
| `cd <directory>`            | Change directory                     |
| `cd ..`                     | Move to parent directory             |
| `mkdir <dir>`               | Create a directory                   |
| `mkdir -p <dir>`            | Create nested directories            |
| `rmdir <dir>`               | Remove an empty directory            |
| `rm <file>`                 | Delete a file                        |
| `rm -r <dir>`               | Delete directory recursively         |
| `rm -rf <dir>`              | Force delete directory               |
| `cp <source> <destination>` | Copy files or directories            |
| `cp -r <dir>`               | Copy directories recursively         |
| `mv <source> <destination>` | Move or rename files                 |
| `touch <file>`              | Create an empty file                 |
| `stat <file>`               | Display file metadata                |

Example:

```
mkdir project
cd project
touch app.py
ls -l
```

---

# 2. File Viewing and Editing

### Theory

Linux provides multiple utilities to read, inspect, and edit files directly from the terminal.
These tools are particularly useful for working with **configuration files, logs, and scripts** on servers.

Some tools allow simple viewing, while others provide full text editing capabilities.

---

### Commands

| Command          | Description                       |
| ---------------- | --------------------------------- |
| `cat <file>`     | Display entire file contents      |
| `less <file>`    | View file page by page            |
| `more <file>`    | Basic pager for viewing files     |
| `head <file>`    | Show first 10 lines               |
| `tail <file>`    | Show last 10 lines                |
| `tail -f <file>` | Monitor file updates in real time |
| `nano <file>`    | Edit file using Nano editor       |
| `vim <file>`     | Edit file using Vim editor        |

Example:

```
tail -f system.log
```

This is commonly used to **monitor log files in real time**.

---

# 3. File Permissions and Ownership

### Theory

Linux uses a **permission-based security model** to control access to files and directories.

Each file has three types of permissions:

* **Read (r)** – view file contents
* **Write (w)** – modify the file
* **Execute (x)** – run the file as a program

Permissions are applied to three categories:

* Owner
* Group
* Others

Example permission format:

```
-rwxr-xr--
```

---

### Commands

| Command                       | Description                  |
| ----------------------------- | ---------------------------- |
| `chmod <permissions> <file>`  | Change file permissions      |
| `chmod +x <file>`             | Make file executable         |
| `chown <user>:<group> <file>` | Change file owner            |
| `chgrp <group> <file>`        | Change file group            |
| `ls -l`                       | View permissions             |
| `umask`                       | Show default permission mask |

Example:

```
chmod 755 script.sh
```

---

# 4. File Searching and Text Processing

### Theory

Linux provides powerful tools for searching files and analyzing text data.
These tools are widely used in **system administration, log analysis, and scripting**.

Utilities such as `grep`, `find`, `awk`, and `sed` allow efficient processing of large text files.

---

### Commands

| Command                    | Description                      |
| -------------------------- | -------------------------------- |
| `find <path> -name <file>` | Search files by name             |
| `find <path> -type f`      | Search only files                |
| `grep <pattern> <file>`    | Search text within file          |
| `grep -r <pattern> <dir>`  | Recursive text search            |
| `locate <file>`            | Quickly find file paths          |
| `which <command>`          | Locate executable                |
| `whereis <command>`        | Locate binary and manual         |
| `awk`                      | Pattern scanning and processing  |
| `sed`                      | Stream editor for modifying text |

Example:

```
grep "error" server.log
```

---

# 5. System Information

### Theory

Linux provides various commands to retrieve system information such as **CPU details, memory usage, uptime, and active users**.

These commands are useful for monitoring system health and troubleshooting performance issues.

---

### Commands

| Command        | Description                |
| -------------- | -------------------------- |
| `uname -a`     | Display system information |
| `hostname`     | Show system hostname       |
| `uptime`       | Show system running time   |
| `whoami`       | Show current user          |
| `who`          | Show logged-in users       |
| `id`           | Display user ID and groups |
| `lscpu`        | CPU information            |
| `free -h`      | Memory usage               |
| `df -h`        | Disk space usage           |
| `du -sh <dir>` | Directory size             |

---

# 6. Process Management

### Theory

A **process** is a running instance of a program.
Linux allows users to monitor, control, and terminate processes using various commands.

This is essential for managing applications and server workloads.

---

### Commands

| Command         | Description                  |
| --------------- | ---------------------------- |
| `ps`            | Show running processes       |
| `ps aux`        | List all processes           |
| `top`           | Real-time process monitoring |
| `htop`          | Interactive process viewer   |
| `kill <PID>`    | Terminate process            |
| `kill -9 <PID>` | Force kill process           |
| `pkill <name>`  | Kill process by name         |
| `jobs`          | Show background jobs         |
| `bg`            | Resume job in background     |
| `fg`            | Bring job to foreground      |

---

# 7. Package Management (Debian/Ubuntu)

### Theory

Package managers are used to install, update, and remove software from the system.

Ubuntu and Debian-based systems use **APT (Advanced Package Tool)** for managing software packages.

---

### Commands

| Command                      | Description                       |
| ---------------------------- | --------------------------------- |
| `sudo apt update`            | Update package list               |
| `sudo apt upgrade`           | Upgrade installed packages        |
| `sudo apt install <package>` | Install package                   |
| `sudo apt remove <package>`  | Remove package                    |
| `sudo apt purge <package>`   | Remove package with configuration |
| `sudo apt autoremove`        | Remove unused dependencies        |
| `apt search <package>`       | Search package                    |

---

# 8. Networking Commands

### Theory

Networking commands are used to diagnose connectivity issues, manage network interfaces, and communicate with remote systems.

These commands are essential for **system administrators and DevOps engineers**.

---

### Commands

| Command                           | Description                    |
| --------------------------------- | ------------------------------ |
| `ping <host>`                     | Test connectivity              |
| `ip a`                            | Display network interfaces     |
| `ip route`                        | Show routing table             |
| `netstat -tuln`                   | Show open ports                |
| `ss -tuln`                        | Modern replacement for netstat |
| `curl <url>`                      | Fetch data from URL            |
| `wget <url>`                      | Download files                 |
| `ssh <user>@<host>`               | Remote login                   |
| `scp <file> <user>@<host>:<path>` | Secure file transfer           |

---

# 9. File Compression and Archiving

### Theory

Compression utilities reduce file size and allow multiple files to be bundled together into a single archive.

This is useful for **backups, distribution, and storage optimization**.

---

### Commands

| Command                            | Description                |
| ---------------------------------- | -------------------------- |
| `tar -cvf archive.tar <files>`     | Create tar archive         |
| `tar -xvf archive.tar`             | Extract tar archive        |
| `tar -czvf archive.tar.gz <files>` | Create compressed archive  |
| `tar -xzvf archive.tar.gz`         | Extract compressed archive |
| `zip archive.zip <files>`          | Create zip archive         |
| `unzip archive.zip`                | Extract zip archive        |
| `gzip <file>`                      | Compress file              |
| `gunzip <file.gz>`                 | Decompress file            |

---

# 10. Miscellaneous Commands

### Theory

These commands provide general utilities for working with the terminal environment.

---

### Commands

| Command         | Description                |
| --------------- | -------------------------- |
| `date`          | Show current date and time |
| `cal`           | Display calendar           |
| `history`       | Show command history       |
| `clear`         | Clear terminal             |
| `echo`          | Print text or variables    |
| `alias`         | Create command shortcut    |
| `man <command>` | Show manual page           |

Example:

```
man ls
```

