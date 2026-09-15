[← Back to Phase 01](./README.md)

# 🖧 Cisco Packet Tracer Labs

> **Tool:** Cisco Packet Tracer — Download free at netacad.com
> **Type:** 🛠️ PRACTICAL — All hands-on lab work

---

## What is Cisco Packet Tracer?

Cisco Packet Tracer is a network simulation tool that lets you build and test real network topologies without physical hardware. Every lab you build here directly maps to skills SOC analysts use daily — understanding how traffic flows, how devices communicate, and how attacks move through a network.

---

## ⚙️ Setup

- [ ] Created free account at netacad.com
- [ ] Downloaded and installed Cisco Packet Tracer
- [ ] Completed the built-in intro tutorial

---

## Lab 01 — Basic LAN

> **Goal:** Connect PCs through a switch and verify communication

**Devices needed:** 2 PCs, 1 Switch

**Steps:**
- [ ] Added 2 PCs and 1 switch to the workspace
- [ ] Connected PCs to switch using copper straight-through cable
- [ ] Assigned static IPs — PC1: 192.168.1.1, PC2: 192.168.1.2, Subnet: 255.255.255.0
- [ ] Pinged PC2 from PC1 — got successful reply
- [ ] Used simulation mode to watch the packet travel

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 02 — Routed Network

> **Goal:** Connect two separate LANs through a router

**Devices needed:** 4 PCs, 2 Switches, 1 Router

**Steps:**
- [ ] Built LAN 1 — 192.168.1.0/24
- [ ] Built LAN 2 — 192.168.2.0/24
- [ ] Connected both switches to router
- [ ] Configured router interfaces with correct IPs
- [ ] Set default gateway on all PCs
- [ ] Pinged from LAN 1 to LAN 2 successfully
- [ ] Watched packet travel through router in simulation mode

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 03 — DHCP Configuration

> **Goal:** Let a router automatically assign IPs to devices

**Devices needed:** 3 PCs, 1 Switch, 1 Router

**Steps:**
- [ ] Configured DHCP pool on router
- [ ] Set PCs to obtain IP automatically
- [ ] Verified each PC received an IP from the pool
- [ ] Checked assigned IPs using `ipconfig` on each PC

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 04 — DNS Setup

> **Goal:** Resolve domain names to IPs inside a simulated network

**Devices needed:** 3 PCs, 1 Switch, 1 Router, 1 Server

**Steps:**
- [ ] Added a server and configured DNS service
- [ ] Created DNS record — test.local → 192.168.1.10
- [ ] Set DNS server IP on all PCs
- [ ] Pinged test.local from a PC — resolved successfully

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 05 — VLAN Configuration

> **Goal:** Separate traffic by department using VLANs

**Devices needed:** 4 PCs, 1 Managed Switch

**Steps:**
- [ ] Created VLAN 10 (HR) and VLAN 20 (IT) on switch
- [ ] Assigned ports to correct VLANs
- [ ] Verified HR PCs cannot ping IT PCs
- [ ] Verified PCs in same VLAN can communicate

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 06 — Inter-VLAN Routing

> **Goal:** Allow VLANs to communicate through a router

**Devices needed:** 4 PCs, 1 Managed Switch, 1 Router

**Steps:**
- [ ] Configured trunk port between switch and router
- [ ] Created subinterfaces on router for each VLAN
- [ ] Set default gateways on PCs
- [ ] Verified VLAN 10 can ping VLAN 20 through router

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 07 — Firewall and DMZ

> **Goal:** Build a network with a firewall separating internal and public zones

**Devices needed:** PCs, Switch, Router, Server

**Steps:**
- [ ] Built internal LAN (private)
- [ ] Built DMZ zone with a web server
- [ ] Configured firewall rules — internal can reach DMZ, external cannot reach internal
- [ ] Tested access from different zones
- [ ] Verified firewall blocks unauthorized traffic

**What I learned:**
> *(write what you learned here after completing)*

---

## Lab 08 — Protocol Simulation

> **Goal:** Watch HTTP, FTP, DNS packets move through the network

**Steps:**
- [ ] Built a basic network with a server
- [ ] Switched to simulation mode
- [ ] Generated HTTP traffic — watched packets layer by layer
- [ ] Generated FTP traffic — observed protocol behavior
- [ ] Generated DNS query — watched resolution process
- [ ] Identified which OSI layer each protocol operates at

**What I learned:**
> *(write what you learned here after completing)*

---

## ✅ Completion Checklist

- [ ] Lab 01 — Basic LAN
- [ ] Lab 02 — Routed Network
- [ ] Lab 03 — DHCP Configuration
- [ ] Lab 04 — DNS Setup
- [ ] Lab 05 — VLAN Configuration
- [ ] Lab 06 — Inter-VLAN Routing
- [ ] Lab 07 — Firewall and DMZ
- [ ] Lab 08 — Protocol Simulation

---

## 📝 My Notes

> *(Add your own notes, shortcuts, and tips here as you learn)*

---

[← Back to Phase 01](./README.md)
