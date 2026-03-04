# 🧵 Tcpdump Filters Cheat Sheet

Useful capture filters for packet capture.

---

## 📘 1. Common Filters

- `port 80`  
- `host 8.8.8.8`  
- `net 192.168.1.0/24`  
- `tcp[tcpflags] & tcp-syn != 0`

📸 Placeholder: tcpdump output.

---

## 🧭 2. Tips

- combine with `-w file.pcap`  
- limit with `-c` for sample size

---
