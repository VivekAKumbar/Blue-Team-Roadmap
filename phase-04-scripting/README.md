[← Back to Dashboard](../README.md)

# 🐍 Phase 04 — Scripting & Automation

> **Timeline:** Weeks 5–8 · **Effort:** 2–3 hrs/day
> You don't need to be a developer. You need functional scripting — parse logs, call APIs, automate tasks.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 4.1 Python Core

| Type | Topic |
|------|-------|
| 📖 THEORY | Variables, data types, operators |
| 📖 THEORY | Control flow — if/else, for loops, while loops |
| 📖 THEORY | Functions and modules |
| 📖 THEORY | File I/O — reading/writing text, CSV, JSON |
| 📖 THEORY | Error handling — try/except |
| 📖 THEORY | Lists, dictionaries, sets |
| 🛠️ PRACTICAL | Write a script that reads a file line by line |
| 🛠️ PRACTICAL | Write a script that handles a missing file without crashing |
| 🛠️ PRACTICAL | Write a function that takes an IP and returns True/False if private |

- [ ] Understand all Python core concepts above
- [ ] Can write a working Python script from scratch
- [ ] Completed TryHackMe Python Basics room

---

## 4.2 Security-Relevant Python Libraries

| Type | Library | What It Does |
|------|---------|-------------|
| 📖 THEORY | `open()` | Read log files line by line |
| 📖 THEORY | `re` | Regex pattern matching in logs |
| 📖 THEORY | `requests` | Call APIs — VirusTotal, AbuseIPDB |
| 📖 THEORY | `json` | Parse structured API responses |
| 📖 THEORY | `csv` | Parse alert CSV exports |
| 📖 THEORY | `hashlib` | Calculate MD5/SHA256 for IOC checking |
| 🛠️ PRACTICAL | Use re to extract all IPs from a log file |
| 🛠️ PRACTICAL | Use requests to query the AbuseIPDB API |
| 🛠️ PRACTICAL | Use hashlib to calculate the MD5 of a file |

- [ ] Used all 6 libraries above in real scripts
- [ ] Can extract data from a log file using regex

---

## 4.3 Python Projects 🛠️ PRACTICAL

> Build each project below and save to GitHub as portfolio artifacts.

- [ ] **Log Parser** — reads auth.log, extracts and counts unique IPs with failed logins
- [ ] **IP Reputation Checker** — takes an IP, queries AbuseIPDB API, prints risk score
- [ ] **Hash Lookup Tool** — calculates MD5/SHA256 of a file, checks against VirusTotal
- [ ] **Phishing URL Analyzer** — extracts URLs from a text file, submits to URLScan.io
- [ ] **Port Scanner** — connects to common ports on a target IP, reports open/closed

---

## 4.4 Bash Scripting

| Type | Task |
|------|------|
| 📖 THEORY | Variables and conditionals in Bash |
| 📖 THEORY | Loops — for and while |
| 📖 THEORY | Reading arguments with $1, $2 |
| 🛠️ PRACTICAL | Write a script that monitors failed SSH logins and alerts if over threshold |
| 🛠️ PRACTICAL | Write a script that backs up a log file with a timestamp |
| 🛠️ PRACTICAL | Write a script that checks if a service is running and restarts if not |

- [ ] Can write a working Bash script with conditionals and loops
- [ ] Built 2 Bash automation scripts

---

## 4.5 PowerShell Scripting 🛠️ PRACTICAL

- [ ] Written a script to find suspicious process names from a list
- [ ] Written a script to query failed logon events and export to CSV
- [ ] Used `Where-Object` to filter results

---

## 4.6 SQL Basics

| Type | Task |
|------|------|
| 📖 THEORY | SELECT, WHERE, GROUP BY, HAVING, ORDER BY |
| 📖 THEORY | Aggregate functions — COUNT(), SUM(), AVG() |
| 📖 THEORY | JOINs — INNER, LEFT |
| 🛠️ PRACTICAL | Write a query to find IPs with more than 50 failed logins in 1 hour |
| 🛠️ PRACTICAL | Complete SQLBolt interactive lessons 1–12 |

- [ ] Understand SELECT, WHERE, GROUP BY
- [ ] Can write a SIEM-style query in SQL
- [ ] Completed SQLBolt lessons 1–12

---

## 4.7 Regular Expressions

| Type | Pattern | Matches |
|------|---------|---------|
| 📖 THEORY | `\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}` | IP addresses |
| 📖 THEORY | `[a-fA-F0-9]{32}` | MD5 hashes |
| 📖 THEORY | `[a-fA-F0-9]{64}` | SHA256 hashes |
| 📖 THEORY | `https?://[^\s]+` | URLs |
| 📖 THEORY | `[\w.-]+@[\w.-]+\.\w+` | Email addresses |
| 🛠️ PRACTICAL | Build each pattern above on regex101.com with a real log sample |
| 🛠️ PRACTICAL | Use re in Python to extract all IPs from auth.log |

- [ ] Can write regex patterns for IPs, hashes, URLs, emails
- [ ] Used regex101.com to test patterns against real log data

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 📖 THEORY | Automate the Boring Stuff with Python — automatetheboringstuff.com | Free book |
| 🛠️ PRACTICAL | TryHackMe Python Basics | Browser lab |
| 🛠️ PRACTICAL | SQLBolt — sqlbolt.com | Interactive SQL |
| 🛠️ PRACTICAL | regex101.com | Regex practice tool |
| 📖 THEORY | Bash Scripting Tutorial — linuxconfig.org | Guide |

---

## ✅ Phase 04 Completion Checklist

**📖 Theory Done**
- [ ] Understand all Python core concepts
- [ ] Know what each security library does
- [ ] Understand SQL SELECT, WHERE, GROUP BY
- [ ] Can read and write regex patterns

**🛠️ Practical Done**
- [ ] Built 5 Python security tools
- [ ] Written 2 Bash automation scripts
- [ ] Written 1 PowerShell investigation script
- [ ] Completed SQLBolt lessons 1–12
- [ ] Used regex101.com to build and test patterns

---

[← Phase 03 Linux](../phase-03-linux/README.md) · [Back to Dashboard](../README.md) · [Next → Phase 05 Security](../phase-05-security/README.md)
