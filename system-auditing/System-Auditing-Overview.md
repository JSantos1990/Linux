# 📋 System Auditing Overview

This document provides an introduction to auditing Linux systems for misconfigurations or suspicious activity.

---

## 🔍 1. What Is System Auditing?

System auditing involves:

- Checking user accounts
- Reviewing installed software
- Inspecting running services
- Checking scheduled tasks
- Ensuring security baselines

📸 Screenshot placeholder: System overview command.

---

## 👤 2. User & Group Auditing

Check users:

`cat /etc/passwd`

Check sudo privileges:

`grep sudo /etc/group`

📸 Screenshot placeholder: passwd file sample.

---

## 📦 3. Installed Software Audit

Commands:

- `dpkg -l`
- `apt list --installed`
- `rpm -qa` (RHEL)

📸 Screenshot placeholder: package list.

---

## 🛠️ 4. Service & Startup Audit

Commands:

- `systemctl list-units --type=service`
- `systemctl is-enabled <service>`

📸 Screenshot placeholder: systemctl output.

---

## 🧭 5. Auditing Checklist

- [ ] Remove unused users
- [ ] Review running services
- [ ] Check cron jobs
- [ ] Review SUID binaries
- [ ] Check for unauthorized software

---

## 📝 6. Notes

More detailed audit walkthroughs will be added as the lab expands.

---
