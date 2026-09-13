[← Back to Dashboard](../README.md)

# 🔒 Phase 05 — Security Fundamentals

> **Timeline:** Weeks 6–10 · **Effort:** 2–3 hrs/day
> Core concepts that appear in every certification, every interview, and every day on the SOC floor.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 5.1 Core Security Principles 📖 THEORY

| Principle | Definition | Attack Example |
|-----------|-----------|---------------|
| Confidentiality | Only authorized users can access data | Data breach, unauthorized access |
| Integrity | Data hasn't been tampered with | Man-in-the-middle, data modification |
| Availability | Systems accessible when needed | DDoS, ransomware |
| Authentication | Proving who you are | Credential theft, brute force |
| Authorization | What you're allowed to do | Privilege escalation |
| Least Privilege | Minimum access needed | Insider threat, over-privileged accounts |
| Defense in Depth | Multiple security layers | Bypassing one control still leaves others |
| Zero Trust | Never trust, always verify | Lateral movement prevention |

- [ ] Can explain CIA Triad with real-world examples
- [ ] Know the difference between Authentication and Authorization
- [ ] Can explain Zero Trust in plain English

---

## 5.2 Common Attack Types

| Type | Attack | How It Works | Detection Method |
|------|--------|-------------|-----------------|
| 📖 THEORY | Phishing | Fraudulent emails trick users | Email gateway logs, header analysis |
| 📖 THEORY | Brute Force | Automated password guessing | Multiple 4625 events, lockouts |
| 📖 THEORY | Credential Stuffing | Using leaked credentials | Many accounts, single source IP |
| 📖 THEORY | Ransomware | Encrypts files, demands payment | Mass file modifications, suspicious process |
| 📖 THEORY | SQL Injection | SQL commands in web forms | WAF alerts, unusual DB queries |
| 📖 THEORY | Man-in-the-Middle | Intercepting communications | Certificate warnings, ARP anomalies |
| 📖 THEORY | Lateral Movement | Moving between systems | Unusual logon patterns, PsExec |
| 📖 THEORY | Privilege Escalation | Gaining higher access | 4672, 4728 on unexpected accounts |
| 📖 THEORY | Data Exfiltration | Stealing data outbound | Unusual traffic, DNS tunneling |
| 📖 THEORY | Supply Chain Attack | Compromising trusted software | Unexpected network connections |
| 🛠️ PRACTICAL | Identify attack type from a SIEM alert description |
| 🛠️ PRACTICAL | Map a given attack to its detection method |

- [ ] Can name and explain all 10 attack types above
- [ ] Know the detection method for each attack

---

## 5.3 Cyber Kill Chain 📖 THEORY

> Framework by Lockheed Martin. Maps the stages of every attack.

| Stage | What the Attacker Does |
|-------|----------------------|
| 1. Reconnaissance | Gathering information about the target |
| 2. Weaponization | Building the attack payload |
| 3. Delivery | Sending the payload (phishing email, drive-by) |
| 4. Exploitation | Triggering the vulnerability |
| 5. Installation | Installing malware or backdoor |
| 6. Command & Control | Communicating with the implant |
| 7. Actions on Objectives | Data theft, destruction, ransomware |

- [ ] Memorized all 7 Kill Chain stages in order
- [ ] Can map a real attack scenario to Kill Chain stages
- [ ] Understand how defenders can break the Kill Chain at each stage

---

## 5.4 MITRE ATT&CK Framework

| Type | Task |
|------|------|
| 📖 THEORY | Understand the 14 tactics and what each means |
| 📖 THEORY | Understand the difference between tactics and techniques |
| 📖 THEORY | Know how sub-techniques work (T1059.001 = PowerShell) |
| 🛠️ PRACTICAL | Navigate attack.mitre.org and find a technique by name |
| 🛠️ PRACTICAL | Look up T1566.001 (Spearphishing Attachment) and read its detections |
| 🛠️ PRACTICAL | Map a phishing attack to the correct ATT&CK techniques |
| 🛠️ PRACTICAL | Find detection gaps for 3 techniques using ATT&CK |

**The 14 Tactics:**
- [ ] Reconnaissance
- [ ] Resource Development
- [ ] Initial Access
- [ ] Execution
- [ ] Persistence
- [ ] Privilege Escalation
- [ ] Defense Evasion
- [ ] Credential Access
- [ ] Discovery
- [ ] Lateral Movement
- [ ] Collection
- [ ] Command and Control
- [ ] Exfiltration
- [ ] Impact

---

## 5.5 Security Frameworks 📖 THEORY

| Framework | Purpose | Key Points |
|-----------|---------|-----------|
| NIST CSF 2.0 | Big-picture security strategy | 5 functions: Identify, Protect, Detect, Respond, Recover |
| NIST SP 800-61 | Incident Response guide | 4 phases: Preparation, Detection, Containment/Eradication/Recovery, Post-Incident |
| CIS Controls v8.1 | Prioritized security actions | 18 controls ordered by priority |
| ISO 27001 | ISMS international standard | Important for GRC roles |

- [ ] Can name the 5 NIST CSF 2.0 functions
- [ ] Can name the 4 NIST SP 800-61 IR phases
- [ ] Know what CIS Controls are and why they are prioritized

---

## 5.6 Incident Response Process

| Type | Phase | What You Do |
|------|-------|------------|
| 📖 THEORY | Preparation | Build IR plans, deploy tools, train the team |
| 📖 THEORY | Detection & Analysis | Monitor alerts, validate true/false positives, classify severity |
| 📖 THEORY | Containment | Isolate affected systems to stop the spread |
| 📖 THEORY | Eradication | Remove the threat — malware, backdoors, compromised accounts |
| 📖 THEORY | Recovery | Restore from clean backups, verify integrity |
| 📖 THEORY | Post-Incident | Write report, lessons learned, update detection rules |
| 🛠️ PRACTICAL | Apply IR phases to a TryHackMe scenario |
| 🛠️ PRACTICAL | Write a mini IR report for a lab exercise |

- [ ] Can explain each IR phase with a real example
- [ ] Know the difference between true positive, false positive, true negative, false negative
- [ ] Applied the IR process to a TryHackMe scenario

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 📖 THEORY | Professor Messer Security+ SY0-701 | 177-episode free YouTube course |
| 🛠️ PRACTICAL | TryHackMe SOC Level 1 Path | Browser learning path |
| 📖 THEORY | attack.mitre.org | Framework reference |
| 📖 THEORY | nist.gov/cyberframework | NIST CSF 2.0 |
| 📖 THEORY | cisecurity.org/controls | CIS Controls |

---

## ✅ Phase 05 Completion Checklist

**📖 Theory Done**
- [ ] CIA Triad explained with real-world examples
- [ ] Know all 10 common attack types and detection methods
- [ ] Memorized all 7 Cyber Kill Chain stages
- [ ] Know all 14 MITRE ATT&CK tactics
- [ ] Know the 5 NIST CSF functions and 4 IR phases

**🛠️ Practical Done**
- [ ] Navigated MITRE ATT&CK and mapped techniques to detections
- [ ] Applied IR phases to a TryHackMe scenario
- [ ] Identified attack type from SIEM alert descriptions
- [ ] Completed TryHackMe SOC Level 1 Path (50%+)

---

[← Phase 04 Scripting](../phase-04-scripting/README.md) · [Back to Dashboard](../README.md) · [Next → Phase 06 Tools](../phase-06-tools/README.md)
