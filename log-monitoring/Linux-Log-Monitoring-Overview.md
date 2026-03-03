# 📑 Linux Log Monitoring & Analysis Overview

This document provides an introduction to Linux log monitoring and analysis, covering the most important log files, common commands, and best practices.  
Screenshots will be added later as the home lab is fully deployed.

---

## 📘 1. Why Log Monitoring Matters

Monitoring logs on Linux is essential for:

- Detecting unauthorized access attempts  
- Identifying service failures  
- Tracking configuration changes  
- Investigating suspicious activity  
- Supporting SOC and incident response workflows  

Logs are one of the most valuable data sources for Blue Team operations.

📸 Screenshot placeholder: Example of a /var/log directory listing.

---

## 📁 2. Key Linux Log Locations

Linux stores logs primarily under:

`/var/log`

Important files include:

- `auth.log` → Authentication activity  
- `syslog` → Core system events  
- `kern.log` → Kernel messages  
- `daemon.log` → Background services  
- `dpkg.log` → Package installation history  
- `ufw.log` → Firewall activity (Ubuntu)  

📸 Screenshot placeholder: Tail of /var/log/auth.log.

---

## 📜 3. Journalctl (systemd)

Most modern Linux systems use **systemd**, which stores logs in an internal journal.

Useful commands:

- `journalctl` → Show system logs  
- `journalctl -u ssh` → Logs for the SSH service  
- `journalctl -b` → Logs from current boot  
- `journalctl -p err` → Show only errors  

Journalctl allows filtering by:

- user  
- service  
- priority  
- time  
- boot  

📸 Screenshot placeholder: Example output of `journalctl -u ssh`.

---

## 🔐 4. Authentication Logs

Authentication logs are critical for security monitoring.

Events to look for:

- Failed SSH logins  
- Successful logins from unusual IPs  
- Sudden sudo escalations  
- Locked accounts  
- PAM failures  

File:

`/var/log/auth.log`

Commands:

- `grep "Failed password" /var/log/auth.log`  
- `grep "sudo" /var/log/auth.log`  

📸 Screenshot placeholder: Failed SSH attempts.

---

## 🌐 5. SSH Activity Monitoring

SSH is a primary target for brute-force and intrusion attempts.

Key indicators:

- Repeated login failures  
- Logins from unknown IPs  
- Root login attempts  
- Sudden successful login after several failures  
- Public key authentication errors  

📸 Screenshot placeholder: SSH brute force attempt.

---

## 🛠️ 6. Service Logs

Each service has its own logs, accessible via:

- `/var/log/daemon.log`
- `journalctl -u <service_name>`

Examples:

- `journalctl -u apache2`
- `journalctl -u ssh`
- `journalctl -u cron`

Monitor for:

- Restarts  
- Failures  
- Permission errors  
- Misconfigurations  

📸 Screenshot placeholder: Cron job logs.

---

## 📊 7. Log Analysis Tools

Common tools include:

- `grep`  
- `awk`  
- `sed`  
- `less`  
- `tail -f` (real-time monitoring)

Example:

`sudo tail -f /var/log/auth.log`

Useful for real-time SOC triage.

📸 Screenshot placeholder: tail -f output.

---

## 🧭 8. Log Monitoring Checklist

- [ ] Review auth.log daily  
- [ ] Monitor sudo usage  
- [ ] Track service restarts  
- [ ] Watch for unexpected IP connections  
- [ ] Monitor firewall logs  
- [ ] Store logs centrally for SIEM ingestion  

---

## 📝 9. Notes

This document provides the foundation for deeper Linux log analysis.  
Screenshots, use cases, and real log samples will be added later as part of the home lab exercises.

---
