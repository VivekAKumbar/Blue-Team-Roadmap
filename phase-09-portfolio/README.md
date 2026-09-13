[← Back to Dashboard](../README.md)

# 📁 Phase 09 — Build Your Portfolio

> **Timeline:** Months 5–9
> Certifications prove knowledge. Projects prove you can do the work.

**Legend:**
> 📖 `THEORY` — Planning and research
> 🛠️ `PRACTICAL` — Build, document, and publish

---

## 9.1 Home Lab Setup 🛠️ PRACTICAL

> Build a lab that mirrors a real enterprise environment.

**Infrastructure**
- [ ] Hypervisor installed — Proxmox (recommended) or VirtualBox (free)
- [ ] Windows Server 2022 VM deployed
- [ ] Active Directory configured on Windows Server
- [ ] Windows 10/11 VM joined to the domain
- [ ] Ubuntu Server VM deployed
- [ ] Sysmon installed on all Windows VMs with SwiftOnSecurity config
- [ ] pfSense firewall deployed (optional but impressive)

**Security Stack**
- [ ] Wazuh SIEM deployed and collecting logs from all VMs
- [ ] Sysmon logs flowing into Wazuh
- [ ] Security Onion deployed for network monitoring
- [ ] TheHive deployed for case management (optional)

**Documentation**
- [ ] Network topology diagram drawn and saved
- [ ] Lab setup guide written as a GitHub README
- [ ] Architecture published in the portfolio repo

---

## 9.2 Project 1 — SIEM Deployment + Dashboards 🛠️ PRACTICAL

> **Goal:** Show you can deploy, configure, and use a SIEM.

- [ ] Wazuh or Splunk deployed
- [ ] Windows Event Logs ingested
- [ ] Sysmon logs ingested
- [ ] Linux auth logs ingested
- [ ] Dashboard built: failed logins panel
- [ ] Dashboard built: suspicious process creation panel
- [ ] Dashboard built: network anomaly panel
- [ ] Full setup documented with screenshots
- [ ] Architecture diagram included
- [ ] Published to GitHub

---

## 9.3 Project 2 — Adversary Emulation with Atomic Red Team 🛠️ PRACTICAL

> **Goal:** Prove you can test detections against real attack techniques.

- [ ] Atomic Red Team installed on a test Windows VM
- [ ] 10+ MITRE ATT&CK techniques executed
- [ ] Verified SIEM detection for each technique
- [ ] Written custom detection rules where SIEM missed
- [ ] Report written: technique → expected alert → actual result → fix
- [ ] ATT&CK technique IDs included for each test
- [ ] Published to GitHub

---

## 9.4 Project 3 — Phishing Analysis Pipeline 🛠️ PRACTICAL

> **Goal:** Document a full phishing investigation workflow.

- [ ] Collected a real phishing email sample
- [ ] Analyzed email headers manually
- [ ] Extracted URLs without clicking — used URLScan.io
- [ ] Submitted attachment to ANY.RUN sandbox
- [ ] Extracted IOCs: sender IP, domain, URL, file hash
- [ ] Python script written to automate IOC extraction
- [ ] Full workflow documented step by step
- [ ] Published to GitHub

---

## 9.5 Project 4 — IR Reports from CTF Challenges 🛠️ PRACTICAL

> **Goal:** Demonstrate professional incident documentation.

Each IR report must include:
- Executive Summary (1 paragraph)
- Timeline of events
- IOC table (IPs, domains, hashes, filenames)
- MITRE ATT&CK technique mapping
- Remediation recommendations

- [ ] IR Report 1 written and published
- [ ] IR Report 2 written and published
- [ ] IR Report 3 written and published
- [ ] IR Report 4 written and published
- [ ] IR Report 5 written and published

---

## 9.6 Project 5 — APT Threat Intelligence Brief 🛠️ PRACTICAL

> **Goal:** Show you can research and document a real threat actor.

- [ ] APT group selected (e.g. APT29, Lazarus Group, FIN7)
- [ ] Researched using MITRE ATT&CK, threat reports, OSINT
- [ ] Brief written: group overview, TTPs, IOCs, detection recommendations
- [ ] All techniques mapped to MITRE ATT&CK IDs
- [ ] SIEM detection rules written for their top 3 techniques
- [ ] Published to GitHub

---

## 9.7 Project 6 — CyderSec 🛠️ PRACTICAL

> **Goal:** Document CyderSec as a portfolio project.

- [ ] CyderSec repo created on GitHub
- [ ] All completed modules uploaded
- [ ] README written explaining the project purpose
- [ ] Linked from the main portfolio and profile README

---

## 9.8 Publishing 🛠️ PRACTICAL

| Platform | Task |
|----------|------|
| GitHub | All 6 projects in dedicated repos with full READMEs |
| GitHub | Profile README updated with all projects |
| LinkedIn | Projects section updated with descriptions |
| Blog/Medium | At least 5 writeups
