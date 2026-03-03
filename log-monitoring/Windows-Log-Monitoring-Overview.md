# 🪟 Windows Log Monitoring Overview

This document introduces the fundamentals of monitoring logs in Windows environments, focused on SOC and incident response.

---

## 📘 1. Key Log Sources

Main logs:

- Security
- System
- Application
- PowerShell
- Sysmon
- Firewall logs

📸 Placeholder: Event Viewer main window.

---

## 🔑 2. Security Log Events

Important IDs:

- 4624: Successful logon
- 4625: Failed logon
- 4768/4769: Kerberos tickets
- 4672: Special privileges assigned
- 4720: User created
- 4728: Added to security group

📸 Placeholder: Security log output.

---

## 🧩 3. Sysmon

Sysmon provides detailed event logging:

- Process creation
- Network connections
- Registry changes
- File modifications

📸 Placeholder: Sysmon event.

---

## 🧭 4. Log Monitoring Checklist

- [ ] Track logons
- [ ] Monitor privilege escalation
- [ ] Watch for failed RDP attempts
- [ ] Monitor PowerShell execution
- [ ] Ingest logs into SIEM

---

## 📝 5. Notes

More examples and screenshots will be added later.

---
