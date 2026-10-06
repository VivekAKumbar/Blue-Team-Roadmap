[← Back to Phase 01](./README.md)

# 🖧 Cisco Packet Tracer Labs

> **Tool:** Cisco Packet Tracer — Download free at netacad.com
> **Type:** 🛠️ PRACTICAL — All hands-on lab work

---

## What is Cisco Packet Tracer?

Cisco Packet Tracer is a network simulation tool that lets you build and test real network topologies without physical hardware. Every lab you build here directly maps to skills SOC analysts use daily — understanding how traffic flows, how devices communicate, and how attacks move through a network.

---

## ⚙️ Setup

- [x] Created free account at netacad.com
- [x] Downloaded and installed Cisco Packet Tracer
- [x] Completed the built-in intro tutorial

---

## Lab 01 — Basic LAN

> **Goal:** Connect PCs through a switch and verify communication

**Devices needed:** 2 PCs, 1 Switch

**Steps:**
- [x] Added 2 PCs and 1 switch to the workspace
- [x] Connected PCs to switch using copper straight-through cable
- [x] Assigned static IPs — PC1: 192.168.1.1, PC2: 192.168.1.2, Subnet: 255.255.255.0
- [x] Pinged PC2 from PC1 — got successful reply
- [x] Used simulation mode to watch the packet travel

**What I learned:**
> *i learned how the packet travel*

---

## Lab 02 — Routed Network

> **Goal:** Connect two separate LANs through a router

**Devices needed:** 4 PCs, 2 Switches, 1 Router

**Steps:**
- [x] Built LAN 1 — 192.168.1.0/24
- [x] Built LAN 2 — 192.168.2.0/24
- [x] Connected both switches to router
- [x] Configured router interfaces with correct IPs
- [x] Set default gateway on all PCs
- [x] Pinged from LAN 1 to LAN 2 successfully
- [x] Watched packet travel through router in simulation mode

**What I learned:**
> *(Connect two separate LANs through a router)*

---

## Lab 03 — DHCP Configuration

> **Goal:** Let a router automatically assign IPs to devices

**Devices needed:** 3 PCs, 1 Switch, 1 Router

**Steps:**
- [x] Configured DHCP pool on router
- [x] Set PCs to obtain IP automatically
- [x] Verified each PC received an IP from the pool
- [x] Checked assigned IPs using `ipconfig` on each PC

**What I learned:**
> *(a router automatically assign IPs to devices)*

---

## Lab 04 — DNS Setup

> **Goal:** Resolve domain names to IPs inside a simulated network

**Devices needed:** 3 PCs, 1 Switch, 1 Router, 1 Server

**Steps:**
- [x] Added a server and configured DNS service
- [x] Created DNS record — test.local → 192.168.1.10
- [x] Set DNS server IP on all PCs
- [x] Pinged test.local from a PC — resolved successfully

**What I learned:**
> *(Resolve domain names to IPs inside a simulated network)*

---

## Lab 05 — VLAN Configuration

> **Goal:** Separate traffic by department using VLANs

**Devices needed:** 4 PCs, 1 Managed Switch

**Steps:**
- [x] Created VLAN 10 (HR) and VLAN 20 (IT) on switch
- [x] Assigned ports to correct VLANs
- [x] Verified HR PCs cannot ping IT PCs
- [x] Verified PCs in same VLAN can communicate

**What I learned:**
> *(Separate traffic by department using VLANs)*

---

## Lab 06 — Inter-VLAN Routing

> **Goal:** Allow VLANs to communicate through a router

**Devices needed:** 4 PCs, 1 Managed Switch, 1 Router

**Steps:**
- [x] Configured trunk port between switch and router
- [x] Created subinterfaces on router for each VLAN
- [x] Set default gateways on PCs
- [x] Verified VLAN 10 can ping VLAN 20 through router

**What I learned:**
> *(Allow VLANs to communicate through a router)*

---

## Lab 07 — Firewall and DMZ

> **Goal:** Build a network with a firewall separating internal and public zones

**Devices needed:** PCs, Switch, Router, Server

**Steps:**
- [x] Built internal LAN (private)
- [x] Built DMZ zone with a web server
- [x] Configured firewall rules — internal can reach DMZ, external cannot reach internal
- [x] Tested access from different zones
- [x] Verified firewall blocks unauthorized traffic

**What I learned:**
> *(Build a network with a firewall separating internal and public zones)*

---

## Lab 08 — Protocol Simulation

> **Goal:** Watch HTTP, FTP, DNS packets move through the network

**Steps:**
- [x] Built a basic network with a server
- [x] Switched to simulation mode
- [x] Generated HTTP traffic — watched packets layer by layer
- [x] Generated FTP traffic — observed protocol behavior
- [x] Generated DNS query — watched resolution process
- [x] Identified which OSI layer each protocol operates at

**What I learned:**
> *(HTTP, FTP, DNS packets move through the network)*

---

## ✅ Completion Checklist

- [x] Lab 01 — Basic LAN
- [x] Lab 02 — Routed Network
- [x] Lab 03 — DHCP Configuration
- [x] Lab 04 — DNS Setup
- [x] Lab 05 — VLAN Configuration
- [x] Lab 06 — Inter-VLAN Routing
- [x] Lab 07 — Firewall and DMZ
- [x] Lab 08 — Protocol Simulation

---

## 📝 My Notes

> *i uplodade all my files *

---

[← Back to Phase 01](./README.md)
