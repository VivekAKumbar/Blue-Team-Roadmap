[← Back to Dashboard](../README.md)

# 🖥️ Phase 02 — Windows Essentials

> **Timeline:** Weeks 3–6 · **Effort:** 2–3 hrs/day
> 90%+ of enterprise environments run Windows with Active Directory. Windows Event Logs are your primary SOC data source.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 2.1 Active Directory

| Type | Task |
|------|------|
| 📖 THEORY | Domains, forests, and trusts — hierarchical AD structure |
| 📖 THEORY | Users, groups, and OUs — how access is organized |
| 📖 THEORY | Group Policy Objects (GPO) — how settings are enforced across machines |
| 📖 THEORY | Kerberos authentication — TGT, TGS, service tickets |
| 📖 THEORY | NTLM — legacy protocol, pass-the-hash attacks |
| 📖 THEORY | Domain Controllers — most critical servers in the enterprise |
| 🛠️ PRACTICAL | Set up a Windows Server VM with Active Directory (TryHackMe lab) |
| 🛠️ PRACTICAL | Create users, groups, and OUs in AD |
| 🛠️ PRACTICAL | Apply a Group Policy Object and verify it works |

- [ ] Understand AD structure — domains, forests, trusts
- [ ] Can explain Kerberos authentication flow step by step
- [ ] Know why NTLM is a security risk
- [ ] Know what a Domain Controller is and why attackers target it

---

## 2.2 Windows Event IDs

| Type | Event ID | Log | Meaning | Security Relevance |
|------|----------|-----|---------|-------------------|
| 📖 THEORY | 4624 | Security | Successful logon | Track who accessed what |
| 📖 THEORY | 4625 | Security | Failed logon | Brute force detection |
| 📖 THEORY | 4648 | Security | Explicit credential logon | Lateral movement |
| 📖 THEORY | 4672 | Security | Special privileges assigned | Admin access granted |
| 📖 THEORY | 4688 | Security | New process created | Malware execution |
| 📖 THEORY | 4720 | Security | User account created | Persistence technique |
| 📖 THEORY | 4728 | Security | Added to security group | Privilege escalation |
| 📖 THEORY | 1102 | Security | Audit log cleared | Almost always malicious |
| 📖 THEORY | 7045 | System | New service installed | Malware persistence |
| 📖 THEORY | 4104 | PowerShell | Script block logging | Malicious PS detection |
| 📖 THEORY | 1 | Sysmon | Process creation | Detailed process tracking |
| 📖 THEORY | 3 | Sysmon | Network connection | C2 communication |
| 📖 THEORY | 11 | Sysmon | File creation | Malware delivery |
| 📖 THEORY | 22 | Sysmon | DNS query | DNS-based C2, DGA |
| 🛠️ PRACTICAL | Find Event ID 4625 in TryHackMe Windows Event Logs room |
| 🛠️ PRACTICAL | Identify a brute force pattern from a sequence of Event IDs |
| 🛠️ PRACTICAL | Spot a privilege escalation from Event ID 4728 in logs |

- [ ] Memorized all Event IDs above
- [ ] Can identify attack patterns from Event ID sequences
- [ ] Completed TryHackMe Windows Event Logs room

---

## 2.3 PowerShell for Investigation 🛠️ PRACTICAL

> Run all commands below in a Windows VM — theory alone is not enough.

- [ ] `Get-WinEvent -FilterHashtable @{LogName='Security'; Id=4625}` — find failed logons
- [ ] `Get-Process | Sort-Object CPU -Descending` — find top CPU processes
- [ ] `Get-NetTCPConnection | Where-Object {$_.State -eq "Established"}` — active connections
- [ ] `Get-ScheduledTask | Where-Object {$_.State -ne "Disabled"}` — find scheduled tasks
- [ ] `Get-ChildItem -Path C:\ -Recurse -File` — find recently modified files
- [ ] `Get-CimInstance Win32_StartupCommand` — check startup programs
- [ ] Exported findings to a CSV file with `Export-Csv`

---

## 2.4 Sysmon 🛠️ PRACTICAL

> **Tool:** Sysmon — free from Microsoft Sysinternals

- [ ] Downloaded Sysmon from Microsoft Sysinternals
- [ ] Installed with SwiftOnSecurity config
- [ ] Verified Sysmon is running as a Windows service
- [ ] Viewed Sysmon logs in Event Viewer
- [ ] Triggered a process creation (Event ID 1) and found it in logs
- [ ] Triggered a network connection (Event ID 3) and found it in logs
- [ ] Completed TryHackMe Sysmon room

---

## 2.5 Persistence Locations

| Type | Location | Why Attackers Use It |
|------|----------|---------------------|
| 📖 THEORY | Registry Run Keys — HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run | Runs on every startup |
| 📖 THEORY | Services — services.msc | Malware installs as a service |
| 📖 THEORY | Scheduled Tasks | Automates malware execution |
| 📖 THEORY | WMI Subscriptions | Advanced, hard to detect |
| 🛠️ PRACTICAL | Check registry run keys on a Windows VM |
| 🛠️ PRACTICAL | List all running services and flag suspicious ones |
| 🛠️ PRACTICAL | View all scheduled tasks and check for anomalies |

- [ ] Know all 4 common persistence locations
- [ ] Can check each location manually on a Windows system

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 📖 THEORY | 13Cubed — Windows Forensics | YouTube |
| 🛠️ PRACTICAL | TryHackMe Windows Fundamentals 1, 2, 3 | Browser labs |
| 🛠️ PRACTICAL | TryHackMe Active Directory Basics | Browser lab |
| 🛠️ PRACTICAL | TryHackMe Windows Event Logs | Browser lab |
| 🛠️ PRACTICAL | TryHackMe Sysmon | Browser lab |

---

## ✅ Phase 02 Completion Checklist

**📖 Theory Done**
- [ ] Understand Active Directory structure
- [ ] Can explain Kerberos authentication flow
- [ ] Memorized all critical Windows Event IDs
- [ ] Know all common persistence locations
- [ ] Know what Sysmon is and its key Event IDs

**🛠️ Practical Done**
- [ ] Can read Event Log sequences and identify attack patterns
- [ ] Ran PowerShell investigation commands in a Windows VM
- [ ] Installed and configured Sysmon
- [ ] Checked all persistence locations on a live system
- [ ] Completed TryHackMe Windows rooms

---

[← Phase 01 Networking](../phase-01-networking/README.md) · [Back to Dashboard](../README.md) · [Next → Phase 03 Linux](../phase-03-linux/README.md)
