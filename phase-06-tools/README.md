[← Back to Dashboard](../README.md)

# 🔧 Phase 06 — Blue Team Tools

> **Timeline:** Weeks 8–14 · **Effort:** 2–3 hrs/day
> These are the tools you will use every day in a SOC. SIEM first, then expand.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 6.1 Splunk — Primary SIEM

| Type | Task |
|------|------|
| 📖 THEORY | What a SIEM does — collects logs, correlates events, generates alerts |
| 📖 THEORY | Splunk architecture — forwarders, indexers, search heads |
| 📖 THEORY | SPL (Search Processing Language) syntax basics |
| 🛠️ PRACTICAL | Install Splunk Free (500MB/day limit) on your VM |
| 🛠️ PRACTICAL | Ingest Windows Event Logs into Splunk |
| 🛠️ PRACTICAL | Find failed logins: `index=windows EventCode=4625` |
| 🛠️ PRACTICAL | Detect brute force with time bucketing using `bin _time span=5m` |
| 🛠️ PRACTICAL | Hunt for PowerShell: `EventCode=4688 New_Process_Name="*powershell*"` |
| 🛠️ PRACTICAL | Build a SOC monitoring dashboard with 3+ panels |
| 🛠️ PRACTICAL | Complete Splunk BOTS CTF at bots.splunk.com |

- [ ] Installed Splunk Free
- [ ] Can write basic SPL queries
- [ ] Built a custom dashboard
- [ ] Completed Splunk BOTS CTF

---

## 6.2 Microsoft Sentinel / KQL

| Type | Task |
|------|------|
| 📖 THEORY | What KQL (Kusto Query Language) is and how it differs from SPL |
| 📖 THEORY | Sentinel data tables — SigninLogs, DeviceProcessEvents, SecurityAlert |
| 🛠️ PRACTICAL | Complete KC7 KQL training game at kc7.dev — free |
| 🛠️ PRACTICAL | Query SigninLogs for failed sign-ins |
| 🛠️ PRACTICAL | Query DeviceProcessEvents for suspicious processes |

- [ ] Understand KQL syntax basics
- [ ] Completed KC7 KQL training
- [ ] Can write basic Sentinel queries

---

## 6.3 Wazuh — Open Source SIEM

| Type | Task |
|------|------|
| 📖 THEORY | Wazuh architecture — manager, agents, dashboard |
| 📖 THEORY | How Wazuh rules work |
| 🛠️ PRACTICAL | Install Wazuh manager (unlimited, 100% free) |
| 🛠️ PRACTICAL | Connect a Windows agent |
| 🛠️ PRACTICAL | Connect a Linux agent |
| 🛠️ PRACTICAL | Review built-in detection rules |
| 🛠️ PRACTICAL | Configure a custom alert threshold |

- [ ] Wazuh installed and running
- [ ] At least 2 agents connected
- [ ] Can read and modify Wazuh rules

---

## 6.4 Network Detection Tools

| Type | Tool | What It Does |
|------|------|-------------|
| 📖 THEORY | Wireshark | Deep packet analysis |
| 📖 THEORY | Suricata | High-performance IDS/IPS |
| 📖 THEORY | Zeek (Bro) | Network metadata and logs |
| 📖 THEORY | tcpdump | CLI packet capture |
| 📖 THEORY | Snort | Signature-based IDS |
| 🛠️ PRACTICAL | Wireshark — follow a TCP stream, identify C2 patterns |
| 🛠️ PRACTICAL | tcpdump — capture traffic from CLI, save to PCAP |
| 🛠️ PRACTICAL | Suricata — run against a PCAP file and review alerts |
| 🛠️ PRACTICAL | Analyze a malware PCAP from malware-traffic-analysis.net |

- [ ] Can capture and analyze traffic in Wireshark
- [ ] Used tcpdump to capture traffic from the command line
- [ ] Ran Suricata against a PCAP and found alerts

---

## 6.5 EDR Concepts 📖 THEORY

| Concept | Details |
|---------|---------|
| EDR vs Antivirus | AV = signature-based file scanning. EDR = behavioral monitoring + detection + response |
| XDR | Extends EDR to include network, cloud, and email data |
| CrowdStrike Falcon | Market leader — cloud-native, threat intelligence |
| Microsoft Defender for Endpoint | Most deployed — deep Windows integration |
| SentinelOne | AI-driven autonomous response |

- [ ] Can explain the difference between EDR and antivirus
- [ ] Know the 3 major EDR vendors and their strengths
- [ ] Understand what XDR adds to EDR

---

## 6.6 Detection Rules

| Type | Task |
|------|------|
| 📖 THEORY | What SIGMA rules are — vendor-agnostic detection format |
| 📖 THEORY | SIGMA rule structure — title, status, logsource, detection, condition |
| 📖 THEORY | What YARA rules are — malware pattern matching |
| 🛠️ PRACTICAL | Read 3 existing SIGMA rules on github.com/SigmaHQ/sigma |
| 🛠️ PRACTICAL | Convert a SIGMA rule to Splunk SPL using sigma-cli |
| 🛠️ PRACTICAL | Write a basic YARA rule to match a string pattern |

- [ ] Can read and explain a SIGMA rule
- [ ] Can convert SIGMA to SPL
- [ ] Written at least one YARA rule

---

## 6.7 Threat Intelligence Tools 🛠️ PRACTICAL

> All free to use. Practice with real IOCs.

- [ ] VirusTotal — submitted a file hash, IP, and domain
- [ ] AbuseIPDB — checked an IP reputation score
- [ ] URLScan.io — submitted a suspicious URL and read the report
- [ ] ANY.RUN — ran a suspicious file in the interactive sandbox
- [ ] Hybrid Analysis — submitted a file and reviewed behavioral analysis
- [ ] Shodan — searched for an IP and read the open ports/services

---

## 6.8 Forensics Tools

| Type | Tool | What It Does |
|------|------|-------------|
| 📖 THEORY | Volatility 3 | Memory forensics — analyze RAM dumps |
| 📖 THEORY | Autopsy | Disk forensics — analyze disk images |
| 📖 THEORY | FTK Imager | Create forensic disk images |
| 📖 THEORY | Chainsaw | Fast Windows Event Log hunting |
| 📖 THEORY | Eric Zimmerman's Tools | Parse Windows artifacts |
| 🛠️ PRACTICAL | Run Volatility on a memory dump from a CTF challenge |
| 🛠️ PRACTICAL | Use Chainsaw to hunt for suspicious Event IDs in an EVTX file |
| 🛠️ PRACTICAL | Use Autopsy to analyze a disk image |

- [ ] Run Volatility on at least one memory dump
- [ ] Used Chainsaw on a Windows event log file
- [ ] Familiar with Autopsy interface

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 🛠️ PRACTICAL | Splunk Free — splunk.com/download | Tool |
| 🛠️ PRACTICAL | Splunk BOTS CTF — bots.splunk.com | Free CTF |
| 🛠️ PRACTICAL | KC7 KQL Training — kc7.dev | Free game |
| 🛠️ PRACTICAL | Wazuh — wazuh.com | Free open-source SIEM |
| 🛠️ PRACTICAL | SigmaHQ — github.com/SigmaHQ/sigma | 3000+ detection rules |
| 🛠️ PRACTICAL | malware-traffic-analysis.net | PCAP exercises |
| 📖 THEORY | TryHackMe — Splunk, Wireshark, Zeek rooms | Browser labs |

---

## ✅ Phase 06 Completion Checklist

**📖 Theory Done**
- [ ] Know what a SIEM does and how Splunk is structured
- [ ] Know the difference between EDR and antivirus
- [ ] Understand SIGMA and YARA rules
- [ ] Know the major forensics tools and their purpose

**🛠️ Practical Done**
- [ ] Installed Splunk Free and ingested Windows logs
- [ ] Written basic Splunk SPL queries
- [ ] Completed Splunk BOTS CTF
- [ ] Written basic KQL queries and completed KC7
- [ ] Installed Wazuh with 2 connected agents
- [ ] Analyzed a malware PCAP in Wireshark
- [ ] Used all 5 threat intelligence tools
- [ ] Run Volatility on a memory dump

---

[← Phase 05 Security](../phase-05-security/README.md) · [Back to Dashboard](../README.md) · [Next → Phase 07 Certifications](../phase-07-certifications/README.md)
