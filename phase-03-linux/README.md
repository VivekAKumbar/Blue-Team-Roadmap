[← Back to Dashboard](../README.md)

# 🐧 Phase 03 — Linux Command Line

> **Timeline:** Weeks 4–7 · **Effort:** 2 hrs/day
> Most security tools and servers run Linux. You need terminal fluency.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 3.1 Navigation & File Operations

| Type | Command | What It Does |
|------|---------|-------------|
| 📖 THEORY | `pwd` | Print current directory |
| 📖 THEORY | `ls -la` | List all files with details |
| 📖 THEORY | `cd /var/log` | Change directory |
| 📖 THEORY | `find / -name "*.log"` | Find files by name |
| 📖 THEORY | `chmod 755 file` | Change file permissions |
| 📖 THEORY | `chown user:group file` | Change file ownership |
| 📖 THEORY | rwx permission system and octal notation | Read/Write/Execute |
| 🛠️ PRACTICAL | Navigate the full filesystem in your Kali VM |
| 🛠️ PRACTICAL | Find all .log files in /var/log |
| 🛠️ PRACTICAL | Change permissions on a file and verify with ls -la |

- [ ] Can navigate the Linux filesystem without looking up commands
- [ ] Understand rwx permissions and octal notation (755, 644, etc.)
- [ ] Can find any file using find and locate

---

## 3.2 Text Processing — Used Daily in Log Analysis

| Type | Command | What It Does |
|------|---------|-------------|
| 📖 THEORY | `grep "error" logfile.txt` | Search for pattern in file |
| 📖 THEORY | `grep -i "failed" auth.log` | Case-insensitive search |
| 📖 THEORY | `grep -r "password" /etc/` | Recursive search |
| 📖 THEORY | `grep -c "404" access.log` | Count matches |
| 📖 THEORY | `awk '{print $1, $4}' access.log` | Extract specific fields |
| 📖 THEORY | `sed 's/old/new/g' file.txt` | Find and replace |
| 📖 THEORY | `sort \| uniq -c \| sort -rn` | Count unique occurrences |
| 📖 THEORY | `wc -l logfile.txt` | Count lines in file |
| 📖 THEORY | `cut -d',' -f1,3 data.csv` | Extract CSV fields |
| 🛠️ PRACTICAL | Count failed SSH logins from /var/log/auth.log |
| 🛠️ PRACTICAL | Extract top 10 IPs from an access log using awk + sort + uniq |
| 🛠️ PRACTICAL | Use sed to anonymize IPs in a log file |

- [ ] Can use grep with -i, -r, -c flags confidently
- [ ] Can extract fields from logs using awk
- [ ] Can chain commands with pipes to answer investigation questions

---

## 3.3 System & Process Investigation 🛠️ PRACTICAL

> Run all commands below in your Kali Linux VM.

- [ ] `ps aux` — listed all running processes
- [ ] `ps aux | grep suspicious` — searched for a specific process
- [ ] `top` and `htop` — monitored processes in real-time
- [ ] `netstat -tulnp` — found all listening ports
- [ ] `ss -tulnp` — modern replacement for netstat
- [ ] `who` and `w` — checked who is logged in
- [ ] `last` — reviewed login history
- [ ] `df -h` and `free -h` — checked disk and memory usage
- [ ] `uname -a` — checked system information

---

## 3.4 Key Log Locations 📖 THEORY

> Memorize these. Every Blue Team investigation starts here.

| Location | What It Contains |
|----------|-----------------|
| `/var/log/` | All system and application logs |
| `/var/log/auth.log` | SSH logins, sudo usage, authentication |
| `/var/log/syslog` | General system messages |
| `/var/log/kern.log` | Kernel messages |
| `/etc/passwd` | User accounts |
| `/etc/shadow` | Password hashes |
| `/etc/crontab` | Scheduled tasks |
| `/tmp/` | Temporary files — malware often lands here |
| `/proc/` | Virtual filesystem with live process info |

- [ ] Memorized all log locations above
- [ ] Can use `tail -f /var/log/auth.log` to monitor logins in real-time
- [ ] Know why /tmp/ is a high-risk directory

---

## 3.5 Bash Pipelines 🛠️ PRACTICAL

> Build and run each pipeline below in your terminal.

- [ ] Count failed SSH login attempts:
  `cat /var/log/auth.log | grep "Failed" | wc -l`
- [ ] Find top 10 source IPs in an access log:
  `cat access.log | awk '{print $1}' | sort | uniq -c | sort -rn | head -10`
- [ ] Find files larger than 100MB:
  `find / -type f -size +100M 2>/dev/null`
- [ ] Monitor live log for errors in real-time:
  `tail -f /var/log/syslog | grep --color "error\|warning\|critical"`

---

## 3.6 OverTheWire Bandit 🛠️ PRACTICAL

> Free wargame at overthewire.org/wargames/bandit
> Each level teaches a real Linux skill through a puzzle.

- [ ] Level 0 — SSH into a remote machine
- [ ] Level 1 — Read a file named with a dash
- [ ] Level 2 — Read a file with spaces in the name
- [ ] Level 3 — Find a hidden file
- [ ] Level 4 — Find the only human-readable file
- [ ] Level 5 — Find a file by size and permissions
- [ ] Level 6 — Find a file owned by a specific user
- [ ] Level 7 — Search inside a large file with grep
- [ ] Level 8 — Find the unique line in a file
- [ ] Level 9 — Find human-readable strings in a binary
- [ ] Level 10 — Decode base64
- [ ] Level 11 — Decode ROT13
- [ ] Level 12 — Decompress a multi-compressed file
- [ ] Level 13 — Use an SSH private key
- [ ] Level 14 — Connect to a port with netcat
- [ ] Level 15 — Connect with SSL/TLS

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 🛠️ PRACTICAL | OverTheWire Bandit — overthewire.org | Wargame 34 levels |
| 🛠️ PRACTICAL | TryHackMe Linux Fundamentals 1, 2, 3 | Browser labs |
| 🛠️ PRACTICAL | LetsDefend — Linux for Blue Team | Course |
| 📖 THEORY | explainshell.com | Command explainer |
| 📖 THEORY | The Linux Command Line — linuxcommand.org | Free PDF book |

---

## ✅ Phase 03 Completion Checklist

**📖 Theory Done**
- [ ] Memorized all key log file locations
- [ ] Understand file permissions and octal notation
- [ ] Know what each text processing command does
- [ ] Know why /tmp/ is a high-risk directory

**🛠️ Practical Done**
- [ ] Navigate the Linux filesystem without notes
- [ ] Used grep, awk, sed for log analysis
- [ ] Built 4 bash pipelines for investigation tasks
- [ ] Monitored processes and network connections live
- [ ] Completed OverTheWire Bandit levels 0–15
- [ ] Completed TryHackMe Linux Fundamentals rooms

---

[← Phase 02 Windows](../phase-02-windows/README.md) · [Back to Dashboard](../README.md) · [Next → Phase 04 Scripting](../phase-04-scripting/README.md)
