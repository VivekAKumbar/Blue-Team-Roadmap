<div align="center">

<h1>🦈 Wireshark Labs</h1>
<h3>Vivek A Kumbar · Network Traffic Analysis · Blue Team</h3>

<i>Hands-on packet analysis practice — every lab documented.</i>

<br/>

<a href="https://github.com/VivekAKumbar/Blue-Team-Roadmap"><img src="https://img.shields.io/badge/Part_of-Blue_Team_Roadmap-1a365d?style=flat-square"/></a>
<a href="https://github.com/VivekAKumbar/Wireshark-Labs"><img src="https://img.shields.io/badge/Tool-Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white"/></a>
<a href="https://github.com/VivekAKumbar/Wireshark-Labs"><img src="https://img.shields.io/badge/Type-Practical_Labs-green?style=flat-square"/></a>

</div>

---

## 📌 What This Repo Is

This repo documents all my Wireshark packet analysis labs as part of my Blue Team learning journey. Each lab includes what I captured, what I found, and what it means from a security perspective.

---

## 🗂️ Lab Index

| # | Lab | Status | PCAP File |
|:-:|-----|:------:|-----------|
| 01 | [Basic Traffic Capture](#lab-01--basic-traffic-capture) | ⬜ Not Started | — |
| 02 | [HTTP Traffic Analysis](#lab-02--http-traffic-analysis) | ⬜ Not Started | — |
| 03 | [DNS Analysis](#lab-03--dns-analysis) | ⬜ Not Started | — |
| 04 | [TCP Three-Way Handshake](#lab-04--tcp-three-way-handshake) | ⬜ Not Started | — |
| 05 | [FTP Traffic Analysis](#lab-05--ftp-traffic-analysis) | ⬜ Not Started | — |
| 06 | [ICMP & Ping Analysis](#lab-06--icmp--ping-analysis) | ⬜ Not Started | — |
| 07 | [ARP Analysis](#lab-07--arp-analysis) | ⬜ Not Started | — |
| 08 | [Malware PCAP Analysis](#lab-08--malware-pcap-analysis) | ⬜ Not Started | — |
| 09 | [Port Scan Detection](#lab-09--port-scan-detection) | ⬜ Not Started | — |
| 10 | [C2 Traffic Detection](#lab-10--c2-traffic-detection) | ⬜ Not Started | — |

---

## Lab 01 — Basic Traffic Capture

> **Goal:** Capture live traffic and identify common protocols
> **Type:** 🛠️ PRACTICAL

- [ ] Opened Wireshark and selected network interface
- [ ] Started a live capture
- [ ] Identified at least 5 different protocols in the capture
- [ ] Applied display filter: `ip.addr == 192.168.1.1`
- [ ] Stopped capture and saved as .pcap file
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> *(what would an analyst look for in this traffic)*

---

## Lab 02 — HTTP Traffic Analysis

> **Goal:** Capture and analyze unencrypted HTTP traffic
> **Type:** 🛠️ PRACTICAL

- [ ] Generated HTTP traffic by visiting an HTTP site
- [ ] Applied display filter: `http`
- [ ] Found GET and POST requests
- [ ] Followed a TCP stream and read the full HTTP conversation
- [ ] Identified any credentials or sensitive data in plain text
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> HTTP sends data in plain text — credentials can be stolen with a MITM attack

---

## Lab 03 — DNS Analysis

> **Goal:** Analyze DNS queries and responses
> **Type:** 🛠️ PRACTICAL

- [ ] Applied display filter: `dns`
- [ ] Identified DNS query and response packets
- [ ] Found which domains were resolved
- [ ] Checked for unusually long subdomain names (DNS tunneling indicator)
- [ ] Checked for high volume of DNS queries to one domain
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> DNS tunneling hides data exfiltration inside DNS queries — long subdomains are the giveaway

---

## Lab 04 — TCP Three-Way Handshake

> **Goal:** Identify and understand the TCP connection process
> **Type:** 🛠️ PRACTICAL

- [ ] Applied display filter: `tcp`
- [ ] Found a SYN packet
- [ ] Found the matching SYN-ACK packet
- [ ] Found the final ACK packet
- [ ] Followed the full TCP stream
- [ ] Identified what application data followed the handshake
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> SYN flood attacks send thousands of SYN packets without completing the handshake — causes DoS

---

## Lab 05 — FTP Traffic Analysis

> **Goal:** Capture FTP traffic and find credentials in plain text
> **Type:** 🛠️ PRACTICAL

- [ ] Set up an FTP connection in a lab environment
- [ ] Applied display filter: `ftp`
- [ ] Found the USER and PASS commands in plain text
- [ ] Followed the TCP stream to see full FTP session
- [ ] Identified files transferred
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> FTP sends credentials in plain text — always use SFTP instead

---

## Lab 06 — ICMP & Ping Analysis

> **Goal:** Analyze ICMP traffic and detect ping sweeps
> **Type:** 🛠️ PRACTICAL

- [ ] Applied display filter: `icmp`
- [ ] Identified Echo Request and Echo Reply packets
- [ ] Generated a ping sweep in lab environment
- [ ] Identified the ping sweep pattern in Wireshark
- [ ] Counted how many hosts responded
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> Attackers use ping sweeps to discover live hosts on a network before launching attacks

---

## Lab 07 — ARP Analysis

> **Goal:** Understand ARP and detect ARP spoofing
> **Type:** 🛠️ PRACTICAL

- [ ] Applied display filter: `arp`
- [ ] Identified ARP request and reply packets
- [ ] Found which MAC address corresponds to which IP
- [ ] Identified duplicate IP-to-MAC mappings (ARP spoofing indicator)
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> ARP spoofing lets an attacker redirect traffic through their machine — classic MITM attack

---

## Lab 08 — Malware PCAP Analysis

> **Goal:** Analyze a real malware traffic sample from malware-traffic-analysis.net
> **Type:** 🛠️ PRACTICAL

- [ ] Downloaded a PCAP from malware-traffic-analysis.net
- [ ] Identified suspicious IP addresses in the traffic
- [ ] Found the initial infection vector
- [ ] Identified C2 communication
- [ ] Extracted IOCs: IPs, domains, file hashes
- [ ] Mapped findings to MITRE ATT&CK techniques
- [ ] Uploaded analysis notes to this repo

**What I found:**
> *(write your findings here)*

**IOCs extracted:**
| Type | Value |
|------|-------|
| IP | — |
| Domain | — |
| Hash | — |

**MITRE ATT&CK mapping:**
| Technique ID | Technique Name |
|-------------|---------------|
| — | — |

---

## Lab 09 — Port Scan Detection

> **Goal:** Identify a port scan in a packet capture
> **Type:** 🛠️ PRACTICAL

- [ ] Generated a port scan in lab environment using nmap
- [ ] Applied display filter: `tcp.flags.syn == 1 and tcp.flags.ack == 0`
- [ ] Identified the scanning IP address
- [ ] Counted how many ports were scanned
- [ ] Identified which ports were open (received SYN-ACK)
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> Port scans are reconnaissance — attackers scan before attacking to find open services

---

## Lab 10 — C2 Traffic Detection

> **Goal:** Identify Command and Control traffic patterns
> **Type:** 🛠️ PRACTICAL

- [ ] Downloaded a C2 PCAP sample
- [ ] Identified beaconing behavior — regular intervals of outbound traffic
- [ ] Found unusual ports used for communication
- [ ] Identified encrypted traffic to unknown external IPs
- [ ] Checked user agent strings for anomalies
- [ ] Uploaded PCAP to this repo

**What I found:**
> *(write your findings here)*

**Security relevance:**
> C2 beaconing is how malware phones home — regular intervals and unusual destinations are red flags

---

## 📚 Resources Used

| Resource | Link |
|----------|------|
| Malware Traffic Analysis PCAPs | malware-traffic-analysis.net |
| Wireshark Display Filter Reference | wireshark.org/docs/dfref |
| TryHackMe Wireshark Room | tryhackme.com |

---

## 🔗 Part of My Blue Team Roadmap

This repo is part of my full Blue Team learning journey.

👉 [Blue-Team-Roadmap](https://github.com/VivekAKumbar/Blue-Team-Roadmap)

---

<div align="center">

<a href="https://github.com/VivekAKumbar"><img src="https://img.shields.io/badge/GitHub-VivekAKumbar-181717?style=flat-square&logo=github"/></a>
<a href="https://tryhackme.com/p/VivekAKumbar"><img src="https://img.shields.io/badge/TryHackMe-VivekAKumbar-red?style=flat-square&logo=tryhackme&logoColor=white"/></a>

</div>
