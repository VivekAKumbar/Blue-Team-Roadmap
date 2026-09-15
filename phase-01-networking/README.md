[← Back to Dashboard](../README.md)

# 🌐 Phase 01 — Networking Fundamentals

> **Timeline:** Weeks 1–4 · **Effort:** 2–3 hrs/day
> Every security alert involves network traffic. You cannot investigate threats without understanding how data moves.

**Legend:**
> 📖 `THEORY` — Concept to understand and memorize
> 🛠️ `PRACTICAL` — Hands-on skill to build and practice

---

## 1.1 OSI Model & TCP/IP Stack

| Type | Task |
|------|------|
| 📖 THEORY | The 7-layer OSI model and how it maps to the 4-layer TCP/IP model |
| 📖 THEORY | What happens at each layer — Physical, Data Link, Network, Transport, Session, Presentation, Application |
| 📖 THEORY | How encapsulation works — data → segment → packet → frame → bits |
| 📖 THEORY | Which layer an attack targets and why it matters for detection |

- [x] OSI model memorized — can name all 7 layers in order
- [ ] Can explain what happens at each layer in plain English
- [ ] Can map TCP/IP layers to OSI layers

---

## 1.2 IP Addressing & Subnetting

| Type | Task |
|------|------|
| 📖 THEORY | IPv4 address structure — 32-bit, dotted decimal notation |
| 📖 THEORY | Private vs public IP ranges — 10.x.x.x, 172.16–31.x.x, 192.168.x.x |
| 📖 THEORY | CIDR notation — /24, /16, /8 and what they mean |
| 📖 THEORY | NAT (Network Address Translation) and why it exists |
| 📖 THEORY | IPv6 basics — 128-bit, hexadecimal notation |
| 🛠️ PRACTICAL | Calculate subnet ranges manually on subnettingpractice.com |
| 🛠️ PRACTICAL | Given an IP + subnet mask, identify network address, broadcast, and host range |
| 🛠️ PRACTICAL | Configure static IPs on devices in Cisco Packet Tracer |

- [ ] Know all private IP ranges from memory
- [ ] Can subnet an IP without a calculator
- [ ] Can identify if an IP is private or public instantly
- [ ] Completed 20+ subnetting drills on subnettingpractice.com

---

## 1.3 Critical Protocols & Ports

| Type | Protocol | Port | Security Relevance |
|------|----------|------|--------------------|
| 📖 THEORY | DNS | 53 | DNS tunneling, DGA detection |
| 📖 THEORY | HTTP | 80 | Credential theft, malware delivery |
| 📖 THEORY | HTTPS | 443 | C2 hiding in TLS |
| 📖 THEORY | SSH | 22 | Brute force, unauthorized access |
| 📖 THEORY | RDP | 3389 | #1 ransomware entry vector |
| 📖 THEORY | SMTP | 25 | Phishing, spoofing |
| 📖 THEORY | FTP | 20/21 | Credential sniffing, exfiltration |
| 📖 THEORY | SMB | 445 | EternalBlue, lateral movement |
| 📖 THEORY | LDAP | 389/636 | Active Directory attacks |
| 📖 THEORY | Kerberos | 88 | Kerberoasting, Golden Ticket |
| 📖 THEORY | Syslog | 514 | Log analysis, SIEM ingestion |
| 🛠️ PRACTICAL | Simulate HTTP, FTP, DNS traffic in Cisco Packet Tracer |
| 🛠️ PRACTICAL | Identify protocols visually by port and color in Wireshark |

- [ ] Memorized all protocols and ports above
- [ ] Can state the security risk of each protocol from memory

---

## 1.4 Network Devices & Architecture

| Type | Task |
|------|------|
| 📖 THEORY | Routers — Layer 3, forward traffic between networks |
| 📖 THEORY | Switches — Layer 2, forward traffic within a network |
| 📖 THEORY | Firewalls — stateful vs stateless packet filtering |
| 📖 THEORY | Proxies — forward vs reverse |
| 📖 THEORY | IDS vs IPS — detect vs prevent |
| 📖 THEORY | VLANs — logical network segmentation |
| 📖 THEORY | DMZ — demilitarized zone for public-facing services |
| 🛠️ PRACTICAL | Build a router + switch + PC topology in Packet Tracer |
| 🛠️ PRACTICAL | Configure VLANs and verify traffic separation |
| 🛠️ PRACTICAL | Add a firewall and DMZ zone to your topology |

- [ ] Can explain the role of each device in a SOC context
- [ ] Know the difference between IDS and IPS
- [ ] Built at least one topology with router, switch, firewall, and VLAN

---

## 1.5 Cisco Packet Tracer Labs 🛠️ PRACTICAL

> **Tool:** Cisco Packet Tracer — Download free at netacad.com
> All tasks in this section are hands-on lab work.

- [ ] Downloaded and installed Cisco Packet Tracer
- [ ] Built a basic LAN — PCs connected through a switch
- [ ] Built a routed network — two LANs connected through a router
- [ ] Configured static IP addresses and verified connectivity with ping
- [ ] Configured DHCP on a router — devices get IPs automatically
- [ ] Set up DNS resolution in a simulated network
- [ ] Built a VLAN topology — separated traffic by department
- [ ] Configured inter-VLAN routing
- [ ] Simulated HTTP, FTP, DNS traffic and watched the flow in simulation mode
- [ ] Used simulation mode to watch packets move layer by layer through OSI
- [ ] Built a topology with a firewall and DMZ zone

---

## 1.6 Wireshark 🛠️ PRACTICAL

> **Tool:** Wireshark — Download free at wireshark.org
> All tasks in this section are hands-on lab work.

- [ ] Installed Wireshark on Kali Linux VM
- [ ] Captured live traffic on a network interface
- [ ] Applied display filters — ip.addr, tcp.port, http, dns
- [ ] Applied capture filters to reduce noise before capturing
- [ ] Followed a TCP stream end to end
- [ ] Identified HTTP, DNS, FTP traffic visually by color and protocol column
- [ ] Spotted an anomaly — unusual port, unknown IP, or large transfer
- [ ] Opened a PCAP from malware-traffic-analysis.net and analyzed it

---

## 📚 Resources

| Type | Resource | Format |
|------|----------|--------|
| 📖 THEORY | Professor Messer Network+ N10-009 | 87-episode free YouTube course |
| 📖 THEORY | Practical Networking YouTube channel | YouTube |
| 🛠️ PRACTICAL | TryHackMe Pre-Security Path | Interactive browser labs |
| 🛠️ PRACTICAL | Cisco NetAcad — Intro to Networks | Free course + Packet Tracer labs |
| 🛠️ PRACTICAL | subnettingpractice.com | Drill site |
| 🛠️ PRACTICAL | malware-traffic-analysis.net | Real-world Wireshark exercises |

---

## ✅ Phase 01 Completion Checklist

**📖 Theory Done**
- [ ] Can explain OSI and TCP/IP stack without notes
- [ ] Know all private IP ranges from memory
- [ ] Memorized all critical protocols and their ports
- [ ] Can explain the role of every network device
- [ ] Understand IDS vs IPS, stateful vs stateless firewall

**🛠️ Practical Done**
- [ ] Can subnet an IP without a calculator
- [ ] Built 3+ topologies in Cisco Packet Tracer
- [ ] Captured and filtered live traffic in Wireshark
- [ ] Analyzed a real malware PCAP
- [ ] Completed TryHackMe Pre-Security networking rooms
- [ ] Completed 20+ subnetting drills

---

[← Back to Dashboard](../README.md) · [Next → Phase 02 Windows](../phase-02-windows/README.md)
