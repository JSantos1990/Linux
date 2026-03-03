# 📁 Linux File Permissions Overview

This document explains Linux file permissions and how they support system security.  
Screenshots will be added once real terminal outputs are captured.

---

## 🔑 1. Permission Types

Linux uses:

- Read (r)
- Write (w)
- Execute (x)

These apply to:

- User (u)
- Group (g)
- Others (o)

📸 Screenshot placeholder: Example of `ls -l` output.

---

## 📊 2. Numeric Permissions

Common numeric values:

- `7 = rwx`
- `6 = rw-`
- `5 = r-x`
- `4 = r--`

Example:

`chmod 755 file.sh`

📸 Screenshot placeholder: chmod example.

---

## 🧬 3. Special Permissions (SUID, SGID, Sticky Bit)

- **SUID** → program runs as owner  
- **SGID** → program runs as group  
- **Sticky bit** → restrict deletion in shared dirs  

Scan SUID binaries:

`find / -perm -4000 2>/dev/null`

📸 Screenshot placeholder: SUID file list.

---

## 🧱 4. Ownership & ACLs

Commands:

- `chown user:group file`
- `setfacl -m u:user:rwx file`

📸 Screenshot placeholder: ACL example.

---

## 🧭 5. Permissions Checklist

- [ ] Remove unnecessary SUID binaries
- [ ] Enforce strict permissions in /etc
- [ ] Use ACLs where needed
- [ ] Disable execution in temporary directories

---

## 📝 6. Notes

More live examples and screenshots will be added later.

---
