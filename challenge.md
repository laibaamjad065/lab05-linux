
# Lab 05 — Security Detective Challenge

## 1. Current User and Home Directory

**Command used:**
```bash
whoami
pwd
```

**Answer:**
- Current username: laibaamjad065
- Current working directory: /home/laibaamjad065/lab05-linux

## 2. Hostname and Ubuntu Version

**Commands used:**
```bash
hostname
cat /etc/os-release | head -2
```

**Answer:**
- Hostname: [ubuntu]
- Operating system: [PRETTY_NAME="Ubuntu 26.04.1 LTS"]

## 3. Memory and Disk Space

**Commands used:**
```bash
free -h
df -h /
```

**Answer:**
- Total RAM: 1.6 GiB
- Available RAM: 927 MiB
- Root filesystem size: 9.8G
- Used disk space: 6.6G
- Available disk space: 2.8G
- Disk usage: 71%

## 4. Users Who Use Bash

**Command used:**
```bash
grep "/bin/bash" /etc/passwd
```

**Answer:**
The command displays user accounts configured to use /bin/bash as their login shell. The actual usernames can be identified from the command output.

## 5. Running Processes

**Command used:**
```bash
ps aux | wc -l
```

**Answer:**
Total lines returned: [240].
Approximate number of processes: [239].

## 6. User Creation and Deletion Evidence

**Commands used:**```bash
sudo grep lab5user /var/log/auth.log | tail -5
sudo journalctl | grep lab5user | tail -20
```

**Answer:**
The authentication logs were checked for evidence of the creation and deletion of the temporary user lab5user. The available log entries should be used to identify timestamps. If the logs do not contain the relevant events, the exact creation and deletion timestamps cannot be verified.

## Conclusion

This challenge practiced Linux user identification, operating system inspection, memory and disk monitoring, Bash-user identification, process counting, and security-log investigation. The temporary lab5user account was removed after completing the user-management task.
