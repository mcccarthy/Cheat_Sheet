# Linux System Administration Cheat Sheet

## 1. User Management

### Create a New User

```bash
sudo adduser <username>
```

### Delete a User

```bash
sudo deluser <username>
```

### List All Users

```bash
cat /etc/passwd
```

### Change User Password

```bash
sudo passwd <username>
```

### Add User to a Group

```bash
sudo usermod -aG <group> <username>
```

---

## 2. Permissions & Ownership

### Change File Permissions

- **r (read), w (write), x (execute)**:

  ```bash
  chmod 755 file.txt  # Owner: rwx, Group: rx, Others: rx
  chmod u+x file.sh   # Add execute permission to user
  ```

### Change File Owner

```bash
sudo chown <owner>:<group> file.txt
```

### View File Permissions

```bash
ls -l
```

---

## 3. Disk Management

### Check Disk Usage

- **View available space on mounted partitions**:

  ```bash
  df -h
  ```

### Check Directory Size

- **Summarize disk usage of a directory**:

  ```bash
  du -sh /path/to/directory
  ```

### List Open File Descriptors

- **View system-wide open files and disk usage**:

  ```bash
  lsof
  ```

---

## 4. Process Management

### View Running Processes

```bash
top
```

### Kill a Process by PID

```bash
kill <pid>
```

### Kill a Process by Name

```bash
pkill <process-name>
```

### Check CPU and Memory Usage

```bash
htop
```

---

## 5. Cron Jobs (Task Scheduling)

### Edit Cron Jobs

```bash
crontab -e
```

### List User Cron Jobs

```bash
crontab -l
```

### Cron Syntax

```
* * * * * command
# ┬ ┬ ┬ ┬ ┬
# │ │ │ │ │
# │ │ │ │ └─ Day of week (0 - 7) (Sunday to Saturday)
# │ │ │ └── Month (1 - 12)
# │ │ └─── Day of month (1 - 31)
# │ └──── Hour (0 - 23)
# └───── Minute (0 - 59)
```

Example: Run a script every day at 2 AM:

```bash
0 2 * * * /path/to/script.sh
```

---

## 6. Networking

### Check Network Configuration

```bash
ifconfig   # (deprecated, use ip instead)
ip a       # List all interfaces
```

### Ping an IP or Hostname

```bash
ping <hostname/IP>
```

### Check Open Ports

```bash
sudo netstat -tuln
```

### Test Connectivity to a Specific Port

```bash
nc -zv <hostname> <port>
```

---

## 7. File & Directory Management

### Copy a File or Directory

```bash
cp file.txt /path/to/destination/
cp -r /path/to/directory/ /destination/
```

### Move or Rename a File

```bash
mv file.txt /path/to/destination/
```

### Remove a File or Directory

```bash
rm file.txt
rm -r /path/to/directory/
```

---

## 8. System Monitoring

### Check System Uptime

```bash
uptime
```

### View Kernel Messages

```bash
dmesg
```

### Check System Logs

- **View system log messages (usually in `/var/log/`)**:

  ```bash
  tail -f /var/log/syslog
  ```

---

## 9. Package Management (apt)

### Update Package List

```bash
sudo apt update
```

### Upgrade Installed Packages

```bash
sudo apt upgrade
```

### Install a Package

```bash
sudo apt install <package>
```

### Remove a Package

```bash
sudo apt remove <package>
```

---

## 10. System Services

### Start a Service

```bash
sudo systemctl start <service>
```

### Stop a Service

```bash
sudo systemctl stop <service>
```

### Check Status of a Service

```bash
sudo systemctl status <service>
```

### Enable a Service on Boot

```bash
sudo systemctl enable <service>
```

---

## 11. SSH & Remote Access

### Connect to a Remote Server

```bash
ssh user@remote_ip
```

### Copy Files to a Remote Server (SCP)

```bash
scp file.txt user@remote_ip:/path/to/destination
```

### Securely Transfer Files with rsync

```bash
rsync -avz /local/path/ user@remote_ip:/remote/path/
```

---

## 12. System Information

### Check System Info

```bash
uname -a
```

### View Memory Usage

```bash
free -h
```

### Check Disk Health (SMART)

```bash
sudo smartctl -a /dev/sda
```

---

## 13. Troubleshooting

### View Recently Installed Packages

```bash
grep " install " /var/log/dpkg.log
```

### Check for Failing Units (Systemd)

```bash
systemctl --failed
```

### List Block Devices

```bash
lsblk
```

### Mount a Disk

```bash
sudo mount /dev/sdX /mnt
```

### View Hardware Information

```bash
lshw
```

---

This cheat sheet covers essential commands and tools for administering a
Linux system.

This should provide a solid starting point for Linux system administration.
