### File and Directory Management
| Command | Description |
|----------|-------------|
| `pwd` | Show current working directory |
| `ls` | List files and directories |
| `ls -l` | List files with details (permissions, size, etc.) |
| `ls -a` | List all files including hidden ones |
| `cd <directory>` | Change directory |
| `cd ..` | Move one directory up |
| `mkdir <dir>` | Create a new directory |
| `rmdir <dir>` | Remove an empty directory |
| `rm <file>` | Remove a file |
| `rm -r <dir>` | Remove a directory recursively |
| `cp <source> <destination>` | Copy files or directories |
| `mv <source> <destination>` | Move or rename files or directories |
| `touch <file>` | Create an empty file |
| `cat <file>` | Display file content |
| `less <file>` | View large files one page at a time |
| `head <file>` | Show first 10 lines of a file |
| `tail <file>` | Show last 10 lines of a file |
| `tail -f <file>` | Continuously monitor file updates (e.g., logs) |
---

### File Permissions
| Command | Description |
|----------|-------------|
| `chmod <permissions> <file>` | Change file permissions |
| `chown <user>:<group> <file>` | Change file owner and group |
| `ls -l` | Check file permissions |
| `umask` | Display default permission mask |

---

### File Searching
| Command | Description |
|----------|-------------|
| `find <path> -name <filename>` | Search files by name |
| `grep <pattern> <file>` | Search text inside files |
| `locate <filename>` | Quickly find file paths (requires `updatedb`) |
| `which <command>` | Locate command executable path |
| `whereis <command>` | Locate command binaries and source |

---

### System Information
| Command | Description |
|----------|-------------|
| `uname -a` | Display system information |
| `hostname` | Display or set system hostname |
| `top` | Display running processes |
| `htop` | Interactive process viewer (if installed) |
| `df -h` | Show disk space usage |
| `du -sh <dir>` | Show directory size |
| `free -h` | Show memory usage |
| `uptime` | Show how long system has been running |
| `whoami` | Show current logged-in user |
| `id` | Show user ID and group info |

---

### Package Management (Debian/Ubuntu)
| Command | Description |
|----------|-------------|
| `sudo apt update` | Update package lists |
| `sudo apt upgrade` | Upgrade all packages |
| `sudo apt install <package>` | Install a package |
| `sudo apt remove <package>` | Remove a package |
| `sudo apt autoremove` | Remove unused dependencies |

---

### Process Management
| Command | Description |
|----------|-------------|
| `ps` | Show running processes |
| `ps aux` | List all processes with details |
| `kill <PID>` | Kill process by ID |
| `kill -9 <PID>` | Force kill process |
| `jobs` | Show background jobs |
| `fg %<job_id>` | Bring background job to foreground |
| `bg %<job_id>` | Resume job in background |

---

### Network Commands
| Command | Description |
|----------|-------------|
| `ping <host>` | Test network connectivity |
| `ifconfig` | Display network interfaces (deprecated, use `ip a`) |
| `ip a` | Show network interface info |
| `netstat -tuln` | Show active connections |
| `curl <url>` | Fetch content from a URL |
| `wget <url>` | Download files from web |
| `ssh <user>@<host>` | Connect to remote machine |
| `scp <file> <user>@<host>:<path>` | Copy files securely between machines |

---

### File Compression
| Command | Description |
|----------|-------------|
| `tar -cvf archive.tar <files>` | Create a tar archive |
| `tar -xvf archive.tar` | Extract a tar archive |
| `tar -czvf archive.tar.gz <files>` | Create a compressed tarball |
| `tar -xzvf archive.tar.gz` | Extract a compressed tarball |
| `zip <archive.zip> <files>` | Create a zip archive |
| `unzip <archive.zip>` | Extract a zip file |

---

### Miscellaneous
| Command | Description |
|----------|-------------|
| `date` | Show current date and time |
| `cal` | Show calendar |
| `history` | Show command history |
| `clear` | Clear the terminal screen |
| `echo "text"` | Display text or variables |
| `man <command>` | Show manual page for a command |

---
