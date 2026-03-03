# 🐧 Linux Hardening Overview

This document provides a high-level introduction to Linux hardening techniques used in cybersecurity and system administration.  
It explains the core areas to secure, the main files and configurations involved, and includes placeholders where screenshots will be added later.

---

## 🔐 1. What is Linux Hardening?

Linux hardening consists of securing the operating system by applying:

- Proper configuration of system services  
- User and permission management  
- Secure network settings  
- Monitoring and logging capabilities  
- Reducing the attack surface  
- Enforcing least privilege  

Hardening is essential for preventing unauthorized access and improving overall system security.

📸 Screenshot placeholder: Example of a hardened SSH configuration.

---

## 👤 2. User & Permission Management

Key hardening steps include:

- Removing unnecessary users  
- Using strong passwords  
- Restricting sudo privileges  
- Reviewing `/etc/passwd` and `/etc/shadow`  
- Using file permissions and ACLs correctly  

Common commands:

- `id`, `who`, `last`, `chage`
- `chmod`, `chown`, `setfacl`

📸 Screenshot placeholder: Output of `ls -l` showing permissions.

---

## 🛡️ 3. SSH Hardening

SSH is often the main remote access method, so securing it is critical.

Typical hardening steps:

- Disable root login  
- Change default port (optional)  
- Disable password authentication (use keys instead)  
- Limit users who can connect  
- Enable rate limiting  

Important file:

`/etc/ssh/sshd_config`

📸 Screenshot placeholder: `sshd_config` hardened example.

---

## 🌐 4. Firewall Configuration

Linux uses different firewalls depending on the distro:

- UFW (Ubuntu)
- firewalld (RHEL/CentOS)
- iptables (legacy)

Typical hardening rules:

- Deny all incoming traffic by default  
- Allow only required services  
- Enable logging  
- Drop invalid packets  

Examples:

- `ufw default deny incoming`
- `ufw allow 22/tcp`
- `ufw enable`

📸 Screenshot placeholder: Firewall rules overview.

---

## 📁 5. File System and SUID/SGID

Important areas to secure:

- Prevent execution in `/tmp`  
- Use `noexec` and `nosuid` where possible  
- Audit SUID binaries (`find / -perm -4000`)  
- Enforce file permission best practices  

📸 Screenshot placeholder: Output of SUID file scan.

---

## 📊 6. Logging & Monitoring

Essential tools:

- `journalctl` (systemd logs)
- `/var/log` structure
- Auditd (advanced auditing)
- Fail2ban (intrusion prevention)

Good practices:

- Monitor authentication logs (`auth.log`)
- Check for repeated failed logins
- Monitor privilege escalations

📸 Screenshot placeholder: `journalctl` output.

---

## 📦 7. Package & Service Management

Key hardening steps:

- Update system regularly (`apt update`, `apt upgrade`)
- Disable unused services using `systemctl`
- Remove unnecessary software  
- Validate package sources  

📸 Screenshot placeholder: List of active services.

---

## 🧭 8. Hardening Checklist (Basic)

- [ ] Disable root SSH login  
- [ ] Enforce SSH key authentication  
- [ ] Remove unused packages  
- [ ] Set firewall default to deny incoming  
- [ ] Monitor logs regularly  
- [ ] Restrict sudo access  
- [ ] Harden `/etc/sysctl.conf`  
- [ ] Disable unnecessary services  

---

## 📝 9. Notes

This document provides the foundation for future practical hardening tasks.  
Detailed guides, step-by-step procedures, and configuration screenshots will be added as the lab grows.

---
