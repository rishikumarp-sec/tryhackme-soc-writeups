# 🛡️ TryHackMe — SOC L1 | Phishing Alert Investigation

> **Room:** Introduction to Phishing | **Role:** SOC L1 Analyst | **Difficulty:** Beginner

---

## 🚨 The Alert

| Field | Value |
|---|---|
| Alert ID | 8816 |
| Severity | High |
| Source IP | 10.20.2.17 |
| Destination IP | 67.199.248.11 |
| URL | http://bit.ly/3sHkX3da12340 |
| Port | 80 (HTTP) |
| Action | **Blocked** ✅ |

---

## 🔍 Investigation

**Immediate Red Flags:**
- `bit.ly` shortener → hides the real destination
- Port 80 / HTTP → unencrypted, suspicious
- Blacklist rule triggered → known bad destination

**OSINT Results:**

| IOC | Tool | Result |
|---|---|---|
| 67.199.248.11 | VirusTotal + AbuseIPDB | 🔴 Malicious |
| bit.ly/3sHkX3da12340 | VirusTotal | 🔴 Phishing URL |

**What I couldn't determine at L1:**
- User behind `10.20.2.17` → no DHCP/AD access
- How URL reached the user → no email logs
- Endpoint status → no EDR access

> These are escalated to L2. At L1, documenting what you *can't* find is just as important as what you *can*.

---

## ✅ Verdict

```
TRUE POSITIVE — PHISHING
Firewall blocked the connection. No breach confirmed.
Escalated to L2 for endpoint scan and user identification.
```

---

## 💡 Key Takeaways

1. **Blocked ≠ fully safe** — user may click it again elsewhere
2. **URL shorteners = always suspicious** — expand and check them
3. **HTTP on port 80** to unknown IPs is a red flag
4. **Document what you can't find** — that's valid L1 work
5. **When unsure → escalate.** Never guess.

---

## 🛠️ Tools Used
[VirusTotal](https://virustotal.com) • [AbuseIPDB](https://abuseipdb.com) • [URLScan.io](https://urlscan.io)

---

*If this helped you, drop a ⭐ — made by a beginner, for beginners* 🙌
