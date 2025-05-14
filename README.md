# 🧪 Homelab-Core

Welcome to my homelab! This repo documents the architecture, configuration, and evolution of my personal network lab used to build real-world IT, networking, and cybersecurity skills. It includes everything from physical setup and VLAN design to firewall deployment and monitoring.

---

## 🔧 Lab Purpose

This homelab is used to:

- Practice **network design, routing, and VLAN segmentation**
- Build and test **Fortinet firewall policies** (FortiGate-VM)
- Prepare for certifications like **CCNA**, **NSE 4**, and **Security+**
- Simulate **SOC workflows** with attack/defense tools
- Improve skills in **Proxmox, virtualization, and infrastructure security**
- Develop technical documentation and process clarity

---

## 🧱 Physical Hardware

| Component | Model / Notes |
|----------|---------------|
| Rack | 9U network rack |
| Switches | Cisco Catalyst 2960, HP 2920 |
| Firewall | SonicWall NSA 2400 (edge NAT) |
| Server | Dell PowerEdge R620 (running Proxmox) |
| Router | Cisco 2901 |
| APs | Netgear ProSafe Dual-Band Wireless-N (x2) |
| Misc | Patch panel, PDU, cable management, UPS (future) |

---

## 🌐 Network Overview

- **Router-on-a-stick setup** using Cisco 2901
- **Trunked VLANs** for segmentation:  
  - VLAN 10: Users  
  - VLAN 20: Wi-Fi  
  - VLAN 30: Servers  
  - VLAN 100: Management  
  - VLAN 99: Native VLAN (blackhole for untagged traffic)
- **DHCP** provided by router per VLAN
- **FortiGate VM** being deployed in Proxmox for NGFW testing

![network-diagram](./network-diagram.png)

---

## 🛠 Current Projects

- [x] VLAN creation and access/trunk port config
- [x] DHCP pools per VLAN (2901)
- [x] Inter-VLAN routing via 2901
- [ ] FortiGate-VM deployment in Proxmox
- [ ] Replace 2901 routing with FortiGate policies
- [ ] VLAN-tagged Wi-Fi SSID via Netgear AP
- [ ] Add Security Onion or Syslog server for alert monitoring

---

## 📁 Repo Structure

```plaintext
homelab-core/
├── configs/              ← Router, switch, FortiGate config exports
├── docs/                 ← Step-by-step writeups (Markdown)
├── logs/                 ← Troubleshooting, changes, lab notes
├── network-diagram.png   ← Topology visual
└── README.md             ← You are here!
```
---

## 📓 Notes & Reflections

This repository isn’t just about configuration—it’s about **the learning journey**.

I’m documenting:
- What I learn  
- Where I get stuck  
- How I solve problems  
- And what I’d do differently next time  

This repo serves as both a **personal reference** and a way to **give back** to others building their own homelab or studying for certifications.

---

## 🧠 Tech I'm Practicing

- Cisco IOS CLI (routing, VLANs, DHCP, ACLs)  
- FortiOS firewall policy configuration  
- Proxmox virtual networking with tagged bridges  
- Network segmentation and inter-VLAN routing  
- Lab documentation and GitHub project logging

---

## 📬 Contact / Connect

If you’re working on your own homelab—or just curious about any part of this project—feel free to connect or fork this repo.  
I’d love to share ideas, configs, or challenges!
